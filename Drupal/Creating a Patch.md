# Creating a Patch

   1. Navigate to project page and select the version control tab
   2. Select the version and show
   3. Copy git clone link
      * example:

 ```
 git clone --branch 8.x-2.x https://git.drupal.org/project/bootstrap_paragraphs.git
cd bootstrap_paragraphs
```

   4. Open terminal (be sure to be in the project root)
   5. Create new branch with the naming convention: issue node # and comment ie., 3034926-2 (comment #2) `git checkout -b 3034926-2`
   6. Open preferred editor and edit the appropriate file and save
   7. Review changes

```
git status
git diff
```

   8. Hold shift : then q and enter to leave the comparison view.
   9. Commit changes

```
git status
git add [file name] or git add . to include all changed files
git commit [file name]
git commit -m “[Name of module] - [name of file] - description of changes and maybe the Drupal.org node #.”
```

   10. Create patch - A patch is the difference between two git "references".
   11. Be sure to be in the project root
   12. Git diff between the two branches to create a patch
       Note: Patch naming convention:
       [project_name]-[fix]-[issue_id]-[old_comment_number] .patch 
       Example: bootstrap_paragraphs-UI_fix-3034926-4.patch

```
git diff 8.x-1.x 3034926-2 > bootstrap_paragraphs-readme-3034926-2.patch
```

   13. Paste command in terminal
   14. Open patch in editor and review 
   15. Return to the issue and add the patch to a new comment
   16. Open issue metadata fieldset and change the following:
       * Status: Needs review
       * Assigned: Unassign
       * Comment
       * Upload file
       * Save


## Patch naming conventions explained
https://www.drupal.org/node/1054616


The (unofficial) patch naming convention that has emerged from the community is:

[project_name]-[short-description]-[issue-number]-[comment-number].patch

[project_name]
Refers to the project's name as it appears in the URL of the project page on
Drupal.org, i.e. http://drupal.org/project/[project_name], or from the git
remote repository location, i.e. http://git.drupal.org/project/[project_name].git 

[short-description]
Is a 1-2 word summary about what the patch does with dashes between the words.

[issue-number]
Appears in the URL of the issue on Drupal.org. For example, if the issue you're
working on is at http://drupal.org/node/9876543, the issue number is 9876543.

[comment-number]
Is the comment on the aforementioned issue that caused another patch file to be
needed or the another one that inspired the patch. If there is no comment
causing the patch to be submitted then none is required for the file name or you
can use a comment-number of 0 (zero) to indicate the original issue. If you're
fixing, changing or improving upon a previously provided patch in a way that has
not yet been documented in a previous comment, you may wish to guess at the
comment number you're about to post by adding 1 to the last comment number on
the issue; please note that this last option is an imperfect method that may not
work as intended on active issues with many people commenting. In this case, the
best advice is to redact your comment offline, and refresh the page just before
you paste in your comment text and attach the patch.
