## Scripting Alert, Info, and Error Messages

Will put "Hello World" below the specified field.

```javascript
current.field_name.setError("Hello World");
```

Will put "Hello World" on the top of the screen.

```javascript
gs.addInfoMessage("Hello World");
```

Will write to the text log on the file system but not to the sys_log table in the database.

```javascript
gs.print("Hello World");
```

Will write to the database and the log file.

```javascript
gs.log("Hello World");
```

## Get Difference of Two Date Times ##

```javascript
getTimeDiff();  

function getTimeDiff(){  
  var startDate = current.u_start_date.getGlideObject();  
  var endDate = current.u_end_date.getGlideObject();  

  current.u_duration = gs.dateDiff(startDate.getDisplayValueInternal(),endDate.getDisplayValueInternal(),false);  

}
```

[1]: https://docs.servicenow.com/bundle/orlando-application-development/page/script/general-scripting/reference/r_ScriptingAlertInfoAndErrorMsgs.html	"Scripting alert, info, and error messages"
