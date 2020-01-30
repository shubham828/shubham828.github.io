---
layout: post
title: Season of KDE
subtitle: Part 1
tags: [KDE, Season of KDE]
---

Hey everyone.. This is the first time, i get the chance to work for an organisation and that too the mighty one - KDE. My project is to add multiple datasets in some of Gcompris activities.

My first exposure to KDE was in December 2020, i was bit lost in Big KDE world at starting but KDE dev's helped me alot to get started started. i would specially like to thanks [Valorie](https://twitter.com/valoriez?lang=en) to have that 2 hour chat with me and told me, how thing's work here.

Half period of the KDE has Passed and Till now it has been awesome, incredible learning experience and it was not that easy as i thought but i have super helpful mentors Johnny Jazeix and Emmanuel Charruau :). i have completed enumerate and smallnumbers2 activities, algebra_by still lefts. 

I started my SoK with smallnumbers2, the main challenge with this activity is it shares same code with some other activities too, so while working on it i have to take care that my patch shouldn't break them. First thing which i have to do is repeat elements from JSON file several times so i have the options to acheive this eigther by modifing previous JSON files or make changes in js file.I choosed second option (ofcourse it was more interesting). The first patch i have submitted was just a rough and ready solution, which Emmanuel discussed with me for several hours and we arrived to a neat approach at the end and i remember it was **5AM** in India. Things was bit smoother after that, my code quality increased then i also modified this algorithm to drop elements randomly where elements which current level is teaching will drop more often than other elements. Later i also added this updated dataset to smallnumbers activity as they both activities were sharing same code.

Second activity i picked is enumerate. Things i have done this activity is -
 * multiple dataset
 * Sublevels
 * OK button to check answer
 * Instruction Window for each level
 * removed need of backspace
 * Improved Visual feedback on answer column

Adding multiple dataset and sublevels in this activity was quite easy and straight forward for me but all other task made me to get out of comfort zone and deal with qml stuff now. They also bring up some bugs -

* If user clicking on Ok button quickly several times is showing wrong verdict even for correct answer, reason behind this is related to the time delay which BONUS takes to appear. I solved this bug by disabling OK button for 2 second after each click but later Johnny asked me to use stop signal of Bonus.qml and it removed the bug in more nicer way.

* Another bug was related to the instruction window. MouseArea of instruction window was overriding the mouseArea of fruits and making them undragable. Challenge here is to keep instruction window always on top of fruits and let pupil to drag fruits hiding behind it. I searched the whole stackoverflow and documentation for the solution but no help :(, then i dropped the problem in mailing list and got the one line solution and that is to toggle the Z-effect of instruction table with opacity.


The remaining activity which is left is most interesting one, as in this i have to make some levels from JSONs and other levels dynamically at runtime and that's why it's going to be bit difficult too.

My journey as Season of KDE 2020 participant is going amazing and i feel lucky to got such wonderful opportunity to work with a huge organisation and to have such dedicated, helpful and appreciating mentors. yeah they never forget to appreciate me, not a single time.

I would also like to thank KDE for origanizing this wonderful program.