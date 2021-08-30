# wower
wower可以帮你一步步编译安装0抽水xmrig挖矿程序，仅支持Debian和ubuntu！

## 安装

安装脚本和后台服务，根据提示输入“XMR钱包地址”、“矿池地址（例如：**mine.c3pool.com:15555**）”和“矿工名称”。

```
wget --no-check-certificate -qO wower.sh 'https://git.io/wower.sh' && chmod a+x wower.sh && ./wower.sh
```

## 使用
开启wower挖矿
```
systemctl start wower
```
重启wower
```
systemctl restart wower
```
停止wower挖矿
```
systemctl stop wower
```

## 设置
后续更改矿池等设置，可直接替换使用以下命令：

```
# 设置挖矿地址和端口
sed -i 's/"url": *"[^"]*",/"url": "挖矿地址:端口",/' $HOME/wower/config.json
# 设置钱包地址
sed -i 's/"user": *"[^"]*",/"user": "钱包地址",/' $HOME/wower/config.json
# 设置矿工名字
sed -i 's/"pass": *"[^"]*",/"pass": "矿工名字",/' $HOME/wower/config.json
# 开启后台模式
sed -i 's/"background": *false,/"background": true,/' $HOME/wower/config.json
```

## 捐赠
如果您觉得脚本对您有用，可以请我喝杯咖啡。
xmr捐助地址：
    82da8smo7MMeJ5baJ553RSZfDUWSfMjHQdmpP98aD4wpZNwArjKdMLDbGZYDqFvNoL75BiDdyTHxKNyijv9bsMmrM1k7rYw
