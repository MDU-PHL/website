# Getting started at MDU

## Get an account

1. See Simon Gleeson (MDU I.T) and ask him to create an MDU account for you.
2. Your login will be your University THEMIS username and password.

## Log in to the server

You need to login using SSH (Secure Shell).

### OS X
You will need to install the [XQuartz](https://www.xquartz.org/) package.
Use the `Terminal` app and type `ssh -X -Y username@marvin.mdu.unimelb.edu.au`
and enter your password when prompted.  

### Windows
You will need to install the [Putty](http://www.putty.org/) and the
 [XMing](https://sourceforge.net/projects/xming/) packages, then enable
 [X11 Forwarding](https://wiki.utdallas.edu/wiki/display/FAQ/X11+Forwarding+using+Xming+and+PuTTY) in Putty.
Install the `Putty` app and use `marvin.mdu.unimelb.edu.au` as the Hostname.

## Test if it works

Type `ls /` and you should see this:
```
bin  bio  boot  dev  etc  home  lib  lib64  lost+found  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
```

To see if graphical applications work:

```
xeyes -geometry 500x500
```
You should see a big window appear with two eyes following your mouse cursor.

## Join our online services

Ask someone to add you to:
* MDU Google Calendar
* Doherty Genomics maling list
* Doherty Genomics Software mailing list
* MDU Bioinformatics Comms: https://mduphl.slack.com
* MDU Bioinformatics Project Management: https://www.meistertask.com/app/project/tvUk2Mhs/
* MDU Github: https://github.com/MDU-PHL

## Regular meetings

* Lab group: Monday 11:00-12:00
* Bioinformatics Clinic: Monday 12:30-13:30
