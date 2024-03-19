#Student Performance Tracking

##Students:
student_id (Primary Key)
first_name
last_name
date_of_birth
gender
grade_level

##Courses:
course_id (Primary Key)
course_name
course_description
teacher_id (Foreign Key to Teachers table if applicable)

##Teachers (Optional, if tracking teacher information):
teacher_id (Primary Key)
first_name
last_name

##Student_Courses (Many-to-Many relationship between Students and Courses):
student_id (Foreign Key to Students table)
course_id (Foreign Key to Courses table)
enrollment_date

##Assignments:
assignment_id (Primary Key)
course_id (Foreign Key to Courses table)
assignment_name
max_score

##Student_Assignment_Grades (To track grades for each assignment per student):
student_id (Foreign Key to Students table)
assignment_id (Foreign Key to Assignments table)
grade
submission_date