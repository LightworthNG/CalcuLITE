/****** DOCUMENTATION ******/
        
/*** 
    
    function equal_was_last_clicked() //the hinge of the programme
    
    Function to check if the equal button was the last button to be clicked,
    if so, return true otherwise false .
    
    this function will access the global variable equal_check
    and checks if it is an empty string[that is equal to button has not been set/clicked]
    so it returns true but if not, returns false .
    
    The returns from this function will be used by display_user_input() to determine
    how input should be displayed.
    
    HOW INPUT SHOULD BE DISPLAYED
    When a user comes and the page loads, the equal_check variable is set 
    to an empty string "" , all his input will be appended/concartenated 
    untill user hits the equal button.
    
    When the equal button is hit, two this happen
    1) All his input is grabbed by the result() function and evaluated
    and the evaluated result is displayed
    
    2) The equal_check variable is modified[changed from an empty string. Anything can go apart from an empty string]. This modification is critical because if the user desires to perform a new calculation, he may choose to clear but  not necessarily because, the 
    state of the equal_check variable[global variable so can be accessed by functions]
    will be used by the display_user_input() function to determine whether to 
        
        clear before displaying user input OR display user input
        
    If the equal_was_last_clicked() function returns true, 
        a) the user input display box s cleared, 
        b) the new value is set and 
        c) the equal_check is unset
    This sequence of actions is necessary for the smooth runing of the calculatorLite.
    
    NEXT VERSIONS
    
    Our next visit will focus more on 
    
    1) Serious validation of user input
    2) User input error handling
    3) Creation of an improved user experience
    
***/


/******SETTING OF GLOBAL VARIABLES ******/
        
/*** 
set a global variable for checking if equal_was_last_clicked .
Depending on its value, the input display screen can be cleared 

***/

/******REGISTER ALL FUNCTIONS USED  ******/

/***
function equal_was_last_clicked()
Function to check if the equal button was the last button to be clicked,
if so, return true otherwise false . 

***/
/***
function display_user_input()
This function is tied to an evenListener which listens to click events 
from all numeric input buttons

The event object is the button that has been clicked

It display the user input onto the display screen
  
***/


/***
function result()
This function is tied to an evenListener which listens to click events 
from equals buttons only

The event object is the equals button that has been clicked

It display the processed user input onto the display screen
  
***/