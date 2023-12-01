# A bit more CSharp and SQL
1. What does ***inheritance*** accomplish for us in C#?

  > | allows the characteristics and behaviors of another base/parent class to follow through to the derived child. Promotes scalability and reusability by modular design |

2. How does ***member inheritance*** work in C#? Does a `Class` inherit all members of the base `Class`?

  > | not all, only those permitted by accessibility level. Additionally, from a derived class, an `override` can be included to override base class members and implement its own version |

3. How does ***accessibility*** affect inheritance?

> | affects visibilty and thereby usage in the overall system.
> Public: accessible from outside the class heirarchy;
> Internal: accessible from within the same assembly, if the derived class is in the same base class;
> Protected: accessible within the class and its derived classes;
> Private: not directly accessible in derived classes, specific to the declaring class. |

4. What is the difference between a `PRIMARY KEY` and a `FOREIGN KEY`

  > | `PRIMARY KEY` refers to the unique id being used to identify an entry of data on a table. `FOREIGN KEY` is a column that refers to an entry in another table, creating an association between the two tables |

5. What is an ***alias***?

  > | a temp name to reference a table or column  |

6. Demonstrate how you would query a join statement that would get all of a doctors patients from the following collections:

  ```SQL
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

  CREATE TABLE patient_doctors (
    id INT NOT NULL AUTO_INCREMENT,
    doctorId INT NOT NULL,
    patientId INT NOT NULL,

    FOREIGN KEY (doctorId)
      REFERENCES doctors(id),
    FOREIGN KEY (patientId)
      REFERENCES patients(id),
  )

  ```

  > |
> technically if just returning a list of patients by a doctor, this works I believe:
```
SELECT
p.*
FROM patients p
JOIN patient_doctors pd ON p.id = pd.patientId
WHERE pd.doctorId = @doctorId;
```
But
```
SELECT
p.*
FROM patients p
JOIN patient_doctors pd ON p.id = pd.patientId
JOIN doctors d ON d.id = pd.doctorId
WHERE d.id = @doctorId;
```
If wanting to additionally format/provide doctor specific information on each patient record
 |






 
