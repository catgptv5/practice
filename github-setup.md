# GitHubとの連携手順

## 既存のリポジトリをGitHubにプッシュする方法

GitHubでリポジトリを作成したら、以下のコマンドを実行します：

```bash
# リモートリポジトリを追加（URLは実際のGitHubリポジトリURLに置き換えてください）
git remote add origin https://github.com/あなたのユーザー名/web-adventure.git

# メインブランチの名前を確認（最近のGitHubはmainがデフォルト）
git branch -M main

# ローカルリポジトリをGitHubにプッシュ
git push -u origin main
```

## 注意事項

1. 初めてGitHubにプッシュする場合は、認証が必要です。
   - HTTPSを使用する場合：GitHubのユーザー名とパスワード（またはトークン）が必要
   - SSHを使用する場合：事前にSSH鍵の設定が必要

2. GitHubのパーソナルアクセストークンを使用する場合（2021年8月以降、パスワード認証は非推奨）：
   - GitHubの設定 → Developer settings → Personal access tokens から生成
   - 少なくとも「repo」スコープを選択

## プッシュ後の確認

プッシュが成功したら、GitHubのウェブサイトでリポジトリを開き、ファイルがアップロードされていることを確認しましょう。

## 以降の冒険の保存方法

新しい進捗があるたびに以下のコマンドを実行します：

```bash
git add .
git commit -m "ミッション名：達成した内容"
git push
``` 