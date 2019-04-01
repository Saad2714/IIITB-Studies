
Hello World!!


How to run code:
1)install Postman,  
2)sudo npm i or npm install mongoose,body-parser,express,express-upload,router,bcryptjs,jsonwebtoken,nodemon
3)then nodemon in terminal

in main project folder..run nodemon on terminal
it will show
 App is running at 5000
MongoDB connected successfully
now..
3) Launch Postman:
	1.Registration:
	  localhost:7000/api/auth/register
	  in body select xxx-url-encoded,
	  fill name,email and password to respective values
	  It is a post request ..Replace with get
	  Click send...
	  a json code will come indicating a profile object...we can add a profile pic too
	  Just created a user profile as a student..

	2.login :
	localhost:7000/api/auth/login
	in body select xxx-url-encoded,
	fill email and password with registered values
	It is a post request
	after login you will get a object with succes:true and a TOKEN..
	this token must be copied without inverted commas...=> Bearer..... 

	3.ask question:
	localhost:7000/api/questions
	in Headers fill Authorization with it's value as token that we copied in login request.
	in body select xxx-url-encoded,
	fill textone  with Doubt or question ("textone"!="textone " ) please mind the space
	fill texttwo with a code..
	name can be anything... but fill (Anonymous)
	It is a post request
	send..
	it wll show a object  with a id..(Question id)
textone,texttwo,user(We can track someone if he is having a fun in serious study platform),name(An  anonymous identity)

4. Answers and Upvotes
	localhost:5000/api/questions/upvote/questionid
	We can upvote a question 
	post request and authorization as token of login
	in question object an upvote will be filled with
	id and user both are weird text

	
	localhost:5000/api/questions/answers/questionid
	in Headers fill Authorization with it's value as token that we copied in login request.
	post request,in body xxxl... text and name fill with answer and anonymous name

after sending...Question object will come with updated upvote array and answer array...



We also created a profile as facebook ...
localhost:5000/api/profile
username ,website,country,portfolio,languages..
after posting you will get an object of user...


if it shows app.crash... please change port to anything like 5656



Happy Coding...
