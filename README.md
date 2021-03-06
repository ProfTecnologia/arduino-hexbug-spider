# Hexbug spider library for Arduino

This library uses an IR LED to send codes that can be understood by an
[Hexbug Spider][1].

The IR LED is expected to be wired to your Arduino's pin #3.

## Code example

Emitting signals.

```c
#include <hexbug-spider.h>

void setup()
{
  Serial.begin(9600);
  Serial.println("Point your IR LED to an Hexbug spider.");
}

void loop()
{
  hexbug_spider_left();
  delay(100);
}
```

## How to install

1. Install the [irdebug.h][2] library.
2. Copy the `lib/hexbug-spider/` directory to your Arduino's library path, for
   example: `sudo cp -r lib/hexbug-spider /usr/share/arduino/libraries/`.
3. Include the `hexbug-spider.h` file into your main Arduino code, for example
   `#include <hexbug-spider.h>`.

## License

> Copyright (c) 2014 José Carlos Nieto, https://menteslibres.net/xiam
>
> Permission is hereby granted, free of charge, to any person obtaining
> a copy of this software and associated documentation files (the
> "Software"), to deal in the Software without restriction, including
> without limitation the rights to use, copy, modify, merge, publish,
> distribute, sublicense, and/or sell copies of the Software, and to
> permit persons to whom the Software is furnished to do so, subject to
> the following conditions:
>
> The above copyright notice and this permission notice shall be
> included in all copies or substantial portions of the Software.
>
> THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
> EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
> MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND
> NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE
> LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
> OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION
> WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

[1]: http://www.hexbug.com/mechanical/spider/
[2]: https://github.com/xiam/arduino-irdebug
