---
layout: post
title:  "Git Process: No man is an island"
date:   2016-01-16 04:07:49
categories: Git 
banner_image: ""
featured: false
comments: true
---

Although I mostly work alone, I strive to follow the best git workflow practices taught by developers from <a href="https://thoughtbot.com" target="_blank">Thoughtbot</a>.  I highly recommend you to join <a href="https://upcase.com" target="_blank">Upcase</a> to learn more.  I think it's amazing, so you should take a look if you are interested.

<!--more-->

First, I will create a new feature branch to work on something.

    git checkout -b al-feature-something

If you look at the git command line, I have <code>al-</code> attached to it.  This is to indicate who is working on this branch.  It's the initials of my first and last name.

I think this is a great procedure if you are working with a team.  I do this for the other developers that are working on the project.  It's all about being courteous and thoughtful for other people as you code.

After I code some ideas that I have for this branch, I save them often so I don't loose my ideas.

    git add .

Until I rebase all the ideas that I coded, I write quick git messages for each git commits (For writing good git commit messages, please read <a href="http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html" target="_blank">A Note About Git Commit Messages</a> by <a href="https://twitter.com/tpope" target="_blank">Tim Pope</a>.  It's a great blog post regarding good git commit messages).

    git commit -m "WIP: Add this and that for this"
    
When you write your git commit message that is still working in progress, it is helpful to write <code>WIP:</code> in front of your message so you know it is an incomplete thought that you are still working on.  This is helpful for other developers that you are working with as well.

After I have some concrete codes for to review, I will rebase all the current commits from the current branch I was working on.  This is so that pull requests are clean and concrete for others to review.  For those of you who are not familiar with <code>git rebase</code>, Thoughtbot has an article about it <a href="https://robots.thoughtbot.com/git-interactive-rebase-squash-amend-rewriting-history" target="_blank">here</a>.
  
    git rebase -i origin/master
    
After code is reviewed by few other developers, you merge your working branch to the master, than <code>git push</code> the origin master.  This will automatically close the pull request from github&mdash;also making the git messages really clean.

Now, it is time to clean up.

I often delete the remote branches first.  You can do this by:
  
    git push origin :your-branch-name
    
I know, it is weird syntax but that is what git requires you to do.  After you deleted your remote branch, you can clean your local machine too.

    git branch -d :your-branch-name
    
That is pretty much it.  I do this even when I code by myself.  It is more work, but it keeps my code accountable and clean.

Chris from Thoughtbot goes more in depth in his <a href="https://upcase.com/mastering-git" target="_blank">Mastering Git</a> class.  I highly recommend his tutorials.

---

#####Resources
Highly recommend signing up for <a href="https://upcase.com" target="_blank">Upcase</a><br />
They have a great module on <a href="https://upcase.com/videos/git-workflow" target="_blank">Git Workflow</a><br />
As well as <a href="https://upcase.com/mastering-git" target="_blank">Mastering Git</a>
