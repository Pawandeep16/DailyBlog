
# DailyBlog Pawandeep Singh Thandi

**Date : 1-Feb-2022**
## Introduction to Linux & Installing Ubuntu



Linux is an open-source operating system like other operating systems such as Microsoft Windows, Apple Mac OS, iOS, Google android, etc. An operating system is a software that enables the communication between computer hardware and software. It conveys input to get processed by the processor and brings output to the hardware to display it. This is the basic function of an operating system.

- Download the linux distribution of your choice from the offical sites.
- Creating Boot pendrive using rufus.exe in windows or IOS.
- Restart the system and open boot menu using boot key according to your system .(Eg.- F8, F2 etc.)
- Select your boot device in boot menu.
- Select Install Ubuntu then Click Noraml Installation.
- Select where to install alongside window or Erase disk or something else.
- Then Click next and start ubuntu installation.
- For More detail about Installation Guide [Click here](https://phoenixnap.com/kb/install-ubuntu-20-04)
<br>

**Date: 2-Feb-2022**
## Introduction to LAMP Stack and Installation

The LAMP stack is a popular open-source solution stack used primarily in web development.LAMP consists of four components necessary to establish a fully functional web development environment. The first letters of the components' names make up the LAMP acronym:
<br>

- Linux is an operating system used to run the rest of the components.
- Apache HTTP Server is a web server software used to serve static web pages.
- MySQL is a relational database management system used for creating and managing web databases, but also for data warehousing, application logging, e-commerce, etc.
- PHP, Perl, and Python are programming languages are used to create web applications.
- Installing lamp on Ubuntu System.
- Verifying by run LAMP on localhost.

**Date : 3-Feb-2022**
## Run Cgi Script
A CGI script is any program that runs on a web server.

**Date : 4-Feb-2022**
## Image to video
I need to Write a Script used to convert a Images into Video</p>

## Moviepy
MoviePy is a Python module for video editing, which can be used for basic operations (like cuts, concatenations, title insertions), video compositing (a.k.a. non-linear editing), video processing, or to create advanced effects. It can read and write the most common video formats, including GIF

- install usign command pip install moviepy
- install imagemagick run the comand sudo apt install imagemagick
   - goto ---- /etc/ImageMagick-6/policy.xml file  
   - In the file comment out the line
   - "policy domain="path" rights="none" pattern="@*" 
   - you can found this at the bottom part of the file


**Date : 5-Feb-2022**

## Concatenate TextClips and Images
Added the text CLips using the TextClip component from the Movepy Liberary 
and Learned the Methods of Conacatenating Two clips with one another

- Develop a method to add Text just after a image and so on 
- Add CSV files to feth the data in to Script 
- Added some Effect to make the video more 
- Convert the Hard Coded Script into Structured Script


**Date : 8-Feb-2022**
## Introduction to Github Pages
- Getting Information What is GitHub Pages.
- Create a New Repository on GitHub.
- Setting Repository as the main branch and setting a theme for GitHub pages.
"policy domain="path" rights="none" pattern="@*"- Learning about Personal access tokens for push Local Repository on GitHub.
- Learning Syntax of Markdown Language in GitHub.
<br>


**Date : 10-Feb-2022**
## Introduction To Frappe FrameWork
Frappe FrameWork is a WebFrameWork written in **Python** and **JavaScript** and at the backend it is suppored by **node** js and database is handelled by the **Mariadb**
The key difference in Frappe compared to other frameworks is that meta-data is also treated as data. This enables you to build front-ends very easily. We believe in a monolithic architecture, so Frappe comes with almost everything you need to build a modern web application. It has a full featured Admin UI called the Desk that handles forms, navigation, lists, menus, permissions, file attachment and much more out of the box.

After setting up Frappe Framework, you can be productive in no time. Creating models, wiring controller code and updating views are all handled by the framework.

**Date : 11-Feb-2022** 
## Installation of Frappe FrameWork on linux based System:
For Installation I Followed the installation Guide at [Click TO Reach](https://frappeframework.com/docs/v13/user/en/installation) <br>
For Frappe FrameWork we need some Pre-requistis i.e.
- **Git**  
- **Python** 
- **Redis** 
- **MariaDB**
- **Node**
- **Bench CLI**
  - Setting Up Bench <br>
   Run the command to create our bench setup
    - bench init frappe-bench
    - cd frappe-bench 
    - bench start
<br>
![image](https://github.com/Pawandeep16/DailyBlog-Pawandeep/blob/main/Images/2.png)

After setting up everything we can Create sites and apps according to our need


 **Date : 12-Feb-2022** 
## Creating a LMS Site on Frappe FrameWork
First we run a command in the terminal 
- bench new-site library.test <br>
It will ask us to set adiministrator password for the site. 
After setting up password we are good to go.

<!-- ![command line](https://github.com/Pawandeep16/DailyBlog-Pawandeep/blob/main/Images/image.png) -->

When we run the command 
- bench start  
It will start the bench and we can run it on localhost with provides link ad default it will run on  8000 port
 ![alt text](https://github.com/Pawandeep16/DailyBlog-Pawandeep/blob/main/Images/2.png)


**Date : 14-Feb-2022** 
## Creating Apps in Frappe
Any kind of applications can be created on frappe wich give more controll and flexible use. 
To create a new app  run command <br>
- bench new-app library_management

The app will create certains fille in the app folder the whole structure is 
- **library_management**: This directory will contain all the source code for your app
- **public**: Store static files that will be served from Nginx in production
- **templates**: Jinja templates used to render web views
- **www**: Web pages that are served based on their directory path
- **library_management**: Default Module bootstrapped with app
- **modules.txt**: List of modules defined in the app
- **patches.txt**: Patch entries for database migrations
- **hooks.py**: Hooks used to extend or intercept standard functionality provided by the framework
- **requirements.txt**: List of Python packages that will be installed when you install this app
![alt text](https://github.com/Pawandeep16/DailyBlog-Pawandeep/blob/main/Images/3.png)


**Date : 15-Feb-2022** 
## Introduction to DocTypes in Frappe:

A DocType is the core building block of any application based on the Frappe Framework. It describes the Model and the View of your data. It contains what fields are stored for your data, and how they behave with respect to each other. It contains information about how your data is named. It also enables rich Object Relational Mapper (ORM) pattern which we will discuss later in this guide. When you create a DocType, a JSON object is created which in turn creates a database table.

To enable rapid application development, Frappe Framework follows some standard conventions.

1. DocType is always singular. If you want to store a list of articles in the database, you should name the doctype Article.
2. Table names are prefixed with tab. So the table name for Article doctype is tabArticle.
3. The standard way to create a DocType is by typing new doctype in the search bar in the Desk.

A DocType not only stores fields, but also other information about how your data behaves in the system. We call this Meta. Since this meta-data is also stored in a database table, it makes it easy to change meta-data on the fly without writing much code.

Before we can create DocTypes, we need to enable developer mode on our bench. This will enable boilerplate creation when we create doctypes and we can track them into version control with our app.

##### bench set-config -g developer_mode true
##### bench start

**Date : 16-Feb-2022** 
### Creating Article DocType for LMS

Go To DocType list and here we can create a new doctype named article :
- Enter the Name for the docType
- Then We select a Module Named LMS which we have created earlier or we can create a new module.
- Now we require fileds for the doctype we created the required below fields in the doctype:
  - Article Name (type = data , and we set it as Mandatory )
  - Image (type = Attach Image )
  - Author ( Data )
  - Description(Text Editor)
  - ISBN(Data) 
  - Status(Select , here we can add a drodown with options Issued and Available )
  - Publisher( Data )
we can also set the naming series for our artcles( as deafult it will use title as series )

After adding the fields, click on Save.Our doctype is created and we can now Add data to our doctype.
Now We can go to the article list and create " Article ".
As we created new article the data wiil be pushed to the database in the form of tables and we can also check its data by giving command in the terminal 

- bench bench --site library.test mariadb

Here it will shoow all the database of a perticluar site.
And we can check and update  our data using differnet sql commands by selecting differnet databasea and tables.

**Date : 17-Feb-2022** 
### Adding functionality to the LMS

A small example in order to provide the full name of the user we defined the following code in the 
```
class LibraryMember(Document):
     #this method will run every time a document is saved
       def before_save(self):
          self.full_name = f'{self.first_name} {self.last_name or ""}'
````


**Date : 18-Feb-2022** 
###  Creating Different Doctypes with required for the LMS :

### Library MemeberShip
It will have the following fileds 

- Library Member (Link, Mandatory)
- Full Name (Data, Read Only)
- From Date (Date)
- To Date (Date)
- Paid (Check)

We will enable the Submitable Part So after save the one must have to submit it and after submit one cant make any changes to the document.


Now for the functionality:

import frappe<br/>
from frappe.model.document import Document<br/>
from frappe.model.docstatus import DocStatus<br/>

```
class LibraryMembership(Document):<br/>
    # check before submitting this document<br/>
    def before_submit(self):<br/>
        exists = frappe.db.exists(
            "Library Membership",
            {
                "library_member": self.library_member,
                "docstatus": DocStatus.submitted(),
                # check if the membership's end date is later than this membership's start date 
                "to_date": (">", self.from_date),
            },
        )
        if exists:
            frappe.throw("There is an active membership for this member")
```

**Date : 19-Feb-2022** 
##  Library Transaction :

- Article - Link to Article
- Library Member - Link to Library Member
- Type - Select with 2 options: Issue and Return
- Date - Date of Transaction

### Adding Validations For the Transaction:

In the library_transaction.py File we going to make some server side code 
For this We added some Code in the library_membership.py file in order to make a track on the valid membership for the library .

![alt text](https://github.com/Pawandeep16/DailyBlog-Pawandeep/blob/main/Images/validationlms.png)<br/>
![alt text](https://github.com/Pawandeep16/DailyBlog-Pawandeep/blob/main/Images/librarysettings.png)<br/>



**Date : 21-Feb-2022** 
##  Form Scripts

Form Scripts are client-side javascript code that enhances the UX of your Forms.

example of this code is:
we write this in .js file 
```js
frappe.ui.form.on('Library Member', {
    refresh: function(frm) {
        frm.add_custom_button('Create Membership', () => {
            frappe.new_doc('Library Membership', {
                library_member: frm.doc.name
            })
        })
        frm.add_custom_button('Create Transaction', () => {
            frappe.new_doc('Library Transaction', {
                library_member: frm.doc.name
            })
        })
    }
});
```
**Date : 22-Feb-2022** 
##  Introduction to Github Pages

- Getting Information What is GitHub Pages.
- Create a New Repository on GitHub.
- Setting Repository as the main branch and setting a theme for GitHub pages.
"policy domain="path" rights="none" pattern="@*"- Learning about Personal access tokens for push Local Repository on GitHub.
- Learning Syntax of Markdown Language in GitHub.

**Date : 23-Feb-2022** 
## Introduction to Reveal.JS, Pandoc, Use of Markdown in Reveal.js

## Reve.js

reveal. js is an open source HTML presentation framework. It's a tool that enables anyone with a web browser to create fully-featured and beautiful presentations for free. Presentations made with reveal. js are built on open web technologies.

- What is Pandoc, Use Markdown in Reveal.js.
- Creating Presentation in Reveal.JS using Markdown only.
- Learn how to show presentation on Local machine.
- Converting .md file into .pdf file using Pandoc.

**Date : 24-Feb-2022** 
##  Introduction to Docker, Virtual Machine and ERPNext

## Docker

Docker is popular virtualization software that helps its users in developing, deploying, monitoring, and running applications in a Docker Container with all their dependencies (frameworks, libraries, etc.) to run an application in an efficient and bug-free manner.Docker Containers are Light-weight, Applications run in isolation,Occupies less space, Easily portable and highly secure, Short boot-up time.

## Virtual Machine

A Virtual Machine (VM) is a compute resource that uses software instead of a physical computer to run programs and deploy apps. One or more virtual “guest” machines run on a physical “host” machine.  Each virtual machine runs its own operating system and functions separately from the other VMs, even when they are all running on the same host. This means that, for example, a virtual MacOS virtual machine can run on a physical PC.

- It can start only a single VM on a VMX.
- It can run only a limited number of VMs on a system.
- It can run multiple containers on a system.
- It can start multiple containers at a time on the Docker engine.
## ErpNext

ERPNext is a full-featured business management solution that helps SMEs to record all their business transactions in a single system. With ERPNext, SMEs can make informed, fact-based, timely decisions to remain ahead in the competition. It serves as the backbone of a business adding strength, transparency, and control to your growing enterprise.

**Date : 25-Feb-2022** 
##  Installing ERPNext Powered by Frappe on our bench: 

- Pre requisite
 - Frappe FrameWork 
- For the perfect installation use this referance [Click here](https://github.com/D-codE-Hub/ERPNext-installation-Guide/blob/main/README.md). 

**Date : 26-Feb-2022** 
##  Introduction to Selenium, Budibase, Coding standard for program
### Selenium 
Selenium is an open source umbrella project for a range of tools and libraries aimed at supporting browser automation. It provides a playback tool for authoring functional tests without the need to learn a test scripting language

### Budibase 
Budibase is a development platform designed for speed and productivity.
With Budibase, developers no-longer experience repetition, long-dev cycles, and frustration. Instead, developers are more productive, happier, and can deliver applications they're proud of in minutes.

### Coding Standards

How to write code in Any script so that it can easily read by other programmer who contribute to your project, take variable name which should be relevant with its function.

- Use appropriate naming conventions.
- Segment blocks of code in the same section into paragraphs.
- Don’t use lengthy functions. Ideally, a single function should carry out a single task.
- Standardize headers for different modules


**Date : 28-Feb-2022**
##  Introduction to Jinja Templating

A Jinja template is simply a text file. Jinja can generate any text-based format (HTML, XML, CSV, LaTeX, etc.). A Jinja template doesn’t need to have a specific extension: .html, .xml, or any other extension is just fine.

A template contains variables and/or expressions, which get replaced with values when a template is rendered; and tags, which control the logic of the template. The template syntax is heavily inspired by Django and Python.

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <title>My Webpage</title>
</head>
<body>
    <ul id="navigation">
    {% for item in navigation %}
        <li><a href="{{ item.href }}">{{ item.caption }}</a></li>
    {% endfor %}
    </ul>

    <h1>My Webpage</h1>
    {{ a_variable }}

    {# a comment #}
</body>
</html>
```

**Date : 1-March-2022**
## Education Domain in Erpnext

ERPNext is a free and open-source integrated Enterprise Resource Planning software developed by Frappe Technologies Pvt. Ltd. and is built on MariaDB database system using Frappe, a Python based server-side framework. ERPNext is a generic ERP software used by manufacturers, distributors and services companies.

The ERPNext Education Module helps to organizing your entire set-up. You can have your entire Student Database, Fee Structure, Staffing Information, Courses, Curriculum Which we used for the Project Nanakana Sahib Public School and Guru Nanak Dev Engineering College Ludhiana.

In this Domain We have 
- Basic Setup
- Student
- Admission
- Fees 
- Schedule
- Learning Management System
- Attendance 
- Assessment
- Tools



**Date : 2-March-2022**
##  Setting Up ErpNext for School

First we setup the parent Company with all the details and under that parent company we setup our school which further related to courses, program , room, student category etc.
then our team divided the work for diferent modules.


**Date : 3-March-2022**
##  Fee Module

In the Fee module we have 

- Fee 
- Fee Structure 
- Fee Schedule
- Fee Components 
- Fee Category 

### Fee 

In the Fee section we can create a fee for an Individual student one by one
We have to enter the Student ,due date and we can aslo edit post time and date 
to create a fee we need some of its components which are described below:

- Prerequisites
  - Student 
  - Fee Structure
  - Fee Category


### Fee Structure

In the fee Structure we can define the type of fee like for which class and category of students what kind of fee should be there

In the fee structure we to provide program , student categor, acedamic year, acedamic term .
The important part we have to define the fee category components which includes the different kind of fee. 

### Fee Category

In the Fee Category we simply add the Different Fee components like Tution fee ,Bus fee,Books etc.

Fee Schedule

- Prerequisites
  - Fee Structure
  - Student group


**Fee schedule** is used to add bulk data for fee according to the Student groups and studnet category.
it will divide the grand_total with each group of students.
just go to fee schedule and click new fee schedule
after creating schedule just click create fee button on top that will create fee for the students

### Payment Entry 

To make a payment 
go to fee list  the select a unpaid status candidate 
Now on the top there is a Tab name Create in which we can select make payment and fill the parameters the then submit.


**Date : 4-March-2022**
##  Adding Fine to teh ouver Due fees 
If the due date exceeds then the fine after due date will be automatically added to the grand total for the student. but my logic didnt fit to the right approach and got some errors realted to the fee schedule . so we are keeing it in the future scope.


**Date : 5-March-2022**
## Chat app For the Site 

In the chat app any visitor for the site can ask for any reviews or querries for their doubts and will be answered in the specific time alloted by us by our facility member. 

**Date : 7-March-2022**
## Learning about how to import data in erpnext from csv file

We can generate a csv template regarding ot a particular doctype and trhe we can add a particular data to ethe data type and then we can add the data in the abundace so it can save time.

**Date : 8-March-2022**
## Learn Module from Frappe School
Gone through all the toturials related to the framework like client scripts and all the advanced stuff. provided by th developers.

**Date : 9-March-2022**
## Meeting App

- Understand the structure of meeting app.
- Understand the javascript code and python code of meeting app.

**Date : 10-March-2022**
## Presentation and discussion of meeting app

- Telling about the importance of doctype in Frappe-Framework.
- Discuss with all team how it works and how we create new custom app.

**Date : 11-March-2022**
## Creating own Noticeboard app
NoticeBoard for an institute regarding to the important information provided by the Institute 
- Create Doctype according to structure discussed in team.
- contains the title,description,signature of the uploader and date 
- Also can see how many have seen the notice.

**Date : 12-March-2022**
##  Created Different Fee Structures on the Server Site 

Implemented Different fee Structures based on the Student Category and the program i.e from lkg to 10th.
So while creating new fees, fees should be added automatically by selecting Fee Structure. We are trying to add an admission fee in Student form along with this we are exploring where all the records are saved so that we keep track how many fees are paid or pending. We track this record in 'Report Student fee collection' doctype. We are also trying to add a penalty on overdue fees but we find this feature is not currently available in erpnext.

**Date : 14-March-2022**
## Learning about Workflow
- Today I'm learning Workflow in ErpNext.
- Understand how to pass control to different manager.
- Trying to implement Purchase order list and trying to approve it from purchase manager and material manager.

**Date : 15-March-2022**
## Dynamic WebPages In Frappe

- First we need to create www directory in any Frappe app.
- Then need to create two files Python file for fetching data from database.
- Other file is html file in which i use jinja template to show record on webpage.

**Date : 16-March-2022**
##  Helping the Teammates realted to their work

As I was free from my task so as being a part of sdc team.I was trying to resolve some of my mate's issues.
helped in chat aapp in order to provide specific roles to specific user so only they get to see their msg.

**Date : 17-March-2022**
## Give Presentation About Github

So being a part of a developer team one must need to Know Github in order to have a seamless conversation , information and code can be shared easily.
Give them about the introduction about github 
the basic github commands
- git init - to initialize a repository 
- git add . to add the whole files and folder 
- git add filename.extension to add the  specific file 
- git commit -m "Your Message" to commit the changes 
- git remote add origin git URL
- git push -u origin [branch name]
- git stash clear	 -to clear all stashed enteries
- git checkout branch_name  move across beanches of specifi reporsitory 
- git status to check the curent status of the files
- git pull origin [branch name] pull changes from the remote url
- form Documentation [Click here](https://github.com/joshnh/Git-Commands) 

**Date : 18-March-2022**
## Understand the code available in Frappe

Understanding the code available in all-products, then we are trying to add items in item lists, then we face problem after few search then We add items in (item lists), then add item in (website item), then setting up e-commerce settings now we successfully use search, prev & next. Now we are trying to apply it in a pagination file so we dont have to do the repetative task again and again in order to maintain the co-relation.


**Date : 19-March-2022**
## Adding Search Filter to the List view of specific data.

After Understandig the code of the Framework I tried to get the inbuild code and make it useful in the List View and Successfully I make it usefull for the List view and made changes as per required.But for sorting I'm working on it.


**Date : 21-March-2022**
## Give presentation on the file Structure of the Framework.
Provide the clean view of the frappe framework about the file structuring with my mate vishal . Just as we create a new app or new website what kind of file are genrated and what kind of file structure it follows and which file is used to do specific fuction or conatins what kind of information 


**Date : 22-March-2022**
## Installing new Erpnext on server
- First we install the new instance of  frappe framework on the Server then install erpnext with education domain.
- After this we are collecting students areound 5000 and teachers (114) data from Nankana Sahib Public School.
- Arranging data according to doctype in erpnext.
- Setting up the school.  

**Date : 23-March-2022**
##  Arrange naming series company wise
While new applicant is registered in system by default system generate naming series. We are trying to change it company wise For eg. if we are member of company A, then naming series include A-2022-00001.</p>
For this we follow official erpnext tutorial [More Detail](https://docs.erpnext.com/docs/v13/user/manual/en/customize-erpnext/articles/company-wise-naming-series#:~:text=The%20need%20is%20to%20create,be%20SINV%2DB%2D0001.)
Using this we get error the we take reference from other discuss.erpnext where we use (.abbr.-.YYYY.-) in option of Naming Series

**Date : 24-March-2022**
## Arranging Student data

- As there are large data of students in school we need to make it correct.
- so we all divide work in team and understanding the concept of filter, concatinate etc. in excel.
- First we export the required format of csv file then we edit the csv file provided by the school according to our need and import thr data to the server.


**Date : 25-March-2022**
## Assessment Module
Assessment procedure to evaluate the students' curricular performance in a period.
Following are the Pre-requists required for the generation of assessment report.
- Assessment Criteria
- Assessment Group
- Grading Scale

**Date : 26-March-2022**
##  Assessment Criteria and Assessment Group

Marks earned are entered based on the ***Assessment Criteria***. For example, if the assessment was conducted for science subjects, then you can evaluate Student in Science on various criteria like Theory and Practical etc.
In ***Assessment Group*** if we wish to conduct an assessment for each Academic Term within an Academic Year e.g MST1,MST2 and ESE then these were the assessment groups.

**Date : 28-March-2022**
##  Assessment Plan and Assessment Result
An Assessment Plan is a schedule to conduct the examination/assessment of a particular course for a group of students studying that course in an on-going academic term.
Prerequisites:
- Student Group
- Course
- Program
- Assessment Group
- Grading Scale

***Assessment Result*** is a log of marks/grades earned by the student for specific Assessment.An Assessment Result is created in the backend based on the marks entered in the Assessment Result Tool.

**Date : 29-March-2022**
## Web Manager Vs Website Manager

- For new users we create web manger who has permission to create webpage,See on website, Search box, can't create webform.
- Website Manager can delete webpage, read webpage but cannot create, Search bar not shown.
- We assign new user web user so that they can access gne11 website with some restriction.

**Date : 30-March-2022**
## Adding New role and Give Permission to new Users
- When we got new user for allow them to create Library Management System we need to give them the access of doctype modules.
- For this we go to doctype list and create new role where new user create doctype by can't delete doctype.
- Similarly for Module we use select permission where user can select module but can't read module.

**Date : 01-April-2022**
## Working with Client Script in Form
Client Script is script in which we add some action on form so that we validate data or do other function.
- Webform script is which is done in webform while creating new webform.
- For Reference we use Web form Scripting Documentation [Click here](https://frappeframework.com/docs/v13/user/en/api/form)

**Date : 02-April-2022**
## User Permissions
A role is a set of permissions assigned to a user so that they can access the documents they need to. For example, a student  will need access to his/her/it courses but will not have access to read or write them.
If in case we need to create a user with some specific permissions we can give it through user permissions.

**Date : 05-April-2022**
## Creating Library Management System
As per official documentation created Library Management App.
 - Install app on site then creating doctype.
 - Use Features like Naming Series, Permission Rules. 
 - Learn Controller methods, Doctype Features, Form Scripts. 
 - Adding Web view for preview Articles on web.

**Date : 06-April-2022**
## 

**Date : 8-April-2022**
## Writing Requirement and Specifications For the Souvenir Project
Today Sir explained us all the requirements of the souvenir project and what is the required outpiut of this project. Sir also explained us the yadein project which was used to generate souvenir of all the students near about 10 years ago And all the technology used in the yadein project. I accepted the souvenir project. So sir told me to first write the requirements and specifications of the projects and to share it with the sir. 


**Date : 9-April-2022**
## Acceptence of the Requirements of Souvenir
Today the requirements and specification of the souvenir project got approval form the sir :) 
After this i immediately started working on souvenir project. Fisrt i created a doctype named souvenir with some fields like name, branch, urn, crn, dob, fathers name, mothers name etc, and there are two sections avialble for the friends Info of friend1, And Info of Friend2 in these field students will fill the details of their friends and comments for them. 
After creating the doctype and giving it web view I created a web-form based on the souvenir doctype and the name of the webform is souvenir-form it has same field as souvenir doctype. I Did all this on my local erpnext.


**Date : 11-April-2022**

## Souvenir on server
After successfully creating the souvenir doctype and souvneir web-form and after checking if it is working or not. Today created the souvenir doctype and souvenir web form on gne11.gnde.ac.in. And  was also working on the education domain of erpnext for nankana sahib public school.
 

**Date : 12-April-2022**

## Souvenir on Server
Today I was working on the souvenir form. On our website i wasn't able
to access the web form due to server exception.Then i created the
souvenir doctype and souvenir webform on my local erpnext system. Sir
told me to refresh the gne11.gndec.ac.in and pray sincerely :) . After
this i was able to access the web form. Now the problem is that the
user is able to attach image in the image field with login. But user
is not able to attach image in the image field  (but user is able to
select image of their choice). I also tried it on my local erpnext
system, on that i am getting same problem.



**Date : 13-April-2022**
## Souvenir and Basic coding guide part-1

Today  working on souvenir web-form sir told us to add some more fields in the souvenir web form and do some changes in it.
Also have read the basic coding guide part-1 it was very fun to read this as like reading they have explained each and every this in a wonderful way.
For the basic coding  fro particular web form I follow this Documnetation [Click Here](https://frappeframework.com/docs/v13/user/en/web-forms)


**Date : 15-April-2022**

## Presentation of Nankana Sahib Public School Project
Today we had a meeting with Satinder Sir and a teacher from Nankana Sahib Public School. In today's meetings we all presented what we have done till now. We showed them the whole workflow to add a student. For which first we need to add a student applicant and explained that there are two methods for this one is online by using web form and another is offline after the application is accepted we can enroll them in the programs by single-2 enrollment of every student and by using the program enrollment tool and we showed them the lms interface of student how student is going to access the programs and courses and quizzes.
After student section we showed them the whole working of instructor how instructor can add content like articles, videos and quizzes in lms, mark the attendance of students etc. After Instructor we presented the HR module how to generate payrolls, salary slips, attendance of employees etc.



**Date : 16-April-2022**

## Fetching data from another doctype in doctype
Today we  were trying to fetch the fields in the souvenir doctype from other doctypes .we were able to fetch branch name (username) etc. After that we were trying to migrate the souvenir doctype. but  not able to do it on my local erpnext as we are getting an error related to supervisor. we were trying to create an app named souvenir so that one can easily fork it from my repository but we are getting error so vishal created an app named souvenir on his local erpnext and added it to his github and wetried to fork it from his repository again we were getting error related to souvenir.


**Date : 18-April-2022**

## Error On local erpnext 
Today we were continuously getting error ;) related to supervisor vishal and I was trying to resolve this issue but after applying solutions for this error we were getting new errors so we uninstalled the local bench then reinstalled it on our local system. After this I created a
new app named Souvenir_Form then installed it on site. Then I have created a new doctype named Souvenir and a web form named souvenir on my local system.



**Date : 19-April-2022**

## Presentation Of all the topics
Today Me and Vishal gave presentation to all my mates in which about the building Structure of Frappe and Erpnext and the Functionality of all the files and folder and their meaning and also procide some demo about the code and the generation of files,,
. Currently I am working on web form validations in order to procide a clean form for the user so that we got proper information and make clg's own form instead of using google forms.


**Date : 20-April-2022**

## Validations on web form
I  implemented the validations in the souvenir web form like
in phone number field user can only enter 10 digits,  and crn and urn
field will accept only 7 digit numbers. Pushed the project
as an app on the github and anyone can install it on their site using this [Link](https://github.com/Pawandeep16/NewSov.git)
Now I was trying to auto populate the data with the users info so that he/she/it did'nt need to fill the fields whose data we already have.





**Date : 21-April-2022**
## Installation of Souvenir app on Gne11
I have installed the souvenir_form app on our [Test Site](gne11.gndec.ac.in) I was getting server exceptions on the web form. After some time it was working well and i was able to enter the data in the form. 



**Date : 22-April-2022**
 
## Validations on web form
Did the validations on web form as previously we had implemented validations on web form but wasn't proper validations. As it was just showing the error message after cancelling the error the user information was getting saved. So it was not proper validations. So we again implemented the validations with proper functions and events and tested it properly as a tester. 
```js
frappe.web_form.validate = () => {
    let data = frappe.web_form.get_values();
    if (data.amount < 1000) {
        frappe.msgprint('Value must be more than 1000');
        return false;
    }
});

```


 **Date : 23-April-2022**

##Working to fetch data from user doctype in souvenir doctype
Trying to fetch the data from user doctype to souvenir doctype. We were searching for the solutions for fetching the fields from another doctype. By default in the erpnect their is "fetch from" option is available in doctypes but we wanted to do it from backend so we implemeted it by using java script events that are present in official documentation of erpnext. We implemented it in js file of souvenir doctype. By using these events we were able to fetch the data like name,email,contact number from user doctype.
Successfully fetched the data using pyhton events and then i Whitelisted these events and used them in the call function in the docype js file and got the data.
```py
from __future__ import unicode_literals
import frappe
from frappe import _
import frappe.client
import frappe.handler

def get_context(context):
    pass

@frappe.whitelist()
def get_detail(user = None):
	p = frappe.db.get_value("User", user, ["email","user_image","mobile_no","birth_date","gender","location","full_name"])
	return p	
        
@frappe.whitelist()
def get_details(user = None):
	p = frappe.db.get_value("Souvenir", user, ["email","image","contact_no","date_of_birth","gender","address","name1"])
	return p	
        
```



**Date : 25-April-2022**

## Fetching Data on web form
Today we were trying to get the prefilled data in the souvenir web form so that user doesn't need to fill the information agaian and again as all the information is previously available. We implemented the same function which we had applied in doctype but these events are not working on the web form. To find the another alternative event we are searching online and watching youtube tutorials but till now we haven't got any
solution ;) . We are trying our best to get it done as soon as possible.
The problem that I was facing was the reason was that the path that seicifies the particular function of the python to trigger was incorrect with a little difference.

**Date : 26-April-2022**

## Presentation on Souvenir Project 
Today I gave presentation to all my mates on souvenir project. I
showed them all the requirements and specification. I also showed them
the overall workflow of the project and what i have done till now and
what is the required output.



**Date : 27-April-2022**

## Successfully fetched data from souvenir doctype to souvenir web form
Today we succesfully fetched the data from souvenir doctype to the souvenir webform :) . But our main task was to get it form user list ;) .
we successfully  did populate the souvenir doctype from user doctype and
then i was trying to fetch the data  to the webform but it didn't work
but when we add data to the souvenir_doctype
it will auto populate the webform.
I found this discussion and here one say fetch doesnt work on webform.


**Date : 02-May-2022**
## Hackathon day 1
### Roles and flow for Parent Comapany:-

***Director***:- Director will have all permissions like fees, salary,
accounts , total gain etc but with read only access.

***Accountant***:- will have permissions to see all the account information
of trust, nsps, gndec.     Accountant will have read, write access to
create the fee and salaries of the employee and also can create the
fee report and salary report.

***HR***:- HR will have permission to create the users and make them
employees, leave allocation, holiday list, salary of employee.
Superintendent

### Roles and flow for Child Comapany:-

***Principal***:- Will have only read only access to all the education
domain related information and HR related information.

***Accountants***:- 1 For students fee and 1 for salaries of employees.
Teaching Incharge:-  Will do all the tasks of academic user like
course scheduling etc.

***HR***:- will create employees and instructors only for Nankana sahib
Public School, leave allocation, salary of employees etc. We need to
show all the reports like employees attendance report, salary report,
leave report etc to the HR..

***Instructors***:- will have access to student attendance, quiz, videos,
article, Diary, Student list etc.


**Date : 03-May-2022**
## Hackathon day 2

***Students***:- will have access of only LMS and on lms they will have
access of programs, Courses, Quizzes, Videos, Articles, daily diary
and attendance.

***Accountant***:- will create the salaries of employees and fees of
students, will generate the balance sheet.

We need to generate all the reports and graphs for necessary
information for each role.

Inventory Management

Today, We created Director user of NSET, Superintendent of NSET,
Principal user of NSPS and HR user of NSPS on erp server and gave them
all the required permissions. And same roles are created on gne11.GNE,
whose credentials are shared in other mail. You can check that roles
with given credentials. Also we learn about Salary Structure and
Salary Component of employees. In meeting with Harpreet sir, we learn
about PF, Taxes, Funds, Earnings and Deductions etc. We will explore
it and implement on gne11.GNE.

**Date : 9 May-2022**
## Image Specifications To Web From

First I tried to get the image path file from the user that uploads it and then from the use of that source
Got the Image Width and Height and then put some conditions and make it validate. First got some errors like it saves the form even after errors shown. the need to put some frappe web form components.In the end It works like charm.
sample code is as follows:
```
  var img = new Image();
                 img.src = value;
                 img.onload = function () {
                     var height = this.height;
                     var width = this.width;
                     console.log(height, width)
                     frappe.web_form.validate = () => {
                     if ((height > 1000 || width > 1000) || (height < 350 || width < 350)) {
                         frappe.throw("Height and Width must be Between 1000px and 350px");
                         return false;
                     }
                     return true;
                 
                 }
     
                 }

```

