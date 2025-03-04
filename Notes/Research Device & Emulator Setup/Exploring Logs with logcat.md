# adb logcat

```
adb logcat -v <log_format>
```

Change the log format - for example using `brief` to get a more condensed version of the log.

# Log Filtering

In some cases there can be lots of log entries which makes it hard to focus on the things that matter. For example if you are only interested in the logs produced by the `MainActivity`, you can use a log filter for that:

```
adb logcat "MainActivity:V *:S"
```

Filter format:

- `MainActivity:V` ensures that logs from the tag MainActivity with a severity of Verbose and above are logged
- `*:S` Ensures that all other Tags are ignored (as nothing will log with log-level Silent or above)

Logging severities:

||Log level|
|---|---|
|V|Verbose|
|D|Debug|
|I|Info|
|W|Warning|
|E|Error|
|F|Fatal|
|S|Silent|