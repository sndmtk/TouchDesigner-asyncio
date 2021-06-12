# TouchDesigner-asyncio

TDAsyncIO.tox is a Component for using the asyncio module in TouchDesigner. It realizes asynchronous processing without affecting the TD runtime by running the event loop only once after every frame. 

## Usage

Parameters
 - Active - The Event Loop can run asynchronous tasks while 'Active' is enabled<br>
 - Cancel All Tasks - Cancel all tasks you created.<br><br>


Code example

``` python
import asyncio

async def test():
    await asyncio.sleep(3)
    print('hello world')

# Run coroutine
coroutines = [test()]
op.TDAsyncIO.Run(coroutines)

# Cancel all tasks
op.TDAsyncIO.Cancel()
```
## License
[MIT](https://github.com/sndmtk/TouchDesigner-asyncio/blob/main/LICENSE)
