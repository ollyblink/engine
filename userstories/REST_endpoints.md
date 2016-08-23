
- login
- recover password
## user
- Register/create
- read 
- update (what can be updated? does this happen only when the password is updated?)
- delete (+delete consent)
## user data
- create data
	- POST createData/topic/:topic/description/:description/...
- read data of a user 
- update data
- delete data
##consent
- create
	- POST createConsent/receiver/:receiver/{constraints/{:constraint}
- read (needs to be exposed? Probably more for reading own consents)
	- GET consents/receiver/:receiver/sender/:sender/
- update (e.g. to change constraints or receiver)
	- UPDATE consents/cId/:cId/receiver/:receiver/{constraint}/{:constraint}
- delete (if the consent isnt required anymore)
	- DELETE consents/cId/:cId