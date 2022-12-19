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
# 環境構築

## 目的

unipp で個人の PC に開発環境を構築する

## 前提

- github アカウントを持っている
- github の unipp リポジトリへの権限を付与されている

# 開発環境概要

### windows の場合

### mac の場合

## wsl のインストール

## Docker のインストール

## リポジトリのクローン

## サービスの構築

```
docker-compose build
docker-compose run --rm next yarn install
```

## コンテナの作成と立ち上げ

```
docker-compose up
```
