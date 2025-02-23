# [日本語] Debian Almquist Shell (dash) true 使用法: 常に成功するコマンド

## Overview
`true` コマンドは、常に成功（終了ステータス 0）を返すシンプルなコマンドです。主にスクリプトやコマンドの条件分岐で、成功を示すために使用されます。

## Usage
基本的な構文は以下の通りです。

```sh
true [options] [arguments]
```

## Common Options
`true` コマンドには特にオプションはありません。常に成功を返すため、引数やオプションは無視されます。

## Common Examples

### 基本的な使用法
成功を示すために `true` を使用する基本的な例です。

```sh
true
```

### 条件分岐での使用
スクリプト内で条件分岐を行う際に、`true` を使って常に成功する条件を作成できます。

```sh
if true; then
    echo "これは常に実行されます。"
fi
```

### ループ内での使用
無限ループを作成する場合にも `true` を使用できます。

```sh
while true; do
    echo "このメッセージは無限に表示されます。"
done
```

## Tips
- `true` コマンドは、スクリプトのテストやデバッグ時に便利です。特定の条件を満たさない場合でも、スクリプトを途中で停止させたくないときに使用できます。
- 他のコマンドと組み合わせて、条件を常に成功させるためのプレースホルダーとして利用できます。