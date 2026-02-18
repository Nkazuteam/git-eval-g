# Git-Eval G ランク: Generalist

ターミナルと Git の基礎を身につけるランクです。

> **このランクは AI 利用禁止です。** 自分の手で叩いて覚えましょう。

## お題: 基本コマンドを使うスクリプトを書こう

ターミナルの基本コマンドを使って、一連の操作を行うスクリプトを書いてください。
`.ps1`（PowerShell）または `.sh`（Bash）のどちらでも OK です。

### やること

1. このリポジトリを clone する
2. `task.ps1` または `task.sh` を作成する
3. スクリプトの中で以下の操作を行う:
   - `mkdir` でフォルダを作成する
   - `cd` でそのフォルダに移動する
   - ファイルを作成する
   - ファイルの中身を表示する（`cat` / `Get-Content`）
   - ファイルをコピーまたは移動する（`cp` / `mv`）
   - ディレクトリの中身を一覧表示する（`ls` / `Get-ChildItem`）
4. ブランチを切って作業する（例: `git switch -c feature/my-task`）
5. commit して push する
6. GitHub 上で PR を作成する

### task.sh の例

```bash
#!/bin/bash
mkdir workspace
cd workspace
echo "Hello, Git-Eval!" > hello.txt
cat hello.txt
cp hello.txt hello_copy.txt
ls -la
```

### task.ps1 の例

```powershell
New-Item -ItemType Directory -Name workspace
Set-Location workspace
"Hello, Git-Eval!" | Out-File hello.txt
Get-Content hello.txt
Copy-Item hello.txt hello_copy.txt
Get-ChildItem
```

### 評価ポイント（100 点満点）

| チェック項目 | 配点 |
|---|---|
| `task.ps1` または `task.sh` が存在する | 20 |
| スクリプトの構文が正しい | 20 |
| ディレクトリ作成コマンドが含まれている | 10 |
| ファイル操作コマンドが含まれている | 10 |
| 一覧表示コマンドが含まれている | 10 |
| CRLF 改行が混入していない（.sh の場合） | 10 |
| コミットが 2 つ以上ある | 10 |
| コミットメッセージが意味のある内容 | 10 |

### 提出方法

push するだけ！ GitHub Actions が自動で評価して Discord に結果を通知します。
