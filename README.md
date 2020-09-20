# Problem_3
isOnline:
Script for scheduled check of websites availability and mail report. Suited for crontab job.

Config:
Create emails.lst file and fill it with each email in new line (as in emails.lst.example). leave an empty line in the end.
eg:my.email@example.com

Create websites.lst file and fill it with each website in a new line (as in websites.lst.example). leave an empty line in the end.
www.wikipedia.com,
www.yahoo.com, 
www.netflix.com 

Note that the script will follow url(s) with 301 (redirect).

Add to crontab:
Add the following lines to crontab config ($ crontab -e)

THIS_IS_CRON=1
*/30 * * * * /path/to/isOnline/checker.sh
