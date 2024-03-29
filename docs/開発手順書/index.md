# 開発手順書

## サマリ

unipp 開発のための手順書です。
以下の内容を内包しています。

1. 必要となる知識
2. unipp の個人開発環境の構築
3. 開発の手順
   - 開発フロー
     - Git 運用について
     - Issue/PullRequest ののラベル付けルール
   - コーディング規約
   - レビューについて

### 1. 必要な知識

## サマリ

- git
  - コードのバージョン管理のための管理のためのツール
  - 参考:https://backlog.com/ja/git-tutorial/
- Docker
  - unipp では環境構築のために利用している
  - docker を用いることで、OS に依存せずに開発できるようにしていうｒ
  - 参考:https://docs.docker.jp/
- TypeScript
  - JavaScript の上位互換であり、静的にコードをを解析するため、実行せずにエラーを検知可能で、バグの予防につながる
  - 参考:https://typescript-jp.gitbook.io/deep-dive/
- React
  - Meta(旧: facebook)が開発した UI 構築のための JavaScript ライブラリ
  - 参考:https://ja.reactjs.org/
- chakra-UI
  - React 向けの UI コンポーネントライブラリ
  - 参考:https://chakra-ui.com/
- Firebase
  - unipp では主に、4 つのサービスを利用している
    - Cloud Firestore
      - NoSQL 型の DB
      - アプリ内で用いるデータを保管
      - 参考:https://firebase.google.com/docs/firestore
  - Cloud Storage for Firebase
    - 写真や動画等の Raw データは Firestore で保存できないため、Cloud Storage で管理している
    - 参考: https://firebase.google.com/docs/storage
  - Firebase Authentication
    - ユーザのアカウント作成, ログイン認証などをを実装するために利用
    - 参考: https://firebase.google.com/docs/auth
  - vercel
    - unipp のデプロイ先
    - main ブランチにコードを push すると、自動でデプロイされるようになっている
    - 参考: https://vercel.com/
# 2. unipp 環境構築手順書

# サマリ

## 目的

- unipp の個人開発をを構築するための手順書です。

## 前提

- VScode をインストールしている
- git をインストールしている
- github アカウントを持っている
- unipp リポジトリへの権限を持っている

## 対象リポジトリ

- Unipp
  - https://github.com/ylab-dev/Unipp

# 開発環境構築手順

## 1.Docker-destop のインストール

### windows の場合

```
  windowsの場合はWSL2をインストールインストールしてから、Docker-desktopをインストールしてください
```

1. [WSL2](https://chigusa-web.com/blog/wsl2-win11/) のインストール
2. [Docker-desktop](https://www.docker.com/products/docker-desktop/) のインストール

### mac の場合

1. [Docker-desktop](https://www.docker.com/products/docker-desktop/) のインストール

## 2.リポジトリのクローン

VScode>Teriminal でターミナルを開き、以下のコマンドを入力する

```
git clone https://github.com/ylab-dev/Unipp.git
```

## サービスの構築

VScode>Teriminal でターミナルを開き、以下のコマンドを入力する

```
docker-compose build
docker-compose run --rm next yarn install
```

## コンテナの立ち上げ

```
docker-compose up
```

## 動作確認

web ブラウザ(google chrome 推奨)上で以下のページにアクセス

```
http://localhost:3000/review
```
# 3.開発手順

# 3.1 開発フロー

## サマリ

- 開発フロー
  - Git 運用について
    - Github flow
    - ISSUE → WIP → push → review (→ push → review)\* n → merge
  - Issue/PullRequest ののラベル付けルール
- コーディング規約
  - これ、どうしようかな
- レビューについて
  - とりま、だれかのレビューを受ける旨を書いてください
