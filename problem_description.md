## Introduction of the problem
We have n **Students** and m **Projects**. Each student rank $k_p$ projects and high rank means they want to work on that project. 
Students also rank $k_s$ other students. High value in this means the student prefer to work with the other. 
Student can only be assigned to 1 project, and each project have upper bound and lower bound for the number of student.

## Terms used to define the problem
$k_p$ is the number of project that each student can rank. <br>
$k_s$ is the number of student that each student can rank. <br>

$P$ is a n $\times$ m matrix that represent the preference of project, $P_{sp}$ represent how much student s want to work on project p. <br>
The value of $P_{sp}$ is integer between $k_p$ and 0. If the value is higher, it indicates that the project is more preferred by the student. <br>

$F$ is a n $\times$ n matrix that represent the preference of project, $F_{ss'}$ represent how much student s want to with student s'. <br>
The value of $F_{ss'}$ is integer between $k_s$ and 0. If the value is higher, it indicates that student s' is more preferred by the student s. <br>

$X$ is a n $\times$ m matrix that represent the assignment of students to projects. <br>
The value of $X_{sp}$ is either 0 or 1. $X_{sp}$ =1 means student s is assigned to project p and $X_{sp}$ =0 represent student s is not assigned to project p. <br>

## Objective and Constrains
#### objective function
$max(\sum_{s=1}^{n} \sum_{p=1}^{m})$
$\sum_{i=1}^{10} t_i$
