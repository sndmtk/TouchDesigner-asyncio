# TouchDesigner-asyncio

TDAsyncIO.tox is a Component for using the asyncio module in TouchDesigner without blocking the TD's main thread by running the event loop only once after every frame. 

## Usage

### Parameters
 - Active - The Event Loop can run asynchronous tasks while 'Active' is enabled<br>
 - Cancel All Tasks - Cancel all tasks you created.<br>

![Parameters](https://drive.google.com/uc?export=view&id=1CQuFqiK7gqOEWgF1YVU6_9ejXxJ_GgWv) <br>

### Code example

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
<br>

## License
[MIT](https://github.com/sndmtk/TouchDesigner-asyncio/blob/main/LICENSE)
