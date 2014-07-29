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

# Configurations #

The available configurations include:

```
MONIT_PORT=${MONIT_PORT-4001}
MONIT_HOST=${MONIT_HOST-127.0.0.1}
MONIT_USER=${MONIT_USER-monit}
MONIT_PASSWORD=${MONIT_PASSWORD-monit}
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
