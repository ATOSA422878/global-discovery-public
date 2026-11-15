# Utility Class GlideScheduleDateTime()

## Example
```javascript
var strConvertedDateTime = new GlideScheduleDateTime("2022-03-03 06:30:00").convertTimeZone("CET", "IST");
var gdtConvertedDateTime = new GlideDateTime(strConvertedDateTime);
gs.info(gdtConvertedDateTime);
```
