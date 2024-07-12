# University-Management-System
#mysql project
MYSQL, SQL, JDBC

I have made all the required data bases in MySQL.

* There are database is university_reg_system having below tables - 

+---------------------------------+
| Tables_in_university_reg_system |
+---------------------------------+
| 1) academicprogram              |
| 2) classschedule                |
| 3) course                       |
| 4) enrollment                   |
| 5) faculty                      |
| 6) prerequisites                |
| 7) student                      |
| 8) v_coursecode                 |
+---------------------------------+

1) academicprogram-
   Query - 
   mysql> select * from academicprogram;
+-----------+----------------------------------+
| ProgramID | ProgramName                      |
+-----------+----------------------------------+
|       101 | Computer Science and Engineering |
|       102 | Electrical Engineering           |
|       103 | Mechanical Engineering           |
|       104 | Biotechnology                    |
|       105 | Civil Engineering                |
|       106 | Chemical Engineering             |
|       107 | Mathematics                      |
|       108 | Physics                          |
|       109 | Chemistry                        |
|       110 | Economics                        |
+-----------+----------------------------------+
10 rows in set (0.02 sec)

2) classschedule -
   Query -
   mysql> select * from classschedule;
+------------+------------+-----------+---------------------+-----------+
| ScheduleID | CourseCode | Day       | TimeSlot            | Location  |
+------------+------------+-----------+---------------------+-----------+
|          1 | CS101      | Monday    | 10:00 AM - 12:00 PM | Room 101  |
|          2 | EE201      | Wednesday | 2:00 PM - 4:00 PM   | Room 201  |
|          3 | MECH301    | Tuesday   | 9:00 AM - 11:00 AM  | Room 301  |
|          4 | BT101      | Thursday  | 1:00 PM - 3:00 PM   | Room 401  |
|          5 | CE101      | Friday    | 11:00 AM - 1:00 PM  | Room 501  |
|          6 | CHEM201    | Monday    | 1:00 PM - 3:00 PM   | Room 601  |
|          7 | MATH301    | Wednesday | 10:00 AM - 12:00 PM | Room 701  |
|          8 | PHY201     | Thursday  | 3:00 PM - 5:00 PM   | Room 801  |
|          9 | CHEM301    | Tuesday   | 2:00 PM - 4:00 PM   | Room 901  |
|         10 | ECO101     | Friday    | 9:00 AM - 11:00 AM  | Room 1001 |
+------------+------------+-----------+---------------------+-----------+

3) course-
   Query -
   mysql> select * from course;
+------------+----------------------------------+-------------+--------------+
| CourseCode | Name                             | CreditHours | InstructorID |
+------------+----------------------------------+-------------+--------------+
| BT101      | Introduction to Biotechnology    |           3 |          204 |
| CE101      | Structural Engineering           |           4 |          205 |
| CHEM201    | Organic Chemistry                |           3 |          206 |
| CHEM301    | Analytical Chemistry             |           4 |          209 |
| CS101      | Introduction to Computer Science |           3 |          201 |
| ECO101     | Microeconomics                   |           3 |          210 |
| EE201      | Electrical Circuits              |           4 |          202 |
| MATH301    | Advanced Calculus                |           4 |          207 |
| MECH301    | Thermodynamics                   |           3 |          203 |
| PHY201     | Quantum Physics                  |           3 |          208 |
+------------+----------------------------------+-------------+--------------+
10 rows in set (0.01 sec)

4) enrollment -
   Query -
