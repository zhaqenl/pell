pell
====

pell is a trivial tool that emits a notification when a host that you
ping'd is alive. By default, when a pong is received, the system bell
emits a short beep, and a desktop notification is displayed.

## Usage

To monitor for pongs from `somehost.foo.bar` every second, sounding
the system bell and displaying a desktop notification if a reply is
received, run:

```
$ pell somehost.foo.bar
```

To do the same as above, sans the bell and desktop notification, run:

```
$ pell -s -n somehost.foo.bar
```

To monitor for pongs from `somehost.foo.bar` every 30 seconds, run:

```
$ pell -i 10 somehost.foo.bar
```
