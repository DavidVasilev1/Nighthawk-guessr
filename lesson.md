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



## Picture Database (Ethan T.)
- ![image](https://user-images.githubusercontent.com/111910633/233181629-36a561c0-8ba5-4644-ac43-274c74a55dff.png)
- Used CRUD methods which have create, read, update, and delete rows in the table.  There is a function called initEasyImages which populates the 'Images' table with data.
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
