# mock_all_fedora #

This script does two things.  First it uses rpmbuild to create a SRPM, and then it runs a mock rebuild.  With the current variables set at the top, it will build RPMs for Fedora 14-16 both i386 and x86_64.  The variables may need to be altered.

## Usage ##
```
mock_all_fedora package.spec
```
## To-Do ##

* Extend to use arguments to allow for greater flexibility

# create_all_repos #

This script will create the databases necessary for a local yum repository and optionally run repoview on each repo.

## Usage ##
```
create_all_repos
```
## To-Do ##

* Configure to be much more flexible and not require editing of variables to change script's behavior
* Better error handling
