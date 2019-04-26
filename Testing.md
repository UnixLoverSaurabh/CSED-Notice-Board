--------------------------Unit testing-----------------

 -----------Signup-----------
test cases-
1a.
Username:Rohit
Email:rohit
password:123
Confirm password:123
Output:Successfully submitted
comment:error should generate due to invalid email

1b.     
Username:Rohit
Email:rohit
password:123
Confirm password:123

Output:You must enter a valid Email
-modified using Datatype Email 

2a.
client change the webpage sorce code,change the email type   
Username:Sonu
Email:sonu
password:12
Confirm password:12
Output:Successfully submitted
comment:error should generate due to invalid email

2b.     
Username:Rohit
Email:rohit
password:123
Confirm password:123

Output:You must enter a valid Email
-modified using php validation 

3.
Username:R
Email:r@g
password:1
Confirm password:1

Output:Successfully submitted
comment:error should generate due to invalid email

4.
Username:p
Email:r@1
password:1
Confirm password:1

Output:Successfully submitted
comment:error should generate due to invalid email

5.
Username:o
Email:1@1
password:1
Confirm password:1

Output:Successfully submitted
comment:error should generate due to invalid email

6.
Username:k
Email:1@2.5
password:1
Confirm password:1

Output:Successfully submitted
comment:error should generate due to invalid email

7.
Username:1
Email:a@b.com
password:12
Confirm password:12

Output:Successfully submitted
comment:error should generate due to invalid Username

8.
Username:1234
Email:c@d.com
password:122
Confirm password:122

Output:Successfully submitted
comment:error should generate due to invalid Username

9.
Username:aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa(360)
Email:c@d.com
password:122
Confirm password:122

Output:Successfully submitted
comment:error should generate due to maximum Username length
modified: By  limiting username size
10.
Username:*
Email:a@b.com
password:12
Confirm password:12

Output:Successfully submitted
comment:error should generate due to invalid Username

11.
Username:bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb(160)
Email:n@t.com
password:1
Confirm password:1

Output:Successfully submitted
comment:error should generate as large Username length.
modified: By  limiting username size

12.
Username:rohit
Email:m@b.com
password:/
Confirm password:/

Output:Successfully submitted
comment:error should generate due to Small length password

13.
Username:rahul
Email:o@b.com
password:12	
Confirm password:21

Output:password and Confirm password does not matched.

14.
Username:nishant
Email:nishant@gmail.com
password:122	
Confirm password:122

Output:Successfully submitted.

15.
Username:pratik
Email:pratik@gmail.com
password:1223	
Confirm password:1223

Output:Successfully submitted.

16.
Username:sunny
Email:p@s.com
password:12	
Confirm password:12

Output:Successfully submitted.

17.
Username:sunny
Email:w@e.com
password:12	
Confirm password:12

Output:Username already exist 

18.
Username:rituraj
Email:s@s.com
password:12	
Confirm password:12

Output:Email already exist

19.
-password not secure due to size
-maximum limi for username is too high, modified to max length of 15         	

     -------login page---------
1.Mysql injection
	-By removing sql injection

Input:
	Username: 1==1'
	password: 1==1'

Output:
	Successful login message displayed
Comment: 
	unauthorized login
Solution:
	Removing special characters	

2.
Username:aaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaaa(360)
password:122
output: incorrect password or username	
comment:successfully signed up using this username but generate login error
modified: By  limiting username size		

3.
Username:bbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbbb(160)
password:1

Output:Successfully loggedin
comment:GUI problem occur due to high user length.
modified: By  limiting username size

3.
Username:sunny
password:1

Output:Successfully loggedin

4.
Username:nishant
password:122

Output:Successfully loggedin

5.
Username:pratik
password:123

Output:Successfully loggedin

6. No size limit for password 	
7. No forgot password facilities.

--------Home page-----
-Notification icon not in use.
-user profile picture  

---------create a new event----
1a.
Title:athletics
Description of the event:marathon race
Venue of the event:play-ground
Date for the event :26-Apr-18	
Time of the event:5:51AM

output:Successfully added event.
comment:Old date even also uploded.
modified:Admin validation,will not approve this event.            

1b.
Title:athletics
Description of the event:marathon race
Venue of the event:play-ground
Date for the event :26-Apr-18	
Time of the event:5:51AM

output:Successfully added event.
comment:            


2.
Title:1
Description of the event:1
Venue of the event:1
Date for the event :26-Apr-19	
Time of the event:5:51AM

output:Successfully added event.
comment:anyone can uplode fake Event.
modified:Admin verification to approve Event then event is broadcast.            

3.
Title:1
Description of the event:1
Venue of the event:1
Date for the event :26-Apr-19	
Time of the event:5:51AM

output:Successfully added event.
comment:Same event is upload twice without any error.

4a.
Title:1
Description of the event:1
Venue of the event:1
Date for the event :26-Apr-19(manual entry)	
Time of the event:5:51AM(manual entry)

modified by: calander is viewed for date,Option fot time

4b.
Title:1
Description of the event:1
Venue of the event:1
Date for the event :26-Apr-19(mouse select)	
Time of the event:5:51AM(mouse select)



----------Event Calander-----
GUI problem:March,June

--------Broadcast-------
1.Old date event remains in Broadcast.
	-modified:comparing date.
2.scroll problem 
	-modified by: no scroll problem
3.click on joined: event displayed on joined page

------Joined-------
scroll problem 
modified by: no scroll problem
click on Leave: shown on Broadcast page



-----------------------Integration testing---------------
-----register--
1.click on register ->Successful redirect to Login page

----login-----
1.click on login ->Successful redirect to index.php page.

---Broadcast---
1.click on join->corresponding notice displayed on joined.

---Joined---
1.click on Leave ->notice will removed from joined 

--------------------------System testing----------------------
1.no mobile compatible
  modified by: mobile compatible.
  Project has been tested on mobile(IOS,Android).
2.Project has been tested on tablete.
3.Project has been tested on Windows operating system.
4.Project has been tested on Linux enviroment.
5.Project has been tested on Microsoft Edge(more compatible),Chrome,Firefox.

---------------------------Acceptance testing-------------------
1.Admin verification for adding new event in database. 
2.Signup/login.
3.Broadcast and Joined facility.
4.View calander.  
5.Event can be created by any user.


blackbox testing
adhoc testing