协程：在一个子程序中中断，去执行其他子程序，不是函数调用，有点类似CPU的中断

协程是在一个线程里，共享资源不需要加锁，效率比多线程高。




## 1、声明协程
协程 通过 async/await 语法进行声明，是编写 asyncio 应用的推荐方式。

await只能在async函数里面使用

比如
```python
import asyncio


async def hello():
    print("Hello world!")
    await asyncio.sleep(1)
    print("Hello again!")


asyncio.run(hello())
```
其中，hello，asyncio.sleep(1)分别是一个协程

## 2、运行协程

1. asyncio.run() 函数用来运行最高层级的入口点 "main()" 函数
2. asyncio.create_task() 函数用来并发运行作为 asyncio 任务 的多个协程。


## 3、可等待对象

