# convert-my-data
This was shancarters project, I'm trying to work on it and improve the types of data we can display

Or maybe I can use:

I believe you could use Papa Parse, which is a JavaScript tool to parse .csv files.

First, input all your data to Excel, and save the file as a .csv

Next use NPM to install Papa Parse:

```
$ npm install papaparse
```
Import your .csv to JS:

```
var file = '/path/to/your.csv';

var content = fs.readFileSync(file, "utf8");
```
Then use this code to parse the .csv to an array:

```

var Papa = require('papaparse');

Papa.parse(content, {
    header: false,
    delimiter: "\t",
    complete: function(results) {
    rows = results.data;
    }
});
```
