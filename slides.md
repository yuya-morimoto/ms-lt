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

<!-- =============== -->
<!-- 1ページ目 -->
<!-- =============== -->

# MicroService For 個人開発

暇だったので Slidev 使ってみた

<div class="pt-12">
  <span @click="$slidev.nav.next" class="px-2 py-1 rounded cursor-pointer" hover="bg-white bg-opacity-10">
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

<!-- =============== -->
<!-- 2ページ目 -->
<!-- =============== -->

# 目次

- 自己紹介
- Monolithic Architecture とは
- MicroService Architecture とは
- BFF パターン とは

---

<!-- =============== -->
<!-- 3ページ目 -->
<!-- =============== -->

# 自己紹介

- 名前：森本悠矢(Lv.23)
- 所属：Web 開発 5G - AirMate(BE,FE を少々)
- 趣味：開発・将棋(居飛車党)・ランニング?
- 最近興味ある技術： [Earthly](https://earthly.dev "Earhly"), [Bazel](https://bazel.build/?hl=en "Bazel")

## ![Icon](/sisyo.png)

---

<!-- =============== -->
<!-- 4ページ目 -->
<!-- =============== -->

# Monolithic Architecture とは

  <img src="/public/monolithic.png">

<style>
  img {
    max-height: 400px;
    margin: 0 auto;
  }
</style>

---

<!-- =============== -->
<!-- 4ページ目 -->
<!-- =============== -->

# Microservice Architecture とは

  <img src="/public/microservice.png">

<style>
  img {
    max-height: 400px;
    margin: 0 auto;
  }
</style>

---

<!-- =============== -->
<!-- 5ページ目 -->
<!-- =============== -->

# BFF パターン とは

  <img src="/public/microservice-bff.png">

<style>
  img {
    max-height: 400px;
    margin: 0 auto;
  }
</style>

---

<!-- =============== -->
<!-- 6ページ目 -->
<!-- =============== -->

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

<style>
  table {
    font-size: 12px
  }
  td {
    font-size: 12px
  }
</style>

---

<h1>以上</h1>

<style>
  h1 {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
  }
</style>
