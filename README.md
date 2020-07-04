# Project-FormGiant
FormGiant Project
Instructions for Running app

Form Giant Project
Steps to run the project


Step 1 : Set up the environment :

1.1	Download MySQL  https://dev.mysql.com/downloads/installer/

1.2	Import below attached database schema in your database instance.

Details steps to import follow :
 https://dev.mysql.com/doc/workbench/en/wb-admin-export-import-management.html


 

OR 

Just execute below queries to create tables:

1.	CREATE DATABASE employeedb;
2.	
CREATE TABLE IF NOT EXISTS `custom_servey` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `emp_id` int(11) NOT NULL,
  `field_name` varchar(128) NOT NULL,
  `field_type` varchar(11) NOT NULL,
  `field_value` varchar(256) NOT NULL,
  PRIMARY KEY (`id`),
  KEY `emp_id` (`emp_id`)
) AUTO_INCREMENT=1 ;



3.	
CREATE TABLE IF NOT EXISTS `employee` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `first_name` varchar(512) NOT NULL,
  `last_name` varchar(512) NOT NULL,
  `emp_id` int(11) DEFAULT NULL,
  `emp_age` int(11) DEFAULT NULL,
  `emp_salary` double DEFAULT NULL,
  `emp_address` varchar(512) DEFAULT NULL,
  `survey_status` varchar(11) NOT NULL DEFAULT 'PENDING',
  PRIMARY KEY (`id`)
) ENGINE=InnoDB  DEFAULT CHARSET=latin1 AUTO_INCREMENT=21 ;


4.	ALTER TABLE `custom_servey`
  ADD CONSTRAINT `servey_emp_fk` FOREIGN KEY (`emp_id`) REFERENCES `employee` (`id`) ON DELETE CASCADE ON UPDATE CASCADE;


Execute above all four queries from MySQL command line.



















Steps 2  : Import Project in your IDE, I am using NetBeans .

2.1 Import :
 

2.2 Open DatabaseManager.java as shown in below screenshot and provide host, dbName, user and password of your MySQL Instance.

 


2.3 Navigate to FormGiantProject.java now as per below screenshot
 


2.4 Right click on the project as I was doing in demo and run the project.

3. Project Usage:

3.1 First login from Administrator
3.2 Create Employees
3.3 Click on the each employee to see their respective custom form, initially they will be empty as user have not created custom forms.
3.4 Exit project and re-run
3.5 Now login using some other user
3.6 After login, click on the row in table and on right side buttons to add row & remove row to custom forms will enable
3.7. Enter Field Name, type, value and click + Row
3.8 Repeat same for all users.
3.9 Login from Administrator to do sum & avg for employees.
3.10 Check user name for which you want sum and avg and click calculate.

Developers:

Lynnesha Cadogan, Dwayne Edwards, Tawana Wilson and LoReese Cummings

