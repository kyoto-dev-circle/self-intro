# self-intro

Kyoto Dev Circle の Phase 0 用リポジトリです。
自己紹介ファイルを Pull Request で追加しながら、Git/GitHub を使った共同開発の基本を練習します。

はじめての人は、まず [docs/git-guide.md](docs/git-guide.md)（Git/GitHub はじめてガイド）を読んでください。

## ルール

- `main` ブランチに直接 push はできません（保護されています）。
- 作業は必ず Issue から始め、ブランチを作って Pull Request を出します。
- 例外として、Claude が行う README と docs/ の更新は、Issue を作らず Pull Request だけで行います。ブランチ名は `docs/内容`（例：`docs/update-task-board`）にし、変更の理由は Pull Request の本文に書きます。マージは長谷川のバイパスで行います。
- 作業の進み具合は、タスクボード（上部の「Projects」タブ →「Kyoto Dev Circle タスクボード」）で管理します。ボードに置くのは Issue のカードだけで、Pull Request には Projects を設定しません。
- マージには、もう1人のレビュー（Approve）が必要です。
- Approve の後に新しいコミットを push すると、承認は取り消されます。直したら、もう一度レビューを頼みます。
- マージ方法は「Merge pull request」だけが使えます（Squash and merge と Rebase and merge は設定で使えなくしています）。
- 例外として、長谷川（maintainers チーム）は Pull Request に限り、Approve なしでマージできます（バイパス）。バイパスは、代表の長谷川が自分の判断で使ってよいことにしています。main への直接 push はできません。
- ブランチ名は `feature/#Issue番号-内容` の形にします（例：`feature/#2-add-hayato`）。
- コミットメッセージは `feat:`、`fix:`、`docs:` などで始めます。

## やること

### 1. リポジトリを自分のPCにコピーする

```
git clone https://github.com/kyoto-dev-circle/self-intro.git
cd self-intro
```

### 2. 作業用のブランチを作る

```
git switch -c feature/#Issue番号-add-自分の名前
```

### 3. 自己紹介ファイルを作る

`members/` フォルダに `自分のGitHubユーザー名.md` を作り、次の内容を書きます。
`members/` フォルダがまだなければ、VS Code の「新しいファイル」で `members/自分のGitHubユーザー名.md` と入力すると、フォルダも一緒に作られます（Git は空のフォルダを記録しないので、誰かのファイルがマージされるまでフォルダは見えません）。

```
# 名前（ハンドルネームでOK）

- 学部・学年：
- 趣味：
- この開発で身につけたいこと：
```

### 4. コミットして push する

```
git add .
git commit -m "feat: 自己紹介を追加"
git push -u origin feature/#Issue番号-add-自分の名前
```

### 5. Pull Request を出す

GitHub のリポジトリページに出る「Compare & pull request」を押し、テンプレートに沿って書いて作成します。
本文に `Closes #Issue番号` と書くと、マージ時に Issue が自動で閉じます。

### 6. レビューしてマージする

相手の PR を読み、コメントを書いて「Approve」します。Approve されたら、PR を出した本人が「Merge pull request」でマージします。

### 7. 最新の main を取り込む

```
git switch main
git pull
```

## 次の練習：コンフリクト

2人で同時に、この README の下にある「メンバー一覧」の同じ行を別々に書き換えて PR を出し、コンフリクトを起こして解消してみましょう。

## メンバー一覧

- （ここに名前を追加）
