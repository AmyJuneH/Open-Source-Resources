# Interdiffs

https://www.drupal.org/documentation/git/interdiff


 * An interdiff is a text file in patch format that describes the changes between two versions of a patch.
 * To create an interdiff
 * `git diff [issue_id]-[old_comment_number] > interdiff-[issue_id]-[old_comment_number]-[new_comment_number].txt`
 * Example: `git diff 3034926-2 3034926-8 > interdiff-3034926-2-8.txt`
