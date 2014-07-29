capbash-monit
==============

Scripts for installing [monit](http://mmonit.com/monit/) monitoring and management tool, should be used in conjunction with capbash

# How to Install #

Install capbash first, more details at:
https://github.com/aforward/capbash

```
git clone https://github.com/aforward/capbash YOUR_REPO_ROOT
cd YOUR_REPO_ROOT
./bootstrap
```

Now you can install monit into your project

```
./capbash install monit
```

# How To Configure #

You will want to edit the monitrc that is copied into your ./assets/monit/monitrc file.

Change the port, host / IP, and username / password.  Here is the default

```
set httpd port 4001
  use address 127.0.0.1
  allow monit:monit
```

# Deploy to Remote Server #

To push the monit script to your server, all you need if the IP or hostname of your server (e.g. 192.167.0.48) and your root password.

```
./capbash deploy <IP> monit
```

For example,

```
./capbash deploy 127.0.0.1 monit
```
