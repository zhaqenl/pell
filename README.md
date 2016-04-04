pell
====

pell is a simple tool that emits a notification when a host that you
ping'd is alive. By default, it runs continuously, and when a pong is
received, a short beep sound is played.


## Usage

To monitor for pongs from `foo.bar.baz` every second, playing an
audio notification if a reply is received, run:

```
$ pell foo.bar.baz
```

To do the same as above, without the audio notifications, run:

```
$ pell -s foo.bar.baz
```

To do the same as above, with visual notifications, run:

```
$ pell -n foo.bar.baz
```

To monitor for pongs from `foo.bar.baz` every 30 seconds, run:

```
$ pell -i 30 foo.bar.baz
```

## Notes

pell exclusively relies on the ping tool. It means that it has the
assumption that ICMP Echo Request packets are allowed to reach the
remote host. and that the remote host is configured to respond to
these packets. Please check the firewall settings.


## Credits

The file `resources/notification.mp3` was recorded by Marianne Gagnon,
with a
[CC Attribution 3.0 license](https://creativecommons.org/licenses/by/3.0/),
and was downloaded from
[soundbible.com/1682-Robot-Blip.html](http://soundbible.com/1682-Robot-Blip.html).
