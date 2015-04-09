# rvm-puma-upstart

It is upstart example script which will help you to manage you ruby app via [puma](http://puma.io/) web server, when ruby is installed via [RVM](https://rvm.io/).

This is simplier version of [puma-jungle](https://github.com/puma/puma/tree/master/tools/jungle/upstart) upstart.


## Why do you want to use it?

* You have found puma-jungle too complicated
* You want to start different puma processes with different users.


## How to use it

Copy this file to `/etc/init/` directory with appropriate name.

Example:
```
cp puma-app-example.conf /etc/init/puma-awesome-app.conf
```

Look at the file and replace what do you want - look at the comments.

And now you can use it like this:

```
start puma-awesome-app
stop puma-awesome-app
restart puma-awesome-app
```

It also will start you application on system boot.
