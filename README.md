# pbauto-javascript-browser
This project is part of the Pandoras Box SDK. It implements an interface to access the Pandoras Box Automation.

## Usage
You can call the API on the PBAuto object.

```javascript
PBAuto.applyView(1);
```

If you need to retrieve values, you can add an optional callback as the last parameter.

```javascript
connection.getSelectedDeviceCount( function(response){
	// response.http holds the HTTP status code
	// response.code holds the Automation Command code
	// both are considered for the convenience value response.ok
	if(response.ok) // check if request was successful
	{
		// response values are automatically parsed and put on the response object
		console.log(response.selectedDevicesCount);
	}
});
```
Response (Raw JSON)
```json
{
	http: 200,
	ok: true,
	code: 81,
	selectedDevicesCount: 2
}
```

## Versioning
The version consists of a major, a minor and a revision field. (major.minor.revision)
If the major version changes, then these changes are incompatible with prior versions. Changes to the minor version indicate backwards compatibility. The revision field is reserved for the Pandoras Box revision that is required to use all features. It might be possible to use the SDK with an older revision of Pandoras Box, but not all the commands will work.

## Contributing
Most of the files in this repository are generated. Please contribute to the template files instead.
https://github.com/coolux/pbauto-generator

v0.1.12086, generated on 2016-02-22