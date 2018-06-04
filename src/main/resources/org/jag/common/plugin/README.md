# plugin

Description: Contributed tasks to build an Eclipse RCP plugin.

**xmlns**: antlib:org.jag.common.plugin

The contribution of tasks is done introducing in the script `<project>` tag the location of the tasks definition:

```xml
<project xmlns:plugin="antlib:org.jag.common.plugin" name="...">
```

* `read.BundleSymbolicName`
	* Description: Reads the value of `Bundle-SymbolicName` defined in the
	`MANIFEST.MF` and stores the value in the `Bundle-SymbolicName` property 
	* Parameters:

	Parameter | Mandatory | Default value | Description
	--- | --- | --- | ---
	`plugin.dir` | Yes | N/A | Plugin root directory

	* Body: N/A
	* Example:

```xml
	<plugin:read.BundleSymbolicName plugin.dir="."/>
```

* `read.BundleVersion`
	* Description: Reads the value of `Bundle-Version` defined in the
	`MANIFEST.MF` and stores the value in the `Bundle-Version` property
	* Parameters:

	Parameter | Mandatory | Default value | Description
	--- | --- | --- | ---
	`plugin.dir` | Yes | N/A | Plugin root directory

	* Body: N/A
	* Example:

```xml
	<plugin:read.BundleVersion plugin.dir="."/>
```

* `read.build.properties`
	* Description: Reads the `build.properties` within the plugin directory
	and stores the properties
	* Parameters:

	Parameter | Mandatory | Default value | Description
	--- | --- | --- | ---
	`plugin.dir` | Yes | N/A | Plugin root directory

	* Body: N/A
	* Example:

```xml
	<plugin:read.build.properties plugin.dir="."/>
```
