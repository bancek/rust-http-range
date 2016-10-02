# rust-http-range

HTTP Range header parser. It parses Range HTTP header string as per RFC 2616.

Inspired by Go's net/http library.

## Overview

Example usage:

```
extern crate http_range;

use http_range::{HttpRange, HttpRangeParseError}

let mut ranges = match HttpRange::parse(range_str, size) {
    Ok(r) => println!("Start {}, length {}", r.start, r.length),
    Err(err) => println!("HttpRange parse error: {:?}", err)
};
```

## Used in

- [iron-send-file](https://github.com/bancek/iron-send-file)

## Author

Luka Zakrajšek

## License

MIT
