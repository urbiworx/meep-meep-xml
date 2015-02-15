# meep-meep-xml
Fast and lightweight XML processor
Meep-Meep-XML is the world first ACME-certified XML parser that comes without additional dependencies, high speed (depending on XML more than 7 times faster than xml2js) and namespace awareness. The initial implementation came with 129 lines of sourcecode, including licenseheader.

#Example usage:
```
var m2xml=require('meep-meep-xml');
var parsed=m2xml.parseXML("<bird age='8'><speed>100</speed></bird>");
parsed.bird.age=14;
console.log(m2xml.renderXML(parsed));
```

#API
parseXML accepts an option parameter as second paramter, for example:
```
m2xml.parseXML("<xml/>",{autoinline:false, ignorenamespace:false});
```
Autoinline automatically converts tags that soley contain tags to attributes, ignorenamespace removes all namespace information.