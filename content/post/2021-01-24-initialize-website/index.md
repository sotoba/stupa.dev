---
title: "2021-01-24 Hugoで静的サイトを生成する"
categories:
  - blog
tags:
  - hugo
slug: 2021-01-24-initilalize-website
date: 2021-01-24T22:47:02+09:00
draft: false
---

## やったこと

- ドメイン取得
- hugoのセットアップ
  - https://gohugo.io/getting-started/quick-start/
- テーマの選択と設定
  - https://docs.stack.jimmycai.com/getting-started
- Netlifyへのデプロイ
  - https://gohugo.io/hosting-and-deployment/hosting-on-netlify/
- DNS設定(Google Domains)
  - Aレコード設定
  - CNAMEレコード設定

## つまったところ

- taxonomiesの概念がそもそもよくわかってなかった
  - https://gohugo.io/content-management/taxonomies/
  - とりあえず既定のcaterogryとtagで最低限の分類はできそう
- Netlify DNSを使わずにGoogle Domainsにドメインの設定をする場合、Aレコードに設定する値がわからなかった
  - https://docs.netlify.com/domains-https/custom-domains/configure-external-dns/#configure-an-apex-domain
  - Google DomainsはルートドメインへのALIASレコード設定ができないので、NetlifyロードバランサーのIPアドレスを決め打ちで設定する(いいのか?)
- AWS Route53でDNSレコード管理しようかと思ったけどDNSSECの解除やらなんやらがダルすぎてやめた
- アバター画像をどこに置いたらいいのかよくわからんかった
  - https://github.com/CaiJimmy/hugo-theme-stack/issues/27
  - ドキュメントをログインが必要なサービスに置くのやめてくれ

## 次にやること

- フォントが簡体字系になっているので日本語フォントを適当に探す
- ブランチ運用考える
