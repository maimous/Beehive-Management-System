# Beehive Management System
[Head First C#](http://www.headfirstlabs.com/books//hfcsharp/)

&nbsp;
## 00 Start the project
* In VS, create a Windows Forms Application project.

&nbsp;
## 01 Build the form
* Add a GroupBox, a ComboBox, a NumericUpDown, Labels, Buttons and a TextBox.

&nbsp;
## 02 Add the Worker class and its constructor
* The constructor just sets the jobsICanDo field, which is a string array. It’s private because we want the queen to ask the worker to do a job, rather than make her check whether he knows how to do it.

&nbsp;
## 03 Add the Worker class properties
* ShiftsLeft is a read-only property that calculates how many shifts are left on the current job.
* CurrentJob is a read-only property that tells the queen which job needs to be done.

&nbsp;
## 04 Add the Worker class methods
* The queen uses the worker’s DoThisJob() method to assign work to him — he checks his jobsICanDo field to see if he knows how to do the job.
* The queen uses the worker’s DidYouFinish() method to tell him to work the next shift. The method only returns true if this is the very last shift that he’s doing the job. That way, the queen can add a line to the report that the bee will be done after this shift.


&nbsp;
## 05 Add the Queen class and its constructor
* The queen keeps her array of workers private because once they’re assigned, no other class should be able to change them…or even see them, since she’s the only one who gives them orders. The constructor sets the field’s value.

&nbsp;
## 06 Add the Queen class methods
* When she assigns work to her worker bees, she starts with the first one and tries assigning him the job. If he can’t do it, she moves on to the next. When a bee who can do the job is found, the method returns (which stops the loop).
* The queen’s WorkTheNextShift() method tells each worker to work a shift and adds a line to the report depending on the worker’s status.

&nbsp;
## 07 Add queen and worker objects in the form's code
* Setting `workerBeeJob.SelectedIndex = 0;` sets the ComboBox to show its first item (so it’s not blank when the form loads.
* Add an array of four Workers.
* Add a Queen.
