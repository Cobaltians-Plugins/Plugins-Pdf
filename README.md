# PDF Plugin

This Cobalt PDF plugin allows you to open a local or remote PDF file in your mobile app from Javascript.

## How to use

* import the plugin to your project as explained [here](https://github.com/cobaltians/cobalt/wiki/Plugins-usage)
* Add the cobalt.pdf.js to your web JS folder
* Add an html link to the cobalt.pdf.js plugin script after the cobalt link in the HEAD tag

### Open a PDF document from JavaScript

use the `cobalt.openpdf` shortcut like this:

```javascript
cobalt.openpdf(myPdfDatas);
```

or with a callback:

```javascript
cobalt.openPdf(myPdfDatas, function(result){...});
```

where data need a JSON Object like this, with direct url:

```javascript
var myPdfDatas = {
'source': 'url',
'path': 'http://example.com/images/cat.png'
};
```

or a PDF stored in assets:

```javascript
var myPdfDatas = {
'source': 'local',
'path': 'sample.pdf',
};
```

And then:
```javascript
cobalt.openpdf(myPdfDatas);
```

### Existing fields to fill are :

| Field | Description | Examples Values | Mandatory |
| ----- | ---- | ----------- | ----------- |
| source | source from where the file comes | 'url', 'local' | YES |
| path | local/remote path of the file     | 'http://example.com/sample.pdf', 'files/sample.pdf' | YES |

## Want more ?

If you have any ideas or improvements to propose, please feel free to do so in the issues tracker!
