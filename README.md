# NoSQL-MongoDB

# Problem5   
question 1   
db.problem5.aggregate([{"$group" : {_id:"$subject", total_marks:{$sum:"$marks"}}}])   
{ _id: 'maths', total_marks: 314 }   
{ _id: 'english', total_marks: 313 }   
{ _id: 'science', total_marks: 311 }   
![image](https://user-images.githubusercontent.com/70503441/159114493-6eb41676-b1ec-4c13-9b6f-67fac3308964.png)   

question 2   
db.problem5.aggregate([{"$group" : {_id:"$subject", maximum_marks:{$max:"$marks"}}}])   
{ _id: 'maths', maximum_marks: 87 }   
{ _id: 'english', maximum_marks: 89 }   
{ _id: 'science', maximum_marks: 86 }   
![image](https://user-images.githubusercontent.com/70503441/159114498-2e4efb78-6990-4efe-8e64-4a9fc0831bf9.png)   

question 3    
db.problem5.aggregate([{"$group" : {_id:"$name", maximum_marks:{$max:"$marks"}}}])   
{ _id: 'Alison', maximum_marks: 86 }   
{ _id: 'Steve', maximum_marks: 89 }   
{ _id: 'Jan', maximum_marks: 0 }   
{ _id: 'Ramesh', maximum_marks: 87 }   
{ _id: 'Rav', maximum_marks: 83 }   
![image](https://user-images.githubusercontent.com/70503441/159114575-80d5af1c-07ca-41de-a3e4-24c92289ec2f.png)   

question 4   
db.problem5.aggregate([{"$group" : {_id:"$name", minimum_marks:{$min:"$marks"}}}])   
{ _id: 'Ramesh', minimum_marks: 59 }   
{ _id: 'Rav', minimum_marks: 62 }   
{ _id: 'Alison', minimum_marks: 82 }   
{ _id: 'Steve', minimum_marks: 77 }   
{ _id: 'Jan', minimum_marks: 0 }   
![image](https://user-images.githubusercontent.com/70503441/159114647-17001040-04e2-4ef5-b9bd-83be8a3ef134.png)   

question5   
db.problem5.aggregate([{"$group" : {_id:"$subject", avg_marks:{$avg:"$marks"}}}, {"$sort": {avg_marks: -1}}, {"$limit": 2}])   
{ _id: 'maths', avg_marks: 78.5 }   
{ _id: 'science', avg_marks: 77.75 }   
![image](https://user-images.githubusercontent.com/70503441/159115645-cec4ab44-eb52-4317-a663-0315c876fbbd.png)   
