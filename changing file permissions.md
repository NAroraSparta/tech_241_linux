# What command changes file permissions?

## To change directory permissions in Linux, use the following:


chmod +rwx filename to add permissions
chmod -rwx directoryname to remove permissions. 
chmod +x filename to allow executable permissions.
chmod -wx filename to take out write and executable permissions.ls
Note that “r” is for read, “w” is for write, and “x” is for execute. 

This only changes the permissions for the owner of the file.

The command for changing directory permissions for group owners is similar, but add a “g” for group or “o” for users:

chmod g+w filename

chmod g-wx filename

chmod o+w filename

chmod o-rwx foldername

To change directory permissions for everyone, use “u” for users, “g” for group, “o” for others, and “ugo” or “a” (for all).

chmod ugo+rwx foldername to give read, write, and execute to everyone.

chmod a=r foldername to give only read permission for everyone.


# To change permissions on a file what must the end user be?

## To change permissions on a file, the end user typically needs to have the appropriate access rights and sufficient privileges. In most cases, this requires the user to have administrative or root-level access to the system or ownership of the file.

## Current owner or Superuser. In Linux, the superuser is the account with unrestricted access to all commands. it is also called root.


# Give examples of some different ways/syntaxes to set permissions on a new file (named testfile.txt) to:
## a. Set User to read, Group to read + write + execute, and Other to read and write only.

    chmod u=r,g=rwx,o=rw testfile.txt

## b. Add execute permissions (to all entities)

    chmod +x testfile.txt

## c. Take write permissions away from Group

    chmod g-w testfile.txt

## d. Use numeric values to give read + write access to User, read access to Group, and no access to Other.

    chmod 640 testfile.txt

