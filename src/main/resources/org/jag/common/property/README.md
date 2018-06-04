[Ant]: https://ant.apache.org

# property

Description: Tasks to help working with properties within the [Ant] script.

**xmlns**: antlib:org.jag.common.property

The contribution of tasks is done introducing in the script `<project>` tag the location of the tasks definition:

```xml
<project xmlns:prop="antlib:org.jag.common.property" name="...">
```

* `check`
	* Description: Check if the property specified using `property` parameter has a value.
	It can be also an environment variable
	* Parameters:

	Parameter | Mandatory | Default value | Description
	--- | --- | --- | ---
	`property` | Yes | N/A | Name of the property to be checked

	* Body: N/A
	* Example:

```xml
	<prop:check property="my_property"/>
```
