When you run df or similar tools on linux, the volume is 100% used. One of the problems is that some logs are using too much space. In this case it was syslog.

Logs are being rotated but not often enough or still too big

Logrotation configured in `/etc/logrotate.d`. For syslog it’s the rsyslog config:
```
/var/log/syslog
{
	rotate 7
	daily
	missingok
	notifempty
	delaycompress
	compress
	postrotate
		/usr/lib/rsyslog/rsyslog-rotate
	endscript
}

/var/log/mail.info
/var/log/mail.warn
/var/log/mail.err
/var/log/mail.log
/var/log/daemon.log
/var/log/kern.log
/var/log/auth.log
/var/log/user.log
/var/log/lpr.log
/var/log/cron.log
/var/log/debug
/var/log/messages
{
	rotate 4
	weekly
	missingok
	notifempty
	compress
	delaycompress
	sharedscripts
	postrotate
		/usr/lib/rsyslog/rsyslog-rotate
	endscript
}
```
At the top it says to create a new file every day and keep the files for 7 days. don't rotate if the file is empty. its ok if its missing. and compress the rotated files. 

adding size `size 100k` to say also rotate when bigger than 100k. 

Should also look at why docker is creating so many logs
