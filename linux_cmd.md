### View all the apps installed
- apt list --installed
- dpkg --get-selections


### whoami vs who am i
- https://unix.stackexchange.com/questions/72177/what-is-pts-0-and-0-0-in-linux-when-typing-who-am-i

The root account is the special user in the /etc/passwd file with the user ID (UID) of 0 and is commonly given the user name, root. It is not the user name that makes the root account so special, but the UID value of 0 . This means that any user that has a UID of 0 also has the same privileges as the root user.


### Journalctl
Journalctl is a utility for querying and displaying logs from journald, systemd's logging service. Since journald stores log data in a binary format instead of a plaintext format, journalctl is the standard way of reading log messages processed by journald.

### rsyslog (log to different files)
rsyslog separates log messages to different files such as /var/log/auth. log , /var/log/syslog and so on.
