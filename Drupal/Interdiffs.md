# Interdiffs

An interdiff is a text file in patch format that describes the changes between two versions of a patch.

For more detailed information, please visit:
 * https://www.drupal.org/documentation/git/interdiff


 ## Assumptions

 * Branches have been named following Drupal best practices.
 * Patches have been named following Drupal best practices.

   1. To create an interdiff, navigate to project root.

 ```
 git diff [issue_id]-[old_comment_number] > interdiff-[issue_id]-[old_comment_number]-[new_comment_number].txt
 ```

 * Example: `git diff 3034926-2 3034926-8 > interdiff-3034926-2-8.txt`
