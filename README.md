# studious-pancake
Step 1: Encountering a Merge Conflict
(When you attempt to merge branches and a conflict arises, Git will notify you:)
$ git merge feature-branch
Auto-merging notification.js
CONFLICT (content): Merge conflict in notification.js
Automatic merge failed; fix conflicts and then commit the result.

Step 2: Open the Conflicted File
(Open notification.js in your preferred text editor to view the conflict markers:)
$ nano notification.js
(Within the file, you'll see conflict markers indicating the differing changes:)
<<<<<<< HEAD
sendNotification("New message received");
=======
sendNotification("You have a new message!");
>>>>>>> feature-branch

Step 3: Resolve the Conflict
(Edit the file to resolve the conflict by choosing the appropriate code or combining changes:)
sendNotification("You have a new message!");
(Ensure you remove all conflict markers (<<<<<<<, =======, >>>>>>>) after resolving.)

 Step 4: Mark the Conflict as Resolved
 After saving the changes, stage the resolved file:
 $ git add notification.js

Step 5: Complete the Merge
Commit the merge to finalize the process:
$ git commit

Step 6: Verify the Merge
Check the status to ensure everything is up to date:
$ git status
On branch main
nothing to commit, working tree clean
