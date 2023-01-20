PowerShell Code Cheat Sheet:
1.	Get-Command: lists all available commands in PowerShell.
2.	Get-Help: provides help and usage information for a command.
3.	Get-Service: lists all services on the system.
4.	Start-Service: starts a service.
5.	Stop-Service: stops a service.
6.	Restart-Service: restarts a service.
7.	Get-Process: lists all processes running on the system.
8.	Start-Process: starts a new process.
9.	Stop-Process: stops a process.
10.	Get-ChildItem: lists the contents of a directory.
11.	New-Item: creates a new item (file or directory).
12.	Remove-Item: deletes an item (file or directory).
13.	Move-Item: moves an item (file or directory).
14.	Copy-Item: copies an item (file or directory).
15.	Get-Content: reads the contents of a file.
16.	Set-Content: writes content to a file.
17.	Add-Content: appends content to a file.
18.	Invoke-WebRequest: sends an HTTP or HTTPS request to a web page.
19.	Invoke-RestMethod: sends a RESTful web request.
20.	ConvertTo-Json: converts an object to a JSON string.
21.	ConvertFrom-Json: converts a JSON string to an object.
22.	$variables: stores values or objects for later use.
23.	if-else statements: performs actions based on a condition.
24.	for loops: repeats actions for a set number of times.
25.	foreach loops: repeats actions for each item in a collection.
26.	function: defines a reusable block of code.
27.	Write-Host: writes output to the console.
28.	Write-Output: sends output to the pipeline.
29.	Out-File: sends output to a file.
30.	Exit: exits the current session of PowerShell.

Example:

```
Get-Process | Where-Object {$_.CPU -gt 50} | Sort-Object -Property CPU -Descending | Select-Object -First 5 | Format-Table -Property Name, CPU
```

This example gets all running process, filters out the ones with CPU usage greater than 50%,
 sorts the remaining processes by CPU usage in descending order, selects the top 5 processes, and displays them in a table with the Name and CPU columns.