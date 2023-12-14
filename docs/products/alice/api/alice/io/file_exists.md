---
title: file_exists
summary: 指定したファイルが存在するかどうかを確認します
date : 2021-07-28
---
### 定義
名前空間:Alice.IO / アセンブリ : Losetta.Runtime.dll / サポート: AliceScript1

属性: 関数

指定したファイルが存在するかどうかを確認します。

```cs title="AliceScript"
namespace Alice.IO;
public bool file_exists(string path);
```

|引数| |
|-|-|
|`path`|確認するファイルへのパス|

|戻り値| |
|-|-|
|`bool`|`path`に既存のファイルが存在し、かつ必要なアクセス許可を持っている場合は`true`、それ以外の場合は`false`。|

### 説明
この関数は`path`にファイルが存在し、かつ必要なアクセス許可を持っている場合は`true`を返します。また、`path`が正しくないパスまたは長さが0の文字列、`null`の場合にも`false`を返します。さらに、呼び出し元が指定したファイルを読み取るためのアクセス許可を持っていない場合、例外は発生せず`false`を返します。

この関数を呼び出した後、ファイルに対して別の操作(ファイルの削除など)を実行する場合、実行する間に別のプロセスがファイルに何らかの操作を行う可能性があることにご注意ください。

`path`には、相対パスと絶対パスのどちらを指定することもできます。
相対パスを指定した場合、カレントディレクトリからの相対パスとして解釈します。

`path`がディレクトリを表す場合、この関数は`false`を返します。
ディレクトリの存在を確認するためには、`directory_exists`を使用してください。
### 例
次の例では、`test.txt`が存在するかどうかを確認します。

```cs title="AliceScript"
using Alice.IO;

bool exists = file_exists("test.txt");

if(exists)
{
    print("ファイルは存在します");
}
```