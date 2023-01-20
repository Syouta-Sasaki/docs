---
title: lock
long_title : lock ステートメント
summary: 現在のオブジェクトに対する相互排他ロックをします
---
### 定義
名前空間:Alice / アセンブリ : Losetta.Runtime.dll / サポート: AliceScript1

現在のオブジェクトに対する相互排他ロックをします

```cs title="AliceScript"
namespace Alice;
void lock(variable item);
```

|引数| |
|-|-|
|`item`|ロックする変数|

### 説明
現在のオブジェクトに対する相互排他ロックを取得し、ブロックを実行してからロックを開放します。
ロックが保持されている間、ロックを保持するスレッドではロックを再度取得し、解放することができます。他のスレッドはブロックされてロックを取得できず、ロックが解放されるまで待機します。
`lock`ステートメントを使うと、1つのスレッドがそのオブジェクトに排他的にアクセスできるように確保できます。
`lock`ステートメントの形式は次のようになります。

```cs title="AliceScript"
lock(x)
{

}
```
この時、`x`は変数を表します。

### 例
以下は、`delay`関数を使用してプログラムを10秒停止します。

```cs title="AliceScript"
delay(10000);
```