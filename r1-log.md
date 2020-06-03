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

### Day 10
* Learnt how to use startActivityForResult() so the child activity opened can send data back to the parent (in this case when a button is clicked, which also finishes the activity)

### Day 11
* I've read a few times now that for monetary values in Java, I should be using the BigDecimal data type instead of double or float. Today I changed my expense calculator app to use BigDecimals for all the figures, which is not as straightforward as it sounds because they work a bit differently to doubles and floats. BigDecimals are immutable so you must create a new one each time you want to use one rather than reassigning the value, and you can't do a simple `total = total + somevalue` to add to it. Instead it's  `total = total.add(somevalue)`. Not difficult but just some extra steps to work out. 
* Figured out how to pass a reference to an image with the intent so that the child activity screen shows a different image according to the list item that opened it.

### Day 12
* Did some Java reading

### Day 13
* Did some iOS/Swift reading

### Day 14
* Did some reading about Android RecyclerViews ahead of starting the fourth (and final) Android app.

### Day 15
* Began work on the NewsPortal app by following some tutorials to work out how to set up the RecyclerView to list news sites. Ran into a similar issue as Day 8 when I tried to declare an ArrayList (to add sites to) before OnCreate. Fortunately I remembered I'd run into this before so solved it a lot faster! Experimented a bit with access modifiers when my IDE showed advice that some things could be a more restricted level. 

### Day 16
* Day 1 of "Sam's Teach Yourself Java in 21 days"

### Day 17
* Did some reading about Android fragments
* Added a fragment to my NewsPortal App and worked out how to bring it to the front when a RecyclerView item is clicked
* Worked out how to pass the label of the clicked item to the fragment, to display it as the heading; will probably use this to determine what else should be shown in the fragment.

### Day 18
* Worked out how to open a URL in a browser when a RecyclerView item is clicked
* Worked out how to send a whole object to a fragment for more efficient loading of data in the fragment
* Added all the required content to the objects, and worked on more efficient ways to construct the news outlet objects and pass data around
* Added a utility method for loading the news outlet's logo into any given ImageView, so the same four lines of code used each time could be replaced by one method that takes a single parameter - the ImageView to load into. The method is able to get everything else from within the object class. 

### Day 19
* Learnt how to make an API request using Volley
* Loaded latest article for Australia from NewsAPI.org in the main activity of my news portal app, opening the link when the article is clicked
* Made a bunch of design improvements, including finding out how to import Google fonts

### Day 20
* Learnt how to load images from URLs using Pisasso library
* Created workaround for an issue with the NewsAPI response where some news outlets can't be directly queried

### Day 21
* Day 2 of "Sam's Teach Yourself Java in 21 days"

### Day 22
* Started learning how to create apps in Xcode with storyboards, using [this dice app tutorial](https://www.ralfebert.de/ios/beginner-tutorials/iphone-app-xcode/)

### Day 23
* Day 3 of "Sam's Teach Yourself Java in 21 days"

### Day 24
* Day 3 of "Sam's Teach Yourself Java in 21 days"

### Day 25
* Started [A Cloud Guru's Intro to AWS course](https://acloud.guru/learn/aws-technical-essentials)

### Day 26
* Started [A Cloud Guru's AWS Cloud Practitioner course](https://acloud.guru/course/aws-certified-cloud-practitioner/) - intro, account setup, billing alarm

### Day 27
* Started on [Ray Wenderlich's iOS/Swift course](https://www.raywenderlich.com/4919757-your-first-ios-and-swiftui-app/) - intro content
* Read documentation for [The Dog API](https://thedogapi.com/) and [The Cat API](https://thecatapi.com/) with a view to using these for an iOS or Android project for uni

### Day 28
* AWS Course - S3 buckets
* Created an iOS app project, started working on the layout

### Day 29
* AWS Course - EC2 intro
* Set up Drupal site for a client project and started on developing the theme
* Set up Android project [DoggyData](https://github.com/doubleedesign/DoggyData) app for uni project

### Days 30-39
* Worked on Drupal site for a client project

### Day 31
* Worked on the layout for DoggyData project
