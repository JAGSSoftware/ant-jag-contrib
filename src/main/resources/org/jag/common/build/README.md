# build

Description: Tasks to help with the build of the project.

**xmlns**: antlib:org.jag.common.build

The contribution of tasks is done introducing in the script `<project>` tag the location of the tasks definition:

```xml
<project xmlns:build="antlib:org.jag.common.build" name="...">
```

* `clean`
	* Description: Removes the specified directory from the project layout
	* Parameters:

	Parameter | Mandatory | Default value | Description
	--- | --- | --- | ---
	`dir` | Yes | N/A | Directory to be removed.

	* Body: N/A
	* Example:

```xml
	<build:clean dir="to_be_removed"/>
```

* `prepare`
	* Description: Creates the specified directory within the project layout
	* Parameters:

	Parameter | Mandatory | Default value | Description
	--- | --- | --- | ---
	`dir` | Yes | N/A | Directory to be created.

	* Body: N/A
	* Example:

```xml
	<build:prepare dir="to_be_created"/>
```
