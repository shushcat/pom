pom
===

A minimalistic time-tracker with logging and a pleasant-sounding chime.

Usage
--------

    pom

An initial task can be optionally provided at the command line, in which case the user will not be prompted until subsequent intervals.

Synopsis
-----------

The `pom` utility prompts for a task, then counts down for a predefined length of time while you work.  When each period ends, `pom` plays a chime and adds a datestamped entry to `~/pom.log` before counting down for a five-minute break period and chiming again.  Every four breaks, a twenty-minute break is triggered, after which the utility exits.

Configuration
--------------

The variables `pom_time` and `pom_logfile` can be set in `~/.pom.rc` or at the top of the script itself.  By default, `time_in_minutes=25` and `logfile=$HOME/.pom.log`.

A simple alternative configuration file, `~/.pom.rc`, might look like this:

    pom_time=10
    pom_logfile="/dev/null"

Extras
------

1. Use `#hashtags` in your messages so you can easily grep for them later.
2. Use `awk`/`grep` to add up time spent on projects, or for specific days.

        awk '/#hacks/ { total += $1 } END { print total / 60 " hours" }' pom.log

Notes
-----

A PowerShell version is available at the repository from which this was derived, [here](https://github.com/tobym/pom).
