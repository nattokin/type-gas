# GASローカル開発環境（TypeScript）

## 概要

- TypeScriptでのGASのローカル開発環境

## 環境構築

```
[local ~]$ cd path/to/type-gas
[local gas]$ npm install
```

### claspのログイン

出力されたURLにブラウザでアクセスして認証する

```
$ npm run clasp login
🔑  Authorize clasp by visiting this url:
https://accounts.google.com/o/oauth2/v2/auth?access_type=offline&scope=https%3A%2F%...
```

## 開発環境

- TypeScript
	- tslint
	- prettier
- モジュール
	- google-apps-script
- テスト
	- なし

## テンプレート利用方法

```
[local ~]$ cd path/to/type-gas
## シンボリックリンクのまま複製
[local gas]$ cp -R template {{project_name}}
## GASプロジェクト作成
[local project_name]$ npm run clasp create --title $(basename $(pwd)) --type standalone --rootDir ./src
```

## その他開発コマンド

### コード整形

```
[local ~]$ cd path/to/type-gas/{{project_name}}
[local project_name]$ npm run lint
```

### push

```
[local ~]$ cd path/to/type-gas/{{project_name}}
[local project_name]$ npm run push
## 以下でも可能
[local project_name]$ npm run clasp push
```

### スクリプトエディタを開く

```
[local ~]$ cd path/to/type-gas/{{project_name}}
[local project_name]$ npm run open
```

### その他claspコマンドの実行

```
[local ~]$ cd path/to/type-gas/{{project_name}}
[local project_name]$ npm run clasp xxx
```
