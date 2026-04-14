# University DB

## entities
- Departments
- Degree Programs
- Courses
- Professors
- Students
- Exams

## tabs

### departments
- id (INT - PK - NOTNULL, UNIQUE, AUTO_INCREMENT)
- name (VARCHAR(50) - NOTNULL)

### degree_programs
- id (INT - PK - NOTNULL, UNIQUE, AUTO_INCREMENT)
- name (VARCHAR(50) - NOTNULL)
- department_id (INT - FK - NULL) 

### courses
- id (INT - PK - NOTNULL, UNIQUE, AUTO_INCREMENT)
- name (VARCHAR(50) - NOTNULL)
- credits (INT - NULL)
- degree_program_id (INT - FK - NULL)

### professors
- id (INT - PK - NOTNULL, UNIQUE, AUTO_INCREMENT)
- name (VARCHAR(50) - NOTNULL)
- surname (VARCHAR(50) - NOTNULL)
- title (VARCHAR(20) - NULL)
- department_id (INT - FK - NULL)

### students
- id (INT - PK - NOTNULL, UNIQUE, AUTO_INCREMENT)
- name (VARCHAR(50) - NOTNULL)
- surname (VARCHAR(50) - NOTNULL)
- degree_program_id (INT - FK - NULL)

### exams
- id (INT - PK - NOTNULL, UNIQUE, AUTO_INCREMENT)
- date (DATE - NOTNULL)

#### course_student
- id (INT - PK - NOTNULL, UNIQUE, AUTO_INCREMENT)
- student_id (INT - FK - NOTNULL)
- course_id (INT - FK - NOTNULL)

#### exam_student
- id (INT - PK - NOTNULL, UNIQUE, AUTO_INCREMENT)
- student_id (INT - FK - NOTNULL)
- exam_id (INT - FK - NOTNULL)
- status (VARCHAR(20) - DEFAULT(enrolled))
- grade (VARCHAR(15) - NULL)

#### course_professor
- id (INT - PK - NOTNULL, UNIQUE, AUTO_INCREMENT)
- course_id (INT - FK - NOTNULL)
- professor_id (INT - FK - NOTNULL)

