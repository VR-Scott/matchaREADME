# Matcha
Matcha is a simple dating site that allows users to meet up with others based on their location, sexual preferences and interests.
This project was an introduction to the fundamentals of advanced web development and other advanced web development technologies and concepts.

## Requirements (Needs Changing)
- PHP
- XAMPP
- JavaScript

## Installation and Setup(Needs changing)
NOTE: This is for setting the project to run on Arch Linux Manjaro using Xampp. Follow your OS specific instructions for other platforms.
- Install Xampp:
    ```
    sudo pacman -S xampp
    ```
- Set up a database user and initialize the database:
    [Mysql Arch Wiki](https://wiki.archlinux.org/index.php/PHP#MySQL/MariaDB)
- Clone the project into the /opt/lampp/htdocs directory
    ```
    git clone https://github.com/tcajee/camagru.git /opt/lampp/htdocs/camagru
    ```
- Start the Xampp servers via the included GUI.
- Initialize the Database tables by calling the setup script [Database Setup](https://localhost/camagru/config/setup.php)
- Navigate to [PHP Myadmin](https://localhost/phpmyadmin/) to verify that the database has been populated.
- After running the setup you will be redirected to [Camagru Home](https://localhost/camagru/)

## Tools & Technologies
#### Back-end:
- NodeJS: An open-source web server environment that uses JavaScript on the server and runs on various platforms
- JavaScript: A general purpose programming language for web that can calculate, manipulate and validate data.

#### Front-end:
- HTML: The standard markup language used to develop web Pages. It only defines the layout of the page contents. 
- CSS: Used to define the style of the website. It augments HTML and can be used to create semi-dynamic websites.
- JavaScript: A programming language that is often used alongside HTML and CSS to make dynamic websites. It is usually referred to as the language of the web because of its strong compatibility with web browsers and HTML.
- React(JSX): JSX(stands for JavaScript XML) makes it easier to write and add HTML in React.
Combining JS and HTML

#### Data Management System (DBMS):
- PostgreSQL: a open-source relational database management system emphasizing extensibility and SQL compliance.

#### Project structure:(Needs changing)
```
camagru
├── app
│   ├── controllers -> Contains all page-specific back-end functionality
│   │   └── *.php
│   ├── lib -> Contains addition helper functionality
│   │   └── helpers
│   │       └── *.php
│   └── views -> Contains templates and all page-specific layouts
│       ├── *.php
│       ├── layouts
│       │   └── *.php
│       └── *.php
├── config -> Contains all initial application and database functionality
│   └── *.php
├── core -> Contains all primary back-end application functionality
│   └── *.php
├── css -> Contains all stylesheets
│   └── *.css
├── img -> Contains all image files
│   └── *.png
│   └── *.jpg
├── index.php -> Main entry point to the application
└── js -> Contains all page-specific client-side functionality and AJAX
   └── *.js
```

## Testing(needs changing)
[Marking sheet linked here](https://github.com/tcajee/camagru/blob/master/camagru.pdf)
- The following are test will be run:
    - Preliminary checks:
        - Usage of PHP for the back-end
        - No external frameworks
        - Config/database.php exists
        - Config/setup.php exists
        - PDO is configured
    - Start the web server.
    - Register and account
    - Login
    - Webcam
    - Public Gallery
    - Settings modification
    - Delete user's own post
    - Password stored securely in Database?
    - Try inject script.
    - Try inject SQL
    - Was AJAX present?
    
- The following are the expected outcomes:
    - Preliminary
        - The back-end of the source code is written in PHP.
        - There are no frameworks used in the source code.
        - You will notice the file config/database.php in the source code.
        - You will notice the file config/setup.php in the source code.
        - You will notice we setup our PDO in the file config/database.php
    - If you start the apache servers from XAMPP and navigate to localhost/(port)camagru you will see the landing page for Camagru.
    - You can navigate to the signup page, enter your credentials and register an account.
    - You should be able to login using the credentials you created.
    - You should be able to navigate to the webcam page and use the webcam after allowing Camagru access to your internal webcam.
    - You should be able to access the public gallery where you can view, like and comment on other users' posts.
    - You should be able to modify your settings and details on the setting page.
    - You should be able to delete your own posts.
    - The Password should be hashed before being stored in the DB.
    - No 'Alert' should show up.
    - No DB information should be displayed.
    - You can see the use of Ajax in the source code.
