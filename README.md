# Blog_Internet_Technologies_Project
This project was submitted as part of my requirements for the course [Advanced Internet Technologies (2008)](http://moodle.cs.huji.ac.il/cs08/course/view.php?id=67707). It was done using HTML, js, jsp, css, and servlets.

User Guide:
 
 installation:
 	1)http://localhost:8080/BLOG/IDS?username=user&password=pass
 	(user = your username, pass = whatever you like)
 	2)http://localhost:8080/BLOG/index.html
 		enter the user and pass you wrote before.
 		 
 	- DirectAccessServlet URL: http://localhost:8080/BLOG/DBAS
Notes:
	- The add post opens by click on add post on the side bar.
	- The add user opens in the same way.
	- You can see comments by clicking on number of comments on each post.
	- You can also click on the title/ date of the post and it will open on 
	  a new page. 
	- most of the features toggle (are viewed and hidden by clicking on them).
	
Theme:
	- Traveling and cultures.
	
Names of all the DB tables:
	I created 2 tables:
	one for users: CREATE TABLE users( 
				  username varchar PRIMARY  KEY,
				  password varchar NOT NULL)
	and another for posts and comments:
				  CREATE TABLE posts (
					id varchar PRIMARY  KEY,
					title text,
					creation_date timestamp without time zone NOT NULL,
					added_by text REFERENCES users(username),
					parent	varchar REFERENCES posts(id) ON DELETE CASCADE,
					content text,
					comments_num integer)
Bonus:
1)  New screen that enables an existing user to add a new user to the User table.
2)  Delete comments.
3)  Using a filter to prevent access to the webpages.
4)  encrypt the password using MD5 (Message-Digest algorithm 5) 
5)  Logout.


Enjoy!
					

