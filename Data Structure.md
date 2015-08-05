#Solin Data Structure

###Using MongoDB.

##User Data Structure

~~~
{
	_id : ObjectId(...),
	email : { type : string, max : 30 },
	password : { type : string, length : 64 },
	username : { type : string, max : 10 },
	statusMessage : { type : string, max : 80 },
	profile : { type : string, length : 64 },
	currentGoal : [{
		_id : ObjectId(...),
		name : { type : string, max : 100 }
	}, ...],
	badges : [ {
		_id : ObjectId(...),
		type : { type : integer }, 
		image : { type : string, length: 64 }
	}, ...],
	friendNumber : { type : integer },
	friends : [ {
		_id : ObjectId(...), 
		profile : { type : string, length : 64 },
		username : { type : string, max : 10 },
	}, ...],
	activities : [ {
		image : { type : string, length : 64 },
		info : { type : string },
		date : { type : date}
	}, ...],
	inventory : [{
		type : integer,
		image : { type : string, length : 64 }, 
		name : string 
	}, ...], 
	personality : {
		O : 3,
		C : 2,
		E : 0,
		A : -1,
		N : 1
	}
}
~~~

##Goal Data Struct
~~~
{
	_id : ObjectId(...),
	name : { type : string, max : 100 },
	date : {
		startdate : date,
		enddate : date
	},
	category : {
		name : string,
		classificateCode : integer
	},
	three-legged : boolean,
	users : [{
		_id : ObjectId(...),
		username : { type : string, max : 10 },
		profile : { type : string, length : 64 },
		term : integer,
		result : [{
			date : date,
			persent : integer,
		}, ...]
	}, ...],
}
~~~