pell
====

pell is a simple tool that emits a notification when a host that you
ping'd is alive. By default, it runs continuously, and when a pong is
received, the system bell sounds a short beep, and a desktop
notification is displayed.

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
$ pell -i 30 somehost.foo.bar
```

## Notes

pell exclusively relies on the ping tool. It means that it relies on
the assumption that ICMP Echo Request packets are allowed to reach the
remote host. and that the remote host is configured to respond to
these packets.
