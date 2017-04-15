[![Build Status](https://travis-ci.org/kuu/parallel-fetch.svg?branch=master)](https://travis-ci.org/kuu/parallel-fetch)
[![Coverage Status](https://coveralls.io/repos/github/kuu/parallel-fetch/badge.svg?branch=master)](https://coveralls.io/github/kuu/parallel-fetch?branch=master)
[![Dependency Status](https://gemnasium.com/badges/github.com/kuu/parallel-fetch.svg)](https://gemnasium.com/github.com/kuu/parallel-fetch)
[![XO code style](https://img.shields.io/badge/code_style-XO-5ed9c7.svg)](https://github.com/sindresorhus/xo)

# parallel-fetch

Fetch with limiting the number of concurrent tasks

## Usage
```
const Loader = require('parallel-fetch');

const loader = new Loader({concurrency: 5});

loader.load('https://foo.com/bar.html', {noCache: true}, (err, result) => {
  if (err) {
    return console.log(`Error: ${err.stack}`);
  }
  console.log(`MIMEType: ${result.mimeType}`);
  console.log(result.data);
});
```
