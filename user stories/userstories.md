As a patient, I want to be able to register with username and password 

1. A user specifies a username and a personal password to register.
2. * optional: registration ends with sending a confirmation email
3. Registration creates a new "Person" entity in the database. 
4. Registration creates a random-generated asymmetric public/private key pair for exchanging data and a symmetric encryption key to encrypt the data
5. The private key is encrypted when stored using the user's password
6. The symmetric encryption key is encrypted when stored using the user's public key
7. The public key is stored without any encryption.

I want to be able to create, read, update, and delete personal health data. 


I want to be able to share this data with my doctor