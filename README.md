# flair

Aggressive css compiler.

---

## Install

Install flair with npm:

    $ npm install flair -g


## Parser

```js
var flair = require('flair')
flair.parse('jinja { name: "jinja" }')
```

The results returned by `flair.parse`:

```
{
  "filename": null,
  "stylesheet": {
    "rules": [
      {
        "selector": "jinja",
        "start": 0,
        "end": 24,
        "declarations": [
          {
            "property": "name",
            "value": "jinja",
            "start": 9,
            "end": 21
          }
        ]
      }
    ]
  }
}
```

The AST structure is the same as [css-parse](https://github.com/visionmedia/css-parse), but extended with `start` end `end`.


## Changelog
