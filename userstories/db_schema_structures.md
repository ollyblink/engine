# Schema Structures #
## UserDB ##
    Person{
    	pId: string/number //Unique identifier
		firstname: string
		lastname: string
		...
		privateKey_encPW: string
		publicKey: string
		encryptionKey_encPbK: string
		pw_hash_salt: string
    }
## DataDB ##
    Data {
		pId: string/number //person's id
		dId: string/number
		date_time: datetime
		topic: string
		description: string
		{attachments: blob}		
	}
## ConsentDB ##
    Consent {
		cId: string/number
		sender: pId //the inviting user
		receiver: pId // the invited user for data access
		encryptionKeySender_encPbKReceiver: string

		constraints { // some could be optional/default implementations
			access-level: enum //read-only, read-update, read-update-delete or so
			topic: string
			*dataItem: dId
		}
		 
 	}