# Hubitat-Device-Drivers
Device drivers for Hubitat home automation
Version 1.1 addresses:
  - A code modification necessary for some Leviton scene controllers which adds buttons 17-20 as the "off" button numbers.
    It would appear that the devices which the original author, Michael Philip Kaufman, used to test the code did not need these values.
    There could be firmware variations from Leviton that modify the mapping (unclear). In my testing, I noted the use of buttons
    17-20 in logs from my devices. I also saw that others users where experiencing the same.
    This update should continue to work for devices not using button 17-20 mappings (untested).
  - Disabled button light updates. The code, as originally authored, performs a broadcast update to all Leviton controllers whenever
    a device is part of a scene of one of the controllers. This results in excessive zwave network traffic and a slow down of the
    network (when there are numerous scene controllers).
