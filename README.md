# WINGs_git_practice
WINGs2021のGitHub勉強会の練習用

## 概要
- 個人でGit・GitHubを使う
- チームでGitHubを使う

## 目標
- VScodeを使って、gitの操作に慣れる。具体的には、addとcommitの2つを理解する。
- コンフリクトを解消する。

gitのバージョンによって、初期ブランチの名前がmasterもしくはmainになりますが、ここでは最新版のmainに統一します。

## 内容
研究室のメンバー紹介についての記事を書くことを通して、Git・GitHubを学ぶ。
大まかな流れは次のようである。

1. 自己紹介 (公開されて良ければ本名で)
2. 家族紹介 (仮名で)
3. 研究室メンバー紹介 (自己紹介の名前を見て)

ファイル名は原則、'name.md'で統一する。コンフリクトを起こすため。
例えば、あなたの名前がskosakaならファイル名は'skosaka.md'とする。

## 自己紹介 個人編
- ローカルレポジトリを作成する。'git init'
- mainブランチにて、'myname.md'ファイルを作成する。
- 自己紹介、名前、身長、体重の順に3回程度コミットする。 'git add' 'git commit' (前後で'git status'すると状態を確認できる。)
- mainブランチに移動する。 'git checkout main'
- mainブランチにmyfamilyブランチをマージする。 'git merge myfamily'
- (myfamilyブランチを削除する。 'git branch -d myfamily')

## 自己紹介 個人編
- GitHubにてリモートリポジトリをself_introductionという名前で作成する。
- 個人のリモートリポジトリに登録する。 'git remote add origin URL' (前後で'git remote'すると状態を確認できる。)
- ローカルリポジトリにリモートリポジトリを反映する。 'git fetch origin main' + 'git merge origin/main' or 'git pull origin main'
- リモートリポジトリにローカルリポジトリを反映する。 'git push origin main'
- GitHubを確認する。

## 家族紹介 個人編
- myfamilyブランチを切る。 'git branch myfamily' + 'git checkout myfamily' or 'git checkout -b myfamily'
- myfamilyブランチにて、自己紹介と同様にコミットを行う。
- リモートリポジトリにローカルリポジトリを反映する。 'git push myfamily' (多分追跡されているはず)
- GitHubにてプルリクエストを送信する。
- GitHubにてリクエストを承認してマージする。

## 研究室メンバー紹介 チーム編
- ローカルリポジトリにリモートリポジトリを反映し、最新の状態にする。 'git pull'  (多分追跡されているはず)
- mynameブランチを切る。 'git branch myname'
- 個人のリモートリポジトリを削除する。  'git remote rm origin'
- 研究室のリモートリポジトリに登録する。 'git remote add origin URL' (前後で'git remote'すると状態を確認できる。)
- ローカルリポジトリにリモートリポジトリを反映する。 'git fetch origin main' + 'git merge origin/main' or 'git pull origin main'
- リモートリポジトリにローカルリポジトリを反映する。 'git push origin myname'
- リモートリポジトリにローカルリポジトリを反映する。 'git push myfamily' (多分追跡されているはず)
- GitHubにてプルリクエストを送信する。
- GitHubにてリクエストを承認してマージする。

## 


## 他己紹介

## 参考記事
### Gitコマンド 実践練習フロー
https://qiita.com/thinkalot/items/817079a952b5f145dbc7
### Git with VScode
https://qiita.com/jesus_isao/items/63557eba36819faa4ad9
### 'git pull'とは
https://qiita.com/wann/items/688bc17460a457104d7d
