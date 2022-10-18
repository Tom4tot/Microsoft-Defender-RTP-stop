# Microsoft Defender Real-Time Protection stop

### Usage guide
- Make sure to disable tamper protection first. For that, go to: Windows Security → Virus and threat protection → Virus and threat protection settings (otherwise the task won't work: tamper protection blocks apps from changing real-time protection settings, including PowerShell).
- Manually disable real-time protection from Windows Security (this should be the last time you need to do it).
- Import the task.

### Purpose of disabling RTP
- No more CPU usage and disk usage from "Antimalware Service Executable".
- Improves privacy.

### Drawbacks
- Obviously, disabling RTP will decrease security; therefore, it's highly recommended to use a firewall in whitelist mode ([simplewall](https://github.com/henrypp/simplewall/) is a great tool for that) as well as scanning your system regularly, especially files from the internet.
- It also involves to disable Tamper protection.

### Benefits from this approach compared to alternatives
- Only uses official Windows features and components (i.e. Task Scheduler and PowerShell).
- Very low on resources.
- Extremely low chances of breaking anything since there is no hack involved (permission bypass, regedit modifications, etc.). Alternatives often break Windows Security completely whereas this allows to keep other features on (except tamper protection, as previously mentioned).
- Very easy to uninstall / pause temporarily: just disable or delete the task.
- Should still work after major Windows updates, except if Microsoft changes things significantly.

### Additional information
- https://en.m.wikipedia.org/wiki/Windows_Task_Scheduler#Column_'Last_Result'
- https://www.reddit.com/r/sysadmin/comments/mnej84/windows_scheduled_tasks_is_it_best_to_use_system/
- https://ss64.com/nt/schtasks.html

### Credits
[Duttyend](https://github.com/duttyend/Microsoft-Defender-RTP-stop)
