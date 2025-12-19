# SQL-Joins
A complete Code of SQL joins and mention all basic code . this is done with my self learning skill .


CREATE TABLE student (
    id CHAR(2) NOT NULL PRIMARY KEY,
    name VARCHAR(24)
);

INSERT INTO student values (1 , "suma" );
INSERT INTO student values (2 , "vasu" );
INSERT INTO student values (3 , "indhu" );
INSERT INTO student values (4 , "appu" );
INSERT INTO student values (5 , "ajay" );

select * from student;

CREATE TABLE course (
 id INT,
 course VARCHAR(50)
 );
  
  INSERT INTO course values 
  (3 , "Accounting"),
  (5 , "Acting"),
  (6 , "Maths"),
  (7 , "Science");
  
  select * from course;
  
**  1 INNER JOIN**
  
select student.id, student.name, course.course
  from student
  inner join course
  on student.id = course.id;
  
 ** 2 LEFT JOIN**
  
select student.id,student.name, course.course
  from student
  left join course
  on student.id = course.id;
  
**  3 RIGHT JOIN**
  
select student.id, student.name , course.course
from student
right join course
on student.id = course.id;

**4 FULL JOIN**

select student.id,student.name, course.course
  from student
  left join course
  on student.id = course.id
  Union
select student.id, student.name , course.course
from student
right join course
on student.id = course.id;

**5 CROSS JOIN **

select student.id, student.name, course.course
from student
cross join course;

6 SELF JOIN

Select s1.id As student1_id,
s1.name as student1_name,
s2.id as student2_id,
s2.name as student2_name
from student s1
join student s2
on s1.id <> s2.id;





