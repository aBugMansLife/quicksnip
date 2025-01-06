---
title: Is Time Between
description: Check if the current time is between the start and end times
tags: time, datetime, timecheck
author: abugmanslife
---

```python
import time

def time_between(time, time_range):
    if time_range[1] < time_range[0]:
        return time >= time_range[0] or time <= time_range[1]
    return time_range[0] <= time <= time_range[1]


// Usage:

current_time = time.strftime("%H:%M", time.localtime())
print(current_time)

if time_between(current_time, ("06:30", "20:30")):
        print("Yes current time is between 06:30 and 20h30")
    else:
        print("No current time is not between 06:30 and 20h30")

if time_between(current_time, ("20:30", "06:30")):
        print("Yes current time is between 20:30 and 06h30")
    else:
        print("No current time is not between 20:30 and 06h30")
```
