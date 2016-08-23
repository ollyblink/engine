
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
- update data
- delete data
##consent
- create
	- POST createconsent/receiver/:receiver/constraints/{:constraint}
- read (needs to be exposed? Probably more for reading own consents)
	- GET consents/receiver/:receiver/sender/:sender/
- update (e.g. to change constraints or receiver)
	- UPDATE consents/cId/:cId/receiver/:receiver/{constraint}/{:constraint}
- delete (if the consent isnt required anymore)
	- DELETE consents/cId/:cId