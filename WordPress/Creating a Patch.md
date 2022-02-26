# Creating a Patch

   1. Navigate to project and select the `code` dropdwon.
   2. Select the `SSH` tab and copy the text in the box.
      * example:

 ```
git@github.com:AmyJuneH/lando.git
```

   3. Open terminal (be sure to be in the project root).
   4. Clone the repo onto your maching using the `git clone` command.

```git clone git@github.com:AmyJuneH/lando.git```

   5. Create new branch for making changes.

```git checkout -b [branch name]```

   6. Open code in editor of choice.
   7. Save and review changes.

```
git status
git diff
```

   8. Hold shift : then q and enter to leave the comparison view.
   9. Commit changes.

```
git status
git add [file name] or git add . to include all changed files
git commit -m “[Project name] - [name of feature] - description of changes.”
```

   10. Create patch - A patch is the difference between two git "references".
   11. Be sure to be in the project root.
   12. Git diff between the two branches to create a patch.


```
git diff [orginal branch] [new branch] > [name your patch].patch
```

   13. Open patch in editor and review 

