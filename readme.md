# Github 101

Congrats on completing your first day of WDI! Let's do a little review quiz and while we're at it, get a little practice using Github!

> **Reminder**: Github is your friend, not your enemy!

## Relevant XKCD

![](http://res.cloudinary.com/briezh/image/upload/v1531164700/git_XKCD_y1vvzk.png)

## Review: Git and Github

Remember, *git* and *github* are two different things! Git is a version control system for managing your source code. Github is a platform to host your code online so others can access it and collaborate with you on it. You can think of Github as social media for Git! For a more detailed explanation, [watch this video](https://www.youtube.com/watch?v=uUuTYDg9XoI)!

### Commit Messages: Best Practices

You can find a [complete list of best practices here](https://gist.github.com/robertpainsi/b632364184e70900af4ab688decf6f53), but in general, your commit message should clearly state what content/features/changes are being added to the code base and be in a complete sentence. Another best practice is to make many commits! Everytime you add something meaningful, even something really small, is a good time for a commit! This way if your code gets all messed up, you can pinpoint the exact change that caused the issue, and you won't lose much working code. Otherwise, if your commits are few and far between and you have to go back to an earlier version, you might end up losing more than you need to!

![](http://res.cloudinary.com/briezh/image/upload/v1531165696/git_commitMessages_rsqm3r.png)

## Directions

#### 1. Fork it!

On the upper righthand corner of this page, you will see a button that says `Fork`. Press that button!!! This will fork it to your personal Github account.

> **Note**: If you have access to multiple accounts or organizations on Github, you may get a pop-up asking you which one you want to use. 

#### 2. Clone it!

Once you have a "fork" of the repository on your own account, you want to clone the code onto your local machine. Do this by copying the clone link. This is a green button to the right of the page. Clicking the copy icon will automatically copy it to your clipboard, or you can highlight the text and press `Cmd + C`.

![](http://res.cloudinary.com/briezh/image/upload/v1531169741/Screen_Shot_2018-07-09_at_1.55.16_PM_kb0fuq.png)

> **Protip**: If you made SSH keys in class, you should use the SSH link. Otherwise, you can use the HTTPS link and you will get prompted for a password before the cloning takes place.

Once you have this link copied, go to your terminal and run the command `git clone THE_LINK_YOU_COPIED`. 

> **Warning**: Make sure the location you clone at is not inside of another git repository!

In general, when coding, we don't repeat ourselves, but let's say it again. A git repository should NOT live inside another git repository!

Did you read the sentence previous to this one? Read it again! Say it out loud! Tell the person next to you! :)

> **Note**: In future assignments, steps 1 and 2 will be referred to as a single unit. You might see a direction like "fork and clone this repository".

#### 3. Navigate to the directory

Wherever you cloned this repository should have made a new folder with the name of the folder being the same as the repository. So, in this case you should have a folder called "github_101". Navigate to this directory.

```bash
cd github_101
```

#### 4. Open it in your text editor of choice

Usually this is Sublime Text, Atom, or VS Code, but feel free to get wild and go with whatever you're most productive with. In class, you most likely set up shortcuts to these text editors. Select the one that's appropriate for what you'll be using throughout the course.

```bash
subl .
```

or

```bash
atom .
```

or

```bash
code .
``` 

#### 5. Answer the Quiz Questions Below

Test your Googling skills and learn something new about Git! Put your answers into the file called `answers.txt`. The file is already provided for you, just fill in your own answers. Please number them!

#### 6. Save and close

Save the answers.txt file when you're done. Close the text editor.

#### 7. Check yourself

Run the following command. 

```bash
git status
```

If you followed the directions up till now, this should tell you that there are "untracked" changes to `answers.txt`.

#### 8. Stage the changes

You can add files to be staged for (ready to go into) the next commit. The following command on your terminal will stage "all" changes in your current folder. The reason we stage files for commits is that we don't necessarily have to check in the changes to all the files, we could potentially just want to check in some of them. Hence what seems to be an extra step. In this case however, there's only one file anyway!

```bash
git add .
```

> **Protip**: The `git init` command is only necessary when you're starting a repository from scratch! Since we used the `clone` command, we already have an initialized repository. 

#### 9. Commit to it!

The following command will add all staged changes (additions, deletions, or modifications) from the last command and put it into a commit. In our case, `answers.txt` should be modified.

```bash
git commit -m "Add my answers to answers.txt"
```

> **Note**: The `-m` in the command stands for "message". Remember our discussion of best practices for commit messages!

#### 10. Push it!

What this step does is take our commits and send them to wherever we specify. In this case, we'll push our changes on our local computer back up to your fork of this repository on your Github account.

```bash
git push origin master
```

In this case, `origin` refers to Github — where the code originated! We can use the push command to push to Github or any another place that might host our repository. We'll also use it to deploy our sites to `Heroku` later in the course. For now, it's important to realize that the code on your Github account and the code on your machine don't match until you send your changes to Github via this push command! 

The `master` at the end of the command refers to the *branch*. Master is always the default branch, and for now, it's the only one we'll use. Later in the course we'll get into branches. 

11. One Last Step!!!

Go into your internet browser and refresh the page with your forked repository. Do you see your changes on Github now?

If so, your one last step is to make a `pull request`. The term is a little bit confusing, but it means to essentially show the original repository the changes you made on your own version. It alerts the owner of the original repository and opens up the code for comments and review. 

> **Protip**: You can double check whether your pull request went through by clicking on the pull requests tab and looking for your username! See the example below (on a different repository).

![](http://res.cloudinary.com/briezh/image/upload/v1531164603/Screen_Shot_2018-07-09_at_12.28.31_PM_fzw4d6.png)

### Deliverables

By the end of this you should have:

* A separate fork of this repository (meaning, a copy on your *own* Github account!)
* A file called `answers.txt` that has numbered answers to each of the questions listed below.
* A pull request against this repository (on WDI-SEA)

## Quiz Questions

#### 1. Who invented Git?

#### 2. What else is the person who invented Git famous for?

#### 3. What year was Git invented?

#### 4. What is the git command to initialize a new repository?

#### 5. In your own words, describe what the command `git push` is doing.

## Additional Resources

* [Git Online Mini-Quiz](https://learn.co/lessons/git-basics-quiz)
* [Git vs Github](https://www.youtube.com/watch?v=uUuTYDg9XoI) (Explains the differences)
* [First Github Commit](https://www.youtube.com/watch?v=QqP7YZlZEOo) (This should be a review of our in-class lesson if you feel you need it!)
* [Git and Github for Poets](https://www.youtube.com/watch?v=BCQHnlnPusY) (This is a non-coder intro to using Git/Github)
* [Commit Messages Best Practices](https://gist.github.com/robertpainsi/b632364184e70900af4ab688decf6f53)
