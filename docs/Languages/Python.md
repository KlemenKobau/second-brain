## Logging

- [Rich](https://github.com/Textualize/rich) - Rich is a Python library for rich text and beautiful formatting in the terminal. 
    The Rich API makes it easy to add color and style to terminal output. Rich can also render pretty tables, progress bars, markdown, syntax highlighted source code, tracebacks, and more — out of the box.

## Async

- Async code in python is still blocking

Running the following code in the REPL will return control back to the user after 10 seconds
```py
import asyncio

async def main():
    print('Hello ...')
    await asyncio.sleep(10)
    print('... World!')

asyncio.run(main())
```

This prints:
```
Hello ...
<Wait 10 seconds>
... World!
<Control is returned back to the user>
```

One way of doing async tasks is with:

```py
loop = asyncio.new_event_loop()
asyncio.set_event_loop(loop)

asyncio.ensure_future(main(), loop=loop)
asyncio.ensure_future(main(), loop=loop)

loop.run_forever()
```

This blocks the main thread, but the result will be as follows

```
Hello ...
Hello ...
<Wait 10 seconds>
... World!
... World!
<Control is not returned!>
```