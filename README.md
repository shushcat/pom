pom
===

A minimalistic time-tracker with logging.

Usage
--------

    pom <task>

Synopsis
-----------

The `pom` utility counts down for a predefined length of time while you work on a task and outputs datestamped logs when each period ends.

Configuration
--------------

The variables `time_in_minutes` and `logfile` can be changed in the `CONFIGURATION` section at the head of the script.  By default, `time_in_minutes=25` and `logfile=$HOME/.pom.log`.

Extras
------

1. Use `#hashtags` in your messages so you can easily grep for them later.
2. Use `awk`/`grep` to add up time spent on projects, or for specific days.

        awk '/#hacks/ { total += $1 } END { print total / 60 " hours" }' pom.log

Notes
-----

A PowerShell version is available at the repository from which this was derived, [here](https://github.com/tobym/pom).
