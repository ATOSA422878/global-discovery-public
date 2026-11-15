# Script Class GlideTinyURL()

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
