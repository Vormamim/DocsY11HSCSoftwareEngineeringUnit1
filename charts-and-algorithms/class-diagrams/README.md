---
icon: book-open
---

# Class Diagrams

Class diagrams provide a visual representation of systems that are implemented using the object-oriented paradigm. They model classes, their attributes and methods, and the relationships between classes.

In software engineering, class diagrams are essential tools for planning and understanding the structure of an application. They help developers and stakeholders visualise how different components of a system interact and how data flows between these components.

A class diagram typically consists of several classes, each represented as a rectangle divided into three sections: the top section contains the class name, the middle section lists the attributes (or properties) of the class, and the bottom section shows the methods (or functions) that operate on the attributes.

<figure><img src="../../.gitbook/assets/image (53).png" alt=""><figcaption><p>From HSC Course Specifications</p></figcaption></figure>

The relationships between classes in a class diagram are depicted using various types of lines, each representing a different type of relationship. These relationships help developers understand how objects in the system are connected, how they interact, and how changes in one class may affect others.

By using class diagrams, developers can effectively plan and communicate the structure of a software system, ensuring that all team members have a shared understanding of the system's architecture. They are not only useful during the design phase but also serve as valuable documentation that can be referred to throughout the software development lifecycle. This helps in maintaining the system, extending its functionality, and onboarding new team members.

## Example

<figure><img src="../../.gitbook/assets/image (54).png" alt=""><figcaption><p>From HSC Course Specifications</p></figcaption></figure>

In the above school management system:

* Each **Person** has the attributes **firstName** and **lastName**, and the **printFullName()** method will display these.
* Both a **Student** and **Parent** will **inherit** attributes from **Person** (parents and students all have full names).&#x20;
* Each **Parent** has an **occupation** and information on whether they are **alumni** (true/false)**.**&#x20;
* Each **Student** has a **studentID** and a **homeroom.** Each student can be enrolled into a class with the **enrolClass()** method.
* Each **Subject** has **1 or more studentIDs** and a **subjectName.** Each subject can display the list of students with the **printStudentList()** method.
* Each **Student** has **1 or more Subjects.**
* Each **Subject** has **0 or more Students.**

