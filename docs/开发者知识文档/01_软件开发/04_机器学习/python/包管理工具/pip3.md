## 网站

[PyPI](https://pypi.org/)

## 常用命令

```bash
pip3 freeze > requirement.txt
```

| 类别                 | conda                  | pip                            |
| ---------- | ---------------------- | ------------------------------ |
| 管理       | 二进制                 | wheel 或源码                   |
| 需要编译器 | no                     | yes                            |
| 语言       | any                    | Python                         |
| 虚拟环境   | 支持                   | 通过 virtualenv 或 venv 等支持 |
| 依赖性检查 | yes                    | 屏幕提示用户选择               |
| 包来源     | Anaconda repo 和 cloud | PyPi                           |


## problems

### Retrying (Retry(total=4, connect=None, read=None, redirect=None, status=None)) after connection broken by ‘SSLError(SSLCertVerificationError(1, ‘[SSL: CERTIFICATE_VERIFY_FAILED] certificate verify failed: self signed certificate in certificate chain(_ssl.c:1076)’))’: /simple/lxml/

我在执行pip3 install package_name 的时候遇到了以上错误，搜了全网，以下方式亲测有效

执行 pip3 install --trusted-host pypi.org --trusted-host files.pythonhosted.org package_name

其中package_name是所需要下载的三方包

