## 開発手順書に書く内容

### 1.環境構築編

1. VSCode のインストール
2. git のインストール
3. Docker Desktop のインストール
   - Mac の場合
   - Windows の場合
     - WSL について記述する必要がある
4. git hub から clone

### 2.開発の流れ

0.  必要となる知識

以下のそれぞれの概要を紹介する(公式サイトのリンクも貼る)

- git
- Docker
- TypeScript(JavaScrip)
- Next.js
- React
- chakra-UI
- Firebase
- vercel

1. 開発の流れ
   - Github flow
   - ISSUE → WIP → push → review (→ push → review)\* n → merge
2. ISSUE を立てる
3. ## 開発フェーズ
# unipp 環境構築手順書

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
