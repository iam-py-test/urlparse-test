### Some tests
#### URL: `http://example.com`
Firefox 96.0 `new URL` on Windows: 
  - Protocol: `"http:"`
  - Hash: `""`
  - Host: `"example.com"`
  - Pathname: `"/"`
  - Origin: `"http://example.com"`

Chromium 93.0.4577.82 `new URL` on Linux:
  - Protocol: `'http:'`
  - Hash: `''`
  - Host: `'example.com'`
  - Pathname: `'/'`
  - Origin: `'http://example.com'`
 
Python 3.9.9 urllib3 1.26.5 `urllib.parse urlparse` on Linux:
  - Scheme: `http`
  - Netloc: `'example.com'`
  - Path: `''`
  - Fragment: `''`

#### URL: `http:///example.com`
Firefox 96.0 `new URL` on Windows: 
  - Protocol: `"http:"`
  - Hash: `""`
  - Host: `"example.com"`
  - Pathname: `"/"`
  - Origin: `"http://example.com"`

Chromium 93.0.4577.82 `new URL` on Linux:
  - Protocol: `'http:'`
  - Hash: `''`
  - Host: `'example.com'`
  - Pathname: `'/'`
  - Origin: `'http://example.com'`

Python 3.9.9 urllib3 1.26.5 `urllib.parse urlparse` on Linux:
  - Scheme: `'http'`
  - Netloc: `''`
  - Path: `'/example.com'`
  - Fragment: `''`
