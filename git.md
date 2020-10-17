## Gitに関するmemo
* clone
```
git clone -b <ブランチ名>or<タグ名>
```
***
* ブランチ移動or作成
```
git checkout -b <ブランチ名>
```
※ ブランチ名が存在しないと新規作成となる
***
* 変更を取り込む(pullする)
```
git fetch origin
git pull
```
※ git fetch originは差分のみをpullしたい場合のみ使う
***
* pushまでの流れ
1. ファイルを変更する
2. 変更したファイルをpushしたいリストに加える
```
git add <pushしたいファイル>
```
3. 変更内容のコメントをする
```
git commit -m "コミットメッセージ"
``` 
※ 複数行でコメントしたい場合、git commit -m "1行目" -m "2行目"・・・とする
4. pushする
```
git push -u origin <ブランチ名>
```
***
* tag確認
```
git tag
```
***
* commit履歴確認
```
git log
```
***
* commit取り消し
```
git revert <commitID>
```