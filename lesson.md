# Big Idea 3 (Data Structures including List, Dictionaries, 2D arrays and Iteration)

## Leaderboard Database (Kaiden and Navan)
- This is the Leaderboard Class and this part is declaring the keys for the data within the class 
    - ![](https://user-images.githubusercontent.com/58792082/233266574-d205a5ce-da6e-4050-84d7-154da8f85670.png)

- These are the setters and getters for the values: username, pointsEasy, pointsMedium, and pointsHard
    - ![](https://user-images.githubusercontent.com/58792082/233268298-a2643fd3-9b52-40fc-81a3-e0cb4de9d89b.png)
    - This is for the password and it also has a function to check if the password matches and a function to encrypt the password 
    - ![](https://user-images.githubusercontent.com/58792082/233268610-1bb0e439-e316-4a7f-b5da-3ee323ce2057.png)
- These display the values of the Leaderboard in JSON values for analyzation, and CRUD functions later on
    - ![](https://user-images.githubusercontent.com/58792082/233268790-7b16a05c-47b9-4177-8ba7-984fd9145553.png)
- These CRUD functions allow us to test out the Create, Read, Update, and Delete
    - ![](https://user-images.githubusercontent.com/58792082/233269089-7c0c5115-45a5-49b1-ab89-978ccd6d74db.png)
- This is the tester data that would populate the database in order to test the data 
    - ![](https://user-images.githubusercontent.com/58792082/233269462-5797df24-7d99-48fa-829d-d98a71dd5fbe.png)
    - The try and except allows the code to continue to function even if there is an error, if there is an error, it is reported but the init_leaderboards() still initializes all of the leaderboards after the error

## Connection of Databases from Frontend to Backend (David and Alex)
We will establish endpoints in the backend, which will ultimately connect to the frontend

The backened takes note of the SQLite database that we use, and runs certain queries over it to filter and return valid values. Additionally, we also used a dictionary data structure to represent the key and value pairs in our JSON data, and also used a list to represent all the valid database entires that we can select from. By creating an API endpoint on our backend, we can thus retrieve this jsondata in the frontend, and display the necessary image or update the necessary variables that is required for program execution 


### Leaderboard (David)

>CRUD is an acronym used to describe the processes needed in a functional program. These include being able to create, read, update, and delete data based on the database used. This allows total control over data sets and allows fro total manipulation of the dataset.

#### Create

![]({{site.baseurl}}/lessonimages/create.png " ")

Parser is used to look through dataset and make sure there are no duplicates and then to make a new data entry.

#### Read

![]({{site.baseurl}}/lessonimages/read.png " ")

Parser is used in order to look through dataset for all values and send them to frontend.

#### Update

![]({{site.baseurl}}/lessonimages/update.png " ")

Parser is used to look for specific data value you are searching for and then update another specific value based on that found data fragment.

#### Delete

![]({{site.baseurl}}/lessonimages/delete.png " ")

Parser is used to look for specific data value you are searching for and then delete that found data fragment.

## JWT (Nikhil)
![Screenshot 2023-04-19 at 11 10 22 PM](https://user-images.githubusercontent.com/111464993/233273969-b65fca5c-9269-4934-a93c-7ec4a4a103ec.png)
<br>
In this pciture there is a function called getPassAPI and the function of it is to generate a random password. 
A function called "getPassAPI" is created, with a default password length of 3.
An empty list called "password" is made to store the password.
A rapid API is used to set up to get random words.
The code asks the website for random words based on the password length.
The random words are added to the "password" list.
Extra random characters are added to make the password longer.
The password list is shuffled to mix the words and characters.
The shuffled list is combined to make the final password.
The password is returned as the result of the function.

The next few functions are just app routes routing to the html file, and generating and saving the password into a json file. 
![Screenshot 2023-04-19 at 11 10 35 PM](https://user-images.githubusercontent.com/111464993/233273967-8a506d87-9eca-4fcf-92dd-afe65df23457.png)
<br> 
There are two functions, register and login, which handle user registration and login for a web application. 
Steps for each
register function:
a. Creates a registration form using the RegisterForm class.
b. If the form is valid, it hashes the password entered by the user.
c. Creates a new user with the provided username and hashed password.
d. Adds the new user to the database and saves the changes.
e. Redirects the user to the login page.
f. If the form is not valid, it displays the registration page with the form.

login function:
a. Creates a login form using the LoginForm class.
b. If the form is valid, it checks if the entered username exists in the database.
c. If the user exists, it checks if the entered password matches the stored password.
d. If the password matches, it creates a token using the username and a secret key.
e. Redirects the user to the dashboard page and stores the token in a cookie.
f. If the username or password is incorrect, it displays the login page with the form.
g. If the form is not valid, it displays the login page with the form.


<br>


![Screenshot 2023-04-19 at 11 10 49 PM](https://user-images.githubusercontent.com/111464993/233273963-a6088d75-6f63-4488-90aa-91548216951b.png)
Just saves it to a json file. 

<br>

![Screenshot 2023-04-19 at 11 10 45 PM](https://user-images.githubusercontent.com/111464993/233273965-ecbd9a2b-4427-4f6d-8a20-018d48e6c4fb.png)

<br>
This code defines two functions, dashboard and logout, which handle user dashboard access and logout for a web application.
dashboard function:
a. The route is set to '/dashboard' with both 'GET' and 'POST' methods allowed.
b. The @token_required decorator is used, meaning a valid token is required to access this function.
c. If the token is valid, the function renders the 'dashboard.html' template, which is the user's dashboard page.

logout function:
a. The route is set to '/logout' with both 'GET' and 'POST' methods allowed.
b. The @token_required decorator is used, meaning a valid token is required to access this function.
c. The function logs out the user by calling logout_user().
d. It then creates a response that redirects the user to the login page.
e. The token cookie is set to expire immediately, effectively removing the token from the user's browser.
f. The response is returned, and the user is redirected to the login page.

<br>

![Screenshot 2023-04-19 at 11 09 45 PM](https://user-images.githubusercontent.com/111464993/233273962-4c26a095-df29-4d4b-ab9a-7c0fd2489163.png)
This code defines a User class and a token_required decorator function for a Flask web application.

User class:
a. Inherits from db.Model and UserMixin to create a database model for user information and provide authentication functionality.
b. id: A primary key column with an integer type for storing unique user IDs.
c. username: A string column with a maximum length of 20 characters for storing usernames. It cannot be empty (nullable=False) and must be unique.
d. password: A string column with a maximum length of 80 characters for storing hashed passwords. It cannot be empty (nullable=False).
This class is used to store user information in a database, and it helps manage user authentication.

token_required function:
a. A decorator function that takes another function f as an argument.
b. The decorator function is defined inside token_required. It checks the token in the user's request and verifies it before executing the function f.
c. First, it extracts the cookie from the request headers and looks for a token in the cookie. If there is no token, it returns a JSON response saying a valid token is missing.
d. If a token is present, it tries to decode and verify the token using the app's secret key and the HS256 algorithm. If the token is valid, it retrieves the current user from the database based on the username in the token's payload.
e. If the token is invalid or decoding fails, it returns a JSON response saying the token is invalid.
f. If the token is valid, it executes the original function f with the current user and any other arguments or keyword arguments passed to it.
The token_required decorator is used to protect routes that require user authentication. It ensures that only users with a valid token can access the protected resources.






![Screenshot 2023-04-19 at 11 09 52 PM](https://user-images.githubusercontent.com/111464993/233273960-f72c048b-f062-4bb8-b834-3af736f8c75c.png)

This code defines two classes, RegisterForm and LoginForm, which are Flask forms used for user registration and login. They are based on the FlaskForm class from the Flask-WTF library. 

RegisterForm class:
a. username: A StringField representing the username input field with validation rules that require it to be between 4 and 20 characters long. It also has a placeholder text "Username".
b. password: A PasswordField representing the password input field with validation rules that require it to be between 4 and 20 characters long. It also has a placeholder text "Password".
c. show_password: A BooleanField that allows users to show or hide the password as they type it.
d. submit: A SubmitField representing the register button.
e. validate_username method: A custom validation method for the username field that checks if the provided username already exists in the database. If it does, a ValidationError is raised, prompting the user to choose a different username.

LoginForm class:
a. username: A StringField representing the username input field with validation rules that require it to be between 4 and 20 characters long. It also has a placeholder text "Username".
b. password: A PasswordField representing the password input field with validation rules that require it to be between 4 and 20 characters long. It also has a placeholder text "Password".
c. submit: A SubmitField representing the login button.

These classes are used to create and validate registration and login forms in a Flask web application. They ensure that the input provided by users meets the specified requirements and helps prevent issues related to invalid data.


## Picture Database (Ethan T.)
- ![image](https://user-images.githubusercontent.com/111910633/233181629-36a561c0-8ba5-4644-ac43-274c74a55dff.png)
- Used CRUD methods which have create, read, update, and delete rows in the table.  There is a function     called initEasyImages which populates the 'Images' table with data.
![image](https://user-images.githubusercontent.com/111910633/233180602-c81c1931-85a4-4d8e-b738-a091eb803d60.png)
-  The table has five columns: id, _imagePath, _xCoord, _yCoord, and _difficulty.
- ![image](https://user-images.githubusercontent.com/111910633/233181071-4442d4c3-8c54-497f-b3bf-d625e6742c05.png)
- This part of the code defines getter and setter methods for the columns in the Images model.  It sets and retrieves the metadata of the image.  Each column has a getter method defined with the @property decorator, which allows the method to be called like an attribute. The getter simply returns the value of the corresponding attribute (e.g., self._imagePath for imagePath).
- ![image](https://user-images.githubusercontent.com/111910633/233181852-9daeed5a-6ab7-4d46-8069-8bcf390ea07a.png)
- The initEasyImages function initializes the database with image metadata for easy difficulty images.



### Picture (Alex)



## Time and Space Complexity of Algorithms (Ethan Z, Alex)
The lesson for time and space complexity of algorithms will consist of demonstrations of sorting algorithms and the different time complexities that they come with on a small scale. This can be acomplished using things such as a deck of cards or even with actual people. An example of how this will work is laying out the cards in a random order on the table, and demonstrating different ways of sorting it. From methods such as bubble sort to methods such as bogo sort, it will be really easy to see exactly how much time it would take for these different sorting algoritms to complete. Then after that, it is easy to understand the concept of time complexity when given a real world example.

Space complexity can be demonstrated by using the same method, however, adding in the extra step of having the cards in a pile. This will show how much space is needed to complete the sorting algorithm. This will easily reveal the concept of space complexity because it allows people to witness a real world, physical example of the concept, turning a really hard to grasp concept into something that is easy to understand.

Additionally, we are also going to analyze certain algorithms within our project to show how such analysis is applicable to real world projects.
