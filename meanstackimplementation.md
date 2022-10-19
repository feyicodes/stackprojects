# MEAN STACK IMPLEMENTATION

This project aims to create familiarization with MEAN stack and deploy it to Ubuntu server.

### MEAN STACK CONSTITUENTS
* MONGODB - A document based database to store and retrieve data
* Express - A Back-end application framework for making request to database, read and wrife functions. It is a minimal and flexible Node.js web application framework that provides features for web and mobile applications.
* Angular - Handles Client and Server Requests. AngularJS provides a web framework for creating dynamic views in web applications. In this project, AngularJS is used to connect our webpage with Express and perform actions on the book register. 
* Node.js - Accepts and displays results to end-user. Used to setup Express routes and Angular controllers.

## STEP 0 - PREPARING PREREQUISITES
I created a virtual server with Ubuntu OS on my AWS account as shown in the snapshots below:

![Image 1](meanimages/img1.png)

![Image 2](meanimages/img2.png)

## STEP 1 - INSTALLING NodeJS
Firstly, I rand the update and upgrade command:
```bash
    sudo apt update && sudo apt upgrade
```
![Image 3](meanimages/img3.png)

Afterwards I added the certificates.

![Image 3](meanimages/img4.png)

*While adding the certificates I saw that node.js 12.X was no longer supported, so I got the certificate for the recommended node.js 14.x version.*

![Image 5](meanimages/img5.png)

![Image 6](meanimages/img6.png)

Then, I installed node.js 

![Image 7](meanimages/img7.png)


## STEP 2: INSTALLING MONGODB
The application to be installed would conssit of fields such as book name, isbn number, author, number of pages.

I imported the release sign in key to authenticate the version to be installed and downloaded the MONGODB app.

![Image 8](meanimages/img8.png)

I installed the mongodb app.

![Image 9](meanimages/img9.png)

I started the server and confirmed it was active.

![Image 10](meanimages/img10.png)

I tried installing npm - Node package manager but it showed an error message:

![Image 11](meanimages/img11.png)

I checked if npm already exists and it has already been installed along with node.js

![Image 12](meanimages/img12.png)

While attempting to run
```bash
    sudo npm install body-parser
```
I encountered an error:

![Image 13](meanimages/img13.png)


In running troubleshoot, I ran the command 
```bash
    npm init -y
```

![Image 14](meanimages/img14.png)

I tried reinstalling body-parser

![Image 15](meanimages/img15.png)

I created accessed the Books directory and initialized the npm project.

![Image 16](meanimages/img16.png)

I created the server.js file and inputted the necessary code.

![Image 17](meanimages/img17.png)

## INSTALLING EXPRESS AND SETTING UP ROUTES TO THE SERVER
I installed the express mongoose app

![Image 18](meanimages/img18.png)

I created apps directory and accessed the directory.

```bash
    mkdir apps && cd apps
```
I created a routes.js file in the books/apps directory and wrote the required code

![Image 19](meanimages/img19.png)

I created book.js file in the books/apps/models directory and worte the necessary code.

![Image 20](meanimages/img20.png)

## STEP 4- ACCESS THE ROUTES WITH AngularJS

Create a public directory under the books directory and add a file named script.js and inputted the required code.

![Image 21](meanimages/img21.png)

Index.html is also created and added in the public directory.

![Image 22](meanimages/img22.png)


