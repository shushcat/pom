pom
===

A minimalistic time-tracker with logging and a pleasant-sounding chime.

Usage
--------

    pom <task>

Synopsis
-----------

The `pom` utility counts down for a predefined length of time while you work on a task and, when each period ends, plays a chime, then outputs a datestamped log entry.

Configuration
--------------

The variables `time_in_minutes` and `logfile` can be set using a `.pom.rc` file in your `$HOME`.  By default, `time_in_minutes=25` and `logfile=$HOME/.pom.log`.

A simple alternative configuration file, `~/.pom.rc`, might look like this:
    time_in_minutes=10
    logfile="/dev/null"

Extras
------

1. Use `#hashtags` in your messages so you can easily grep for them later.
2. Use `awk`/`grep` to add up time spent on projects, or for specific days.

        awk '/#hacks/ { total += $1 } END { print total / 60 " hours" }' pom.log

Notes
-----

A PowerShell version is available at the repository from which this was derived, [here](https://github.com/tobym/pom).
