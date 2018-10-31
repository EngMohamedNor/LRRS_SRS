-

The document in this file adapts the IEEE Guide to Software Requirements Specifications (Std 830-1993).


      
1.	INTRODUCTION
The Lab Report Repository Can Handle all the details about Lab reports The details include posting lab reports  and setting deadline for them by teachers  ,  submission of lab reports by students , Marking lab reports . The Lab Report Repository System is an Automated version of manual lab Report management.

1.1 PURPOSE
This SRS Document contains the complete software requirements for the Lab Report Repository system (LRRS) and describes the design decisions, architectural design and the detailed design needed to implement the system. It provides the visibility in the design and provides information needed for software support. New reliable and fast  Lab Report Repository system software with the great customers support. It'll help you with your daily  Lab Report management routines and deliver you from your paperwork.   

1.2 SCOPE
The Lab Report Repository system is developing for general purpose and used to replace old paper work and email based systems .This system increases the efficiency of lab report submission and result reporting for both teachers and students. The system will allow the teacher to Publish lab reports, set deadline for them , extend the the deadline for sick students and also to publish the results for students. and for students the system will allow for them to submit lab reports through the system in confidence way and to view results of their work when published by teachers.
This system will benefit both the students and teachers and the institution in general and it reduces the headaches related to Lab report publication and submission ,the students will get a centralized location for all their lab report assignments and they will not miss any assignment.


1.3  DEFINITIONS, ACRONYMS, AND ABBREVIATIONS
LRRS  -  Lab Report Repository system.
PHP     -  server side scripting language
SRS      -  Software Requirements Specification
SQLite -  relational database management system 
IEEE   - The Institute of Electrical and Electronics Engineers, Inc.

1.4 REFERENCES
(a)	‘Software Engineering’ by K.K. Aggarwal & Yogesh Singh, New Age Publishing House, 2nd Ed.
(b)	IEEE Recommended Practice for Software Requirements Specifications – IEEE Std 830-1998.
(c)	IEEE Standard for Software Test Documentation – IEEE Std. 829-1998.

2.	Overall Description
The Lab Report Repository system allows authorized admin members to create courses ,Student and teacher account, assign courses for teachers . The registered teachers can post Lab reports through the system and set deadlines for them. The students registered in a course can get all lab report assignments posted by teachers and can submit their work through the system. The teacher can post results for students. This system  Can be used in various educational institutes across the globe and simplifies work of institutes.





2.1. Product Perspective
The proposed system shall be developed using client/server architecture and be compatible with  both Linux and Microsoft Windows Operating System. The front end of the system will be developed using  PHP  and backend will be developed using  SQLite . 
2.1.1. System Interfaces
None
2.1.2. User Interfaces
The LRRS will have following user-friendly and menu driven interfaces
a.	Login: to allow the entry of only authorized users through valid login email and password.
b.	Create Teachers : to create Teachers by the Administration.
c.	Register Students : to register new Students by the Administration.
d.	Create Courses : to Create courses by  the Administration.
e.	Join Course : to Register at specific course by students using course ID.
f.	Accept Students : To Accept students joining specific Course  by teachers
g.	Post Lab Report: to post new Lab report and assign deadline for it by Teachers.
h.	Update deadline : to update deadline for specific students(sick students) or for all by teachers
i.	Lab Report Submission : to Submit lab report before the deadline by students.
j.	Lab Report Result Posting : to Post Lab results for students (Done by Teachers)
k.	View Lab Report Result :  to view lab report results by Students 
l.	Notification Panel : to notify  teachers for the lab report submissions by their students and to notify students for Newly posted Lab reports in the courses they already joined.
m.	Logout : Securely logout form the system and end your session.(by All logged users)



2.1.3. Hardware Interfaces
a)         Screen resolution of at least 640 x 480 or above.
c)        Computer and mobile systems will be in the networked environment as it is a multi-user system.

2.1.4. Software Interfaces
a)   MS-Windows or Linux Operating System 
b)   XAMPP Web Server
c)   SQLite for backend
d)   PLATEFORM : PHP SCRIPTING LANGUAGE
e)    INTEGRATED DEVELOPMENT ENVIRONMENT(IDE): NOTEPAD++

2.1.5. Communication Interfaces
None
2.1.6. Memory Constraints
At least 4 GB RAM and 500 GB space of hard disk will be required to run the software. The hard disk requirement may be increased based on the Number of students using the system and the system will provide alerts about disk space availability.

2.1.7. Operations
None



2.1.8. Site Adaptation Requirements
The terminal at client site will have to support the hardware and software interfaces specified in the section 2.1.3 and 2.1.4 respectively.

2.2. Product Functions
The LRRS will allow access only to authorized users with specific roles (System administrator, Teacher and Student). Depending upon the user’s role, he/she will be able to access only specific modules of the system. 
A summary of major functions that the LRRS will perform
	A login facility for enabling only authorized access to the system.
	System administrator will be able to add, modify or delete Teachers, students and courses
	Students will be able to Joint courses and submit lab reports 
	System administrator will be able to generate reports.

2.3. User Characteristics
	Qualification: At least matriculation and comfortable with English.
	Experience: Should be well versed/informed about the registration process in courses.
	Technical Experience: Elementary knowledge of computers

2.4. Constraints
	There will only be one administrator.
	The delete operation is available only to the administrator. 
To reduce the complexity of the system, there is no check on delete operation. Hence, administrator should be very careful before deletion of any record and he/she will be responsible for data consistency.

2.5	Assumptions and Dependencies
	The login Id and password must be created by system administrator and communicated  to the concerned user confidentially to avoid unauthorized access to the system.
	It is assumed that a student registering for Courses has paid desired university fee. 
	Registration process  for courses will be open only for specific duration.

        2.6  Apportioning of Requirements
                Not Required

3.1.1	Hardware Interfaces
As stated in Section 2.1.3

3.1.2	Software Interfaces
As stated in Section 2.1.4

3.1.3	Communication Interfaces
None

3.2 Functional Requirements
     3.2.1 LOGIN 
     A. Use Case Description

	1  Introduction
    This use case documents the steps that must be followed in order to log into the  
     LRRS.
	2  Actors
Administrator
Student 
Teacher
3  Pre-Condition
  The user must have valid login Id and password.
4 . Post Condition
  If the use case is successful, the actor is logged into the system. if not, the system    
   state remains unchanged.

   5.  Basic Flow
Starts when actor wishes to login onto the LRRS.
i.	The system requests that the actor specify the function he/she would like to perform (either Login, Change Password)
ii.	Once the actor provides the requested information, one of the sub flows is executed.
•	If the actor selects “Login”, the Login sub flow is executed.
•	If the actor selects “Change Password”, the Change Password sub flow is executed.

