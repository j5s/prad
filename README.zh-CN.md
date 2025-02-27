# prad

Web directory and file discovery.

## Usage

```shell
➜ prad  .\prad.exe -h
╱╱╱╱╱╱╱╱╱╱╭╮
╱╱╱╱╱╱╱╱╱╱┃┃
╭━━┳━┳━━┳━╯┃
┃╭╮┃╭┫╭╮┃╭╮┃
┃╰╯┃┃┃╭╮┃╰╯┃
┃╭━┻╯╰╯╰┻━━╯
┃┃
╰╯ v0.0.1

web directory and file discovery.

Usage:
  C:\prad.exe [flags]

Flags:
INPUT OPTIONS:
   -u, -url string         url to scan
   -wf, -word-file string  wordlist file

WORD OPTIONS:
   -we, -word-ext string     word extension
   -wp, -word-prefix string  word prefix
   -ws, -word-suffix string  word suffix

OUTPUT OPTIONS:
   -fc, -filter-code int   filter by status code
   -ec, -exclude-code int  exclude by status code

OTHER OPTIONS:
   -concurrent int  concurrent goroutines (default 10)
   -proxy string    proxy
   -timeout int     timeout (default 5)
```

```shell
➜ prad  .\prad.exe -u http://127.0.0.1:8000
╱╱╱╱╱╱╱╱╱╱╭╮
╱╱╱╱╱╱╱╱╱╱┃┃
╭━━┳━┳━━┳━╯┃
┃╭╮┃╭┫╭╮┃╭╮┃
┃╰╯┃┃┃╭╮┃╰╯┃
┃╭━┻╯╰╯╰┻━━╯
┃┃
╰╯ v0.0.1

404 - http://127.0.0.1:8000/.svn
404 - http://127.0.0.1:8000/admin
404 - http://127.0.0.1:8000/login
404 - http://127.0.0.1:8000/.git
404 - http://127.0.0.1:8000/backup
404 - http://127.0.0.1:8000/manager
200 - http://127.0.0.1:8000/.idea
```

## Features

- [x] 自定义字典
- [x] 自定义字典扩展名
- [x] 自定义字段前缀、后缀
- [x] 自定义 URL 替换位置
- [x] 支持代理
- [x] 并发数设置
- [x] 过滤状态码
- [x] 排除状态码
- [x] 超时控制
- [ ] QPS 限制
- [ ] 自定义 headers
- [ ] 进度保存
