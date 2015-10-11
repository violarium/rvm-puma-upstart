# rvm-puma-upstart

It is upstart example script which will help you to manage you ruby app via [puma](http://puma.io/) web server, when ruby is installed via [RVM](https://rvm.io/).

This is simplier version of [puma-jungle](https://github.com/puma/puma/tree/master/tools/jungle/upstart) upstart.


## Why do you want to use it?

* You want to use [RVM](https://rvm.io/);
* You have found [puma-jungle](https://github.com/puma/puma/tree/master/tools/jungle/upstart) too complicated;
* You want to start different puma processes with different users.


## How to use it

For example, you have app, installed into: **/home/webapp/awesome/current**

Create RVM-alias.
```
rvm alias create awesome ruby-2.2.3@default
```

Copy this file to `/etc/init/` directory with appropriate name.

```
cp puma-app-example.conf /etc/init/awesome.conf
```

And now you can use it like this:

```
start awesome
stop awesome
restart awesome
status awesome
```

It also will start you application on system boot.


For customization look at the file and replace what do you want - look at the comments.
