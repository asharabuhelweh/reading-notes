**Git is a DVCS that stores data in a file system made up of snapshots. Each time you save a changed version of your project — called commit — Git creates a snapshot of the file and stores a reference to it. If the file has not changed, Git only stores a reference to the already-stored identical version of it.**
**Local Operations**
Git mostly relies on local operations because most necessary information can be found in local resources. This allows for process expediency because a project’s history resides on the local disk, eliminating the need to fetch history information from the server, and allowing one to continue work on a project even when not online or on a VPN.
**Tracking Changes**
Every single change applied to any file or directory is tracked by Git. And, as the gatekeeper, Git will always detect file corruption or loss of information in transit.
**Loss of Data**
Git is set up to greatly minimize the possibility of irreversible damage to files, such as accidentally lost data. Git makes it extremely difficult for a snapshot of your file that is committed to be lost.

***States***
Files in Git can reside in three main states: **committed, modified and staged.**
***Committed***
Data is securely stored in a local database
***Modified***
File has been changed but not committed to the database
***Staged***
Flagged a file’s changed version to be committed in the next snapshot

![states](https://blog.udemy.com/wp-content/uploads/2015/08/image066.png)

**Tracking and Staging a New File**
Single File
Track one file only by using the following format:
***git add filename***

All Files
Track all files in a repository by using the following command:
$ git add *
*After using these commands, files are tracked and staged for committing.
After adding a new file called EXAMPLE, you would see information regarding changes to be committed when using the git status command:
**$ git status**

**Committing a File**
After staging one or multiple files, you should commit the changes and record what you did within the commit message:

***$ git commit -m “made change x,y,z”***
*This step has committed changes for the file or files (you can have one commit message for multiple files, if applicable) to the HEAD.

**Committing All Changes**
***$ git commit -a***
*This command commits a snapshot of all modifications to tracked files in the working directory.

**Pushing Changes**
Next, you would push changes to a remote repository. We will discuss remote repositories in more depth in the next section. For now, we will look at a general overview of pushing changes to remotes.
Example:
***$ git push origin master***

**remote command**
By running the git remote command, you can view the short names, such as “origin,” of all specified remote handles.

By using git remote -v, you can view all the remote URLs next to their corresponding short names.

reading-notes[main]$ git remote -v
origin  https://github.com/asharabuhelweh/reading-notes.git (fetch)
origin  https://github.com/asharabuhelweh/reading-notes.git (push)