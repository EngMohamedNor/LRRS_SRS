=========================================================================================================
**-**
=========================================================================================================
*the document in this file adapts the ieee guide to software requirements specifications (std 830-1993).*
\ 
\ 
\ 
**mnc/md**
**10/31/2018**
\ 
=========================================================================================================

**Table of contents**

1. Introduction 21.1 purpose 21.2 scope 21.3 definitions, acronyms, and
abbreviations 31.4 references 31.5 overview 2. The overall description
32.1 product perspective 42.1.1 system interfaces 42.1.2 interfaces
42.1.3 hardware interfaces 52.1.4 software interfaces 52.1.5
communications interfaces 52.1.6 memory constraints 52.1.7 operations
52.1.8 site adaptation requirements 62.2 product functions 62.3 user
characteristics 62.4 constraints 62.5 assumptions and dependencies 72.6
apportioning of requirements 73. Modeling Requirements 73.1 external
interfaces 7 *3.2 functional requirements 8*

**1. Introduction**

The lab report repository can handle all the details about lab reports.
The details include posting lab reports and setting deadline for them by
lecturers , submission of lab reports by students , marking lab reports
. The lab report repository system is an automated version of manual lab
report management.

   **1.1 Purpose**

This SRS document contains the complete software requirements for the
lab report repository system (LRRS) and describes the design decisions,
architectural design and the detailed design needed to implement the
system. It provides the visibility in the design and provides
information needed for software support. New reliable and fast lab
report repository system software with the great customers support.
It'll help the daily lab report management routines and deliver its
users from the paperwork.

**1.2 Scope**

The lab report repository system is developing for general purpose and
used to replace old paperwork and email based systems . This system
increases the efficiency of lab report submission and result reporting
for both lecturers and students. The system will allow the lecturer to
publish lab reports, set deadline for them , extend the deadline for
sick students and also to publish the results for students. For students
the system will allow them to submit lab reports through the system in
convenient way and to view results of their work when published by
lecturers.

This system will benefit both the students and lecturers and the
institution in general and it reduces the headaches related to lab
report publication and submission. Tthe students will get a centralized
location for all their lab report assignments and they will not miss any
assignment.

**1.3 Definitions, acronyms, and abbreviations**

**LRRS -** Lab Report Repository System.

**PHP -** Server Side Scripting language

**SRS -** Software requirements Specification

**MySQL -** Relational Database Management System 

**IEEE -** The institute of electrical and electronics engineers, inc.

**TA** - Teaching Assistant.

**2. Overall description**

The lab report repository system allows authorized admin members to
create courses ,student lecturer, and TA accounts, assign courses for
lecturers . The registered lecturers can post lab reports through the
system and set deadlines for them. The students registered in a course
can view all lab report assignments posted by lecturers in that course
portal and can submit their work through the system. The lecturer can
post results for students. This system can be used in various
educational institutes across the globe and simplifies work of
institutes.

**2.1. Product perspective**

The proposed system shall be developed using client/server architecture
and be compatible with both Linux and Microsoft windows operating
system. The system will be developed using PHP as web scripting language
and MySQL as the backend database.

**2.1.1. System interfaces**

**None**

**2.1.2. User interfaces**

**The LRRS will have the following user-friendly and menu driven
interfaces**

a. Login: to allow the entry of only authorized users through valid
   login email or student id and password.

b. Create lecturers : to create lecturers by the administration.

c. Students registration: students can register with their passport
   number & student id

d. Student groups : create course groups for group assignments , one
   student creates group (he/she will be the group admin) and then
   invites others to join, and other students could accept/reject the
   group invite.

e. Create courses : to create courses by the administration or
   lecturers.

f. Join course : to register at specific course by students using course
   id.

g. Accept students : to accept students joining specific course by
   lecturers & TAs. The member acceptance step can be disabled in course
   portal setting by the lecturer.

h. Post lab report: to post new lab report and assign deadline for it by
   lecturers.

i. Update deadline : to update deadline for specific students(sick
   students) or for all by lecturers.

j. Lab report submission : student can submit his/her lab report
   individually or for his group (if he/she is the group admin) before
   the deadline.

k. Lab report result posting : to post lab results for students (done by
   lecturers & TAs)

l. View lab report result : to view lab report results by students

m. Notification panel : to notify lecturers for the lab report
   submissions by their students and to notify students for newly posted
   lab reports in the courses they already joined.

n. Visitor portal : visitors can see public lab reports without
   authentication.

o. 

..

   **2.1.3. Hardware interfaces**

   A) Screen resolution of at least 640 x 480 or above.

   C) Computer and mobile systems will be in the networked environment
   as it is a multi- user system.

   **2.1.4. Software interfaces**

   A) Ms-windows or Linux operating system

   B) EasyPHP web server

   C) MySQL database for backend

   D) Platform : PHP scripting language

   E) Integrated Development Environment(IDE): Sublime

   **2.1.5. Communication interfaces**

   **None**

   **2.1.6. Memory constraints**

   At least 4 GB ram and 500 GB space of hard disk will be required to
   run the software. The hard disk requirement may be increased based on
   the number of students using the system and the system will provide
   alerts about disk space availability.

   **2.1.7. Operations**

   None

   **2.1.8. Site adaptation requirements**

   The terminal at client site will have to support the hardware and
   software interfaces specified in the section 2.1.3 and 2.1.4
   respectively.

