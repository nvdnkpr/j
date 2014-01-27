# J

Simple data wrapper that attempts to wrap [xlsjs](http://npm.im/xlsjs) and [xlsx](http://npm.im/xlsx) to provide a uniform way to access data

## Node Library

```
var J = require('j');
```

`J.readFile(filename)` opens the file specified by filename and returns an array
whose first object is the parsing object (XLS or XLSX) and whose second object
is the parsed file.  

`J.utils` has various helpers that expect an array like those from readFile:

- `to_csv(w) / to_dsv(w, delim)` will generate CSV/DSV respectively
- `to_json(w)` will generate JSON row objects
- `to_html(w)` will generate simple HTML tables
- `to_xml(w)` will generate simple XML 

## CLI Tool 

The node module ships with a binary `j` which has a help message:

```
$ bin/j.njs --help

  Usage: j.njs [options] <file> [sheetname]

  Options:

    -h, --help             output usage information
    -V, --version          output the version number
    -f, --file <file>      use specified workbook
    -s, --sheet <sheet>    print specified sheet (default first sheet)
    -l, --list-sheets      list sheet names and exit
    -S, --formulae         print formulae
    -j, --json             emit formatted JSON rather than CSV (all fields text)
    -J, --raw-js           emit raw JS object rather than CSV (raw numbers)
    -X, --xml              emit XML rather than CSV
    -F, --field-sep <sep>  CSV field separator
    -R, --row-sep <sep>    CSV row separator
    --dev                  development mode
    --read                 read but do not print out contents
    -q, --quiet            quiet mode

  Support email: dev@sheetjs.com
  Web Demo: http://oss.sheetjs.com/
```

## License

Please consult the attached LICENSE file for details.  All rights not explicitly granted by the Apache 2.0 license are reserved by the Original Author.