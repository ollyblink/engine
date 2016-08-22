
# As a Doctor
## I want to access the record's of a patient and view a document. ## 
As a user I am already registered and logged in.

1. Search for a patient from a list of available patients
	1. * Optional: List all patients that have shared consent with this doctor. ??
2. The doctor views the patient's record
3. The doctor tries to access a document e.g. the patient's medical history or previous results of exams
4. The request is validated by checking for a matching consent using the *Doctor's Public Key* and the *patient's encryption key*
	1. Access is granted
		1. There is a consent record in the database with this combination found.
		2. The *patient's encryption key* is returned  and used to retrieve the patient's proteced data record (the database)
		3. The data is decrypted and returned to the doctor
		4. The doctor views the document of the patient
	2. Access is denied
		1. 
