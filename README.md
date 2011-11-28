# mock_all_fedora #

This script does two things.  First it uses rpmbuild to create a SRPM, and then it runs a mock rebuild.  With the current variables set at the top, it will build RPMs for Fedora 14-16 both i386 and x86_64.  The variables may need to be altered.

## Usage ##

Run the following from your rpmbuild SPEC directory

### Mock for Fedora ###

```
# Specifying the directory to output mock logs and final RPMs
mock_all_fedora --resultdir ${HOME}/rpmbuild/RPMS/"%(dist)s"/"%(target_arch)s" package.spec

# Using default mock results dir
mock_all_fedora package.spec
```

### Mock for CentOS ###

```
# Specifying the directory to output mock logs and final RPMs
mock_all_centos --resultdir ${HOME}/rpmbuild/RPMS/"%(dist)s"/"%(target_arch)s" package.spec

# Using default mock results dir
mock_all_centos package.spec
```

## To-Do ##

None planned, but if you have a request please open an issue

# create_all_repos #

This script will create the databases necessary for a local yum repository and optionally run repoview on each repo.

## Usage ##

With the **--init** option you can also create the necessary directory structure to host a local yum repository.

Depending on the **--distro** argument passed the defaults are to use the following
* Fedora 14-16 for i386, x86_64, and src
* CentOS 4-6 for i386, x86_64, and src

Valid arguments for **--distro**: **(NOTE: Capalization matters)**
* All - Builds both Fedora and CentOS
* Fedora
* CentOS

```
# Build yum repo for both Fedora and CentOS
create_all_repos --distro All

# Create repo directory structure for both Fedora and CentOS and initialize repository
create_all_repos --init --distro All
```
## To-Do ##

* Better error handling

Additional features can be requested via the issue tracker
