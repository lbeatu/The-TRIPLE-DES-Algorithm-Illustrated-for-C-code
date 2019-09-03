# The-DES-Algorithm-Illustrated-for-C-code

by writer J. Orlin Grabbe

The **DES (Data Encryption Standard)** In cryptography, Triple DES (3DES or TDES), officially the Triple Data Encryption Algorithm (TDEA or Triple DEA), is a symmetric-key block cipher, **which applies the DES cipher algorithm three times to each data block.**

While the government and industry standards abbreviate the algorithm's name as TDES **(Triple DES)** and TDEA (Triple Data Encryption Algorithm), RFC 1851 referred to it as 3DES from the time it first promulgated the idea, and this **namesake has since come into wide use by most vendors**, users, and cryptographers

## **3-KEY Triple DES**

Before using 3TDES, user first generate and distribute a 3TDES key K, which consists of three different DES keys K1, K2 and K3. This means that the actual **3TDES key has length 3×56 = 168 bits.** The encryption scheme is illustrated as follows

The encryption-decryption process is as follows

- Encrypt the plaintext blocks using single DES with key K1.

- Now decrypt the output of step 1 using single DES with key K2.

- Finally, encrypt the output of step 2 using single DES with key K3.

The output of step 3 is the ciphertext.

Decryption of a ciphertext is a reverse process. User first decrypt using K3, then encrypt with K2, and finally decrypt with K1.

Due to this design of Triple DES as an encrypt–decrypt–encrypt process, it is possible to use a 3TDES (hardware) implementation for single DES by setting K1, K2, and K3 to be the same value. This provides backwards compatibility with DES.

Second variant of Triple DES (2TDES) is identical to 3TDES except that K3is replaced by K1. In other words, user encrypt plaintext blocks with key K1, then decrypt with key K2, and finally encrypt with K1 again. Therefore, 2TDES has a key length of 112 bits.

Triple DES systems are significantly more secure than single DES, but these are clearly a much slower process than encryption using single DES.

## **Algoritm**

![](https://www.tutorialspoint.com/cryptography/images/encryption_scheme.jpg)

## \*\*Source: http://page.math.tu-berlin.de/~kant/teaching/hess/krypto-ws2006/des.htm
