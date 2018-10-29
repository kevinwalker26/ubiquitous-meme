# X-Team 112 Badger Planner

See https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#code for tips on using *Markdown* tags to format __.md__ files

## Goal

Work as a team to create a project proposal for your X-team to complete together.
The project does not have to be extremely difficult,
but there must be work to do for each member of your team.
You may reference figures using "See figure 1".  
Be sure to submit corresponding image files, i.e. figure1.png (or figure1.jpg) for each figure.

## Grading: To earn full credit, your team's proposal must include:

* (md) documentation: [this file] describing purpose and use of your program

* Description of a program that has:

  ** a main Java program class in a file named Main.java
  
  ** a custom data structure designed and built by your team
  
  ** comprehensive testing of individual units
  
 Caution: You are not being asked to implement this program, at least not yet. 
 We just want your group to make a proposal or pitch for your program.
 
 Tip: Your custom data structure can be composed of or extensions of data structures that you have learned and used in previous programming assignments.  We're looking for decisions about how to build a high-level data structure that will likely have lower-level components.

## Problem Description

It can be difficult to keep track of all the things you have going on during the semester. It is common for students to lose track of assignments, exams, and projects and even more common to not start them early enough. What if there was a way for you to insert assignments, exams, and projects into a planner that would automatically start notifying you prior to the due date so you don't forget about it or have to cram?

## Proposed Solution

A program that could solve this problem would store upcoming assignments, exams, and projects and notify the user as the due dates approach. It would change notification beginning times based on the category of the item. These notifications would persist until the due date has passed or the item has been marked as completed. 

## Questions to answer for Exercise #2

1. Name: Badger Planner


2. Output: Describe the output your program will produce. Include and example format of the output produced.

The output will be some sort of notification. The email will be a base string value that is concatenated with the inputs to give an alert. It may have to send multiple notifications at different times.  Another form of output will be within the app which is described below. 


3. Input: Describe the data that is needed to solve your problem. Include an example format of the input data.

The item's due date, the name of the item, the priority of the item (how urgent the item should be completed) and the course that the item is for, as well as a boolean variable that marks whether the item has been completed or not. From the user interface it will be inserted into the text boxes and be accepted as multiple separate strings following this format  
`<(name) (mm dd yy) (course) priority>`  
This has the first three items as type string and then priority will be an integer.


4. User Interface: Describe a user interface for your program.  Use text menus or a simple graphic user interface.

When user enter the interface, on the left of the graph is the current assignments that users need to complete. The interface will send notifications to users according to the priority of assignments. On the right there is a list of completed assignment which records completed assignments. When the assignments are completed, the interface will move the assignment from left to right. The bottom line are operations to create a new assignment. 

[Sample User Interface](https://drive.google.com/open?id=1hKOlTOXYx_IMB-r_j_UAClqE0BM5muOl)


5. Types List: Break your solution idea down into units that you think can be implemented with a single class.

For our Bader Planner class, one field would be to the data structure of some custom type of priority queueue, a PlanningQueue. The priority would be determined by the urgency input that the user enters. The priority queueue would hold custom objects for the assignments. This assignment object would have a due date field, name, class, completed, and an urgency. There would also be a field for the display object that would hold different utitlity display objects such as the buttons, text boxes, check boxes.

Name each interface or class and briefly describe its function or purpose.

* PlanningQueueADT . describe the functions and rules for the queue
* PlanningQueue . the queue that holds the different objects and both the uncompleted and completed assignments ordered by priority
* Assignment . a class for the custom assigment object
    * Fields:
        * int dueDay
        * int dueMonth
        * int dueYear
        * String name
        * int priority
        * String course
        * boolean completed
* PlanDisplay . a class for the diplay object that uses the multiple display utilities such as the buttons, text boxes, and check boxes   
Our code will be white box tested using JUnit. We will use the coverage tool within Eclipse to reach this white box testing goal. Key items to test will be checking an item for completion, what is displayed when there are no assignments and error handling when the inputs for a new assignment is not done correctly.

## Edit and Submit this file and any figures referenced by this document.

