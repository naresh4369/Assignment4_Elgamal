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


Written in python, please enter the Plaitext so it will print all steps.

Sample i/p & o/p:

Enter message.Hello


g used= 16713838749946005777753829865777492667974330041343
g^a used= 14525919215546645311320261083641515319541583258139
g^k used=  20177404449211858919840443192690346292172041879829
g^ak used=  768088040165664148210684019851985852139398402071
Original Message= Hello
Encrypted Maessage= [55302338891927818671169249429342981354036684949112, 77576892056732078969279086005050571066079238609171, 82953508337891728006753874144014472031055027423668, 82953508337891728006753874144014472031055027423668, 85257772458388720451385926203570429587473222629881]


Decryted Message= Hello

