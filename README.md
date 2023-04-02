# deno_numpy

[![Tags](https://img.shields.io/github/release/tjosepo/deno_numpy)](https://github.com/tjosepo/deno_numpy/releases)
[![deno doc](https://doc.deno.land/badge.svg)](https://doc.deno.land/https/deno.land/x/numpy@0.2.0/mod.ts)
[![Tests](https://github.com/tjosepo/deno_numpy/actions/workflows/tests.yml/badge.svg)](https://github.com/tjosepo/deno_numpy/actions/workflows/tests.yml)

Deno bindings for [Numpy](https://numpy.org/), the fundamental package for
scientific computing.

## Usage

Install Python, then:

```js
import np from "https://deno.land/x/numpy@0.2.0/mod.ts";

const x = np.arange(15, { dtype: np.int64 }).reshape(3, 5);
np.put(x, np.arange(5, 15, 2), -99);
console.log(x);
// array([[  0   1   2   3   4]
// [-99   6 -99   8 -99]
// [ 10 -99  12 -99  14]])

console.log(x.max({ axis: 1 }));
// array([ 4  8 14])
```

For more info, visit https://numpy.org/doc/stable/

## Contributing

You can help me make this project better! More info
[here](https://github.com/tjosepo/deno_numpy/blob/master/CONTRIBUTING.md).

## Other

Special thanks to DjDeveloper and Elias Sjögreen for creating
[deno_python](https://github.com/denosaurs/deno_python).
