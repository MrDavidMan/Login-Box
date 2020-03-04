# Login-Box
Simple Python Login Box

# What this is

This is a simple register and login GUI that can store usernames and passwords and process login requests.

## Installation 
This program runs on Python 3 and the main driving module for this is Tkinter. 

**WARNING:** This program will **NOT** work if you are running Python 2. The Tkinter module has two variations of itself. One is for Python 2 and the other is for Python 3. This program is written for tkinter version 8.6 and Python 3.6.4.

Tkinter comes packaged with Python 3 so there should be no need to pip install anything.

To test tkinter and check the verison open a command prompt and type:

> `python`

> `import tkinter`

> `tkinter.TkVersion`

This will tell you that tkinter is working and what version is currently installed.

## Using this Program

1) Navigate to the folder that LoginBox.py is in
2) Launch via clicking the mouse or hitting shift+Right Mouse Button to open a command prompt in the current directory and type `python LoginBox.py`
3) Once launched the application will open and begin to run until exit

## How This Program Works

1) This program works using tkinter and the integrated os module built into Python 3

2) With our GUI application we can input and store usernames and passwords and parse that information to check for matching credentials to find a success or failure

### Functions:

#### `def main_screen():` This is our drive function that will start the entire process.

* Using a global variable `screen` we assign the tkinter module to it and then set its geometry as well as a title. I have named te title "Notes 1.0" but this program could be used for any program that requires a log in system. The remainder of this function is for the two buttons on the home screen. Login and Register. These will create more screens as the program is used.

#### `def register():`This function is for creating user accounts as well as providing passwords for the,

* **WARNING!:** This program is a simple program that creates passwords in _CLEAR TEXT_ there is **_NO_** hashing or salting done here.   Please be aware of this when using this infront of any program you use it with

* Here we create our global variables that will be used later outside of scope and assign `username` and `password` to StringVar() which will let us itterate through them later


* We assign our elements and provide the corresponding text to their respective fields

#### `def register_user():` This function is used to actually create a user accounts in the same directory that the program is in and input a username and associated password with a line ("\n") in between the two

* With the help of the OS module this will create a text file we write our data to

#### `def login():` This is for when we have a user already registred and wish to login to what ever program is behind our login box


 * We create another global variable but this time called `screen2` as it creates another window that can be manipulated with

 * We assign its place on the window and its geometery as well as create two more global variables called `username_entry1` and 
 `password_entry1` that will go on to be tested to see if they match the current username and password needed to login
 
 * After clicking "Login" we will go through a verification process to test our credentials
 
 #### `def login_verify():` Here we test for a pass or failure of our input
 
 * We grab our data we inputed into the username and password field and will open the text file that matches our username
 
 * The program will test the two fields and the program will execute one of three functions: "Login Success", "Password_not_Recognised", or "User not Found"
 
 
 #### `def login_success():` This function will show a window for success followed by an "OK" button
 
 #### `def password_not_recognised():` This function will run when a user account enters an invalid password followed by an "OK" button
 
 #### `def user_not_found():` This function will run if the program iterates through the file direcory and can not find a user account that matches the input followed by an "OK" button
 
 #### The delete functions serve to delete (.destroy) the frames when we hit "OK" after their respective function is called.



