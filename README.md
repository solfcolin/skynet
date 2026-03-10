这个版本和官方的版本完全一致，并且会一直合并最新的修改；由于skynet极其精简的内核，所以实现这个调试器并没有修改框架的代码，只是增加了几个额外的模块：

cjson 用于进行json格式的数据交换。

-------------------------------------------------------------------------------------------------------------------------
## ![skynet logo](https://github.com/cloudwu/skynet/wiki/image/skynet_metro.jpg)

Skynet is a multi-user Lua framework supporting the actor model, often used in games.

[It is heavily used in the Chinese game industry](https://github.com/cloudwu/skynet/wiki/Uses), but is also now spreading to other industries, and to English-centric developers. To visit related sites, visit the Chinese pages using something like Google or Deepl translate.

The community is friendly and almost all contributors can speak English, so English speakers are welcome to ask questions in [Discussion](https://github.com/cloudwu/skynet/discussions), or submit issues in English.

## Build

For Linux, install autoconf first for jemalloc:

```
git clone https://github.com/cloudwu/skynet.git
cd skynet
make 'PLATFORM'  # PLATFORM can be linux, macosx, freebsd now
```

Or:

```
export PLAT=linux
make
```

For FreeBSD , use gmake instead of make.

## Test

Run these in different consoles:

```
./skynet examples/config	# Launch first skynet node  (Gate server) and a skynet-master (see config for standalone option)
./3rd/lua/lua examples/client.lua 	# Launch a client, and try to input hello.
```

## About Lua version

Skynet now uses a modified version of lua 5.5.0 ( https://github.com/ejoy/lua/tree/skynet55 ) for multiple lua states.

Official Lua versions can also be used as long as the Makefile is edited.

## How To Use

* Read Wiki for documents https://github.com/cloudwu/skynet/wiki (Written in both English and Chinese)
* The FAQ in wiki https://github.com/cloudwu/skynet/wiki/FAQ (In Chinese, but you can visit them using something like Google or Deepl translate.)
