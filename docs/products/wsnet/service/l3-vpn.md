---
title : L3VPN
summary : Layer3-VPN接続は、WSNETの基本サービスです。すべてのアカウントで使用できます。
date : 2024-04-12
---

### 概要
L3VPN接続サービスを使用すると、L3レベルでWSNETに接続でき、セキュアな通信環境を使用できます。

### 利用方法

1. サービスを使用する前に、WSNETへの加入が必要です。
2. 以降の接続方法については、[チュートリアル](../tutorial/index.md)をご覧ください。

### 注意事項

- 接続方式はOpenVPNまたはSoftEtherプロトコルのみとなります。
- ネットワーク内でDHCPサーバーを動作させることはできません。
- 使用者側のネットワークでブリッジ接続、モニタリング接続およびルーターを動作させることはできません。
- 非IPパケットはすべてDropされます。