# #100DaysOfCode Log - Round 1 - [Leesa Ward]

The log of my #100DaysOfCode challenge. Started on [April 4, 2020].

## Log

### Day 1
My first task is an Android unit converter app. It's required to handle lengths, weights, and temperatures. 
* Installed Android Studio
* Worked out how to set up and run an emulator
* Started by following a tutorial for a basic length unit converter, using an input text field, two spinners (drop-downs), a button that runs the conversion method, and the result text field.
* Changed the conversion method to use switches instead of if/else statements because it's neater.

### Day 2
* Wrote new spinner adapters for the "to" field and a method to change which one is used according to the selected value in the first spinner. All units are now shown in the "from" field, but, for example, if a length unit is selected then only lengths can be selected for the "to" field. This prevents users from attempting to convert centimetres to degrees celsius, for example. 
* Many examples of unit conversion methods work by returning a number to multiply the input by to get the result. However, this doesn't work for temperatures as the formula is more complex. I altered my conversion method to run a formula and save the result in a variable (rather than saving the multiplier for use in another method).
* Worked on the interface design - added labels, made the layout neater, reordered fields. Learnt about settings like margins and positioning elements after other elements.
* Worked out how to allow the spinner to have slightly different labels than the actual unit names (e.g. "Degrees Celsius" while still using the unit name in the code. I did this by altering the method that gets the unit name from the spinner to remove the word "degrees" before doing anything.
* Worked out how to close the on-screen keyboard when the button is clicked for a smoother user experience (otherwise the result field would be covered by the keyboard). 

### Day 3
* Forked this repo and wrote up what I did on my unit converter over the weekend

My next task is a timer app, required to have the ability to start, pause, and reset, as well as automatically saving the previous time. 

### Day 4
* Built layout for Android timer app
* Learnt how to apply colours, and more layout settings such as how to align text and put two buttons side-by-side.

### Day 5
* Got most of my timer working - start/stop buttons 
* Start button changes to pause button when timer is running
* Message is updated upon stopping, and timer resets
* Previous time not saved persistently yet. 

### Day 6
* Worked out how to save the time persistently using shared preferences, when the appropriate lifecycle methods are run
* Worked out how to keep the timer running and state persistent when the device is rotated (saving/restoring instance state)

### Day 7
* Troubleshooted issue with data saving on device reorientation when it shouldn't - learnt that the onDestroy() lifecycle callback is run on device reorientation, and that there is an isFinishing() check I can run to check whether the app is actually being closed or the device is simply being reoriented, and run my functions (or not) accordingly. 
* Started work on the next task, a basic expense calculator application, by familiarising myself with the requirements and concepts of list view and intents.

### Day 8
* Set up layouts for main activity of expense calculator app. Learnt the hard way (through a big, difficult-to-understand error message) that I can't declare variables for the interface elements (in this case the ListView) at the top of the activity (before onCreate) because the app doesn't know they exist before onCreate().

### Day 9
* Learnt the basics of Intents and how to send basic data from one activity to the next. 
