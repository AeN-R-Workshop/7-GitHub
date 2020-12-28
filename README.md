# Template
Template repository for the Nansen Legacy R workshop: GitHub session.

Below, you can find instructions on what each participant has to do in this session.

Part 1: Working on your own repository

  1. Create your own repository (the green button that says 'New' on the organisation home page)
  
  2. Navigate to where you want to work. Some useful bash commands for those unfamiliar with working in a terminal.
  
    pwd - lists the full path name of the current working directory
    ls - lists the contents of the current working directory
    cd - change directory. You can do this relative to where you are currently located. Press TAB to autocomplete
    mkdir - make a new directory

  3. Clone the respository so you can work on it on your local computer. Use the URL of the repo page.
  
    git clone https://github.com/...
  
  Navigate into it.
  
    cd NAME_OF_REPO_YOU_HAVE_CLONED

  3. Working locally now, create a basic .txt file in the repository using your favourite text editor. This could contain anything, e.g.
    a) Your top 5 favourite music artists
    b) A list of things you need to buy from the shop
    c) As many names beginning with the letter 'L' that you can think of.
    
  For example:
  
    notepad newFile.txt

  4. 'Add' the changes you have made in the repo to the staging area.
  
    git add newFile.txt

  5. Commit these changes, with a suitable message
  
    git commit -m "Created file newFile.txt"
  
  6. Push these changes to the origin on GitHub. Here, 'origin' refers to where the repo is hosted online, and 'main' is the default name of the branch (previously master in repos created before October 2020).
  
    git push origin main
  
  7. Pull the local repository. This pulls any changes that may have been made to the repository. 
  
    git pull
  
  *This isn't neccessary in this case as you know that you are the only person working on your respository, but it is a good habit to pull after your have pushed to check if any changes have been made by someone else. 
  
  8. Create a new branch for testing. This is good practice when you don't want to make changes to the main branch.
  
    git branch testBranch
    
    git checkout testBranch
  
  OR IN ONE LINE
  
    git checkout -b testBranch
  
  9. Make some changes to your repository. You can create a new file or change existing files.
  
  10. Add and commit your changes.
  
    git add newFile.txt secondFile.txt thirdFile.txt
    
    git commit -m "Write something brief and useful here"
  
  11. Checkout the main branch again. Merge your test branch with the main branch. Delete your test branch.
  
    git checkout main
    
    git merge testBranch
    
    git branch -d testBranch
  
  12. Push your changes.
  
    git push origin main
    
  13. Repeat steps 7 to 12 until you feel comfortable with this process.
  
 
Part 2: Working together on a repository

  1. Creator of respository: Add someone else to your repository so that they can also make changes.
  
  2. Collaborator: Clone the repository so you can work on it on your local computer. Navigate into it.
  
    git clone https://github.com/...
  
  3. Collaborator: Create a new branch, make some changes, add and commit (steps 8 to 10 in part 1). DO NOT MERGE.
  
  4. Collaborator: Push these changes to the origin
  
    git push origin testBranch
  
  5. Collaborator: Navigate to the repository online on GitHub
  
  6. Collaborator: Submit a pull request
  
  7. Creator of repository: Depending on your account setup, you may have received an email regarding this pull request. Go to your repo on GitHub. You can now review it and, if you choose to, accept the changes and merge them with the main branch. This can all be done on the GitHub page.
  
  
Part 3: Suggesting changes to someone else's repository.

To avoid confusion, please don't start this part until you are certain that the person whose repository you are forking has also completed part 2 step 7.

  1. Fork the repository to your personal page. This creates a copy of the repository.
  
    git clone https://github.com/...
  
  2. Clone this forked repository so you can work on it locally.
  
  3. Create a branch, make changes, add, commit (steps 8 to 10 in part 1). DO NOT MERGE.
  
  4. Push these changes to your forked repository online
  
    git push origin testBranch
  
  5. Submit a pull request. Here, you are requesting that the changes you have made on your forked repository should be pulled into the original project.
  
  6. Creator of repository: Review the pull request as in part 2 step 7.
