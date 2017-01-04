# pingmonitor

This is a simple cross-platform (Windows and Unix) command-line tool written in python that uses the system's `ping` command to monitor the status of a list of hosts (IPs or hostnames) and prints (and optionally logs) a timestamped message when the status of any of those hosts changes (e.g. they go offline / online).


# Linux usage example:
`pingmonitor --no-gateway google.com example.com 8.8.8.8`


# Windows usage example:
`pingmonitor -l ping_log.txt google.com`


# sample output:

```
$ pingmonitor google.com
2017-01-04 15:08:18 monitoring: google.com example.com 10.0.0.1
2017-01-04 15:08:18 google.com is up
2017-01-04 15:08:18 example.com is up
2017-01-04 15:08:19 10.0.0.1 is up
2017-01-04 15:12:57 example.com is down, was up for 4m 38s
2017-01-04 15:13:09 example.com is up, was down for 12s
2017-01-04 15:54:18 example.com is down, was up for 41m 8s
2017-01-04 15:54:56 example.com is up, was down for 38s
```

