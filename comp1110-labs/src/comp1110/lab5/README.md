# COMP1110 Lab 5

## Purpose

In this lab you will write a simple Java FX program and use any spare time to prepare for lab test 2.

**It is essential that you complete this lab and have a tutor mark it off**.

## Tasks

1.  **Pulling upstream commits in GitLab**

	Remember that your labs and assignment repos are *forks*; your own variation of some other repo.   Once you've made the fork, your repo is independent and won't see any subsequent changes to the repo from which your fork was taken.

	Sometimes it is valuable to be able to pull changes from the repo from which you originally forked, and apply those changes to your repo.   In the case of our class, this is true if the master repo is updated with corrections or improvements.  In such cases, it would be good if you could relatively easily merge those changes into your own repo.   In this lab exercise you will learn how to do that.

	The [terminology](http://stackoverflow.com/questions/2739376/definition-of-downstream-and-upstream) of an *upstream* repo is often used to refer to the one from which a repo is derived.   In your case, the *upstream* repo is the one from which your repo was forked.  Git has [advanced](https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes) mechanisms for pulling changes from an upstream repo; we'll just look at something quite specific in this lab.   Much of this is supported by IntelliJ, but unfortunately, the crucial first step of [specifying](https://git-scm.com/book/en/v2/Git-Basics-Working-with-Remotes#Adding-Remote-Repositories) the address of the upstream repo is [not supported](https://youtrack.jetbrains.com/oauth?state=%2Fissue%2FIDEA-87099) by IntelliJ at the moment, which is why we did not introduce these ideas earlier.

	**Individual Exercise: Labs Repo**

	Everyone should compete the following exercise.   In these steps you will update your *personal* comp1110-labs repo with some changes.

	0. Quit IntelliJ if you have it open.
	1. Start a terminal (use the menu at top left).
	2. Change directory (cd) into the folder that contains your intelliJ projects (`cd IdeaProjects`).
	3. Change directory (cd) into your labs repo (`cd comp1110-labs`).
	4. Display the currently known remote repos for the project (`git remote -v`).
	5. Add the comp1110 labs repo as a remote upstream repo (`git remote add upstream https://gitlab.cecs.anu.edu.au/comp1110/comp1110-labs.git`).
	6. Now open your comp1110-labs repo in IntelliJ.
	7. Prepare to pull changes (VCS -> Git -> Pull...).
	8. Use the drop-down menu to change the 'Remote' to be `upstream(https://gitlab.cecs.anu.edu.au/comp1110/comp1110-labs.git)`.
	9. Refresh the list of branches by clicking the refresh button to the right of the dropdown.
	10. Select the `upstream/master` branch.
	11. Click `Pull`.  This should behave just like a merge from your last lab exercise, and work without further interaction.   If not, you may need to merge, in which case you should consult your tutor if you're unsure what to do.
	12. Bring up the `Version Control` panel at the bottom of your IntelliJ window, and select `Log`, and notice that you now have new changes in your history.
	13. Commit and push your merge.

	After you pull remote commits into your repo, commit, and push them, they will be visible to all clones of your repo.   Go to the GitLab web page for your labs repo, and use the `Commits` and `Network` menu options (on the left menu) to see how the changes you pulled have been integrated into your own repo.

	You can pull your changes into other clones of your labs repo (such as on your home computer).

	**Group Exercise: Assignment Repo**

	**One** group member should do the following.   Once complete, each of the other group members can pull the changes.

	0. Quit IntelliJ if you have it open.
	1. Start a terminal (use the menu at top left)
	2. Change directory (cd) into the folder that contains your intelliJ projects (`cd IdeaProjects`)
	3. Change directory (cd) into your assignment repo (`cd comp1110-ass2-<yourgroup>` or `cd comp1140-ass2-<yourgroup>`).
	4. Display the currently known remote repos for the project (`git remote -v`).
	5. Add the comp1110 assignment2 repo as a remote upstream repo (`git remote add upstream https://gitlab.cecs.anu.edu.au/comp1110/comp1110-ass2.git` or `git remote add upstream https://gitlab.cecs.anu.edu.au/comp1110/comp1140-ass2.git`).
	6. Now open your comp1110-ass2 (or comp1140-ass2) repo in IntelliJ
	7. Prepare to pull changes (VCS -> Git -> Pull...)
	8. Use the drop-down menu to change the 'Remote' to be `upstream(https://gitlab.cecs.anu.edu.au/comp1110/comp1110-ass2.git)' or 'upstream(https://gitlab.cecs.anu.edu.au/comp1110/comp1140-ass2.git)`.
	9. Refresh the list of branches by clicking the refresh button to the right of the dropdown.
	10. Select the `upstream/master` branch.
	11. Click `Pull`.  This should behave just like a merge from your last lab exercise, and work without further interaction.   If not, you may need to merge, in which case you should consult your tutor if you're unsure what to do.
	12. Bring up the `Version Control` panel at the bottom of your IntelliJ window, and select `Log`, and notice that you now have some new changes in your history.
	13. Commit and push your change.
	14. Your group members can now pull your change to their clones of the group repo.


	You can repeat these steps to pull further changes into your forks of class repos.   You only need to perform the steps on one of your clones and then the changes will be visible (after pulling) at each clone of your repo.   You can do this on the lab computers (as in this exercise) or on your home computer.   If you have linux or MacOS on your computer, the process is identical to the above.   If you have windows on your computer, you will need to use [git bash](https://git-for-windows.github.io) rather than a terminal to set your upstream remote (steps 2-6).


2.  **Use JavaFX to create a simple window with a moving 'ant'.**

    In the Java package comp1110.lab5, within your comp1110-labs repository, create a new Java class, `Ant`, that draws the path of an ant that is walking randomly around a JavaFX window. This should look a little like a scribbling on a page. If the ant walks off the edge of the screen re-center the ant and continue the random walk. Use the basic template from the code from lecture X01. In addition to that, you may find the following helpful:
    ````java
    ...
    primaryStage.setScene(scene);
    
    Timeline timeline = new Timeline(new KeyFrame(Duration.millis(100),
                                ae -> {
                                       /* your code goes here */
                                      }));
    timeline.setCycleCount(Animation.INDEFINITE);
    timeline.play();
    primaryStage.show();
    ...
   ````
    that little bit of code will be called once every 100 milliseconds (10 times a second).

3. **Prepare for lab test 2.**

    Use any spare time you have to work on preparing for lab test 2 and working on your group assignment.
