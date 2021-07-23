# What is the difference between a primary key and a foreign key?

> Primary Keys are unique identifiers for their own record in a table. Foreign Keys are used on other tables as a reference to their record on a different table.

# What is an Alias?

> It is a reference to one row in a table, used in sql to perform a foreach in js. 

# Demonstrate how you would query a join statement that would get all of a doctors patients from the following collections:

CREATE TABLE doctors (
  id INT NOT NULL AUTO_INCREMENT,
  -- CODE OMITTED
  PRIMARY KEY (id)
)

CREATE TABLE patients (
  id INT NOT NULL AUTO_INCREMENT,
  -- CODE OMITTED
  PRIMARY KEY (id)
)

CREATE TABLE roll (
  id INT NOT NULL AUTO_INCREMENT,
  doctorId INT NOT NULL,
  patientId INT NOT NULL,

  FOREIGN KEY (doctorId)
   REFERENCES doctors(id),
  FOREIGN KEY (patientId)
    REFERENCES patients(id),
)

> SELECT d.*, p.*, r.* FROM roll r JOIN doctors d ON r.doctorId = d.id JOIN patients p ON p.id = r.patientId;

https://github.com/Derek-Wallace/contractor