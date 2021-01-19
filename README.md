# Instructions for the Nansen Legacy R workshop: GitHub session.

Below, you can find instructions on what each participant has to do in this session. Whilst it should be possible to work through this without any experience with Git, the webinar I hosted (An introduction to Git and GitHub - see Yammer) provides more understanding of what each step does. You can view this webinar for reference throughout; everything covered in this session should be included. There are also many excellent explanations for each step online, since Git and GitHub are widely used.

**Part 1: Working on your own repository**

In part 1, we will get familiar with some basic commands on GitHub. Below is a common workflow that you might adopt if you are working on a repository by yourself - although the workflow in part 2 can also be used when working on one person repositories too!

  1. Create your own repository (the green button that says 'New' on the organisation home page). Make it public, and select the options to include a README and license file (GNU Public License v3.0). The optional description will populate the README.md file.
  
  2. Working locally now, open your Git Bash terminal. Linux users can open their regular terminal. Navigate to where you want to work. Some useful bash commands for those unfamiliar with working in a terminal.
  
    pwd - lists the full path name of the current working directory
    ls - lists the contents of the current working directory
    cd - change directory. You can do this relative to where you are currently located. Press TAB to autocomplete
    mkdir - make a new directory

  3. Clone the respository so you can work on it on your local computer. Use the URL of the repo page.
  
    git clone https://github.com/...
  
  Navigate into it.
  
    cd NAME_OF_REPO_YOU_HAVE_CLONED
  
  You can show the remote 'origin' of this repo using the command
  
    git remote -v

  3. Create a basic .txt file in the repository using your favourite text editor. This could contain anything, e.g.
    a) Your top 5 favourite music artists
    b) A list of things you need to buy from the shop
    c) As many names beginning with the letter 'L' that you can think of.
    
  For example:
  
    notepad newFile.txt

  Of course you can use Git on more complicated files, but let's make the files themselves as simple as possible for now. They are not the focus of this session!
  
  4. Save your file in the repo. 'Add' the changes you have made in the repo to the staging area.
  
    git add newFile.txt
    
  To show what has been added:
  
    git status
    
  This can also be used to show the status after later stages in this exercise.

  5. Commit these changes, with a suitable message
  
    git commit -m "Created file newFile.txt"
  
  6. Push these changes to the origin on GitHub. Here, 'origin' refers to the URL of where the repo is hosted online, and 'main' is the default name of the branch (previously master in repos created before October 2020).
  
    git push origin main
  
  7. Pull the local repository. This pulls any updates that exist on GitHub to your local repository. 
  
    git pull
  
  *This isn't neccessary in this case as you know that you are the only person working on your respository, but it is a good habit to pull after your have pushed to check if any changes have been made by someone else.* 
  
  8. Create a new branch for testing. This is good practice when you don't want to make changes to the main branch, which should be only the main workflow (approved/released versions).
  
    git branch testBranch
    
    git checkout testBranch
  
  OR IN ONE LINE
  
    git checkout -b testBranch
  
  9. Make some changes to your repository. You can create a new file or change existing files.
  
  10. Add and commit your changes.
  
    git add newFile.txt secondFile.txt thirdFile.txt
    
    git commit -m "Write something brief and useful here"
  
  11. Checkout the main branch again. Merge your test branch with the main branch. Assuming this runs without error, delete your test branch.
  
    git checkout main
    
    git merge testBranch
    
    git branch -d testBranch
  
  12. Push your changes. Have a look at your GitHub repo online! You should see your updates.
  
    git push origin main
    
  13. Repeat steps 7 to 12 until you feel comfortable with this process.
  
 
**Part 2: Working together on a repository**

In part 2, we will focus on collaborating with other people on a project. Below outlines the best practice for this. You will get the opportunity to add someone else to the repository you created in Part 1, so they can make updates. You will then be able to approve (if you wish!) these updates before they are merged into the main workflow. You will also get the opportunity to be added to someone elses repository, so you can see both sides of how it works.

  1. Creator of respository: Add someone else to your repository so that they can also make changes. To do this, go to your repository on GitHub. On the top bar, go to 'Settings'. On the left bar, go to 'Manage Access'. Then press the green button 'Invite teams or people' and write in the email of the person you want to add. 
  
  2. Collaborator: Go to https://github.com/notifications. Accept access to the repo. Then open your Git Bash terminal. Clone the repository so you can work on it on your local computer. Navigate into it.
  
    git clone https://github.com/...
  
  3. Collaborator: Create and checkout a new branch, make some changes, add and commit (steps 8 to 10 in part 1). DO NOT MERGE.
  
  4. Collaborator: Push these changes to the origin. This time, note that you are pushing the branch you have created, not the main branch.
  
    git push origin testBranch
  
  5. Collaborator: Navigate to the repository online on GitHub
  
  6. Collaborator: Submit a pull request - a green button labelled 'Compare & pull request' should have appeared at the top of the page. You can leave a comment for the creator of this repo; why are you submitting this pull request? This can be more extensive than the commit message. This is a great way to log changes you are making to a repository, and can even be done if you are working on a repository by yourself; you can merge you own pull requests!
  
  7. Creator of repository: Depending on your account setup, you may have received an email regarding this pull request. Go to your repo on GitHub. You should see a number '1' next to Pull requests on the bar at the top of the page. You can now review it and, if you choose to, accept the changes and merge them with the main branch. This can all be done on the GitHub page. You can also leave a comment to start a conversation with the person who created the pull request, before you accept or reject it.
  
  
**Part 3: Suggesting changes to someone else's repository**

There might be times that you want to suggest updates to a repository that you are not assigned to. Perhaps you have been using a script that someone else has developed, but it doesn't work on your data. Maybe there is a mistake, or perhaps you want to make improvements to the script. Let's look at how this works.

To avoid confusion, please don't start this part until you are certain that the person whose repository you are forking has also completed part 2 step 7.

  1. In the top right of the repo you want to make a copy of, select 'Fork'. Fork the repository to your personal account - don't worry, you will be able to delete it later. This creates a copy of the repository on your personal page. You should be automatically redirected to the forked repo on GitHub - notice that it says this in the top left of the page. By default, 'forking' will copy only the main branch, which should be production ready.
  
  2. Clone this forked repository so you can work on it locally. 
  
    git clone https://github.com/...
  
  3. Create a branch, make changes, add, commit (steps 8 to 10 in part 1). DO NOT MERGE.
  
  4. Push these changes to your forked repository online
  
    git push origin testBranch
  
  5. Go to the forked repo on GitHub. Change the branch you are viewing by using the drop-down icon that will say 'main' by default (below '<> Code' at the top left of the page). You should now see that this branch is 1 commit (or more) ahead of the main branch in the original repository you forked. Submit a pull request. At the top, you can see and select what you are pulling to and from. Here, you want to request that the changes you have made on the test branch of your forked repository should be pulled into the main branch of the original project.
  
  6. Creator of repository: Review the pull request as in part 2 step 7.
  
If you want to delete the repository on your personal page, navigate to it, and select settings > options > scroll to the bottom and select 'Delete this repository'.
