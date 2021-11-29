# Assignment4_Elgamal
Elgamal algo

Three parts:
1) A key generator
2) The encryption algorithm
3) The decryption algorithm.

1.Key Generation:

Alice chooses a secret key 1<=a<=p-1.
Computes A=g^a mod p.
Alice se1<=k<=p and the public key pk=(p, g, A) to Bob.

2.Encryption:

Bob chooses a unique random number key 1<=k<=p-1.
Uses Alice’s public key pk and key k to compute the ciphertext (c1,c2) =Epk(m) of the plaintext 1<=m<=p-1 where c1=g^k mod p and c2=m.A^k mod p.
The ciphertext (c1,c2) is sent to Alice by Bob.

3.Decryption:
Alice computes x=c1^a mod p  and its inverse x^-1 with the extended Euclidean algorithm.
Computes the plaintext m’=Dsk(c1,c2)= x^-1.c2 mod p where m’=m.
