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
[local gas]$ cp -R template [project_name]
[local gas]$ cd [project_name]
## GASプロジェクト作成
### 通常
[local project_name]$ npm run clasp create -- --title $(basename $(pwd)) --type standalone --rootDir src/
### スプレッドシート
[local project_name]$ npm run clasp create -- --title $(basename $(pwd)) --type standalone --rootDir src/
```

## 開発コマンド

### コード整形

```
[local project_name]$ npm run lint
```

### プロジェクト作成

```
[local project_name]$ npm run clasp create  -- --title [project title] --type [project tyoe] --rootDir src/
```

### プロジェクトのclone

```
[local project_name]$ npm run clasp clone [project] -- --rootDir src/
```

### スクリプトエディタをブラウザで開く

```
[local project_name]$ npm run open
```

### コードをpush

```
[local project_name]$ npm run push
```

### コードをpull

```
[local project_name]$ npm run pull
```

### その他claspコマンドの実行

```
[local project_name]$ npm run clasp comand_name xxx
# --option 形式のオプション付きの場合
[local project_name]$ npm run clasp comand_name xxx -- --option_a yyy --option_b zzz
```
