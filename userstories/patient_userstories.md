**As a patient...**

**I want to be able to register with username and password.**

1. A user specifies a username and a personal password to register.
2. *Optional: registration ends with sending a confirmation email.
3. Registration creates a new "Person" entity in the database. 
4. Registration creates a random-generated asymmetric public/private key pair for exchanging data.
	1. The private key is encrypted when stored using the user's password.
	2. The public key is stored without any encryption.
5. Registration creates a random-generated symmetric encryption key to encrypt the data.
	1. The symmetric encryption key is encrypted when stored using the user's public key or password (see questions).
	

**I want to be able to create, read, update, and delete personal health data.** 

1. A user logs in with the specified username and password.
2. The encrypted private key and encrypted encryption key are transferred to the client.
3. The private key is decrypted and used to decrypt the encryption key.
4. The encryption key is returned to the system.

**I want to be able to share this data with my doctor.**

1. A user invites another user to read and update 