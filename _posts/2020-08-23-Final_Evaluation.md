---
layout: post
title: Final Evaluation
subtitle: Part 7
tags: [KDE, Google Summer of Codes]
---

Hi everyone,

Pheww!... GSoC coding period is in its last stage, The final evaluation is starting from tomorrow, I am really happy that all activities have been finished on time, 7 of them already merged in master and I hope the last one would also merge soon.

This month, I have worked on the last two remaining activities -

- Build the same model
- Find the details 


## Build the same model
![Crane Activity](/img/crane.gif "Crane Activity")

I started working on the activity earlier this month. The goal was to split levels in multiple datasets based on whether levels contain images or words of the same lengths.

In the first commit, I have designed datasets myself and pushed it but after mentor’s reviews, this initial design turns out to be a bad one especially for the translator’s points of view. As we don’t need the exact translation of words, just replacing a word to any other word of the same length would be enough for the activity. So, It’s better to give translators a list of words and ask them to replace this list with another list containing words of the same length instead of asking them to change one word by one word in the dataset file. Now, I was clear that requirement is list of words, not individual separated words but the next question was where to put this list? either in datasets itself or in the javascript file? This question took another good discussion with mentors and finally, I have added words list in js file whereas the list of URLs of images in the dataset itself.

![Crane Dataset Activity](/img/crane_dataset.png "Crane dataset Activity")

Here you can see the key “wordLength” in all the levels, javascript code checks this key, and select a word of the same length from the internal lists for this level.

We also need a feature to add customizable word in level for future admin/server interface. For this, I added the functionality in the code such that if we replace the key “wordLengh”: 3 with “word” : “cat”, code will adapt it and show the word “cat” for this level instead of taking the word from internal lists.

## Find the details.
This activity is also the child activity of “babymatch” ( remember “Chronos” and “locate the region” ? ), As babymatch already supports multiple datasets, I have just enabled it for this activity by setting “useMultipleDataset: true” and added all datasets file containing links of boards. I really felt nostalgia while working on this :) as I did the exact same thing in Locate the region activity and also in Chronos (I worked on Chronos before the GSoC and at that time, I added the multiple datasets in babymatch).

So this is how I ended up with all the activities listed in my proposal.

![Taks List](/img/tasks.png "task List")

Eagerly waiting for the “details” activity to get merged so I can check this too (Marking these tasks as done is my favorite work :) ).