**2.2. Product functions**

The LRRS will allow access only to authorized users with specific roles
(system administrator, lecturer, TA and student). Depending upon the
user’s role, he/she will be able to access only specific modules of the
system. Visitors can only view public reports without the need for
authorization. The administrator creates lecturers , TA user accounts
and course portals. Administrator assigns lecturer and TA to each course
portal. To make the system more flexible we will allow the lecturer to
create his/her own course portals. Students create their user accounts
using their student id and Passport/ID numbers. Once student creates his
own user account he/she can browse course portals in the system and join
them. Based on the setting for each course portal (managed by the its
lecturer) the joining may require to be accepted by the lecturer. The
lecturer posts lab reports inside course portals and the students can
view/download them and submit their work for the lab report through the
system.

**A summary of major functions that the LRRS will perform**

-  A login facility for enabling only authorized access to the system.

-  System administrator will be able to add, modify or delete lecturers,
   students and courses

-  Lecturer will be able to post lab reports in course portals and mark
   student submissions.

-  Students will be able to join courses and submit lab reports

**2.3. User characteristics**

-  Qualification: at least matriculation and comfortable with English.

-  Experience: should be well versed/informed about the registration
   process in courses.

-  Technical experience: elementary knowledge of computers

**2.4. Constraints**

-  There will only be one administrator.

-  The delete operation is available only to the administrator.

   To reduce the complexity of the system, there is no check on delete
   operation. Hence, administrator should be very careful before
   deletion of any record and he/she will be responsible for data
   consistency.

**2.5 Assumptions and dependencies**

-  The login id and password must be created by system administrator and
   communicated to the concerned user confidentially to avoid
   unauthorized access to the system.

-  It is assumed that a student registering for courses has paid desired
   university fee.

**2.6 Apportioning of requirements**

Not required

**3. Modeling Requirements**

**3.1 UML Use Case Diagram**

**3.1.1 : Use Case diagram**

The purpose of this diagram is to demonstrate how objects will interact
with LRRS and map out the basic functionality of the system.

Main actors

I.   Administrator

II.  Student

III. Lecturer

IV.  |image0|\ Visitor

**3.1.2 : Use Case Descriptions**

1) **Use Case:** Login

**Actors:** Admin, Lecturer, TA, Student

**Type:** Primary and essential

**Description:** Initiated when a user attempts an action that is
restricted. The user is then prompted to enter in their username and
password in order to proceed.

2) **Use Case:** Create Course Portals

**Actors:** Admin , Lecturer

**Type:** Primary and essential

**Description:** Allows admin and lecturer to create course portals.

3) **Use Case:** Post lab reports

**Actors:** Lecturer

**Type:** Primary and essential

**Description:** Allows the lecturer to post new lab report in a course
portal.

4) **Use Case:** Manage lab report deadline

**Actors:** Lecturer

**Type:** Primary and essential

**Description:** Allows the lecturer to manage lab report deadline for
all students or for specific student.

5) **Use Case:** Evaluate lab report submissions

**Actors:** Lecturer

**Type:** Primary and essential

**Description:** Allows the lecturer to evaluate and mark lab report
submissions in course portals.

6) **Use Case:** Accept students joining course portals

**Actors:** Lecturer

**Type:** Secondary

**Description:** Allows the lecturer to accept students joining his/her
course if the new portal members are to required to get acceptance for
the teacher according to portal's setting.

7) **Use Case:** Register in the system

**Actors:** Student

**Type:** Primary and essential

**Description:** Allows students to create their own user accounts in
the system using their student id and passport/id numbers.

8) **Use Case:** Join Course

**Actors:** Student

**Type:** Primary and essential

**Description:** Allows students to join course portals to view and
submit lab reports.

9) **Use Case:** Create/join Course groups

**Actors:** Student

**Type:** Primary and essential

**Description:** Allows students to Create or join groups in course
portals so that students can submit group lab reports.

10) **Use Case:** Submit lab report

**Actors:** Student

**Type:** Primary and essential

**Description:** Allows students to submit lab report to the lecturer in
course portals.

11) **Use Case:** View lab reports results

**Actors:** Admin

**Type:** Primary and essential

**Description:** Allows the students to check results posted by the
lecturer for their lab report submissions.

12) **Use Case:** View public lab reports

**Actors:** Visitor

**Type:** Primary and essential

**Description:** Allows visitors to view public lab reports without the
need for authentication.

**3 . 2 Database diagram**

|image1|\ The database schema is the blueprints of the system database,
it represents the description of a database structure, data types, and
the constraints on the database. The database will consist of 10 tables.

**4. References**

   (a) ‘Software Engineering’ by k.k. Aggarwal & yogesh singh, new age
   publishing house, 2\ :sup:`nd` ed.

   (b) IEEE recommended practice for software requirements
   specifications – IEEE std 830-1998.

   (c) IEEE standard for software test documentation – IEEE std.
   829-1998.

.. |image0| image:: media/image1.png
   :width: 7.14583in
   :height: 6.01042in
.. |image1| image:: media/image2.png
   :width: 7.72917in
   :height: 4.02083in
