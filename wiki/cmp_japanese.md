# [日本語] Debian Almquist Shell (dash) cmp の使い方: ファイルの内容を比較する

## 概要
`cmp` コマンドは、2つのファイルをバイト単位で比較し、最初に異なるバイトの位置を表示します。ファイルが同一であれば、何も出力しません。

## 使用法
基本的な構文は次のとおりです。

```
cmp [オプション] [引数]
```

## 一般的なオプション
- `-l`: 異なるバイトの位置とその値をリスト表示します。
- `-s`: 出力を抑制し、ファイルが同一かどうかだけを返します。
- `-i`: 指定したバイト数を無視して比較します。

## 一般的な例
以下は `cmp` コマンドの実用的な例です。

### 例1: 2つのファイルを比較する
```bash
cmp file1.txt file2.txt
```
このコマンドは、`file1.txt` と `file2.txt` を比較し、最初に異なるバイトの位置を表示します。

### 例2: 異なるバイトの位置をリスト表示する
```bash
cmp -l file1.txt file2.txt
```
このコマンドは、異なるバイトの位置とその値をリスト形式で表示します。

### 例3: ファイルが同一かどうかを確認する
```bash
cmp -s file1.txt file2.txt
```
このコマンドは、`file1.txt` と `file2.txt` が同一であるかどうかを確認し、出力を抑制します。

## ヒント
- `cmp` コマンドは、バイナリファイルの比較にも使用できます。テキストファイルだけでなく、画像や音声ファイルなども比較可能です。
- 大きなファイルを比較する場合、`-s` オプションを使用して、結果を簡潔に確認することができます。
- 異なるバイトの詳細を確認したい場合は、`-l` オプションを活用すると便利です。