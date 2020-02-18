---
layout: post
title: Season of KDE Final Report
subtitle: Part 2
tags: [KDE, Season of KDE]
---
SoK is finally ended yesterday and it's been a great learning experience for me. In these last 40 days, it really made me lot more comfortable and confident as a open source contributor :).

In my previous report - [previous report](https://shivam8287.github.io/2020-01-30-sokStatus/). I mentioned about the completion of smallnumbers and enumerate activity.

Now, till the end. i have successfully completed the last remaining algebra activity and all three activities are successfully merged in gcompris multiple_dataset branch.

New changes i have made in four algebra activities:-
* Added multiple dataset
* OK Button to check answer

Challenge i found while working on this activity is to merging of Activity's previous settings with multiple dataset dialog. i tried to look in other activities to find how it is actually implemented but no luck. Later with some smart use of grep command, i found that it is implemented in core files and i need to follow the same pattern as other activities and problem fixed. Another problem which Animtim noticed is reordering of levels in wrong way. it was appearing like - 1,10,2,3,4,5,6,7,8,9. Here it was easy to guess that some code is sorting level folders lexicographically and not like a numbers. i discussed it with Allon and Animtim and found the exact solution in js documentations and finally able to fix it with only one line change in core part. 

Final look of activity

![Algebra Activity](/img/algebra.png "Algebra Activity")
![Dataset](/img/dataset.png "dataset")


With this final task, i have successfully completed SoK2020. now i am eagerly waiting for gcompris release so my work will reach users and kids around the world.

i once again thank my mentors and KDE for making this winters awesome. 
