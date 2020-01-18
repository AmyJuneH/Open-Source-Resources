# Applying a patch locally

## From the command line:

 * Navigate to the module’s project page on Drupal.org
 * Download the project repo
 * Select the version control tab
 * example:  `git clone --branch 8.x-2.x https://git.drupal.org/project/bootstrap_paragraphs.git`
 * Download the patch that requires testing
 * From the command line navigate into the project root
 * `cd project_name`
 * `git apply -v [location/path_of_patch]`
 
 
 * To avoid accidentally including the patch file in future commits, remove it:
`rm  [patchname.patch]`
