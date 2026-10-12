1. What is the difference between a working directory, the staging area, a commit, and a remote repository?

- Working directory is where we edit files and work on your code.
- Staging area is where we hold up some files we want to commit before actually committing them.
- A commit is a snapshot of the working directory that is saved into git history (a series of these would make up the history of the repository).
- A remote repository in git is basically like our local repository except it is hosted on the cloud and is the place where we push and pull from, which enables us to collaborate with others.
<br>
<br>

2. What do HEAD, main, and origin refer to in a normal repository?

- HEAD is a pointer to the current branch or commit that we are working on.
- main is a pointer to the latest commit on our primary branch.
- origin is just a default name (alias) for the URL of the remote repository (where the remote is on the internet) that, for git, is hosted on the cloud.
<br>
<br>

3. Why should you pull or fetch recent main changes before starting new work?

To make sure that we are working on top of the latest version of the code.
<br>
<br>

4. What is the difference between fetching and pulling?

Fetching downloads remote changes from the remote repository to the local repository without altering our code, while pulling will try to merge the changes with our local code.
<br>
<br>

5. What is the difference between merging and rebasing? When is rebasing a shared branch dangerous?

Merging creates a new commit node with 2 parent nodes without changing any previous commit nodes. Rebasing moves an entire branch to another commit node and is dangerous because it directly alters the parent node at the start of the branch. For the parent pointer, the commit hash changes, result nodes are new commit nodes and the original commit nodes become orphaned. If a team member is working on the original nodes, this will cause a lot of digital confusion and merge conflicts when the team member tries to pull the changes.
<br>
<br>

6. Why are pull requests useful even though they are not part of Git itself?

Lets others to review and merge code into a specific branch, good for collaboration and code review.
<br>
<br>

7. In Task 4, Git created a new commit called Merge branch 'can'. Why was a new commit needed?

Want: merge two different branches that have independent histories without rewriting each of their histories. Having a merge commit is like a bridge between the two branches and is a way to preserve the history of both.
<br>
<br>

8. In Task 5, both branches changed src/main.cpp. Why did can_id merge by itself but @version and loop() did not?

Because can_id was only altered (updated) in main, and the can_id of the branch was just from a previous version of main that did not change in the branch. For version and loop(), the changes were made in both branches which made git confused on which to keep as they seem equally important.
<br>
<br>

9. In Task 6, which workflow ran when you pushed to ci, and which did not? Why? What does the CI workflow protect the team from?

Documentation deployment workflow ran (Doxygen GitHub Pages Deploy Action) due to a push to the main branch. Since it generates this documentation directly from comments inside the code, it protects the team from reading blind or outdated code instructions. Also, CI workflow means that reviewers can easily see that code compiles before requesting changes.
<br>
<br>

10. What does a .gitignore file do, and why does it not remove a file that was already committed? Why is .pio in .gitignore?

.gitignore is a configuration file that tells git which files to ignore. However, it only stops git from tracking newly created files, rather than the ones git is already tracking. .pio is auto-generated so saving it is redundant.

