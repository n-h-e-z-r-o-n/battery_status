# battery_status

The above is a script written in Visual Basic Script (VBScript) that is used to monitor the battery status on a Windows computer. The script uses the Windows Management Instrumentation (WMI) interface to query the system for battery information.

The first lines of code create an instance of the SWbemLocator object, which is used to connect to the WMI service on the local machine (".") using the "root\wmi" namespace.

The script then uses the ExecQuery method to query the "batteryfullchargedcapacity" class, and stores the results in the variable "oResults". This query retrieves the full charged capacity of the battery. The value is stored in variable "iFull"

Next, the script enters an infinite loop. Within the loop, the script uses the ExecQuery method to query the "batterystatus" class, and stores the results in the variable "oResults". This query retrieves the remaining capacity of the battery and whether the battery is charging or not. The values are stored in variables "iRemaining" and "bCharging" respectively.

The script then calculates the percentage of the battery's remaining capacity by dividing the "iRemaining" value by the "iFull" value and multiplying by 100. The result is stored in the variable "iPercent"

The script then checks if the battery is charging and if the remaining capacity is greater than 90%, and if both conditions are true, it shows a message box with the message "Battery is at " & iPercent & "%"

Thee script then will check the percentage of remaining capacity and if it's below 10% it will show the message "Battery is at " & iPercent & "%, Please charge your device" with an exclamation mark.

The script then waits for 30 seconds before repeating the loop.
