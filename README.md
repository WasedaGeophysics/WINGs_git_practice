# WINGs_git_practice
WINGs2021のGitHub勉強会の練習用

## 概要
- 個人でGit・GitHubを使う
- チームでGitHubを使う

## 目標
- VScodeを使って、gitの操作に慣れる。 'git add' 'git commit' 'git push' 'git pull'
- チーム開発におけるコンフリクトを解消する。
- 余力がある人は同様の操作をTerminalにて実施する。

# 内容
研究室のメンバー紹介についての記事を書くことを通して、Git・GitHubを学ぶ。
大まかな流れは次のようである。

1. 自己紹介 (公開されて良ければ本名で)
2. 家族紹介 (仮名で)
3. 研究室メンバー紹介 (自己紹介の名前を見て)

ファイル名は原則、'name.md'で統一する。コンフリクトを起こすため。
例えば、あなたの名前がskosakaならファイル名は'skosaka.md'とする。
なお、gitのバージョンによって、初期ブランチの名前がmasterもしくはmainになりますが、ここでは最新版のmainに統一します。

## 個人編
### 自己紹介 ローカルリモートリポジトリ
- ローカルレポジトリを作成する。'git init'
- mainブランチにて、'myname.md'ファイルを作成する。
- 自己紹介、名前、身長、体重の順に3回程度コミットする。 'git add' 'git commit' (前後で'git status'すると状態を確認できる。)

### 自己紹介 リモートリポジトリ
- GitHubにてリモートリポジトリをself_introductionという名前で作成する。ただし、README.mdファイルは作成しない。
- 個人のリモートリポジトリに登録する。 'git remote add origin URL' (前後で'git remote'すると状態を確認できる。)
- ローカルリポジトリにリモートリポジトリを反映する。 'git fetch origin main' + 'git merge origin/main' or 'git pull origin main'
- リモートリポジトリにローカルリポジトリを反映する。 'git push origin main'
- GitHubを確認する。

### 家族紹介 ブランチ
ブランチを切りまくって、家系図を作ります。
- myfamilyブランチを切る。 'git branch myfamily' + 'git checkout myfamily' or 'git checkout -b myfamily'
- myfamilyブランチから、fatherブランチを切る。 'git branch father'
- fatherブランチに移動する。 'git checkout father'
- fatherブランチにて、父親や父親の家族について.mdファイルを作成し、それぞれコミットする。
- myfamilyブランチに移動し、motherブランチを切る。 'git checkout myfamily' + 'git branch mother'
- motherブランチに関してもfatherブランチと同様の操作を行う。
- branchを確認する。 'git branch' (main, myfamily, father, motherの4つ)
- myfamilyブランチに移動する。 'git checkout myfamily'
- myfamilyブランチにfatherブランチをマージする。 'git merge father'
- myfamilyブランチにmotherブランチをマージする。 'git merge mother'
- リモートリポジトリにローカルリポジトリを反映する。 'git push myfamily' (多分追跡されているはず)
- GitHubにてプルリクエストを自分に送信する。
- GitHubにてリクエストを自分で承認してマージする。

## チーム編
## 研究室メンバー紹介 
- リモートリポジトリを複製し、ローカルリモートリポジトリを作成する。 'git clone URL'  ('git init'や'git remote add origin URL'が要らなくなる)
- ローカルリポジトリにリモートリポジトリを反映する。 'git fetch origin main' + 'git merge origin/main' or 'git pull origin main'
- リモートリポジトリにローカルリポジトリを反映する。 'git push origin myname'
- GitHubにてプルリクエストをタスク管理者のGitHubに送信する。
- GitHubにてリクエストをタスク管理者が承認してマージする。 (みんなが違う名前でファイル名を作成していれば、コンフリクトは発生しないはず。)
- みんなプルリクエストが完了したら、ローカルリポジトリにリモートリポジトリを反映し、最新の状態にする。 'git pull'  (多分追跡されているはず)
- 

## 


## 他己紹介

## 参考記事
### Gitコマンド 実践練習フロー
https://qiita.com/thinkalot/items/817079a952b5f145dbc7
### Git with VScode
https://qiita.com/jesus_isao/items/63557eba36819faa4ad9
### 'git pull'とは
https://qiita.com/wann/items/688bc17460a457104d7d
