# Database

## 初回クローン時

```
git clone git@github.com:ITProject2023-Twitter-clone/Database.git
cd Database
```

## docker

### コンテナ起動
```
docker compose up -d
```

### コンテナ終了
```
docker compose down
```

### コンテナ内に入るとき
```
docker container exec -it twitter-clone-db bash
```

## Postgresql

### ログイン
```
psql -U ユーザ名 -d データベース名
# パスワード入力
```

## ブランチ命名規則

参考サイト：[git-flow 図解](https://zenn.dev/yuki0410/articles/3360a6078d8e8c)

| ブランチ名 | 意図 | 派生元 | マージ先 |
| :-- | :-- | :-- | :-- |
| main | 現公開 | - | - |
| release | 次公開準備 | develop | main<br>develop |
| hotfix/* | 緊急修正 | main | main<br>develop |
| develop | 開発 | main | release |
| fix/* | 修正 | develop | develop |
| feature/* | 機能追加 | develop | develop |

`*` には操作対象となる名称を付与する．
