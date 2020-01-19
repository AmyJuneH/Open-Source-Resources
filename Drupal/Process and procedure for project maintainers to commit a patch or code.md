# Process and procedure for project maintainers to commit a patch or code to Drupal.org

## Committing a Patch to Drupal.org

Assumptions:
 * You are a maintainer of the project
 * You have uploaded you SSH credentials
 
Process:
 * Navigate to Project’s Issue Queue and select the issue
 * Select the patch to apply and it should open in a new page
 * Right click anywhere on the page and select “Save as” from the dropdown and take note of the path
 * Tip: you can drag the file into the terminal window and it will output the path.
 * /Users/admin/Desktop/admin_status-d8-README-3005183-2.patch
 * Open a terminal and navigate to the project’s root.
 
 Apply the patch
 * git apply -v [path/patchname.patch]
 * git apply -v /Users/admin/Desktop/admin_status-d8-README-3005183-2.patch
 * Check the git status
 * git status
 * Add the file
 * git add .
 * Navigate back to the issue queue
 * Select the users to attribute
 * copy the command in the commit window
 * In the terminal enter a commit message
 * git commit -m 'Issue #3003371 by andrewozone, ajlib, volkswagenchick: Remove roadmap from help page' --author="git git@3430095.no-reply.drupal.org"
 * Check the log to see if the changes are correct
 
Push the changes
 * git push
 * Navigate back to the issue queue
 * Make a comment about fixing
 * Thank the contributors, checking to see if everyone got a credit
 * Mark meta data as fixed
