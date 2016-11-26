# DHPy
This module helps you to generate Diffie Hellman Keys for Augmented String progocols
# Usage
import DHPy
Alice = DHPy.DiffieHellman()
Bob = DHPy.DiffieHellman()

Alice_PubKey = Alice.gen_public_key()  						# g^a mod p
Bob_PubKey = Bob.gen_public_key()	   						# g^b mod p
Alice_SharedKey = Alice.gen_shared_key(Bob_PubKey)			# g^ab mod p
Bob_SharedKey = Bob.gen_shared_key(Alice_PubKey)			# g^ab mod p
Bob_AugmentPassword = Bob.gen_gpowxw(password_hash)			# g^bw mod p

