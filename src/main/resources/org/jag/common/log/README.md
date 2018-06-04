# log

Description: These are contributed tasks for logging the [Ant] target or operations.

**xmlns**: antlib:org.jag.common.log

The contribution of tasks is done introducing in the script `<project>` tag
the location of the tasks definition:

```xml
	<project xmlns:log="antlib:org.jag.common.log" name="...">
```

Unlike any other logging system, the levels of logging is for information only, it doesn't filter
by logging level.

* `init`
	* Description: Initializes the logger. It must come among the first lines in the [Ant] script
	* Parameters:

	Parameter | Mandatory | Default value | Description
	--- | --- | --- | ---
	`dir` | Optional | Current directory, `.` |  Directory where to write the logs to.
	`file` | Optional | `${ant.project.name}_${DSTAMP}${TSTAMP}.log` | Log file where to write the log entries to.

	* Body: N/A
	* Example:

			<log:init/>

* `logger`
	* Description: Writes a message with level `level` in logger
	* Parameters:

	Parameter | Mandatory | Default value | Description
	--- | --- | --- | ---
	`level` | Yes | N/A | Level of logging

	* Body: Message to be written to logger
	* Example:
	
			<log:logger level="error">Message to log</log:logger>

* `error`
	* Description: Writes a message with level _error_ in logger
	* Parameters: N/A
	* Body: Message to be written to logger
	* Example:
	
			<log:error>Message to log</log:error>
		
* `warn`
	* Description: Writes a message with level _warn_ in logger
	* Parameters: N/A
	* Body: Message to be written to logger
	* Example:
	
			<log:warn>Message to log</log:warn>

* `info`
	* Description: Writes a message with level _info_ in logger
	* Parameters: N/A
	* Body: Message to be written to logger
	* Example:
	
			<log:info>Message to log</log:info>
		
* `verbose`
	* Description: Writes a message with level _verbose_ in logger
	* Parameters: N/A
	* Body: Message to be written to logger
	* Example:
	
			<log:verbose>Message to log</log:verbose>
		
* `debug`
	* Description: Writes a message with level _debug_ in logger
	* Parameters: N/A
	* Body: Message to be written to logger
	* Example:
	
			<log:debug>Message to log</log:debug>
