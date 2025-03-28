# [日本語] Debian Almquist Shell (dash) who コマンド: ユーザーのログイン情報を表示する

## Overview
`who` コマンドは、システムに現在ログインしているユーザーの情報を表示します。このコマンドを使用することで、誰がシステムにアクセスしているかを簡単に確認できます。

## Usage
基本的な構文は以下の通りです。

```
who [options] [arguments]
```

## Common Options
- `-a`: すべての情報を表示します。
- `-b`: 最後のシステムブート時間を表示します。
- `-q`: ログインしているユーザーの名前と数を簡潔に表示します。

## Common Examples
以下に、`who` コマンドのいくつかの実用的な例を示します。

### 現在のログインユーザーを表示
```
who
```

### すべての情報を表示
```
who -a
```

### 最後のシステムブート時間を表示
```
who -b
```

### ログインしているユーザーの数を表示
```
who -q
```

## Tips
- `who` コマンドは、システムの監視やトラブルシューティングに役立ちます。
- 定期的に `who` を実行して、システムのセキュリティを確認することをお勧めします。