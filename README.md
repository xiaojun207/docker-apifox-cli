# docker for apifox-cli
Apifox CLI 命令行镜像运行

## Apifox CLI 命令行运行
Apifox CLI 主要用来以命令行方式运行 Apifox 的 测试用例或测试套件。

## 快速启动

```
docker run --rm -v /data/apifox-cli.json:/data/apifox-cli.json  xiaojun207/apifox-cli:latest apifox run /data/apifox-cli.json -r cli,html,json -n 100
```
* 其中apifox-cli.json文件为，在 【Apifox】 ->【测试用例】和【测试套件】-> “导出”

## apifox-cli 参数说明
```
通过指定 Apifox 测试用例或测试套件的 URL 或 文件路径运行测试

Options:
  -r, --reporters [reporters]           指定测试报告类型, 支持 cli,html,json (default: ["cli"])
  --out-dir <outDir>                    输出测试报告目录，默认为当前目录下的 ./apifox-reports (default: "./apifox-reports")
  --out-file <outFile>                  输出测试报告文件名，不需要添加后缀，默认格式为 apifox-report-{当前时间戳}-0 (default: "apifox-report-2022-07-27-21-06-35-895-0")
  -n, --iteration-count <n>             设置循环次数
  -n, --iteration-count <n>             设置循环次数
  -d, --iteration-data <path>           设置用例循环的数据 (JSON 或 CSV)
  --external-program-path <path>        指定 [外部程序] 的所处文件路径，默认值为命令当前执行目录
  --database-connection <path>          指定 [数据库配置] 的所处文件路径，使用 URL 测试的时候必须指定
  --ignore-redirects                    阻止 Apifox 自动重定向返回 3XX 状态码的请求
  --silent                              阻止 Apifox CLI 输出到控制台
  --color <value>                       开启/关闭控制台彩色输出 (auto|on|off) (default: "auto")
  --delay-request [n]                   指定请求之间停顿间隔 (default: 0)
  --timeout-request [n]                 指定接口请求超时时间 (default: 0)
  --timeout-script [n]                  指定脚本预执行/后执行接口运行超时时间 (default: 0)
  -k, --insecure                        关闭 SSL 校验
  --ssl-client-cert-list <path>         指定客户端证书配置路径 (JSON)
  --ssl-client-cert <path>              指定客户端证书路径 (PEM)
  --ssl-client-key <path>               指定客户端证书私钥路径
  --ssl-client-passphrase <passphrase>  指定客户端证书密码 (for protected key)
  --ssl-extra-ca-certs <path>           指定额外受信任的 CA 证书 (PEM)
  --verbose                             显示所有接口请求的详细信息
  -h, --help                            display help for command

```


## 更多参数，参考
https://www.apifox.cn/help/cli/#%E5%AE%9E%E6%97%B6%E8%BF%90%E8%A1%8C%E5%9C%A8%E7%BA%BF%E6%95%B0%E6%8D%AE
