# ContosoUniversity - Lab 4
Tutorial: Get Started with Entity Framework 6 Code First using MVC 5
- In this project , you will learn how to build an ASP.NET MVC 5 application that uses Entity Framework 6 for data access . This tutorial uses the Code First workflow
- In this project , you will perform the following tasks : 
  - Create an MVC web app
  - Set up the site style
  - Install Entity Framework 6
  - Create the data model
  - Create the database context
  - Initialize DB with test data
  - Set up EF 6 to use LocalDB
  - Create controller and views
  - View the database
  
# BODY  
- Create an MVC web app
  - you need to open the visual studio and create a C# web project using the ASP.NET Web Application (.NET Framework) template . And name of project is ContosoUniversity 
 ![add text](https://github.com/vuhoangg120699/ContosoUniversity/blob/master/ContosoUniversity/Img/1.png) 
  - In New ASP.NET Web Application - ContosoUniversity, you must select MVC and then click OK to create 
  
- Set up the site style
  - you select Views\Shared\_Layout.cshtml, and make the following changes:
    - Change each occurrence of "My ASP.NET Application" and "Application name" to "Contoso University".
    - Add menu entries for Students, Courses, Instructors, and Departments, and delete the Contact entry.
 ![add text](https://github.com/vuhoangg120699/ContosoUniversity/blob/master/ContosoUniversity/Img/2.png)
 
- Next , in Views\Home\Index.cshtml, replace the contents of the file with the following code to replace the text about ASP.NET and MVC with text about this application:
 ![add text](https://github.com/vuhoangg120699/ContosoUniversity/blob/master/ContosoUniversity/Img/3.png)
 
- Install Entity Framework 6
  - From the Tools menu, choose NuGet Package Manager, and then choose Package Manager Console.
![add text](https://github.com/vuhoangg120699/ContosoUniversity/blob/master/ContosoUniversity/Img/4.png) 

  - In the Package Manager Console window, enter the following command:
![add text](https://github.com/vuhoangg120699/ContosoUniversity/blob/master/ContosoUniversity/Img/5.png) 

- Create the data model
  - in this step , you'll create entity classes for the Contoso University application. You'll start with the following three entities:
   - Student.cs 
   ![add text](https://github.com/vuhoangg120699/ContosoUniversity/blob/master/ContosoUniversity/Img/6.png)
   - Enrollment.cs
   ![add text](https://github.com/vuhoangg120699/ContosoUniversity/blob/master/ContosoUniversity/Img/7.png)
   - Course.cs 
   ![add text](https://github.com/vuhoangg120699/ContosoUniversity/blob/master/ContosoUniversity/Img/8.png)
   
- Create the database context
  - The first , you must create a folder with the name "DAL" in the ContosoUniversity project by right-click the project in Solution Explorer and click Add => New Folder . 
  - In DAL folder , you need create a new class file named SchoolContext.cs, and replace the template code with the following code:
![add text](https://github.com/vuhoangg120699/ContosoUniversity/blob/master/ContosoUniversity/Img/9.png)

- Initialize DB with test data
  - Next , in the DAL folder, you create a new class file named SchoolInitializer.cs and replace the template code with the following code, which causes a database to be created when needed and loads test data into the new database.
![add text](https://github.com/vuhoangg120699/ContosoUniversity/blob/master/ContosoUniversity/Img/10.png)
  - To tell Entity Framework to use your initializer class, add an element to the entityFramework element in the application Web.config file (the one in the root project folder), as shown in the following example:
![add text](https://github.com/vuhoangg120699/ContosoUniversity/blob/master/ContosoUniversity/Img/11.png)

- Set up EF 6 to use LocalDB
  - In this tutorial, you'll work with LocalDB. Open the application Web.config file and add a connectionStrings element preceding the appSettings element, as shown in the following example. 
![add text](https://github.com/vuhoangg120699/ContosoUniversity/blob/master/ContosoUniversity/Img/12.png)

- Create controller and views
  - Right-click the Controllers folder in Solution Explorer, select Add, and then click New Scaffolded Item.
  - In the Add Scaffold dialog box, select MVC 5 Controller with views, using Entity Framework, and then choose Add.
 ![add text](https://github.com/vuhoangg120699/ContosoUniversity/blob/master/ContosoUniversity/Img/13.png) 
 
  - In the Add Controller dialog box, make the following selections, and then choose Add:
  - Model class: Student (ContosoUniversity.Models)
  - Data context class: SchoolContext (ContosoUniversity.DAL).
  - Controller name: StudentController (not StudentsController).
![add text](https://github.com/vuhoangg120699/ContosoUniversity/blob/master/ContosoUniversity/Img/14.png) 
  - then you click Add 
  
- After that , you click Ctrl + f5 and run the project , you will receive the result : 
![add text](https://github.com/vuhoangg120699/ContosoUniversity/blob/master/ContosoUniversity/Img/demo%20gif.gif) 

 