mysql> select * from enrollment;
+--------------+-----------+------------+--------------+-------+
| EnrollmentID | StudentID | CourseCode | Status       | Grade |
+--------------+-----------+------------+--------------+-------+
|            1 |         1 | CS101      | Enrolled     | NULL  |
|            2 |         2 | EE201      | Not Enrolled | NULL  |
|            3 |         3 | MECH301    | Enrolled     | NULL  |
|            4 |         4 | BT101      | Not Enrolled | NULL  |
|            5 |         5 | CE101      | Enrolled     | NULL  |
|            6 |         6 | CHEM201    | Enrolled     | NULL  |
|            7 |         7 | MATH301    | Not Enrolled | NULL  |
|            8 |         8 | PHY201     | Enrolled     | NULL  |
|            9 |         9 | CHEM301    | Enrolled     | NULL  |
|           10 |        10 | ECO101     | Enrolled     | NULL  |
+--------------+-----------+------------+--------------+-------+
10 rows in set (0.01 sec)

5) faculty-
   Query -
   mysql> select * from faculty;
+-----------+-----------------------+---------------------------+--------------+
| FacultyID | Name                  | ContactInfo               | DepartmentID |
+-----------+-----------------------+---------------------------+--------------+
|       201 | Dr. Anupam Singh      | anupam.singh@email.com    |          101 |
|       202 | Prof. Kavita Reddy    | kavita.reddy@email.com    |          102 |
|       203 | Dr. Prakash Verma     | prakash.verma@email.com   |          103 |
|       204 | Prof. Anjali Gupta    | anjali.gupta@email.com    |          104 |
|       205 | Dr. Rajat Sharma      | rajat.sharma@email.com    |          105 |
|       206 | Prof. Sunita Kumar    | sunita.kumar@email.com    |          106 |
|       207 | Dr. Abhishek Desai    | abhishek.desai@email.com  |          107 |
|       208 | Prof. Meera Choudhury | meera.choudhury@email.com |          108 |
|       209 | Dr. Rohit Reddy       | rohit.reddy@email.com     |          109 |
|       210 | Prof. Preeti Mehta    | preeti.mehta@email.com    |          110 |
+-----------+-----------------------+---------------------------+--------------+
10 rows in set (0.01 sec)

6) prerequisites -
   Query -
mysql> select * from prerequisites;
+--------+-------------+-----------+
| Pre_Id | course_code | ProgramID |
+--------+-------------+-----------+
|      1 | CS101       |       101 |
|      2 | EE201       |       102 |
|      3 | MATH301     |       103 |
|      4 | CE101       |       104 |
|      5 | CHEM201     |       105 |
|      6 | PHY201      |       106 |
|      7 | CHEM301     |       107 |
|      8 | MATH301     |       108 |
|      9 | ECO101      |       109 |
|     10 | BT101       |       110 |
+--------+-------------+-----------+
10 rows in set (0.01 sec)
      
7) student -
   Query -
  
mysql> select * from student;
+-----------+-----------------+---------------------------+-----------+
| StudentID | Name            | ContactInfo               | ProgramID |
+-----------+-----------------+---------------------------+-----------+
|         1 | Amit Sharma     | amit.sharma@email.com     |       101 |
|         2 | Priya Patel     | priya.patel@email.com     |       102 |
|         3 | Rahul Singh     | rahul.singh@email.com     |       103 |
|         4 | Neha Gupta      | neha.gupta@email.com      |       104 |
|         5 | Sandeep Kumar   | sandeep.kumar@email.com   |       105 |
|         6 | Kavita Verma    | kavita.verma@email.com    |       106 |
|         7 | Aniket Reddy    | aniket.reddy@email.com    |       107 |
|         8 | Smita Desai     | smita.desai@email.com     |       108 |
|         9 | Rajat Choudhury | rajat.choudhury@email.com |       109 |
|        10 | Pooja Mehta     | pooja.mehta@email.com     |       110 |
+-----------+-----------------+---------------------------+-----------+
10 rows in set (0.01 sec)

9) v_coursecode -
   Query -
mysql> select * from v_coursecode;
+------------+-------------------+
| courseCOde | name              |
+------------+-------------------+
| MATH301    | Advanced Calculus |
+------------+-------------------+
1 row in set (0.00 sec)

I have fired on each and every query in SQL on this databases to test it.

Thank You.

