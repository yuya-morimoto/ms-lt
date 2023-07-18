---
theme: seriph
background: /background.jpg
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Slidev First Slide

  Learn more at [Sli.dev](https://sli.dev)
drawings:
  persist: false
transition: slide-left
title: MicroService For 個人開発
hideInToc: true
---

# MicroService For 個人開発

暇だったのでついでに Slidev 使ってみた

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-purple bg-opacity-10">
    Press Space for next page <carbon:arrow-right class="inline"/>
  </span>
</div>

<div class="abs-br m-6 flex gap-2">
<a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub"
    class="text-xl slidev-icon-btn opacity-50 !border-none !hover:text-white">
<carbon-logo-github />
</a>

</div>

---

# 目次

- 自己紹介
- アーキテクチャについて
  - Monolithic Architecture とは
  - Microservice Architecture とは
  - BFF パターン とは
  - 比較
- 個人開発について
  - 個人開発やってる理由・目的
  - システム構成
  - Microservice 採用してみたメリデメ
  - 今回の推し技術
- 最後に

---

# 自己紹介

- 名前：森本悠矢(Lv.23)
- 所属：Web 開発 5G - BE,FE を少々
- 趣味：開発・将棋(居飛車党)・ランニング?
- ハマっていること：Vim(Neovim)
- 最近興味ある技術： [Earthly](https://earthly.dev "Earhly"), [Bazel](https://bazel.build/?hl=en "Bazel")

## ![Icon](/sisyo.png)

---

<h1 class="abs-center">アーキテクチャについて</h1>

---

# Monolithic Architecture とは

  <img src="/public/monolithic.png" class="img-center">

---

# Microservice Architecture とは

  <img src="/public/microservice.png" class="img-center">

---

# BFF パターン とは

  <img src="/public/microservice-bff.png" class="img-center">

---

# 比較

<table>
    <thead>
        <tr>
            <th></th>
            <th>Monolithic</th>
            <th>Microservice</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <th scope="row">設計</th>
            <td>単一のコードベースでAPIも少ない<br/>比較的設計が容易</td>
            <td>相互通信する独立したコンポーネントでAPIも多い<br/>設計は複雑化</td>
        </tr>
        <tr>
            <th scope="row">データ整合性</th>
            <td>同一プロセス・共通DBを使用するため整合性が取りやすい</td>
            <td>サービス毎に別プロセス、別DBを使うので整合性が取りにくい</td>
        </tr>
        <tr>
            <th scope="row">リソース管理</th>
            <td>共通コードの管理がしやすい<br/>デプロイ単位が大きくテストやデプロイに時間がかかる</td>
            <td>リポジトリが複数になり管理しにくい(Monorepoで一元化)<br/>デプロイ単位が小さくテストやデプロイ時間短縮</td>
        </tr>
        <tr>
            <th scope="row">スケーリング</th>
            <td>細かいスケーリングが出来ない</td>
            <td>機能毎にスケーリングが可能(認証のみスケールアップする等)</td>
        </tr>
        <tr>
            <th scope="row">技術(言語・FW)</th>
            <td>基本的に1言語&自由な言語・FW</td>
            <td>機能毎に自由に選定可能&基本的に軽量FW&<br/>通信速度のためgRPC等扱えると良い&柔軟性あり</td>
        </tr>
        <tr>
            <th scope="row">コスト</th>
            <td>比較的抑えめ</td>
            <td>プロセス(コンテナ)が増えコストがかかりやすいが、細かいスケーリングやFaaSを混ぜて抑えることも可能そう</td>
        </tr>
    </tbody>
</table>

---

<h1 class="abs-center">個人開発について</h1>

---

# 個人開発やってる理由・目的

- 要領悪い人間
  - 1.なんかこの技術おもろそう気になる
  - 2.ドキュメント読む・チュートリアルする
  - 3.理解度浅い
  - 4.なんか作るか
- 0-1 での新規開発が好き

---

# システム構成

  <img src="/public/my-system.png" class="img-center">

---

# Microservice 採用してみたメリデメ

- メリット
  - 技術の幅が広がりやすい
  - 1 度の開発で複数の技術使える(Swift, TCA, Go, Nest, Pulumi あたりは初戦)
  - MicroService \* BFF の体験
  - 技術への飽きが来にくい
- デメリット
  - 初期段階での設計辛い
  - コストかかりそう...

---

# 今回の推し技術

- Pulumi
  - プログラミング言語で IaC 組める
- SwiftUI \* The Composable Architecture
  - Redux(Flux)とほとんど同じ考え方で状態管理できる
- CloudRun で Sidecars 可能に(2023/05 くらいから)

---

<h1 class="abs-center">最後に</h1>

---

<h1 class="abs-center">好きな技術使いましょう</h1>

---

<h1 class="abs-center">以上</h1>
