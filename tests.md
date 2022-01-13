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
 
 #### URL: `example.com`
Firefox 96.0 `new URL` on Windows: `Uncaught TypeError: URL constructor: example.com is not a valid URL.` <br>
Chromium 93.0.4577.82 `new URL` on Linux: `Uncaught TypeError: Failed to construct 'URL': Invalid URL`
Python 3.9.9 urllib3 1.26.5 `urllib.parse urlparse` on Linux: 
  - Scheme: `''`
  - Netloc: `''`
  - Path: `'example.com'`
  - Fragment: `''`

#### URL: `//:example.com`
Firefox 96.0 `new URL` on Windows: `Uncaught TypeError: URL constructor: //:example.com is not a valid URL.`
Chromium 93.0.4577.82 `new URL` on Linux: `Uncaught TypeError: Failed to construct 'URL': Invalid URL`
Python 3.9.9 urllib3 1.26.5 `urllib.parse urlparse` on Linux: 
  - Scheme: `''`
  - Netloc: `''`
  - Path: `':example.com'`
  - Fragment: `''`

#### URL: `evilcyberhacker.com://example.com`:
Firefox 96.0 `new URL` on Windows: 
  - Protocol: `"evilcyberhacker.com:"`
  - Hash: `""`
  - Host: `""`
  - Pathname: `"//example.com"`
  - Origin: `"null"`
Chromium 93.0.4577.82 `new URL` on Linux:
  - Protocol: `'"evilcyberhacker.com:"'`
  - Hash: `""`
  - Host: `""`
  - Pathname: `"//example.com"`
  - Origin: `"null"`
Python 3.9.9 urllib3 1.26.5 `urllib.parse urlparse` on Linux: 
  - Scheme: `'evilcyberhacker.com'`
  - Netloc: `'example.com'`
  - Path: `''`
  - Fragment: `''`

#### URL: `http://#example.com`:
Firefox 96.0 `new URL` on Windows: `Uncaught TypeError: URL constructor: http://#example.com is not a valid URL.`
Chromium 93.0.4577.82 `new URL` on Linux: `Uncaught TypeError: Failed to construct 'URL': Invalid URL`
Python 3.9.9 urllib3 1.26.5 `urllib.parse urlparse` on Linux: 
  - Scheme: `'http'`
  - Netloc: `''`
  - Path: `''`
  - Fragment: `'example.com'`

#### URL: `http:/example.com/evilcyberhacker.com`
Firefox 96.0 `new URL` on Windows: 
  - Protocol: `"http:"`
  - Hash: `""`
  - Host: `"example.com"`
  - Pathname: `"/evilcyberhacker.com"`
  - Origin: `"http://example.com"`
Chromium 93.0.4577.82 `new URL` on Linux:
  - Protocol: `'"http:"'`
  - Hash: `""`
  - Host: `"example.com"`
  - Pathname: `"/evilcyberhacker.com"`
  - Origin: `"http://example.com"`
Python 3.9.9 urllib3 1.26.5 `urllib.parse urlparse` on Linux: 
  - Scheme: `'http'`
  - Netloc: `''`
  - Path: `'/example.com/evilcyberhacker.com'`
  - Fragment: `''`
 #### URL: `http://evilcyberhacker.com\@example.com`
 Firefox 96.0 `new URL` on Windows:
  - Protocol: `"http:"`
  - Hash: `""`
  - Host: `"example.com"`
  - Pathname: `"/"`
  - Origin: `"http://example.com"`
Chromium 93.0.4577.82 `new URL` on Linux:
  - Protocol: `"http:"`
  - Hash: `""`
  - Host: `"example.com"`
  - Pathname: `"/"`
  - Origin: `"http://example.com"`
Python 3.9.9 urllib3 1.26.5 `urllib.parse urlparse` on Linux: 
  - Scheme: `'http'`
  - Netloc: `'evilcyberhacker.com\\@example.com'`
  - Path: `''`
  - Fragment: `''`
#### URL: `http:\\example.com\evilcyberhacker.com` (\ escaped in browsers)
 Firefox 96.0 `new URL` on Windows:
  - Protocol: `"http:"`
  - Hash: `""`
  - Host: `"example.com"`
  - Pathname: `"/evilcyberhacker.com"`
  - Origin: `"http://example.com"`
Chromium 93.0.4577.82 `new URL` on Linux:
  - Protocol: `"http:"`
  - Hash: `""`
  - Host: `"example.com"`
  - Pathname: `"/evilcyberhacker.com"`
  - Origin: `"http://example.com"`
Python 3.9.9 urllib3 1.26.5 `urllib.parse urlparse` on Linux: 
  - Scheme: `'http'`
  - Netloc: `''`
  - Path: `'\\example.com\\evilcyberhacker.com'`
  - Fragment: `''`
#### URL: `http://example.com@evilcyberhacker.com` (todo)
#### URL: `http:\/example.com` (todo)
