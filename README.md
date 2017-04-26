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
