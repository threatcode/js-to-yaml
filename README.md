# JS TO YAML

[![CodeQL](https://github.com/threatcode/js-to-yaml/actions/workflows/codeql.yml/badge.svg)](https://github.com/threatcode/js-to-yaml/actions/workflows/codeql.yml)

> A node module to convert JSON to pretty YAML

## Installation

`npm install --save js-to-yaml`

## Usage

#### `index.js`

```javascript
const fs = require('fs');
const YAML = require('js-to-yaml');
const json = require('input.json');

const data = YAML.stringify(json);
fs.writeFile('output.yaml', data);
```

#### `input.json`

```json
{
  "a": 1,
  "b": 2,
  "c": [
    {
      "d": "cool",
      "e": "new"
    },
    {
      "f": "free",
      "g": "soon"
    }
  ]
}
```

#### `output.yaml`

```yaml
a: 1
b: 2
c:
  - d: "cool"
    e: "new"
  - f: "free"
    g: "soon"
```

## Testing

`npm test`
