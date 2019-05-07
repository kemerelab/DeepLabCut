===========
Action Plan
===========

Some improvements we can make:

1. Fix buggy GUI toolboxes--for example, event loops not even exiting in some cases. Potentially redo with PySide2 or other toolkit
2. If a project config file exists, the `create_new_project` function returns None and the config file path has to be set manually. This can be handled more gracefully
3. Log commands to a file instead of just printing to stdout, so we have a record whenever something goes wrong
4. Add GUI interfaces for config file generation
5. Place all yaml templates in separate files instead of hard-coding string inside .py file
6. Remove need to execute shell script when downloading pre-trained models
7. Consistent docstring, remove `ilikemyfunctionnamestobereallylong` type functions. This is not a Java project.

=================
Development Notes
=================

1. If we end up using a Qt-based GUI toolkit, we should use the officially supported PySide2 bindings. pip has the latest version
but sometimes there are conflicts with other packages, so we should stick with the version on conda-forge. It is built with an
earlier version of Qt but we only need the basic features, so it will be ok. When 5.12+ gets packaged for conda, we can switch to that.
2. It seems that DLC interfaces with a DeeperCut implementation, hence the .mat files. It could be worth investigating whether
we can eliminate this and rely only on pure Python data constructs.