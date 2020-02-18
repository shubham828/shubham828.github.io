---
layout: post
title: Season of KDE Final Report
subtitle: Part 2
tags: [KDE, Season of KDE]
---
SoK has finally ended yesterday and it's been a great learning experience for me. In these last 40 days, it really made me lot more comfortable and confident as an open source contributor :).

In my previous report - [previous report](https://shivam8287.github.io/2020-01-30-sokStatus/). I mentioned about the completion of smallnumbers and enumerate activities.

Now, till the end. I have successfully completed the last remaining algebra activity and all three activities are successfully merged in Gcompris multiple_dataset branch.

New changes that I have made in four algebra activities:
* Added multiple dataset
* OK Button to check answer

The major challenges I faced while working on this activity is to merge of Activity's previous settings with multiple dataset dialog. I tried to look in other activities to find how it is actually implemented but no luck. Later with some smart use of grep command, I found that it is implemented in core files and I need to follow the same pattern as other activities and problem was fixed. Another problem which Animtim noticed is reordering of levels in wrong way. They were appearing like - 1,10,2,3,4,5,6,7,8,9. Here it was easy to guess that some code is sorting level folders lexicographically and not like a numbers. I discussed it with Allon and Animtim and found the exact solution in js documentations and finally able to fix it with only one line change in core part. 

Final look of activity

![Algebra Activity](/img/algebra.png "Algebra Activity")

![Dataset](/img/dataset.png "dataset")


With this final task, I have successfully completed SoK2020. now I am eagerly waiting for gcompris release so my work will reach users and kids around the world.

I once again want to thank my mentors and KDE for making my this winters awesome. 
