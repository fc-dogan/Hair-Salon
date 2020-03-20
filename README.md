# _Eau Claire's Salon _

####  MVC web application to manage hair salon's stylists and clients  , March 20 2020_

#### By _**Fatma C. Dogan**_

## Description

A web application for managing Eau Claire's Salon's employees(stylists) and their clients.

## Project Specifications

| Behavior | Input | Output |
|---|:---|:---:|
|When the user runs the application, they receive a welcome message along with the links for `see all stylists`. | Home page | Welcome to the Eau Claire's Salon!<br> ``see all stylists``|
|When the user clicks "see all stylist", receives a list of stylists | ``see all stylists`` | Stylists <br>  ``add a new stylist  `` |
|When a user clicks on "add a new stylist ", they recevies a form to add a new stylist| ``add a new stylist  `` | Add a new Stylist <br> Name : |
|When a User Adds a new stylist they are directed to the Stylists list page | Name: Claire | ``Claire`` |
|When a user clicks on a `Client list ` under stylist name, they receive a list of Clients of that Stylist | stylist "Claire" <br> `Client list `  | "Claire's Clients" <br> list of clients |



## Setup/Installation Requirements

### Install .NET Core

* Download the .NET Core SDK [Software Development Kit](https://dotnet.microsoft.com/download)
* Open the .Net Core SDK file and install
* To confirm installation was successful, run the ```$ dotnet --version``` command in your terminal

### Install MySQL Community Server and MySQL Workbench

#### on macOS:
_Download the MySQL Community Server DMG File [MySQL Community Server page](https://dev.mysql.com/downloads/file/?id=484914). 
* Follow along with the installer until you reach the configuration page. Once you've reached Configuration, set the following options (or user default if not specified):_
      * use legacy password encryption
      * set password 
      * click finish

* Verify MySQL installation by opening Terminal and entering the command ``mysql -uroot -p{your password here}``.  
  You can exit the mysql program by entering exit.

_Download MySQL Workbench DMG file [ MySQL Workbench page](https://dev.mysql.com/downloads/file/?id=484391). 
* Install MySQL Workbench to Applications folder. 
* Open MySQL Workbench and select Local instance 3306 server, then enter the password you set. If it connects, you're all set._

#### on Windows:
_Download the MySQL Web Installer [MySQL Web Installer ](https://dev.mysql.com/downloads/file/?id=484919) 
* Choose Custom setup type
* When prompted to Select Products and Features, choose the following: 
    * MySQL Server (Will be under MySQL Servers) 
    * MySQL Workbench (Will be under Applications)
* Select Next, then Execute. Wait for download and installation 
* Advance through Configuration as follows:
  - High Availability set to Standalone.
  - Defaults are OK under Type and Networking.
  - Authentication Method set to Use Legacy Authentication Method.
  - Set password to epicodus. You can use your own if you want but epicodus will be assumed in the lessons.
  - Unselect Configure MySQL Server as a Windows Service.
* Complete installation process

_Add the MySQL environment variable to the System PATH. Instructions for Windows 10:_
* Open the Control Panel and visit _System > Advanced System Settings > Environment Variables..._
* Select _PATH..._, click _Edit..._, then _Add_.
* Add the exact location of your MySQL installation and click _OK_. (This location is likely C:\Program Files\MySQL\MySQL Server 8.0\bin, but may differ depending on your specific installation.)
* Verify installation by opening Windows PowerShell and entering the command ``mysql -uroot -p{your password here}``. It's working correctly if you gain access to the MySQL command line. 
  You can exit the mysql program by entering `exit`


### Download this repository

_Download Manually:_

* Navigate to https://github.com/fc-dogan/Hair-Salon.git
* Click the green "Clone or Download" button.
* Click "Download ZIP".
* Click downloaded file to unzip.
* Open folder called "Hair-Salon".

_In Terminal:_

* Navigate to where you want this application to be saved, i.e.:
```cd desktop```
* Clone the file from GitHub with HTTPS
```git clone https://github.com/fc-dogan/Hair-Salon.git ```
* Open file in your preferred text editor
 ```cd Hair-Salon ```
* Change directories into the project directory
  ``` cd Hair-Salon/HairSalon ```

* Restore all dependencies
  ``` dotnet restore```


### Setup Database
```
> CREATE DATABASE fatma_dogan;
> USE fatma_dogan;
> CREATE TABLE `stylists` (
  `StylistId` int NOT NULL AUTO_INCREMENT,
  `Name` varchar(255) DEFAULT NULL,
  PRIMARY KEY (`StylistId`)
);
> CREATE TABLE `clients` (
  `ClientId` int NOT NULL AUTO_INCREMENT,
  `Name` varchar(255) DEFAULT NULL,
  `StylistId` int DEFAULT '0',
  PRIMARY KEY (`ClientId`)
);

```
_To run this application:_

* Build the project and dependencies
   ```dotnet build```
* Run the program
  ``` dotnet run```
   Note: To exit, simply press ```Ctrl + C```
* Open the local hosted server
  ``` http://localhost:5000 ```



## Known Bugs

_No known bugs at this time._


## Technologies Used

* C#
* .Net Core 2.2
* ASP.NET Core MVC
* MySQL, MySQL Workbench
* Entity Framework Core
* VS Code
* CSS
* Bootstrap

### License

[MIT](https://choosealicense.com/licenses/mit/)

Copyright (c) 2020 **_Fatma C. Dogan_**