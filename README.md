# mock_all_fedora #

This script does two things.  First it uses rpmbuild to create a SRPM, and then it runs a mock rebuild.  With the current variables set at the top, it will build RPMs for Fedora 14-16 both i386 and x86_64.  The variables may need to be altered.

## Usage ##

Run the following from your rpmbuild SPEC directory

```
# Specifying the directory to output mock logs and final RPMs
mock_all_fedora --resultdir ${HOME}/rpmbuild/RPMS/"%(dist)s"/"%(target_arch)s" package.spec

# Using default mock results dir
mock_all_fedora package.spec
```
## To-Do ##

None planned, but if you have a request please open an issue

# create_all_repos #

This script will create the databases necessary for a local yum repository and optionally run repoview on each repo.

## Usage ##
```
create_all_repos
```
## To-Do ##

* Configure to be much more flexible and not require editing of variables to change script's behavior
* Better error handling

Additional features can be requested via the issue tracker
