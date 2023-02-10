# Polygon ID Phase 2 Trusted Setup Ceremony

This repository contains the transcript of the Phase 2 Ceremony.

This ceremony runs the trusted setup for 6 circuits:

* **authV2** - circuit for doing authentication
* **credentialAtomicQueryMTPV2** - circuit to prove statements (defined using zkQuery lang) based on MTP proofs of
  credential issuance
* **credentialAtomicQueryMTPV2OnChain** - same as previous one, but for on-chain usage (includes authentication)
* **credentialAtomicQuerySigV2** - circuit to prove statements (defined using zkQuery lang) based on signature of issuer
* **credentialAtomicQuerySigV2OnChain** - same as previous one, but for on-chain usage (includes authentication)
* **stateTransition** - circuit to verify correctness of on-chain transition of identity states

Circuit source code can be found in [circuits repo](https://github.com/iden3/circuits).

For this ceremony we used the tag `v1.0.0` [circuits](https://github.com/iden3/circuits/releases/tag/v1.0.0) with commit
hash `a6aa4641f9b8736fab3e721be727701890d2a85e`

For verifying the ceremony see: [VERIFY.md](VERIFY.md)

Final result with zkey files, verification keys and witness calculator source code on cpp and js can be downloaded 
[here](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/v1.0.0_trusted_setup.zip) (172Mb).

The same including all intermediary zkeys - [here](https://iden3-circuits-bucket.s3.eu-west-1.amazonaws.com/v1.0.0_trusted_setup_full.zip) (2.2Gb).

## Contributions

### AuthV2 Circuit

| Attestation                       | Contributor                                          | Contribution Hash                                                                                                                                                |
|:----------------------------------|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [0001_Oleksandr](/0001_Oleksandr) | [Oleksandr Brezhniev](https://keybase.io/obrezhniev) | `3b888662 7db3ee82 5234b33d 4ff5ccbd`<br>`5c5ee909 c62b3d09 3ecd65ae b27dd1b7`<br>`9dd19c42 3417fd78 2f82ac46 dc8a5656`<br>`99cc0fb8 4819e23d 10df80e3 ba3132d9` |
| [0002_Dmytro](/0002_Dmytro)       | [Dmytro Sukhyi](https://keybase.io/dimasu)           | `cd7bb3ba fa880b57 49c185fe c6e1fd26`<br>`fcd3493f 51ab17d9 2b976a68 ff869cbc`<br>`248b2648 48bcd700 2891596f 4b0c6990`<br>`43a8b933 0519bdb6 c7a24073 57140e18` |
| [0003_Andriian](/0003_Andriian)   | [Andriian Chestnykh](https://keybase.io/andriianc)   | `015bc19d 58ece60c 201c9dd6 ba26dbbf`<br>`8c996c58 27bec226 a08cf57b 2e856fb8`<br>`2cbeeab2 bb6935dc 23fdb5fe 8b17aa3b`<br>`518f7073 10efe147 c420aedb 345577c3` |
| [0004_Eduardo](/0004_Eduardo)     | [Eduardo Antuña Diez](https://keybase.io/eduadiez)   | `d8e1ca37 fa1e547b 00dc9967 a00a6392`<br>`84b7bfee 182f613b 060ee401 1c75ee5c`<br>`efb88872 1f903243 8955bc1c 3eb344e3`<br>`d4116671 62065b13 2e76ff2e d87a6a70` |
| [0005_Ron](/0005_Ron)             | [Ron Kahat](https://keybase.io/troncho)              | `d20d3bac 99210895 5e461267 9083739c`<br>`101fcae9 681b4696 089be0f1 4f31c2d6`<br>`bf5cd432 e6baf180 1b9f354a 030da764`<br>`1ecc352b d6196d5a a480bbe1 c1094ada` |
| [0006_Mircea](/0006_Mircea)       | [Mircea Nistor](https://keybase.io/mirceanis)        | `046b6063 fc35b778 6f0a8ad4 c414117c`<br>`bdaf95a0 49244135 3106223a 2e715de0`<br>`9cedfcce 73066d83 8919fb63 6f2fba04`<br>`5af18208 6a3d2643 fcaca296 d20f9fe1` |
| [0007_Gabin](/0007_Gabin)         | [Gabin](https://keybase.io/gabin536)                 | `26f4bb01 13b901ec 126de841 830ae6d6`<br>`cef9037c 974dbe0b ac125141 fdf8ebf6`<br>`ae7c71bf bc904cef 24d3c211 cc99deeb`<br>`9cec63f4 04571505 9e912b1b 17342b61` |
| [0008_Jordi](/0008_Jordi)         | [Jordi Baylina](https://keybase.io/jbaylina)         | `b43b135c 033560bf a5a53bdb 41b9a0a1`<br>`6f600e34 66741a8d 66728f8c a3765766`<br>`65cfcb09 a212f938 9e07609a ac479e0a`<br>`a2bb84d1 cede3a2d cd034c2b ca2be925` |
| [0009_Illia](/0009_Illia)         | [Illia Korotia](https://keybase.io/cryptoillia)      | `ce18231a d94b05fb dcebb40e 9999874f`<br>`e5e2d8da 24f08dab 03517cd6 0cbedf3c`<br>`65f2bab2 2a066f1d 0084753e ceb6c9fe`<br>`04ddcba5 37e18ad3 10a4d08b 683b1ad1` |
| [0010_Dhadrien](/0010_Dhadrien)   | [dhadrien.eth](https://keybase.io/dhadrien_eth)      | `a5537e7b f2576f83 280eaee9 2c12826b`<br>`96aa350e a66db9ce 75b22c05 f244829b`<br>`f4f15e01 061ff08e 9e1630f5 8258fa0d`<br>`442b2942 9d87aa26 81700839 cc19ad07` |
| [0011_Leo](/0011_Leo)             | [leo21.eth](https://keybase.io/leo21sismo)           | `cfce2581 6636da94 2748859e 1d8924de`<br>`57ca9190 ac56cd59 17f27471 8c09a4ce`<br>`8dc577c0 fd5be61b 57fa09df 786e2965`<br>`14253187 d001beaf e4bf04d0 1f28470d` |
| [0012_Mark](/0012_Mark)           | [Mark Bessmertnyy](https://keybase.io/mbessmertnyy)  | `6fac7d89 964aa79a 7dc7a4c2 c4178384`<br>`6a605cd9 7b734620 975c34ca 8081fb0c`<br>`0131e540 ac21a7b8 0372c076 857cc560`<br>`bdc20688 281997f2 aa1014a9 bfbe770f` |

b2sum circuit_final.zkey:

````
696d3ca244a7e52b5ca9632b63d7363339691edf07478ba8b16e5c3449e0fbfcd19945907b222dd5ee39ed598836e1efd5329033d68175d0d7ab376eb889c909
````

### CredentialAtomicQueryMTPV2 Circuit

| Attestation                       | Contributor                                          | Contribution Hash                                                                                                                                                |
|:----------------------------------|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [0001_Oleksandr](/0001_Oleksandr) | [Oleksandr Brezhniev](https://keybase.io/obrezhniev) | `4b61e8a9 a0676559 c1c3c90e 670194ff`<br>`01b7e703 342ec271 f72f4333 60ffb5f3`<br>`bce530cf 78fe821f c558be7b 04299ff8`<br>`688a2917 a7c638e9 cae9ac89 f881c291` |
| [0002_Dmytro](/0002_Dmytro)       | [Dmytro Sukhyi](https://keybase.io/dimasu)           | `a618d9ba 9d993cbb daf389a9 1541ad5b`<br>`ee422387 af06a7d0 2966f34c c608b75c`<br>`236b9132 f369b519 fc31c00e d2b14775`<br>`e291095a 5cc4ff32 3d7c2151 1bdccaae` |
| [0003_Andriian](/0003_Andriian)   | [Andriian Chestnykh](https://keybase.io/andriianc)   | `3d47b159 2b14b04c 09fbf9d7 e0bd021c`<br>`cac9e3e6 1f8b6a97 58f58288 28d01bd1`<br>`cf96e0de 28d96219 7a8a8a40 b0075f13`<br>`02eb93a8 3e365af3 89b34ebc 7e54f116` |
| [0004_Eduardo](/0004_Eduardo)     | [Eduardo Antuña Diez](https://keybase.io/eduadiez)   | `3ba0622a 9c7bc666 19515230 ef1df54c`<br>`e2c5f425 6e7ee2e7 314ade59 c1a88358`<br>`f4d88492 bfc8e966 36669993 2569e1f2`<br>`e17dbaf2 96a0e940 634f3fd8 721325ca` |
| [0005_Ron](/0005_Ron)             | [Ron Kahat](https://keybase.io/troncho)              | `ca3cc347 9cd38b36 8500da84 a6e07ec4`<br>`0e4ddea8 8747b06d f5958758 fe7bd16a`<br>`628b7910 432754d7 ca82c35c 30eee748`<br>`8e72ce7a d809cfff 017eaacb d6f4eec5` |
| [0006_Mircea](/0006_Mircea)       | [Mircea Nistor](https://keybase.io/mirceanis)        | `24a04fc6 22f62485 8cbd4d4d 55b08790`<br>`a4eaadc5 78875b3a 205be8f6 bd6b9080`<br>`86635120 dac228d2 f7961d26 8046e36c`<br>`bfac7a7c d1be305d cc9b2dbb 0673141a` |
| [0007_Gabin](/0007_Gabin)         | [Gabin](https://keybase.io/gabin536)                 | `f2c3fb75 c0746e22 995ed6ce 3dd0d10e`<br>`2dfb3a09 73252d94 f03d1d67 1712dd22`<br>`e7d6d9c4 ab7f754e 52e54c42 39bab05e`<br>`56f09020 99271f29 2215279c 433db456` |
| [0008_Jordi](/0008_Jordi)         | [Jordi Baylina](https://keybase.io/jbaylina)         | `5552573d 38f8a900 790782c8 8fbd2413`<br>`1d7d4a27 86e3d602 4c3aee63 2bc0471c`<br>`07824c8a 5be97df4 bfd83b67 75af5f11`<br>`fb980fa9 d1dca3c5 ca668fe9 4687e1da` |
| [0009_Illia](/0009_Illia)         | [Illia Korotia](https://keybase.io/cryptoillia)      | `2b923c13 e1ac7c3b 16136f2b 119b5630`<br>`04c0f868 046b61df 1f2217f1 085423fa`<br>`83cffb2f ec3da868 274f3ba0 ee88a66e`<br>`2752e8fd 0cc277a0 0d0ecad4 d53c5b43` |
| [0010_Dhadrien](/0010_Dhadrien)   | [dhadrien.eth](https://keybase.io/dhadrien_eth)      | `0eb7fe81 53023e14 b6b4f962 a87b5861`<br>`fe7def21 9cd04f6b 82ec5f93 8136ac57`<br>`debcd708 5e14da2c 060a657b 8ea4b3e4`<br>`72fc9c60 1a96ef02 91aba7a2 418dc9fd` |
| [0011_Leo](/0011_Leo)             | [leo21.eth](https://keybase.io/leo21sismo)           | `074ebd12 1f2e82f2 23be9a5b a92edd4d`<br>`2c8b7e3a 188e6eaf da6ab05e c0f2cdd8`<br>`a78d4c71 5b7746e0 0f40bd43 e36ee716`<br>`c0c46f05 0939b9bd 86aa3124 8fac1104` |
| [0012_Mark](/0012_Mark)           | [Mark Bessmertnyy](https://keybase.io/mbessmertnyy)  | `1158e51c 0bf3c3af 2217a53c f4932249`<br>`79a51267 88a956a2 e9dc24aa f59ea288`<br>`8d38b9aa acbad841 06828789 0722fe41`<br>`5f9ca366 39b90e95 3f13f7ff 0988a80e` |

b2sum circuit_final.zkey:

````
52774a5c0a6ba5cc6862e0c81678b56b9c3b5b43f8d8fe2f5d13fd1697d5b80fccaf86f8f5af556ce0a0cc1bde3f0a349745806aac5a18f47b68df7cc2374a43
````

### CredentialAtomicQueryMTPV2OnChain Circuit

| Attestation                       | Contributor                                          | Contribution Hash                                                                                                                                                |
|:----------------------------------|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [0001_Oleksandr](/0001_Oleksandr) | [Oleksandr Brezhniev](https://keybase.io/obrezhniev) | `e51729d1 ddf4c37d 26f0d935 b72a3530`<br>`3f8251f8 a17ebe6a cc656f87 cceac0b4`<br>`99c58de6 d8fd1c4f c3106667 0af1b9a2`<br>`af35000f 5af5372f f4630367 c95106bf` |
| [0002_Dmytro](/0002_Dmytro)       | [Dmytro Sukhyi](https://keybase.io/dimasu)           | `041f6d1b 210b9633 087659da 93f5e73a`<br>`bfc6365b c6486012 16bd2e84 57e30ec5`<br>`2915ec4e 94f2ffb4 6af1c610 9ea40cc9`<br>`74cc4f1f 5e7d4efb abe98d04 84de3de8` |
| [0003_Andriian](/0003_Andriian)   | [Andriian Chestnykh](https://keybase.io/andriianc)   | `987e693e 408f166b 9472f243 806ca21a`<br>`7ef1660f 8350a4cd dccab1cd 951f561d`<br>`87265e6c 2212e9aa 15d5f565 5a167906`<br>`1dd49ebe 3d16e8ad ad487e38 dc235dc7` |
| [0004_Eduardo](/0004_Eduardo)     | [Eduardo Antuña Diez](https://keybase.io/eduadiez)   | `0dd6d568 00675c7c 715dfcb5 b02d8057`<br>`0a18b8b9 4a0461d9 d908fa70 2a493440`<br>`5d535837 e06a1bb7 9e3b6dd6 b13adf18`<br>`f8f5f80f bb167061 1a04dab1 c374cef6` |
| [0005_Ron](/0005_Ron)             | [Ron Kahat](https://keybase.io/troncho)              | `acdcbb0a f38bd323 2fa7e2dd 8b5a3944`<br>`4c276a65 a4703309 29085cd7 be791733`<br>`25a438a5 81bf59eb bca5c96a 2fd46f53`<br>`b2bd6d74 91113c7f 58ab1755 530d095f` |
| [0006_Mircea](/0006_Mircea)       | [Mircea Nistor](https://keybase.io/mirceanis)        | `1c690abb 4b8900ff 5b5e52a7 51444881`<br>`0a93c003 0b93821e bd9315e8 cc28fae1`<br>`bdbda7a2 c4318d28 a60eb54a 69fc0fa3`<br>`2e80c611 7d2f0233 9137cd1a 8a5632fd` |
| [0007_Gabin](/0007_Gabin)         | [Gabin](https://keybase.io/gabin536)                 | `50684727 1fe200ac 47afc0a3 4d0cdd0d`<br>`bff35261 5d565617 7143336d ccb3b7c5`<br>`0c0d24b2 8dcd9f13 afbcb8ce d75c9183`<br>`8baa7cf9 f1816f04 5da3fbf5 275cba48` |
| [0008_Jordi](/0008_Jordi)         | [Jordi Baylina](https://keybase.io/jbaylina)         | `b2bfc07f 315a20e1 7832dec6 2bfa7fdc`<br>`df6701e1 18aee9a1 caf6c82f 5a5612f6`<br>`d3b69309 190c70eb ee88897d c4cd22cf`<br>`5c9e5f02 da2df154 e04114ee f12ba916` |
| [0009_Illia](/0009_Illia)         | [Illia Korotia](https://keybase.io/cryptoillia)      | `da1f824d 95342a35 513afc18 dee18c8e`<br>`02a29a34 33c98b4c 2f1ec7ad 44f957c7`<br>`039ed937 10942521 72121355 80d936be`<br>`e8ed9997 772c3a34 f12ef0a9 74538a0f` |
| [0010_Dhadrien](/0010_Dhadrien)   | [dhadrien.eth](https://keybase.io/dhadrien_eth)      | `e1caeb98 12e46ac4 3f9a2949 b7f01ca0`<br>`5401e934 8b52b9b2 60c50b57 c0d8516e`<br>`95eb8007 c24a6968 3a20c6ab 63ccaeaf`<br>`43a6477f 1ddcafb2 3ec62e9d e79e26d2` |
| [0011_Leo](/0011_Leo)             | [leo21.eth](https://keybase.io/leo21sismo)           | `43cbe2bf 961e2b3d 8b0c5696 1810825e`<br>`da4cfdae 502635f0 c4746620 6de0f5f6`<br>`56ef2786 e64ab4ca 091d4aa6 1c4be846`<br>`deb4fa6d e6cf3b2f 1bd57ea8 2bf68874` |
| [0012_Mark](/0012_Mark)           | [Mark Bessmertnyy](https://keybase.io/mbessmertnyy)  | `0d9508f0 0cf82cda dfebee8b 3f1805de`<br>`424df618 27e6b25d 0404c363 783bd040`<br>`8c8c6e01 453e1c4d a253d2d9 9a6ff1b4`<br>`c9a9b191 a608b950 a55ca6cd 8f9cb8bb` |

b2sum circuit_final.zkey:

````
de1d27850352123df6d11bb9525b098bcfa41072f20ea7fb1bf046b3923ae0a9770861fdd687871a27b91d3ff493c7f20b29844323a74442561c2d5db87bf7dc
````

### CredentialAtomicQuerySigV2 Circuit

| Attestation                       | Contributor                                          | Contribution Hash                                                                                                                                                |
|:----------------------------------|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [0001_Oleksandr](/0001_Oleksandr) | [Oleksandr Brezhniev](https://keybase.io/obrezhniev) | `b131f544 e2659be3 b102602c 83c3fa4b`<br>`708db122 c6725c80 2ba7210a 10d5f946`<br>`8cf67805 757f5dff 9156ae20 686df448`<br>`75f162b2 83f8b79d fc816375 7f110a8b` |
| [0002_Dmytro](/0002_Dmytro)       | [Dmytro Sukhyi](https://keybase.io/dimasu)           | `bec76af1 50b28f9a 9aba1ea1 db8a2fe5`<br>`26f80261 ccfbe367 8057fd00 16f1c60a`<br>`cc2305e7 44f65bcb 50074b17 43d3b018`<br>`2e82f8b3 f9739e13 503b11da 26f528c0` |
| [0003_Andriian](/0003_Andriian)   | [Andriian Chestnykh](https://keybase.io/andriianc)   | `4ab8f729 2021f3cd 6b047fef b41bbc6a`<br>`44439e95 ff73e06d 8a7c0bb7 9a4188d6`<br>`453e43a1 4e265404 3ad99c5d 264a4677`<br>`87a99ce6 199b909c 88f0332e 052a1bbb` |
| [0004_Eduardo](/0004_Eduardo)     | [Eduardo Antuña Diez](https://keybase.io/eduadiez)   | `573988de 6fe2245c b4e9deb9 96a6dea5`<br>`4a5c74b9 45c909a5 1dd1eee4 dc30ff56`<br>`74368f3d e275ccfa 38faed70 2830c565`<br>`a803b157 7f4e6a8d f6ec9d7e 8024e117` |
| [0005_Ron](/0005_Ron)             | [Ron Kahat](https://keybase.io/troncho)              | `3dc36bbf f67c6ce6 0df77f78 dba7a42c`<br>`8647eaa3 399987c5 b20afa1b 35e19a3d`<br>`75ddee1a 4da9bcf1 3e6ed13b e3dd076b`<br>`a7ae92fb 215cfa49 622c44b8 16e2481f` |
| [0006_Mircea](/0006_Mircea)       | [Mircea Nistor](https://keybase.io/mirceanis)        | `128dddc2 b6be2f33 9ecd454a 2b1e9e75`<br>`34a006c0 9a831f79 b3481b8e 0b799cd2`<br>`7c55c468 3aa1cb00 0b6ed573 92342244`<br>`956a2cbb 007d1e26 346eddde c7147822` |
| [0007_Gabin](/0007_Gabin)         | [Gabin](https://keybase.io/gabin536)                 | `d2cfe497 4bbcf694 53ecb1e0 1c1c7f82`<br>`dfc1ccde b2fe4156 46012d57 4a21f8e6`<br>`69af1cd7 f1e5927a b272ec60 8983f350`<br>`c9fa1e0a 2d96ef3b e66ce71f f99d3705` |
| [0008_Jordi](/0008_Jordi)         | [Jordi Baylina](https://keybase.io/jbaylina)         | `4e7151a4 342de05e 4840de88 a6f73fa7`<br>`80a68df0 b8dab5b8 c6304ff7 f8a0b8c8`<br>`706ca679 6cb7ecf4 1bfd43a5 da9571df`<br>`6762861a cb721e7b be014f2b 9fda9a6f` |
| [0009_Illia](/0009_Illia)         | [Illia Korotia](https://keybase.io/cryptoillia)      | `ad3f5064 99a2f1ff 2af79b6e 1b611479`<br>`35a6dc3b a376260e a67fefa2 46a4832d`<br>`2f617f5b b295b455 69bec5f4 b1c09281`<br>`426db8e6 3567d616 32a918b1 81018b23` |
| [0010_Dhadrien](/0010_Dhadrien)   | [dhadrien.eth](https://keybase.io/dhadrien_eth)      | `007ae9ba 93711d93 11d4957f 4ab75cc5`<br>`6dbc592c b5b0a629 9ff448a3 ec2ea425`<br>`a9a5d6cd ee73c134 a9070092 9274a485`<br>`073a31bc a9f97bb3 34ad4ea5 d4d6d8ac` |
| [0011_Leo](/0011_Leo)             | [leo21.eth](https://keybase.io/leo21sismo)           | `930c362d 5f190ba0 015acb06 b92b51ec`<br>`7f310a40 c9aa0f19 59762bc6 ed87dbf6`<br>`ac114041 ba54eb17 10a36694 d03ce3e2`<br>`574a2487 2db178b0 412419a0 57ca5c37` |
| [0012_Mark](/0012_Mark)           | [Mark Bessmertnyy](https://keybase.io/mbessmertnyy)  | `77603797 6ddc5004 ebbde7c7 00b00108`<br>`4421c05b 234897c0 e0d325e5 383e43d0`<br>`dd05d6af 7935cac7 5d07e920 21597a47`<br>`f9c2c300 3e27965b 02d53a21 a2008f90` |

b2sum circuit_final.zkey:

````
a987613b0d668faef06e367e849ba87d67433c6673d7fbd97ffe6695f567d67f309ad1a01dd97e5746b43b8c8e489f9d955e07dba9650f3578d8f6f7db7c7101
````

### CredentialAtomicQuerySigV2OnChain Circuit

| Attestation                       | Contributor                                          | Contribution Hash                                                                                                                                                |
|:----------------------------------|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [0001_Oleksandr](/0001_Oleksandr) | [Oleksandr Brezhniev](https://keybase.io/obrezhniev) | `dee94593 486ed559 d096d127 37ee2195`<br>`633bf722 6d1cb5f5 75b7bafb 75ec96f3`<br>`f29b1919 9eebf462 a64b198b c629cb95`<br>`7efd29c2 a0fd9a83 d7c74969 41bc8e79` |
| [0002_Dmytro](/0002_Dmytro)       | [Dmytro Sukhyi](https://keybase.io/dimasu)           | `7a543ebb 8f1b8b86 0ba90c2e 6fcd82ef`<br>`533a1578 2ddd69a9 d8c3c446 78304159`<br>`bf341747 f0b9148d 6af2b745 d4a10dee`<br>`0e4f4fcd ec6feae4 4f09f157 3d85aa58` |
| [0003_Andriian](/0003_Andriian)   | [Andriian Chestnykh](https://keybase.io/andriianc)   | `16bb58d4 914f0eba a7248ec3 ee8dbcae`<br>`6c22193e bb8bfd66 70b9174d 8a9b1a39`<br>`d4ba253f abfc57d6 f3adf57f 4e30b058`<br>`4ce87809 60541445 86bf89dd 38ca8ff8` |
| [0004_Eduardo](/0004_Eduardo)     | [Eduardo Antuña Diez](https://keybase.io/eduadiez)   | `a364a813 6c0ccfef 7b1939c2 4f7485ba`<br>`1907ec1e 36d87e92 8c533682 cd1acba1`<br>`cffda686 efb1bdc6 3d2cbbc4 7db69840`<br>`6fd6eb47 e69bab75 1f132c4a d57c8660` |
| [0005_Ron](/0005_Ron)             | [Ron Kahat](https://keybase.io/troncho)              | `ff02a304 1cf350cd 0d9f6810 42244aae`<br>`0f465e96 5623bebd 97bc9dc7 2798ee3f`<br>`bcf984e7 204e2841 e48607f8 d07e43fa`<br>`33a909ef 74d61d85 057e9adb e3304214` |
| [0006_Mircea](/0006_Mircea)       | [Mircea Nistor](https://keybase.io/mirceanis)        | `474b0028 2d7503cc cce42d2d 4654a6d8`<br>`270dfc6f 0b19e0e7 499b4f60 fa9981f0`<br>`3e5d185e 4a91ca9d ffabb159 db1453f1`<br>`e91da281 c3deb922 dd4ae1de 274dcb3a` |
| [0007_Gabin](/0007_Gabin)         | [Gabin](https://keybase.io/gabin536)                 | `55d0b679 198f8111 56c1a6be c3b85b10`<br>`eef6c5c8 319caa56 18ca5274 0f4fab9a`<br>`fb35b956 6230dd8f c3b2b931 8546c086`<br>`87eef6f4 ebf2b7a3 ed13d9dc a6d610d0` |
| [0008_Jordi](/0008_Jordi)         | [Jordi Baylina](https://keybase.io/jbaylina)         | `2efb79b3 1deae7b4 b9ec88d3 62b96663`<br>`3963d121 62e202d6 b5d4d6d1 b60c0d14`<br>`65da39fc 7f28627a b99644c1 8cd3ea81`<br>`2c667786 0c595441 3ff1f7b3 20f7884f` |
| [0009_Illia](/0009_Illia)         | [Illia Korotia](https://keybase.io/cryptoillia)      | `327a0c82 034c38e0 963ea054 ac4187ad`<br>`ca2579d7 8335dd90 4c0a8705 6284047b`<br>`dc48afee 62ec0186 2b641fcb 78d8db00`<br>`d6d0c0b1 fe186891 44788dba 2f327d6f` |
| [0010_Dhadrien](/0010_Dhadrien)   | [dhadrien.eth](https://keybase.io/dhadrien_eth)      | `a9082100 47e5a069 f8d7d9e0 80c92926`<br>`884c21fb c909cd5c 4988fcec c2a39345`<br>`54201a42 854fb9ca 9c257597 7c23c629`<br>`da73b30e 45243a68 534975f2 87b9f037` |
| [0011_Leo](/0011_Leo)             | [leo21.eth](https://keybase.io/leo21sismo)           | `7d6be090 fdbfe9e7 584e7944 5ddc1788`<br>`6bc12218 c9918774 10be15b4 a853b71e`<br>`8a4d7b53 74d9f402 ca26f556 844d04c2`<br>`7231977d 70660ae6 e1f592ce 247f1fe1` |
| [0012_Mark](/0012_Mark)           | [Mark Bessmertnyy](https://keybase.io/mbessmertnyy)  | `2b2b4aa2 ea477141 ed145f86 d8538b2b`<br>`741bcbe2 6e5e29cb a9dc65d1 267956c1`<br>`c15bfdb7 23a73355 426dc335 1e9e2219`<br>`0c952db0 39234756 3f4dd8d8 d3f6ef5e` |

b2sum circuit_final.zkey:

````
3b86b09b1b74002664d9751cdbcc12d536025e21dbc29e8b5bc267cb489f38f20def697a69f9464d4cfec50a798e6d1fe1ee6ea39acb0a41680b9845b700659f
````

### StateTransition Circuit

| Attestation                       | Contributor                                          | Contribution Hash                                                                                                                                                |
|:----------------------------------|:-----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [0001_Oleksandr](/0001_Oleksandr) | [Oleksandr Brezhniev](https://keybase.io/obrezhniev) | `baa4d44d 094ef934 c4759357 6885255e`<br>`05ce02c5 2093bda4 9cbcb965 9b4a71fe`<br>`94490eeb 29ac832b f0cf1fc1 f5169fd8`<br>`75455e55 9a1ebf4a f5c6126b 68d1e208` |
| [0002_Dmytro](/0002_Dmytro)       | [Dmytro Sukhyi](https://keybase.io/dimasu)           | `b22d7045 37a83cc6 c0313a90 6268e9b2`<br>`009bc222 61cb152f 987d7e81 2179ef56`<br>`cd3edb40 f224bf1c 79d29ba0 5c857ab8`<br>`4a7a1ed1 e3a529b7 3e58ff72 df2afcec` |
| [0003_Andriian](/0003_Andriian)   | [Andriian Chestnykh](https://keybase.io/andriianc)   | `934fd71a 1ebad326 53523054 09c56f6e`<br>`daf7f7a9 b98d83d8 b0410084 e8c1950a`<br>`092fbaed a97c2801 b9347646 7d492487`<br>`8a996afb f1023526 5d1db224 81f44381` |
| [0004_Eduardo](/0004_Eduardo)     | [Eduardo Antuña Diez](https://keybase.io/eduadiez)   | `7741f826 23bbcac9 8532a779 32a0659c`<br>`be16f7f2 ca501301 d7c0374c 16b6e014`<br>`721be962 979067ad 61deb362 8fa9ddb3`<br>`93e7ec94 60193f9e fc777cc0 7519ba2e` |
| [0005_Ron](/0005_Ron)             | [Ron Kahat](https://keybase.io/troncho)              | `9eacf2df 4735d374 cf0e2ee9 a267fb5c`<br>`984dbd6d 0299ad8c 084de142 4486c351`<br>`1eed4283 b91243df dcbb2f72 3f935ac3`<br>`4ecade0b cd914fa1 df1dd6cb b8c6e777` |
| [0006_Mircea](/0006_Mircea)       | [Mircea Nistor](https://keybase.io/mirceanis)        | `f55156d2 6ecca341 e62a8a74 025981d4`<br>`7a7bd30e d7de422c b643360c 1e42978b`<br>`b3345f4f 1d6d78ca a47c91ae ed152e51`<br>`60677d40 6b0c2f32 411671d3 f77f6e3f` |
| [0007_Gabin](/0007_Gabin)         | [Gabin](https://keybase.io/gabin536)                 | `46a5927b d1c1e22a 4dadf59c 84714f54`<br>`abd941c6 1492d00c 1a3ee908 daba6bcf`<br>`73d4db5b d665bf41 40c18838 89d6b92e`<br>`9bd9ba57 76f1ce82 e1645e33 7cf2417f` |
| [0008_Jordi](/0008_Jordi)         | [Jordi Baylina](https://keybase.io/jbaylina)         | `814ee1f4 f853f399 4a1526b9 4225909e`<br>`1264ea1f 941ba268 17489431 ee5b7b2d`<br>`76eed84a dbef080b 37df9742 28b01127`<br>`ca8ecac4 3128ef1d 37da75fc 8dea6fe1` |
| [0009_Illia](/0009_Illia)         | [Illia Korotia](https://keybase.io/cryptoillia)      | `cd28b727 6f0aa454 6088599c f48dc0cb`<br>`f3409c23 e244f791 aee1bf42 571dc8cf`<br>`9efc24ad 7441539e 68c983e5 8f90fbc1`<br>`21c5ff9c d981cbb8 f0696103 bae948ec` |
| [0010_Dhadrien](/0010_Dhadrien)   | [dhadrien.eth](https://keybase.io/dhadrien_eth)      | `5226599f 166788ef dada90e7 ac497039`<br>`fa566849 ee86b800 62f7e830 ec476558`<br>`dab5c41f 0bf5ec00 e8bc1f9f a52236e0`<br>`9bda46c7 ad270a23 6e60e16a a5137dfe` |
| [0011_Leo](/0011_Leo)             | [leo21.eth](https://keybase.io/leo21sismo)           | `f0120b82 c008e300 197b612c f4d84613`<br>`4c6c3c02 c2b22ac4 2ccefbf1 885b90f9`<br>`146c7091 63ef1d58 cec3877f 8860d0a4`<br>`54a5c53a 1c307f68 c83aa003 a8a93509` |
| [0012_Mark](/0012_Mark)           | [Mark Bessmertnyy](https://keybase.io/mbessmertnyy)  | `e0462ece e9d049ab 7cddaa5d 53be546b`<br>`07933de1 fcaea63a 0260bda2 24592e0f`<br>`98879fe4 9fe8ed14 4cf95f6a a235624e`<br>`63cdc450 921d486a 7c01e416 dedd0261` |

b2sum circuit_final.zkey:

````
c05fbc2115ddc98fb9f8b9530e14b180fce13b38f290c91d1913f23cd0e66cd8c30fa9ea3454bdf1f12ece7a03defd278f86a709c463af2362c110d1481b4577
````
