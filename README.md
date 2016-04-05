pell
====

pell is a simple periodic host monitor that utilizes ping to check for
host availability. It can also be used to perform logging functions,
with an easy-to-parse output suitable for data extraction and
analysis. By default, when a host that you ping’d is alive, it emits a
short beep sound. It runs continuously until an INT, TERM, or KILL is
received.


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

To monitor for pongs from `foo.bar.baz` every minute, saving the
output to `foo.bar.baz.log` run:

```
$ pell -i 60 foo.bar.baz | tee -a foo.bar.baz.log
```

To convert `foo.bar.baz.log` file to CSV, for graphing and data
analysis:

```
$ sed 's/ /,/g' foo.bar.baz.log > foo.bar.baz.csv
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
