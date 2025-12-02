# Welcome to Bug Wrangler Ranch

This first self-assessment is for you to hone several Core Skills that you need as a software developer.

Taking your time now to be thorough, reflective, patient and curious will give you the foundation to be successful throughout the rest of this course and your career.

If you rush this, or think of it as a test to be "passed", then you will already be on the wrong path.

> 🧨 Make sure you answer the vocabulary and understanding questions at the end of this document before notifying your coaches that you are done with the project

## Description

Slim Jenkins offers a vacation package for people who have always wanted to join a cattle driving team across the American Midwest.

He calls it the **Kansas Slim's Cattle Adventure**.

People join a team of experienced drovers who will train them in the basics of herding cattle and driving them across hundreds of miles to their destination at Old Red's Ranch.

Unfortunately, someone gained access to the code that produces an outline of the adventure to the paying customers, so Slim has hired you to examine and fix the code.

## Learning Objectives

Here are your learning objectives for this self-assessment.

1. Able to use the debugger to step through existing code to discover root causes of bugs.
2. Drawing a sequence diagram for a project.
   > Use the [sequencediagram.org](https://sequencediagram.org/) site to generate your sequence diagram. Make sure you save your work as you go.
3. Demonstrate learning efficiency by researching concepts you haven't seen before using your peers, mentors, and the World Wide Web as resources.
4. Awareness of when you need help, and then seeking it out.

## Example Output

If you are able to fix all of the bugs, you will output similar to what is below. It will not be identical, but similar.

```sh
************************************************
**  K A N S A S   S L I M ' S   C A T T L E   **
************************************************

\|/         (__)
     '------(oo)
       ||   (__)               \|/
       ||w--||     \|/
   \|/
            \|/                     (__)
                             '------(oo)
                               ||   (__)
                               ||w--||     \|/

You will be accompanying 5 drovers as they drive 50 cattle to Old Red's Ranch for grazing

The herd is made of up the following types of cattle:
Ankole-Watusi,Brown Swiss,Brown Swiss,American Angus,Brown Swiss,
Ankina,American Angus,Ankina,Brown Swiss,Ankole-Watusi,Brown Swiss,
Brown Swiss,American Angus,Ankina,Ankole-Watusi,Brown Swiss,Brown Swiss,
Ankina,Brown Swiss,Ankina,Ankole-Watusi,Brown Swiss,Brown Swiss,
Ankole-Watusi,American Angus,Brown Swiss,American Angus,Ankole-Watusi,
Ankole-Watusi,American Angus,Ankina,Ankina,Ankina,Ankole-Watusi,
American Angus,Brown Swiss,American Angus,Brown Swiss,American Angus,
American Angus,Ankina,Brown Swiss,American Angus,Ankina,Brown Swiss,
American Angus,Ankole-Watusi,Ankina,American Angus,Brown Swiss

Here is the team of drovers you will be joining
        * Melvyn Hethron
        * Yancy Gresley
        * Willabella Attarge
        * Ynes Gyenes
        * Farlie Spere


Your journey will take you through the wildness of the American Midwest and across the following terrain
        * forest
        * plain
        * river
        * mountain
```

1. In the **main** module, one of the first lines of code is `const drovers = hireDrovers(cattleToDrive)`. Explain what the value of the `drovers` variable is when that line of code runs.
   > The variable "drovers" is an array
   
   > the value of "drovers" is an array that holds the 5 drovers objects that are randomly picked from our database.
2. At the bottom of the main module, you will see the following code - `for (const drover of drovers)`. Explain what the values of both the `drover` and the `drovers` variables are.
   > these variables are Objects
   
   > Drover is a variable that holds one object from the drovers array during each iteration (each time the loop runs). the loop iterates through the array and on each iteration drover gets assigned the next object in the list.
3. In the **journey** module, there is a `journeyMaker()` function. In that function, there is a variable named `areas` which will have the value of an object. Use your debugger to show what the value of each key is on that object. Use [Loom](https://www.loom.com) to record your session.
   > Your public Loom URL here. https://www.loom.com/share/bb16e29ff24e45f3b6a915a4deb5959b
4. Also in the **journey** module, there is the following code:
   ```js
   for (let forestNumber = 0; forestNumber < areas.forests; forestNumber++) {
      journey.push("forest")
   }
   ```
   Explain this code with your best vocabulary.
   > The code above is a for loop that takes the array variables and loops it through the objects repeatedly till it goes through the whole list and provides the data in the local scope
   
   > the for loop executes the code inside the curly brackets repeatedly. Each time it runs, it pushes (adds) the string "forest" to the journey array. this repeats until forestNumber is no longer less than areas.forests.
   >this is a for loop we are setting the forestNumber variable to 0. It's telling it where to start. then were going to check if forestNumber is less than areas.forest (which is 2). So long as this condition is true it will add one to forestNumber each time it runs. The code will then push the string forest to the journey array.The loop will continue to run until the condition is false   

5. Explain the value of the `database` variable in the **database** module. Be as comprehensive as possible.
   > The value of database is a variable. it was created to store the information for the module that we can access when needed 

   > database is an object. it serves as the main data structure for storing information about the bug ranch operation. the database object contains two arrays
   
   1. cattleTypes- this is an array containing objects that represent different breeds of cattle. Each cattle breeds object has two properties: an ID and a breed there are 4 cattle breed objects in this array.

   2. drovers- This is an array containing 50 objects that represent individual cattle herders. each drover object has 4 properties: ID, first_name, last_name, and gender.

   this database object stores all the essential information needed for the applications-what types of cattle exist and who drovers are. It's exporting at the bottom with module.exports, which means other files can import and use this data.


   6. In the **drovers** module, there is a `hireDrovers()` function. You will notice the following code on that line - `(herdSize)`. What is that defining, and where does it get its value?
   > I believe the variable herdSize is coming from the cattle.js module 

   > (herdSize) is a parameter. It's a placeholder for the argument that the function will pass in. in this case the argument we are passing in is the variable cattleToDrive which is 50.
   
   
## When You Are Done

After you have answered all the questions above, you need to push all of your code back up to Github. Follow these instructions.

1. Be in the `bug-wrangler-ranch` directory.
2. `git add --all`
3. `git commit -m "Code complete"`
4. `git push origin main`

Then go to the Learning Platform and click the **Self-assessment Complete** button.
