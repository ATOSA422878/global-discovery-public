# Script Class GlideElementPhoneNumber()
## Description
GlideElementPhoneNumber is a ServiceNow server-side and global script class used to handle, parse, and validate E.164 and legacy phone number fields.

## Purpose
Allows scripts to interact with phone number fields, extract country/territory details, and validate formatting against system phone territory tables (sys_phone_territory and sys_phone_validate).

## Common Methods:
- setPhoneNumber(number): Sets or updates the phone number value to be processed.
- getTerritory(): Retrieves the country or territory associated with the phone number.
- getGlobalDisplayValue(): Returns the formatted global E.164 representation of the number.

## Application Scope Limitation
As noted by developers on the ServiceNow Developer Forum, GlideElementPhoneNumber is restricted and generally not permitted within private application scopes (it is intended for global scope). 

## Configuration & Properties
Behavior is controlled via system properties like glide.phone_number_e164.strict and glide.phone_number_e164.allow_national_entry. For setup details and catalog workarounds, check out the ServiceNow Community HRSD Guide. 
## Example

```javascript
var objPhoneNumber = new GlideElementPhoneNumber();
var isValidPhoneNumber = objPhoneNumber.setPhoneNumber( '+49 170 123456789', true);
gs.info(isValidPhoneNumber);
gs.info(objPhoneNumber.getTerritory());
```

## Attribution
Assistance of Google Gemini

## Notes
- [1] [E.164 phone number field configuration](https://www.servicenow.com/docs/r/yokohama/platform-administration/r_ConfigureE.164PhoneNumberFields.html) | ServiceNow Documentation
- [2] [Getting country from Phone Number (E164) field in a script?](https://www.servicenow.com/community/developer-forum/getting-country-from-phone-number-e164-field-in-a-script/m-p/1575325) | ServiceNow Community
- [3] [Setting up phone number validation on Now Platform](https://www.servicenow.com/community/hrsd-articles/setting-up-phone-number-validation-on-now-platform-phone-number/ta-p/2444496) | ServiceNow Community
