# Tools-MET-quiz-
README

Project Name
THE MET QUIZ

PythonSquad Group Member
Xinya Yan xy2382
Brian Park bsp2120
Zhen Luo zl2723
Nan Xiang nx2147

Purpose of the project 
The project will create a user-interactive quiz on different objects on display in the Metropolitan Museum with randomly generated multiple-choice questions. 

Output
The output is a GUI window which generates the image of an object on each page and a related multiple-choice question. The user will be able to choose from 4 answers and be told if the choice is correct or not and the correct answer if answered wrongly. The program will also keep track of the user’s performance, in terms of number of correctly answered questions out of the total number of questions.
The questions can be about the artist, time period, or region.

Coding Process
1. Extracted database containing all information of objects on display at the Metropolitan Museum
2. Used pandas to delete unused columns. Formatted entries that have overlapping and inconsistent contents (e.g. France, South France), repeated information (e.g. one datapoint being "France, Italy, France"), typos, or multidata types (e.g. century was listed as strings or floats at random). Cleared vague entries (e.g. unknown, perhaps, probably, etc.). Added a new column for valid image links
3. Created a new csv document holding the cleaned data
4. Created a dictionary containing question category as key, and list of valid object ids corresponding to each of our three question categories as corresponding values to each key. Created a similary formatted dictionary that contains question category as key, and list of unique values correspond to each category.  
5. Created functions to randomly select a category from the set of artist, region, and time, and then randomly select an object id from the valid_id_list accordingly
6. Created functions to determine the content of the question stem, the object title, object image, related information link. Four choices were created while making sure that they don't have overlapping words. Choices were assigned to ABCD randomly
7. Created functions to record the letter corresponding to the correct answer and to check if the correct answer is chosen
8. Created functions to come up with the next question and refresh all setups for the previous question
9. Created functions to count the total number of questions that have been answered and the correctly chosen ones
10. Established a GUI class with labels and buttons connecting with the functions to display the desired content
11. Implemented a quit button so that the user can choose to stop whenever he/she wants to
12. Adjusted the layout of the GUI window

RUN INSTRUCTION
Run through the GUI file for the pop-up window to show. Then you can click out the buttons to check the functionality of the implementation (and your knowledge about the MET objects). 

Requirements
Pandas / numpy / re / tkinter / random / urllib.request / request / Image, ImageTk / BytesIO / webbrowser
