# COMP1110 Lab 1

## Purpose

The first lab is intended to ensure that you have become familiar with the basic tools we will be using throughout the semester in the labs at ANU and on your own computer (if you plan to use one).

**It is essential that you complete this lab and have a tutor mark it off**.   We want you to do this now so that you can focus on course content from the first day of week two rather than be distracted by concerns over how the tools work.   This is your chance to get yourself established and familiar with the tools with the assistance of the course tutors.  Please make the most of the opportunity.

I have created a step-by-step [video](http://cs.anu.edu.au/courses/COMP1110/howto/lab1.mp4) showing you how to complete this lab in the lab environment.

## Tasks

1. **Set up your GitLab account.**

    You will use GitLab throughout the semester to manage all of your coursework.

    First you need to set up your GitLab account.  Log in to a lab computer, open a browser, and go to GitLab http://gitlab.cecs.anu.edu.au.   Log in to GitLab using the LDAP tab of the Sign in section of the front page.   You should type your student ID and your normal password.

    Go to Profile Settings, which is accessible via a gear icon at top right.   Feel free to update your GitLab personal profile if you wish.

    This completes your GitLab setup.

2.  **Fork the comp1110 labs repo.**

     In GitLab jargon, to fork a repo means to create a fresh copy of the repo where the copy will be owned by you.   The class has its own labs repo which serves as a template for yours.   You and every other student will fork the class labs repo to create your own.  You  can't commit changes to the class repo (only the lecturer can do that), but you can commit changes to your own forked repo.

    To fork the repo, go to the GitLab page for the labs repo https://gitlab.cecs.anu.edu.au/comp1110/comp1110-labs.  Notice that when you go to that page, the name of the repo at upper left is `comp1110/comp1110-labs`.  This tells you that the owner of this repo is `comp1110` (before the `/`), and that among their repos this one is called `comp1110-labs` (after the `/`).

    Now click  `Fork`  at upper right.   You may have to select which GitLab account to use; select your account.   You now have your own version of the labs repo.  Notice that the name at top left will have changed to reflect that you own this new repo.   It should now say something like `Robin Smith/comp1110-labs` (but with your name on the left).  A box at the right will remind you of where this new repo came from (the box may be hidded if your window is too narrow, in that case there should be chevron (`<`) in the right margin, click on it to bring the information on the right into view).   You will use this repo to complete the remainder of your labs (not just this week).   Unlike the class repo, this one is yours; you can make changes to it.    So far, however, your repo exists only on GitLab (i.e. in 'the cloud').

    Soon you will be making a working copy (clone) that you can edit on the lab computer.   Later you can do the same on your own computer.   *Although you might have multiple clones of your repo on different devices, the definitive version always resides on GitLab, in the cloud.*

3.  **Find this document within your labs repo.**

    At this point in the lab you should see `Your Name/comp1110-labs` at top left of your GitLab page in your browser.   If not, you can navigate there by clicking your avatar (top right), and then clicking the project under `Personal projects` (upper right).  Click the `Files` tab in the `comp1110-labs` project view.

     You can navigate to your own version of *this* document within GitLab.  Click the `Files` tab in the left sidebar, then navigate through `src`, to `comp1110`, and then to `lab1`.  The files inside `lab1` should be shown at the top, followed by your own copy of this document.   If you're in any doubt about whose version of the document you're looking at, check the banner at the top and you should see your name.   You can also check the URL in the navigation bar of your browser and it should be something like: `https://gitlab.cecs.anu.edu.au/u1234567/comp1110-lab1/tree/master/src/comp1110/lab1`.


4.  **Start and Configure IntelliJ**

    Use the menu at top left on the lab machine, and find IntelliJ under the `Programming` sub-menu.

    If this is the first time you have started IntelliJ on the lab machines, there are a few once-only steps that you'll need to take.

    1. You will see a dialogue titled `Complete Installation` that will ask whether you want to import a previous configuration.   Use the default (no import), and click 'OK'.

    2. You will next see a dialogue titled `Configure IDEA` that will allow you to set the UI Theme.  I suggest that you select `Skip all and set defaults`.

    3. Next you may see a dialogue titled `Authenticate`, prompting you for a password.   Just click `Cancel`.

    You should now see a splash screen titled `Welcome to IntelliJ IDEA`.

    In the next step you will use this splash screen to clone your labs repo.   During that step you will also have to configure IntelliJ to recognise the correct version of Java.

5. **Clone your labs repo.**

    Select `Git` from the drop-down menu `Check out from Version Control` on the initial IntelliJ splash screen.  Use your browser to navigate to your GitLab project page and find the URL of your repo.   When you're on the correct GitLab page, you should have the lab repo name at the top left (`Your Name/comp1110-labs`).   Click on the project icon at top left of your GitLab page.  You should see the address of your repo.   Click `HTTPS` to see the http form of the address.  It will be something like `https://gitlab.cecs.anu.edu.au/u1234567/comp1110-labs.git` (you can [configure IntelliJ](https://www.jetbrains.com/idea/help/using-git-integration.html) to use ssh rather than https, but that is optional and outside the scope of this lab).  Select that text and copy it into the IntelliJ dialogue.   Click `Test` to verify that you are correctly set up.    If the test fails, carefully check that you've copied the URL correctly.   You may see a warning message in the IntelliJ dialogue that tells you that `The parent path /students/u1234567/IdeaProjects must exist.`   To fix this, click the little elipsis (...) below the `Test` button.  Press `Alt+Insert` to create a new folder in your home directory.   Name it `IdeaProjects` and click OK.   The error message should go away allowing you to clone the repo.   Press `Clone`.   You will be prompted for your username and password and a checkbox will ask if you would like the password to be remembered.  IntelliJ will also ask whether you wish to [set up a master password](https://www.jetbrains.com/idea/help/handling-passwords-for-git-remote-repositories.html#d686468e18637).  The choice is yours but having IntelliJ remember the password and protect it with a master password is convenient and secure.  You will now see a `Tip of the Day` from IntelliJ.   You may find it helpful to read these tips as you learn more about IntelliJ.

6. **Complete initial setup of the IntelliJ environment.**

    Press `Alt+1` to open the comp1110-labs project.   Navigate to `comp1110-labs.jar`, find `comp1110`, `lab1`, and then `HelloWorldTest`.   If you accidentally click on this file you may get a dialogue from IntelliJ asking whether you are prepared to accept terms and conditions associated with their decompiler (which allows you some insight into how code was written just by looking at the result of the compilation).   It is not particularly important how you respond to this; if unsure, then just defer your decision till later.  If you right-click on the file you should find an option to `Run...`.  Select `Lab1Tests`.   (You can also access this from a drop-down menu at the top right of the window to the left of a green arrow.)   At this point you may well receive an error message from IntelliJ stating that `the SDK is not specified`.   After clicking `OK`, you should find a dialogue with `Module SDK` as a drop-down menu.   Select `New...` then `jdk` in the dialogue, type `/usr/local/non-free/jdk-latest` and then select `OK`.   Accept the popup asking if you want to set up the created SDK on project, click `Apply` at bottom right, and then click `OK`.   Try running `Lab1Tests` again (you should just be able to click the green arrow at top right, which will re-run the last task).   You should now see a different message:  `java.lang.NoClassDefFoundError: comp1110/lab1/HelloWorld`.   This means you've not yet created the code that we're trying to test.   The next step solves this problem.

7. **Create a simple class and test it.**

    Navigate to the blue `src` folder.   Continue to navigate to `comp1110` and `lab1`.  Inside that folder you'll see `README.md`, which is a copy of this file, the lab instructions.  While the `lab1` folder is selected, right-click and select `New...` and the choose `Java class`.   Name the class `HelloWorld` (be sure to be precise about the naming of the class, including the upper case `W`).   You will be asked whether you would like to add the class to Git.   Say `Yes`.

    You should now see a very simple piece of code.  Click your mouse to the left of the closing brace (`}`), which is just below the word `public`.  Type the letters `psvm` and you should find an IntelliJ dialogue that recognises this as a shortcut for a main() method declaration.   If you press enter you should find new text appears, with your cursor below the newly added word `public`.  This is the main method for your new class; the code that will be run by default when your class is executed.   Right now the method is empty, so it will do nothing.

    Now add code to print out `Hi`.  Type `sout`, which is another IntelliJ shortcut, this time for producing code for printing strings.   Press enter to generate the code `System.out.println("")`.  This will print a new line containing what is between the quotes (nothing!).   Move your cursor between the quotes and add the word `Hi`.   Save your file (either via the `File` menu or with `Ctr+S`). Now use the `Run` menu and select `Run...`.   Choose `HelloWorld`.  Your little program should now run.   You should see a new sub-window with the word `Hi` in black text.

    Now test your program by choosing `Lab1Tests` from the dropdown menu next to the green arrow at the top of the screen towards the right.   Look carefully at the output below.   It should state that it has `Done: 6 of 6` and `Failed: 6`, and there will be a bar of red to the left.  Look more carefully at the brownish text below and you'll discover what's wrong with your code.   One of the tests is checking for an exclamation mark.   Change your program so that it prints `Hello`.  Re-run the test and you should find that you failed fewer tests.   Try again with `Hello world`, and then finally with `Hello world!`.  You should pass all tests.   Notice that the testing is very pedantic.  You need to have the correct number of spaces, correct punctuation, correct case, etc.

8. **Repeat steps 4-7 on your own computer.**

    The next step will commit your work and push it to GitHub.  Before you do that, you should repeat the exercise above on your home computer and/or laptop.   It is **essential** that you successfully complete steps 4-7 on your personal computer by the end of week one.   We will do *everything we can* to assist you during that period.   However, if you did not take opportunity during week one, you *must not* expect any assistance from your tutor with your home environment.

    First you need to ensure that your home environment has IntelliJ and java installed.  See the how-to videos for details on exactly how to do that.  Once you have that working, complete steps 4-7 on your own computer.

    You may also wish to repeat steps 5-7 on the lab computers to better familiarise yourself.   If so, you should quit IntelliJ and then use a file manager or the command line to navigate to your IdeaProjects folder and delete the comp1110-labs folder within it.  Having done that you should be able to complete steps 5-7 (otherwise the work you have just completed will get in the way of you repeating the exercise).

9. **Commit and push your work.**

    Once you have completed your work on both the lab computer and your own, you should commit your new HelloWorld class and push it to GitLab.  Use the `VCS` menu (Version Control Systems) to find  `Git`, `Commit File..`.  You should see your HelloWorld file highlighted.   Type in a commit message, such as `Finished HelloWorld and passed all tests!`.  Click `Commit`.   Committing will commit all of the changes you've made as a single change, but will *not* propagate those changes back to GitLab or any other repo.  For your changes to be visible on GitLab or on clones on other devices, you need to first *commit*, and then *push* your changes.  Ignore the warning, and click `Commit` on the next dialogue.  Select `Commit and Push`.   You should see a small notification stating that the Push was successful.   Now go to your GitLab page.  Click the `Commits` tab and you should see your commit has shown up on GitLab.   This means that the change you made in IntelliJ has been committed and propagated into GitLab.  You can now see that change on other devices when you clone and pull from GitLab.

10. **Share your repo with your tutor.**

    Until you decide to share it, your new repo is only accessible by you (and I, since comp1110 is automatically added as a group member when you fork).   You therefore need to make it accessible to your tutor to allow them to assess your work.

    1.  Go to your GitLab page and navigate to your comp1110-labs repo.
	2.  Go to the `Settings` tab.
	3.  Select `Members` from the tab at left.
	4.  Click `New Project Member`
	5.  Identify your tutor and set their access level to `Reporter`
	6.  Click `Add users`.

    You will need to repeat this step if your tutor changes.

11. **Approach your tutor to have your lab marked**.

    Once you have shared your repo with your tutor, approach your tutor to have your lab marked off.
   
