# bash-backup-script
BASH backup script to tar up files/directories and ftp them to a remote server.

This script was originally written to backup the online coordination system used by the Indiana Repeater Council.  As with most projects, as it developed it grew in complexity and functionality.  As it stands now, in its current version, we have all the functionality currently required.  However, changeds or improvements will likely happen.

I'm posting this on GitHub so that folks looking for something similar can perhaps use what I've done here as a learning tool or an example.

There isn't too much complexity involved, but here is the order of operation:

1). Verify the backup directory (/tmp/backup) exists.
2). Clean the backup directory, just in case something has wondered in.
3). Create a tarball of the application directory
4). Append the Apache2 config file to the existing tarball
5). Append the Apache2 document root to the existing tarball
6). GZip the tarball
7). FTP tarball to a primary off-site FTP server
8). FTP tarball to a secondary off-site FTP server
9). Clean the backup directory again, to be thorough.

That's it.  Enjoy.
