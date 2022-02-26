# Creating a Patch

   1. Navigate to project and select the `code` dropdwon
   2. Select the `SSH` tab and copy the text in the box
      * example:

 ```
git@github.com:AmyJuneH/lando.git
```

   3. Open terminal (be sure to be in the project root)
   4. Clone the repo onto your maching


   5. Open preferred editor and edit the appropriate file and save
   6. Review changes

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
    FIXME

```
git diff fixme
```

   13. Paste command in terminal
   14. Open patch in editor and review 
   15. Return to the issue and add the patch to a new comment
   16. Open issue metadata fieldset and change the following:
       *FIXME


## Patch naming conventions explained
FIXME
