---
layout: manual
title: Reminders
manual: tasks
order: 100
---

Let's face it; some developers just aren't that reliable, and often need to be regularly reminded about their tasks. You can use the Reminders Tab for this. 

While viewing a task, click the Reminders Tab heading, and you will see a list of existing reminders. To send out a regular reminder to someone, use the form provided. Select the developer's name, enter the frequency of time you wish to have the reminders sent, and type a short message. A sample message is provided, as shown in the image.

<img src="/images/manual/addreminder.jpg" class="img-responsive" alt="Reminder Tab">

### Enabling reminder support in Flyspray 1.0

Flyspray 1.0 uses schedule.php called by a cronjob (or from command line for testing). Here are 2 crontab examples for setting it up:

```crontab
# min hour dayofmonth month dayofweek  command
# check every 7th minute on every hour
7  * * * * php flyspray/schedule.php
```

```crontab
# min hour dayofmonth month dayofweek  command
# check every 5 minutes
*/5 * * * * php flyspray/schedule.php
```

Check if the command line version you setup in the crontab is similiar to the php version of the webserver.
Some hosters provide different versions of php on the command line like 'php-5.4'. Find out by typing php [TAB][TAB] (shell autocompletion) to see which php versions are available there.

#### Reminder on Windows

Untested: Setup the regular invoking of schedule.php by using the Task Scheduler of Windows.

### Enabling reminder support in Flyspray < 1.0

Flyspray has a background daemon to regularly trigger various scripts. You need two things to make it work:

  * *reminder_daemon* must be set to "2" in [flyspray.conf.php](/docs/flyspray.conf). 
  * It must be possible for the script to run forever. So [set_time_limit()](http://php.net/set_time_limit) must not be disabled.

If you can't use the background reminder daemon for whatever reason, you need to activate the schedule.php regularly another way. One method would be using a task scheduler (like 'cron') to make a download program (like 'wget') retrieve the file every five or ten minutes, in this case set the value to "1" instead of "2". You don't need to save it anywhere, just send it to the bit bucket. Merely retrieving the file causes it to run, and thus, send the reminders out.

If you have the ability to use cron on your system, you might automate wget with a command such as this:

<code>wget -q -O /path/to/logfile.txt http://www.mydomain/flyspray/schedule.php</code>

Note that you have to modify the file before you can use it that way. <code>while(true)</code> needs to be changed to <code>while(false)</code>. Also, you can only run this file from a *local* machine.


To easily activate schedule.php from your web server itself, go to URL "http://127.0.0.1/.../flyspray/schedule.php" in a web browser / client where ... denotes whatever sub-directories your flyspray installation might be located. If you do not receive the message "You are not authorized to start ..." and are presented with nothing in your web browser then it means that you have successfully started the notification daemon and notifications should go out as expected. You can just close your web browser down or click stop in your web browser since the PHP script should run indefinitely on the web server as long as it is configured properly.
