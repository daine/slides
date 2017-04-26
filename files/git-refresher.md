# git
### a refresher

<br />

NOTES
TADA! No notes, really

=====
## What is git again?
Distributed Version Control System
<div class="fragment">- Keeps track of changes in your files</div>
<div class="fragment">- Keeps track of code revisions</div>
/////
## Why would we use it?
<div class="fragment">- Worry-free innovation</div>
<div class="fragment">- Deployments</div>
<div class="fragment">- Minimizes user downtime</div>
<div class="fragment">- Team contribution</div>
<div class="fragment">- Keeps your sanity</div>

NOTES
- Never lose code again
- Freeze/pack code for deployment to test and production environments
- Easily revert to a previous revision if something breaks
- Work on the same codebase at the same time with other people
- Keep  your sanity


/////
## What do I need?
- Install git ([docs](http://webspinner.bcgov/gitbooks))
- Install SourceTree (optional git GUI/desktop application)
- Login to http://webspinner.bcgov/gitlab
=====
## The git process
### Three stages in a repository
<div class="fragment">1. Working area/directory</div>
<div class="fragment">2. Staging area</div>
<div class="fragment">3. Repository (`.git`(local), remote)</div>
NOTES
- Working area - local changes
- Staging - Preparation for commit
- Repository - committed changes, changes written in history
-- can be local or remote

/////
#### Local Repository
<div class="fragment">`.git` folder at the top level directory of your project</div>
<div class="fragment">- exists in your project folder</div>
<div class="fragment">- 1 project = 1 local git repo</div>
/////
#### Remote Repository
<div class="fragment">- Can either be a **colleague's PC** or a **central git server**</div>
<div class="fragment">- For simplicity, let's focus on having a ***central git server***</div>
/////
#### Central Git server
We have a central git server for our repositories in webspinner

<br />

git@webspinner.bcgov

<small>*(more on this later)*</small>
=====
### WebSpinner
## YAY!
![Happy](images/gifs/happy.gif)<!-- .element height="25%" width="25%" -->

NOTES
After a few months of setting up, we can finally see our code in a UI friendly way
/////
![GitLab](images/stacked_wm_no_bg.png)<!-- .element height="25%" width="25%" -->
<div class="fragment">a web application for our central git server</div>
<div class="fragment">- an open-source repository manager</div>
<div class="fragment">- similar to github.com</div>

NOTES
- GitLab is a web application that provides an interface to our git repos
/////
#### GitLab features
|Features||
|--|--|
|Code Reviews|x|
|Deployment tools|x|
|Source code management tools|x|
|Issue Tracking|x|
|Time Tracking|x|
|Continuous Integration *(automated builds)*|x|
|Cycle analytics *(time it takes for an idea to get to production)*|x|
|Host static html pages *(GitLab Pages)*|x|


=====
### Code Reviews
<div class="fragment">- A peer or senior will review your code
![anxious](images/gifs/anxious.gif)<!-- .element height="50%" width="50%" -->
</div>
<div class="fragment">- Improves code design, quality and readability</div>

<div class="fragment">- Helps in finding mistakes overlooked by the original author</div>
/////
 No git commits = No code reviews
=====
### Back to git process
<div class="fragment">[Local]</div>
<div class="fragment">
|<br />
|<br />
V
</div>
<div class="fragment">[Remote]</div>
NOTES
After you've committed your code in your local repository, you may want to send it to the central remote repository/server so that other people will have access to it.

/////
## Local
<div class="fragment">[Working]</div>
<div class="fragment">
|<br />
|<br />
V
</div>
<div class="fragment">[Stage changes]</div>
<div class="fragment">
|<br />
|<br />
V
</div>
<div class="fragment">[Commit changes]</div>

NOTES
- Working = active development
- Staging - clean up code for committing
- Commit - Ready for the whole world to look at, hey, you're committed!
/////
## Pushing to remote
<div class="fragment">[Pull remote changes]</div>
<div class="fragment">
|<br />
V
</div>
<div class="fragment">[Merge changes *(auto)*]</div>
<div class="fragment">
|<br />
V
</div>
<div class="fragment">[Stage/Commit merged changes]</div>
<div class="fragment">
|<br />
V
</div>
<div class="fragment">[Push commits]</div>
NOTES
- Pull remote changes to make sure you have the most current version if anyone changes something
- If there are new changes, git will automatically merge them if possible
- If a merge is not successfull (new changes are similar to your code or affects the same lines), you'd have to manually do a merge

=====
## **master** vs **branch** vs **tags**
/////
## master
main development copy

/////
## branch
<div class="fragment">- features</div>
<div class="fragment">- bug fixes</div>
/////
## branch
|branch|environment|
|-|-|
|test|Test|
|release|Production|

/////
# tag
<div class="fragment">a snapshot of the code</div>
/////
# tag
|branch|environment|tag|desc|
|-|-|-|-|
|test|Test|1.0.0|*test-ready code, v1.0.0*|
|release|Production|1.0.0|*stable release v1.0.0*|
|release|Production|1.2.0|*stable release v1.2.0*|



=====
## Homework
Add your existing datamarts to git

RRT -
http://webspinner.bcgov/gitlab/cdw/datamarts/rrt

NOTES
Visit page
Explain the command line instructions
Explain the ssh link at the top if using SourceTree
/////
### Example datamart in git

[Git: Verification and Audit Unit](http://webspinner.bcgov/gitlab/cdw/datamarts/vau)
NOTES:
Go to Commits > Initial Commit
Click on "22 changed files"
- index.py

Demonstrate code reviews
