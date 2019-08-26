
# easemusic

解锁网易云音乐客户端变灰歌曲

参考项目 [UnblockNeteaseMusic](https://github.com/nondanee/UnblockNeteaseMusic)

## 运行

源码运行

```
$ node app.js
```

Docker

```
$ docker pull perryzou/easemusic
```

```
$ docker run perryzou/easemusic
```

### 配置参数

```
$ easemusic -h
usage: easemusic [-v] [-p port] [-a address] [-u url] [-f host]
                           [-o source [source ...]] [-t token] [-e url] [-s]
                           [-h]

optional arguments:
  -v, --version                   output the version number
  -p port, --port port            specify server port
  -a address, --address address   specify server host
  -u url, --proxy-url url         request through upstream proxy
  -f host, --force-host host      force the netease server ip
  -o source [source ...], --match-order source [source ...]
                                  set priority of sources
  -t token, --token token         set up proxy authentication
  -e url, --endpoint url          replace virtual endpoint with public host
  -s, --strict                    enable proxy limitation
  -h, --help                      output usage information
```

## 客户端配置

 - PAC 模式
 
填写脚本地址 `http://127.0.0.1:8080/proxy.pac`

 - 全局代理模式

填写服务器地址 `127.0.0.1` 和端口号 `8080`
| 平台    | 基础设置 |
| :------ | :------------------------------- |
| Windows | 设置 > 工具 > 自定义代理 (客户端内) |
| UWP     | Windows 设置 > 网络和 Internet > 代理 |
| Linux   | 系统设置 > 网络 > 网络代理 |
| macOS   | 系统偏好设置 > 网络 > 高级 > 代理 |
| Android | WLAN > 修改网络 > 高级选项 > 代理 |
| iOS     | 无线局域网 > HTTP 代理 > 配置代理 |

> 由于网易云 Windows 客户端的 Bug，测试代理会报错 "该代理不可使用"，实际并不影响 
> 看到 HTTP Server running @ http://0.0.0.0:8080
> 之后出现如 MITM > ... 的请求日志即配置成功

## 其他帮助
参考项目 [UnblockNeteaseMusic](https://github.com/nondanee/UnblockNeteaseMusic)
帮助页面 [食用指南](https://github.com/nondanee/UnblockNeteaseMusic/issues/22)


## 许可

The MIT License