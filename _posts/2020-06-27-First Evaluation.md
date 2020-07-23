---
layout: post
title: First Evaluation
subtitle: Part 5
tags: [KDE, Google Summer of Codes]
---
Hi everyone

It has been two weeks since my last post. In this time period, I took forward my project, adding multiple datasets and completed “share pieces of candies” and “locate the regions” activities.

Our motive behind adding multiple datasets in activities is to make the difficulty range of activities wider. This way the same activity can be easily configured to be played by pupils of different ages or capabilities.

 *GCompris code has been divided into two parts/folders i.e “activities” and “core” part*s.

## Activities parts
The Activities folder includes the implementation of each activity, it contains 1 folder per activity and every folder further contains a QML file, javascript file, and resource folder. Here QML is for designing the user interface, javascript (.js) files contain the main logic of the activity and resource folders, as the name suggests it, contains all the resources for activities. Images are good examples for resource folder.

## Core Parts
Many elements i.e, help button, bonus which pupils see after successfully completing the level, menu bar and even the base container of each activity are the same in many activities. So, obviously rewriting them every time for each activity is time-consuming and makes the code difficult to maintain.  This is why we have a core folder that contains core files which can be easily imported and used by any activity.

Visualization is always easy :).

```
src/
 activities/
        sudoku/
            Sudoku.qml
            Sudoku.js
            resources/
    core/
        ActivityBase.qml
        Bonus.qml    
```
Multiple dataset is implemented in core components of Gcompris. So, whenever I say I have added multiple datasets in an activity, it means I have changed the code of the activity to adapt multiple datasets and added JSON files. We use 1 JSON file to represent 1 dataset and datasets are a resource for an activity so we put them inside the resource folder.

I can further show you the json file and how anyone can easily customize them by discussing my past week’s work on share pieces of candies.



## Share Pieces of Candy
![Share Activity](/img/share.png "Share Activity")

As the name suggests, in this activity pupils have to equally distribute candies between their friends.
<br><br><br><br>


![Share Dataset Activity](/img/share_dataset.png "Share Dataset Activity")
<p align ="center">These are the datasets </p> <br><br>

![Share JSON Activity](/img/share_json.png "Share JSON Activity")

Part of JSON file, which anyone can use to customize levels


We always try to make these keys self-explanatory. One can change values and rerun the application to see the effects.

In Proposal, I planned to only have 2 datasets for this activity but later I found that we have some random levels too, in which we can’t guarantee the extra candies. So after discussing with mentors, we decided to add one flag for each level (you can see the “randomisedInputData” flag in above JSON pic) and the third dataset, which will contain randomized levels.
The Share activity contains lots of levels, sublevels and instructions and I have to edit all those instruction strings according to the data, which was very much prone to typos, that’s why I also asked my sister to test it before pushing the code for review. I found out at the end that I still missed some full stops and other typos :(.



## Locate The Regions
The second activity I worked on is “locate the regions”. My merge request for this activity has been merged today! Yes, now it's a merge request instead of differential. KDE has moved to GitLab now :).
The activity shares the  “babymatch” activity code and I’ve already added the multiple datasets mechanism in “babymatch” some months back while working on “chronos” which inherits from  babymatch. So this time it was very easy. I just had to add JSON files, no change in the logic part.



![Locate Dataset](/img/locate_dataset.png "Locate Dataset")
Here you can see we have divided the datasets country wise, and you know JSON is easily configurable so it’s easy for us to add more countries later, we don’t need to change any JS or QML part of the activity.

The next activity I am picking to add datasets is Categorisation. I will discuss that in my next blog.

Have fun!
