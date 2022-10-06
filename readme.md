A convenience class for web scraping that I re-use a lot.

Dependencies:

- `selenium` for controlling the browser
- `PyVirtualDisplay` to run the browser headless
- `lxml` and `cssselect` for easier traversing of HTML

Also requires [`chromedriver`](https://sites.google.com/a/chromium.org/chromedriver/).

Supports:

- All the basic functionality of `selenium`, with some convenience methods
- Taking screenshots of pages
- Saving/loading cookies

# Basic Usage

```python
from browser import Browser

b = Browser(
    cookies_file='data/cookies.json',
    virtual_display=True,
    log_file=None)

b.visit('https://www.google.com')
html = b.html()
divs = html.cssselect('div')
```

See `browser/browser.py` for more.