---
title: Except
long_title : array.Except
summary: 現在の配列と指定された配列の差集合を取得します
---
### 定義
名前空間:Alice / アセンブリ : Losetta.Runtime.dll / サポート: AliceScript2.2

現在の配列と指定された配列の差集合を取得します

```cs title="AliceScript"
namespace Alice;
array Except(array other);
```

|引数| |
|-|-|
|`other`|差集合を求めるもう一方の配列|

|戻り値| |
|-|-|
|`array`|現在の配列と`other`の差集合|

### 例
以下は、`1`、`2`の含まれる配列と`2`、`3`の含まれる配列の差集合を求めます。

```cs title="AliceScript"
var a = [1,2];
var b = [2,3];
print(a.Except(b)); // 出力例 : [1,3]
```