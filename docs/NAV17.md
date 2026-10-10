---\
layout: default\
title: Creating, Using, and Merging branches.\
nav_order: 17\
---\
\
Introducing Branches\
\
\
In Git, branches are like alternate timelines in a sci-fi movie.\
They allow you to work on different features or fixes without affecting the main project\
timeline until you choose to merge the timelines back together.\
\
\
Creating a new branch:\
git branch \<branch-name\>\
\
Switching to a branch:\
git checkout \<branch-name\>\
\
Create and switch in a single command:\
git checkout -b \<branch-name\>\
\
Merging Branches\
\
Branching allows for isolated development, and merging brings those developments\
back into the main timeline.\
Let's say we've been working and committing to an experimental branch and we\
want to merge those commits back into main:\
\
git checkout main\
git merge experimental\
