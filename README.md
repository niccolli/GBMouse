# GBMouse 

ゲームボーイ本体の部分

## ビルド手順

[giginet/gbdk](https://hub.docker.com/r/giginet/gbdk) を利用します。

```
$ docker pull giginet/gbdk
$ docker run -it --rm -v `pwd`:/gbdk giginet/gbdk /opt/gbdk/bin/lcc -o /gbdk/mouse.gb /gbdk/mouse.c
```

## カートリッジRAM

- 0xA000: 送信 (MBC→BLE)
- 0xA001: 受信 (BLE→MBC)
