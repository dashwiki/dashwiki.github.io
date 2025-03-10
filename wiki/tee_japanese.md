# [日本語] Debian Almquist Shell (dash) tee の使い方: 標準出力をファイルに書き込む

## 概要
`tee` コマンドは、標準入力を受け取り、それを標準出力に表示しつつ、指定したファイルにも書き込むことができるコマンドです。これにより、データをリアルタイムで確認しながら、同時にファイルに保存することができます。

## 使用法
基本的な構文は以下の通りです。

```bash
tee [オプション] [引数]
```

## 一般的なオプション
- `-a` または `--append`: 指定したファイルに追記します。デフォルトではファイルは上書きされます。
- `-i` または `--ignore-interrupts`: 割り込み信号を無視します。

## 一般的な例
以下に、`tee` コマンドのいくつかの実用的な例を示します。

### 例 1: 標準出力とファイルへの書き込み
```bash
echo "Hello, World!" | tee output.txt
```
このコマンドは "Hello, World!" を表示し、同時に `output.txt` に書き込みます。

### 例 2: ファイルに追記
```bash
echo "追加の行" | tee -a output.txt
```
このコマンドは "追加の行" を `output.txt` に追記します。

### 例 3: 複数のファイルに書き込み
```bash
echo "データ" | tee file1.txt file2.txt
```
このコマンドは "データ" を `file1.txt` と `file2.txt` の両方に書き込みます。

## ヒント
- `tee` コマンドを使用する際は、出力を確認しながらファイルに保存できるため、デバッグやログの取得に便利です。
- スクリプト内で `tee` を使用することで、処理の進行状況をリアルタイムで確認しながら、ログファイルに記録することができます。