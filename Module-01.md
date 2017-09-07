# Module 1: Git Basics

***

## Getting Started

Prior to completing the module below it is highly recommended that you look at the following learning material. Even if you consider yourself a Git expert, there is material in the resources below that even seasoned users are unaware of.

Official Documentation

- [Git's Official Documentation Book](http://git-scm.com/book)

Code School

- [Try Git](http://www.codeschool.com/courses/try-git)
- [Git Real](http://www.codeschool.com/courses/git-real)
- [Git Real 2](http://www.codeschool.com/courses/git-real-2)

Tuts+

- [Git Essentials](https://tutsplus.com/course/git-essentials)

***

## The Test

Note: This module primarily assumes you are using Terminal, and may not cover necessary or extra steps you might need to take when using Git client (such as SourceTree or Tower).

1. Init a new `local` git repo called `git_test`.
2. Create a `remote` repository in your personal GitHub namespace called `git_test`, and add it as a remote repo (in Terminal or your Git client).
3. Create a new file called `friends.txt` with the first and last name of 5 people on lines 1-5.
4. Add the file to the local repo.
5. Commit the file to the repo with a message of, "these are my friends".
6. Push your changes to the `remote` repo.
7. Go into GitHub, view the `friends.txt` file, edit it to add a 6th friend, and commit it in the browser with the message, "added another friend".
8. Next, pull the code to your `local` repo.
9. Create a branch in `local` called `party`, and switch to it (`checkout`).
10. Now, in the `party` branch, add 4 more friends' names to `friends.txt` (for a total of 10). Commit those changes with a message of, "adding more friends for the party".
11. Next, switch back to the `master` branch, edit the `friends.txt` file (which has 6 friends) and add 9 more friends (for a total of 15). Make sure you include some of the friends you added in the `party` branch, but not all of them.  Commit this with a message of, "new friends".
12. Now, merge the `party` branch into the `master` branch. This should cause a CONFLICT. Edit the `friends.txt` file and fix the merge conflict, removing any duplicate names. The total number of names you'll have at the end of this process will depend on the number of people you duplicated between the `master` and `party` branches.
13. Commit the changes using the default merge message.
14. Push all branches to the `remote` repository.
15. Switch to the `party` branch (in `local`) and rebase it from the `master` branch. Push the `party` branch updates to the `remote` repo.
16. In the `party` branch (in `local`), create a new file called `family.txt` with 2 family member's names on line 1 and 2.
17. Add the `family.txt` file, then stash it. Switch to the `master` branch, pop the stash, and stage the file in the repo.
18. Now create another file called `pets.txt` with 2 names of your pets. If you don't have any, make them up.
19. Commit that file (there should now be two), with the message "some of my family and pets".
20. Edit the current staged commit and split it into 2 separate commits, 1 for each file with messages, "my family", for family.txt and, "my pets", for pets.txt. Then, push to the remote repo.
21. Look at the git log in `oneline` and verify your commit messages.
22. In a new working (`local`) directory, create a totally new git repo called `community`. Create a new repo of the same name in your GitHub (`remote`) account (in your own namespace). Add the `remote` to your `local` git repo.
23. Create a new file (in `local`) called, `address.txt` with your address in it. Stage, commit, and push the changes with a relevant commit message.
24. Next, bring in your `git_test` repo to the `community` repo as a submodule. Stage your changes and commit with a relevant commit message.
25. Now, go into the `git_test` submodule folder, add a file called `todo.txt` and put a todo item in it. Stage, commit, and push the file (to the `git_test` repo).
26. Exit out of the `git_test` folder/submodule and go into to your `community` repo's root. Stage the `git_test` folder/submodule, add a commit with the message "first commit with submodule" and push to the remote repo.

***

## Wrapping Up

When you are done, verify you have pushed your changes to GitHub. Please create a tag called `v1.0` with a message of "ready for review" in both the `git_test` and `community` repos. Be sure your tags are pushed to the remote repository and are visible in GitHub.

In the `community` repo, create an issue titled **Review Module 1 - Git Basics** and `@mention` your mentor and team leader.
