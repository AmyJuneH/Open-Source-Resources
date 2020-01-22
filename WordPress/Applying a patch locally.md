# Applying a patch locally

## From the command line:

 * Navigate to the module’s project page on Drupal.org
 * Download the project repo
   * FIXME
 * Download the patch that requires testing
 * From the command line navigate into the project root
 * `cd project_name`
 * `git apply -v [location/path_of_patch]`
 
 
 * To avoid accidentally including the patch file in future commits, remove it:
`rm  [patchname.patch]`
