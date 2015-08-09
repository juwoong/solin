#Solin Data Structure
Using MongoDB.

##### Types
```js
ImageId = { type: String, max: 64 }
```

##User Data Structure
```js
{
	email : { type : String, max : 30 },
	password : { type : String, length : 64 },
	name : { type : String, max : 100 },
	profileImage : ImageId,
	statusMessage : { type : String, max : 80 },
	currentGoals : [ObjectId], 
	friends : [ObjectId], 
	activities : [Activity],
	inventory : [Item], 
	personality : {
		O: Integer,
		C: Integer,
		E: Integer,
		A: Integer,
		N: Integer
	} // TODO: need some discussion with Logan Lee
}
```

##Goal Data Struct
```js
{
	name : { type : String, max : 100 },
	startDate : Date,
	endDate : Date,
	category : {
		name : String,
		code : String
	},
	threeLegged : Boolean,
	users : [{
		userId : ObjectId,
		username : { type : string, max : 10 },
		profile : { type : string, length : 64 },
		startAt : Date,
		result : [{
			date : Date,
			percent : Integer,
		}, ...]
	}, ...],
}
```

## Activity
```js
{
	image : ImageId,
	info : String,
	createdAt : Date
}
```

## Item
```js
{
	type : String,
	image: ImageId,
	name : String 
}
```
