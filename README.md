PHING-VERSION
=======

Version management with phing and git.

CONCEPT
-------

Use git tags to simplify version management and release.  Improvements over the standard git tag functionality are:

* Automated version names with project prefix and time stamp
* Shorter and simpler commands
* Better control over releases and rollbacks

USAGE
-----

Look at phing targets:

```
$ phing -l
```

* phing version-list - List all currently available versions. These are a subset of all git tags.
* phing version-create - Create a new version of the project based on the latest commit in current working directory.
* phing version-push - Push all local versions and branches to the remote git repository.
* phing version-pull - Pull all versions and branches from the remote git repository.
* phing version-checkout - Switch current working directory to a specific version.

NOTES
-----

When doing 'phing version-checkout', the latest available version will be used.  Also, a file called version.txt will be created,
which will hold the name of the checked out version.  This file should be added to .gitignore .  This file is used for building
deployment logs and diff changelogs before or after release.


AUTHOR
------
Leonid Mamchenkov <leonid@mamchenkov.net>
