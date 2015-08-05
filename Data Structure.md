#Solin Data Structure

###Using MongoDB.

##User Data Structure

~~~
{
	email : { type : String, max : 30 },
	password : { type : String, length : 64 },
	username : { type : String, max : 100 },
	profile : { type : String, length : 64 },
	statusMessage : { type : String, max : 80 },
	currentGoal : [Goal],
	badges : [{
		type : { type : Integer }, 
		image : { type : String, length: 64 }
	}, ...],
	friends : [ObjectId], 
	activities : [ {
		image : { type : String, length : 64 },
		info : { type : String },
		date : { type : Date }
	}, ...],
	inventory : [{
		type : Integer,
		image : { type : String, length : 64 }, 
		name : String 
	}, ...], 
	personality : 
		O : 3,
		C : 2,
		E : 0,
		A : -1,
		N : 1
}
~~~

##Goal Data Struct
~~~
{
	name : { type : String, max : 100 },
	date : {
		startDate : Date,
		endDate : Date
	},
	category : {
		name : String,
		code : String
	},
	threeLegged : Boolean,
	users : [{
		username : { type : string, max : 10 },
		profile : { type : string, length : 64 },
		term : integer,
		result : [{
			date : Date,
			percent : Integer,
		}, ...]
	}, ...],
}
~~~
