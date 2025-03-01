Download link :https://programming.engineering/product/project2-normalization-and-query-processing/

# Project2.-Normalization-and-Query-Processing
Project2. Normalization and Query Processing
Package Delivery System

“You are a DBA in this company”

Goal : The goal of this project is to provide a realistic experience in the physical design, query processing implementation and maintenance of a small relational database you made in Project 1.

Application Description (Same as Project 1):

The application is a package delivery company (e.g. FedEx, UPS, DHL, CJ Logistics). The company needs to keep track of packages shipped and their customers. To find out more about this application, think about any experiences you may have had shipping packages and receiving packages, and browse shippers’ web sites.

In our hypothetical company, the manager assigned to solicit database design proposals is not very computer literate and is unable to provide a very detailed specification.

Here are a few points to consider :

There are different kinds of service possibly based upon the type of package(flat envelope, small box, larger boxes), the weight of the package, and the timeliness of delivery (overnight, second day, or longer).

Some customers have a contract with the shipper and bill their shipments to an account number. They are billed monthly. Other customers are infrequent customers and pay with a credit card. Certain shipments are prepaid, as is might be the case of someone is returning something that was purchased by phone or Internet (e.g. returning clothes that don’t fit, or returning malfunctioning electronics, returning damaged book ).

For the most part, the shipping company does not care what is being shipped. However, there are cases where it matters. Some examples include


hazardous materials

international shipments, for which a customs declaration stating the contents and their value is needed

The company needs to track packages from the time the customer drops it off (or it is picked up by the company) until the time is is delivered and signed for. Take a look at the online tracking offered by various shipping companies to get an idea of how this service works. If you are having something shipped to you, you’ll find you can get every little detail of where the package is, where it has been, and to where it is currently headed. Beyond what the customer sees, the company itself needs to know on which truck or plane or warehouse the package is at any point in time.

Tracking is not just an “in the present” issue. The company may want to look back in time and find out where the package was yesterday, for example. It may also want to look at data from the standpoint of a truck or warehouse.

There are other aspects to the operation of the company besides package tracking such as the routing of trucks and planes, the assignment of staff to them, etc. For this project, we’ll consider only the package handling and billing aspects of the database.

Project Requirements :

BCNF Decomposition

Check your logical schema, and decompose your Logical Schema to BCNF form if they are not

Use the same process learned in the lecture.

Every entity and relationship must satisfy the BCNF dependency.

DATABASE SYSTEM PROJECT

3

Physical Schema Diagram

After creating an decomposed logical schema diagram, you must create a Physical Schema diagram.

Create the physical schema diagram using Erwin. Select “Physical” in Erwin data modeler.

Be sure to identify data types, domain, constraints, relationship type, allowing nulls and so far.

Queries

The queries listed below are those that your client (the manager from the package delivery company) wants turned in. They may provide further hints about database design, so think about them at the outset of the project. (A total of 7 different queries)

(Type I) Assume truck 1721 is destroyed in a crash.

(Type I-1) Find all customers who had a package on the truck at the time of the crash. (1)

(Type I-2) Find all recipients who had a package on that truck at the time of the crash. (2)

(Type I-3) Find the last successful delivery by that truck prior to the crash. (3)

(Type II) Find the customer who has shipped the most packages in the past year. (4)

(Type III) Find the customer who has spent the most money on shipping in the past year. (5)

(Type IV) Find those packages that were not delivered within the promised time. (6)

(Type V)Generate the bill for each customer for the past month. Consider

creating several types of bills. (7)

– A simple bill: customer, address, and amount owed.

A bill listing charges by type of service.

An itemize billing listing each individual shipment and the charges for it.

Customers like their bills to be readable. While the client will accept a relational table coming from Oracle as the bill, it would be “nice” to have a good-looking bill.

We should execute these queries within MySQL DBMS what you managed. The customers can check all results from these query execution.

We use ODBC with C language API to implement your Database model (will be discussed in practice session)

4. Code implementation

-We will use Visual Studio 2019(or 2022) and MySQL connector(ODBC)

(To understand about ODBC, read chapter 5 of the textbook. Pg. 194.)

-Implement C code to execute your queries in MySQL DBMS you built

-The program must use file inputs from text file which have CRUD queries as text format (ex. e.g. CREATE, INSERT, UPDATE, DELETE)

-The program has a user interface to handle each TYPE. Program runs until put quit instruction.




-After selecting one type in menu, user puts values of query as stdin and print the result of query execution as stdout.



–Only TYPE I has submenu for subtypes. The submenu should appear when user inputs ‘1’ in the query menu.



-Keep running each type of query until user inputs “0” in stdin. (for all types of query)

– When user inputs 0, the program should go back to the query select menu

What to turn in :

(1) Decomposed Logical Schema Diagram (.png or .jpg)

-Decompose your logical schema you made in project 1 in Erwin. –student_id.png (ex. 20209999.png)

(2) Physical Schema diagram (.erwin)

-Change the decomposed logical schema into a physical schema diagram –student_id.erwin (ex. 20209999.erwin)

3. Program (.zip)

-Describe you code with comment (if necessary)

-It should be able to build and execute in Visual Studio 2019(2022) with MySQL C APL

-Inside the zip file, there should be a code file (.c or .cpp), and text files containing CRUD queries. (And any other files needed to build your program if necessary)

-Zip your whole program folder if possible, for –student_id.zip (ex. 20209999.zip)

4. Report File (.pdf)

-Describe the detail explanation how you decompose each relationship to BCNF, see testing one of your relationship result by simplified test in lecture notes. You need to at least explain all the entities and relationships you changed from project 1.

-Describe the detail explanation about your Physical Schema diagram and ODBC implementation within MySQL that you made.

-MAKE YOUR OWN DESCRIPTION on physical schema and ODBC C language codes.

–[project2]student_id.pdf (ex. [project2]20209999.pdf)

NOTICE :


Submit your soft copy to Cyber Campus. (softcopy includes png, Erwin, code and pdf file you wrote). Check the last page of this document.

Submit your hardcopy to box in front of AS816 before the deadline.

(hardcopy includes everything except the Program file)

DON’T COPY ANYTHING FROM YOUR FRIENDS AND WEB SOURCES. IF YOU VIOLATE THIS, YOU WILL GET F FOR THIS COURSE.

Check the location one more time before you turn in your assignment.


Here is an example of what students should submit to the cyber campus.

A total of 4 files should be submitted.



In the hard copy, all the files except the .zip file should be submitted.
