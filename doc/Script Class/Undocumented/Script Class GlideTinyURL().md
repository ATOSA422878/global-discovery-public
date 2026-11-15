# Script Class GlideTinyURL()

## Table Name
Tiny URL [sys_tiny_url]

## Usage
```javascript
GlideTinyURL().createTinyURL(url <string>);
GlideTinyURL().createTinyURLWithCustomLength(url <string>, length <integer>)
```

## Example
```javascript
var urlString = "/now/nav/ui/classic/params/target/sys.scripts.modern.do";
var tinyURL = new GlideTinyURL().createTinyURL(urlString);
gs.debug(urlString);
gs.debug(tinyURL);
```

## Reference
- [Tiny URLs In ServiceNow](https://www.linkedin.com/posts/maik-skoddow_servicenow-activity-7402602649902276608-yze2) | Maik Skoddow, LinkedIn
