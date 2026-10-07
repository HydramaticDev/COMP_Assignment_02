---\
layout: default\
title: Tags\
nav_order: 9\
---\
\
Tags in Git are like bookmarks for important events or milestones in your project.\
They're often used to mark release points (v1.0.0, v1.1.0, etc.).\
\
Creating a new lightweight tag:\
\[git tag \<tag-name\>\]\
\[git tag \<tag-name\> \<commit hash\>\]\
This will tag the current or specified commit with the provided name.\
Tag names should not include spaces. They should only include characters \[a-z\], \[A-Z\],\
numbers \[0-9\] and the dash/hyphen \[-\].\
\
Annotated tags store additional metadata such as the tagger's name, email, date, and\
an optional message.\
\[git tag -a \<tag-name\> -m "your message here"\]\
\
Checkout to the tag: You can treat the tag like a branch/commit, and checkout to the\
tag's point in history. For instance, git checkout \<tag-name\> .\
List tags: You can list all the tags in the repository using git tag or git tag -l . To\
narrow the list based on a search pattern, you can use \[git tag -l "\<search-\
pattern\>"\].\
\
Show tag information: If you have annotated tags, you can view the associated\
information with git show \<tag-name\> .\
Compare differences: You can compare the differences between the tagged state of\
the code and the current HEAD using git diff \<tag-name\> .\
