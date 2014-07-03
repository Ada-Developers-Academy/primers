Perforce 
========

###Resources for installation and getting started:
Go to http://www.perforce.com/downloads/Perforce/20-User and install
P4V: Visual Client (gui)
P4Merge: Visual Merge Tool (gui for merging)
P4Web: Web Client and (optional web interface)
P4: Command-Line Client (use the command line).

###Specs:
Perforce is version control software like Git.

###Strengths:
It allows multiple users to checkout a file and edit it, while continuously maintaining a single codebase (called trunk). This common shared codebase can be used by anyone, anywhere.

It's scalable; Perforce manages a lot of really big files well.

Perforce is set up so that you can't submit when the build is red.  (You should check your build monitor's before submitting anyway.)


###Use cases:

When installing Perforce, you'll need to find out from your team which code bases you'll need access to and download those.

At least once a day, you'll need to sync those files by right clicking on the file name (eg. trunk) and selecting "Get latest version"

To start, create a pending CL (changelist) to store your relevant files.
In the P4 square [INSERT SCREENSHOT], right click and select "create pending changelist"
Add a description so that it will make sense to you and your workspace (you can edit before submitting).

Open the needed files in your IDE.  Press return to activate the page; a popup window will appear asking where you'd like to put the file.  You can select your pending CL from the drop down menu; otherwise, the file will be placed in Perforce's default folder. Refresh Perforce, and you'll see your files whereever you placed them.

Code like crazy.

Run in your IDE.

Perforce saves your files as you go.

Before you submit, you should have your code reviewed by a colleague.  First, shelve your your edited files.  Perforce automatically creates a "shelved" folder in your pending CL.  Just drag your files to there, and send your colleague your pending CL number so that s/he can find it. 

After you've done a code review and it's been approved, you're ready to submit!

Right click your pending CL and select "Edit pending CL."  Make sure your description would be helpful to anyone outside your team.  I usually add the story ID number for reference too.

Assuming the build is green, click submit.




Common problems or errors:
<!-- Visual mess when there's a merge conflict.
- talk about other options instead of merge
- talk about three screens -->


Anything that you wish someone would have told you before you started:

<!-- Overview of what Perforce talks to
  P4 - this is the command-line client
  P4V - this is version control
  P4Web 
  IDE - integrated development environment, such as IntelliJ IDEA and Eclipse.

  Keywords/phrases:
  workspace



Main steps/features you'll need to get started:
-syncing workspace
-Shortcuts that help
-changelist (CL)
  purpose of
  how to create
-incl. screenshots of key pieces
-What to avoid:
-Resources: -->



