
- login
- recover password
## Person
- Register/create
	- POST createPerson/firstname/:fname/lastname/:lname/{additional_info}/{:additional_info}
- read 
	- GET persons/pid/:pid
- update (what can be updated? does this happen only when the password is updated?)
	- UPDATE persons/pid/:pid/{updatable_item}/{:updatable_item}
- delete (+delete consent)
	- DELETE persons/pid/:pid
## user data
- create data
	- POST createData/topic/:topic/description/:description/...
- read data of a user 
	- GET readData/person/:pId/topic/:topic/description/:description/... --> for a specific data item e.g. one document
	- GET readData/person/:pId --> returns all the data of a person
	- GET readData/data/:dId --> return all the data of this entry
- update data
	- POST updateData/data/:dId/topic/:topic/description/:description/...
	- POST updateData/data/:dId/attachment/:atId/attachmentContent/:dataOfAttachment
	- POST updateData/data/:dId/attachmentContent/:dataOfAttachment
- delete data
	- POST deleteData/data/:dId --> all the data entry + consents
	- POST deleteData/data/:dId/attachment/:atId --> deletes only an attachment + consent (if available only for this attachment)
##consent
- create
	- POST createConsent/receiver/:receiver/{constraints/{:constraint}
- read (needs to be exposed? Probably more for reading own consents)
	- GET consents/receiver/:receiver/sender/:sender/
- update (e.g. to change constraints or receiver)
	- UPDATE consents/cId/:cId/receiver/:receiver/{constraint}/{:constraint}
- delete (if the consent isnt required anymore)
	- DELETE consents/cId/:cId