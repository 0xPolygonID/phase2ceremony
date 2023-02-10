# Verification of the ceremony guide

In order to verify the circuit, you will need a regular machine.

## Requirements

* Snarkjs 0.5.0
* Circom 2.1.3

## Get circuits

Clone [iden3/circuits](https://github.com/iden3/circuits) repo to circuits folder, checkout tag v1.0.0.

## Verify Powers of Tau

We are using powersOfTau files generated for Polygon Hermez. Download following files:

```bash
cd circuits/build
wget https://hermez.s3-eu-west-1.amazonaws.com/powersOfTau28_hez_final_17.ptau
```

Check the blake2b hash of the ptau files:
```bash
b2sum *.ptau
```

The result should be:

```
6247a3433948b35fbfae414fa5a9355bfb45f56efa7ab4929e669264a0258976741dfbe3288bfb49828e5df02c2e633df38d2245e30162ae7e3bcca5b8b49345  powersOfTau28_hez_final_17.ptau
```

If you are also interested in verifying the powers of tau, you can check [this blog post](https://blog.hermez.io/zero-knowledge-proofing-hermez-a-quick-guide-to-our-cryptographic-setup/) and [this other](https://blog.hermez.io/zero-knowledge-proofing-hermez-preparephase2-update/)

## Verify r1cs circuits match source code

```
./compile-circuit.sh circuits/authV2.circom build/powersOfTau28_hez_final_17.ptau
./compile-circuit.sh circuits/credentialAtomicQueryMTPV2.circom build/powersOfTau28_hez_final_17.ptau
./compile-circuit.sh circuits/credentialAtomicQueryMTPV2OnChain.circom build/powersOfTau28_hez_final_17.ptau
./compile-circuit.sh circuits/credentialAtomicQuerySigV2.circom build/powersOfTau28_hez_final_17.ptau
./compile-circuit.sh circuits/credentialAtomicQuerySigV2OnChain.circom build/powersOfTau28_hez_final_17.ptau
./compile-circuit.sh circuits/stateTransition.circom build/powersOfTau28_hez_final_17.ptau
```

##### Circuit hashes
```
cd ~/circuits/build
b2sum */circuit.r1cs
```

The hashes should be following:

```
504801f17410f99e85b27672c26f50e29137a61553569b5a60652a059ba7324af1f6866aef423e85a373236296a9746c629aa438579942dcf446edd39cf749cb  authV2/circuit.r1cs
2e7e2b8e6dad4ac713be8791604db0c6faa7882b9cde7cb029403c52cae2dde82b1905dd7bcf6a2d2b945f624ee18a40d3e75ded2953a8990cfa7693458344ed  credentialAtomicQueryMTPV2/circuit.r1cs
5ab3094ad40eac290f9ae2d3cb140e53b488dc4987d6da517019d50cccfabd1817c46583addca42f0fbae0e95bb09e6131c089585d4aec2dc88141538b027364  credentialAtomicQueryMTPV2OnChain/circuit.r1cs
1059051dc1e0cdda278c11da958221abbd9b738ef08d5ea41d01d944d3b9a424bd4606f1e07f8c2314a37587c581bbb3f3d12dbc429d52d63085ff1214111bbe  credentialAtomicQuerySigV2/circuit.r1cs
de62bff354ca14d663ab9aa289bd3037313dc299f294bef1957b8849af68859e5fe4cdba37a8c3ed7cffb36ded169fa63f201c9d47dd08d7d8d0ef7b25981ea3  credentialAtomicQuerySigV2OnChain/circuit.r1cs
dff6b9f2533cac4c9421a2062645ff0c7fe035c796be005d997e2088e3d84346a83ed0ff6edb1332957d85be4a2eae89c78ae97cecf2578522425f5b44f2c5c8  stateTransition/circuit.r1cs
```

We used Circom v2.1.3 for compilation (the latest version at the moment of the ceremony). So if you results do not match try using this version.


## Verify zkey files

##### AuthV2 circuit
```
snarkjs zkv authV2/circuit.r1cs powersOfTau28_hez_final_17.ptau authV2/circuit_final.zkey -v
```

The circuit hash must be:
```
                3cc6707e 1f35bd91 c4942e6e 90a9cc0a
                1b282221 fc80821f c7bfde44 51450e85
                fa6be1a9 0820c4ca 3f5bf48e d1e56d59
                e02b1bba 0255a52e a8916a2a bd7fc9fe
```

If you want to check an intermediary circuit, Substitute _final by the intermediary response you want.

You can check all the contributions at the end of command output. You should check all the signatures of the transcript and see that the declared contribution hash of each participant matches the ones here.

As far as there is a single attestation you trust, you can consider the ceremony for this circuit safe.

##### CredentialAtomicQueryMTPV2 circuit
```
snarkjs zkv credentialAtomicQueryMTPV2/circuit.r1cs powersOfTau28_hez_final_17.ptau credentialAtomicQueryMTPV2/circuit_final.zkey -v
```

The hash of the circuit must be:
```
                f12cd7bf 892fd794 d9de5d21 fb0190ef
                261ed63a 4d2af815 b56fe952 e5419838
                1ab84b84 917845fe d7776844 3bfca03f
                9fc973ae 17ea0ff8 39a8ae13 61290897
```

##### CredentialAtomicQueryMTPV2OnChain circuit
```
snarkjs zkv credentialAtomicQueryMTPV2OnChain/circuit.r1cs powersOfTau28_hez_final_17.ptau credentialAtomicQueryMTPV2OnChain/circuit_final.zkey -v
```

The hash of the circuit must be:
```
                2546854f 0a4c797b 6140eeab c2862ae7
                c2d71e8e de47af5e 968ff48a 5737b1de
                d255b1ea 749f1fe1 94dada52 0e62d9ce
                1807e5b2 1e599832 13cd7d84 4b4efe04
```

##### CredentialAtomicQuerySigV2 circuit
```
snarkjs zkv credentialAtomicQuerySigV2/circuit.r1cs powersOfTau28_hez_final_17.ptau credentialAtomicQuerySigV2/circuit_final.zkey -v
```

The hash of the circuit must be:
```
                fe16a95f ef9401ca b2d9b409 c8c9c7e6
                6b0eb46c a5ceca5a 8e7f2432 fbdce18e
                a064ee41 4dfc0637 a866dcce 7d1f337d
                2fb5961e aac172ef f06aa7b8 42229ac0
```

##### CredentialAtomicQuerySigV2OnChain circuit
```
snarkjs zkv credentialAtomicQuerySigV2OnChain/circuit.r1cs powersOfTau28_hez_final_17.ptau credentialAtomicQuerySigV2OnChain/circuit_final.zkey -v
```

The hash of the circuit must be:
```
                0ab00f94 d9fdfb77 f76846da 4406f2bb
                512d6f41 b4ca05fb 9ed55c4b 3ed8b2d8
                b0be1a54 7f8a278c 4142581d b370e4db
                88032a20 50a929e9 d2919670 cc840fd1
```

##### StateTransition circuit
```
snarkjs zkv stateTransition/circuit.r1cs powersOfTau28_hez_final_17.ptau stateTransition/circuit_final.zkey -v
```

The hash of the circuit must be:
```
                5f278c18 41fc8b29 48e8ef9a dd4cc192
                bfaf34a4 82d31e02 a7515465 24df9fd7
                8f9f70ab 0f36ee73 4886d400 776dd4dc
                870d6063 aa10bf0d aecfa1dc d8a918a2
```

