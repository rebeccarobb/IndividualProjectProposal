# Book Project : 
**Rebecca Robb Open Source Project Proposal**

## Project Abstract
This open source project is a book tracker web application that is practically an organized library interface.
The user can add books to a "to read" list, "currently reading" list,
"read" list or "did not finish" list. These lists are appropriately called "shelfs". There is a rating scale and you can also 
track your progress towards a goals like number or books or pages. Features included are: satistics, exporting data,
user registration and accounts, importing books and more to come. 

## Project Relevance
This project is linked to the educational goals of this class because it can practically apply to
object oriented design, design patterns, debugginging, accessing databases, graphic user interface, and test driven development.
This is relevant because shelves are objects, refactoring can use different design models, there are several databases used for the books, 
the entire web app is a GUI, and there are failing tests that need the code to be refactored. 
This goal is important goal because it will allow students to get experience properly managing the project, 
create version control, and deal with issue tracking in a practical application. 

## Conceptual Design
I have several proposed contributions that could benefit to the proposed open source project. An existing proposed issue is for user valiadation when the user clicks on the 'log in' or 'create account' buttons, error messages should appear for password and confirm passwords fields if they were left blank or if the passwords do not match.  Another issue open is allowing books to span multiple genres, perhaps with a genre array. For this open source project you must be assigned an issue so if these are taken there are other open issues. To avoid this completely we could add features. A possibility in the existing open source project is adding a feature where you can share the books to a friend. I also found a front end styling feature currently is an issue because the books page is not responsive across platforms formats like the iPhoneX. We could also try to add images to books and inculde a search by genre feature. 

**Login Page UML:**
<a href="https://ibb.co/kqFQ5Bg"><img src="https://i.ibb.co/MPLMZSD/Screen-Shot-2021-02-21-at-3-39-04-PM.png" alt="Screen-Shot-2021-02-21-at-3-39-04-PM" border="0"></a>


## Background
Git Repo: 
<https://github.com/Project-Books/book-project>

***Building***
- JDK 11 (no later versions) usable on IntelliJ. (Uses resuable free components for java web apps: Spring Boot and Vaadin 14)
- If you have Node.js installed it must be atleast 10.0 or Vaadin will automatically install it
- MySQL8.0 OR Docker engine for linux or Docker desktop for Windows or MacOS.

**Running**

1. Clone the repository
2. Import the project as a maven project into your favourite IDE (or run maven on the terminal)
3. Start Docker engine (Linux) or Docker desktop (Windows or macOS)
  
Then, if you want to use Docker, follow one of the 3 approaches below: ( I personally used the third. ) 

#### 1. Start locally with only MySQL running in docker

4. Build the project at the root using `./mvnw clean install` (Unix) or `mvnw.cmd clean install` (Windows)
5. Start the MySQL database using `docker-compose up -d mysql phpmyadmin`
    - May need to add `sudo` to this command on Unix
6. Start the application using `java -jar target/book-project-0.0.1-SNAPSHOT.jar` 

#### 2. Start using docker-compose in production mode

4. At the root of the project, build the project in production mode using one of the following commands. In production mode all UI components are packaged in a jar file.
    - `./mvnw clean package -Pproduction` (Unix), or 
    - `mvnw.cmd clean package -Pproduction` (Windows)
5. Start the MySQL Database and book project app using `docker-compose up --build`
    - May need to add `sudo` to this command on Unix
    
#### 3. Start locally with Vaadin live reload (the tests do not run)

We recommended this approach if you need to work on the frontend with Vaadin. This approach allows you to use 
Vaadin Live reload which prevents you from needing to re-run the server every time or manually refresh your browser 
(i.e. it's a lot quicker). 

4. Start the MySQL database using `docker-compose up -d mysql phpmyadmin`
    - May need to add `sudo` to this command on Unix
5. Run the project from your IDE or with Maven:
    - `./mvnw spring-boot:run` on Unix
    - `mvnw.cmd spring-boot:run` on Windows
   
If you're running the app from your IDE, after making a Vaadin-related change, build the app from your IDE after making
any changes.

### Access site

After following the instructions for running the app above, go to `localhost:8080`. Then, log in with the details below:
- Username: `user`
- Password: `password`

### Fixing Lombok errors

You may find lots of errors for things like the log statements, or the entities not having constructors. 
You can find instructions on how to fix this for IntelliJ and Eclipse in our [troubleshooting wiki page](https://github.com/knjk04/book-project/wiki/Troubleshooting). 
Other common errors and solutions are also in the troubleshooting page.

### Access database

To access the MySQL database when docker-compose is running:

1. Go to `http://localhost:8081/`
2. Log in with the settings below.
    - User Name: `root`
    - Password: `rootpassword`
3. Click on connect


## Required Resources
This project is doable on MacOS, Linux, and Windows. 
