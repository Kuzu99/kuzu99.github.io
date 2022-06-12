# React Getting Started

## Reactを始めてみよう

- [getting-started](https://ja.reactjs.org/docs/getting-started.html)

## コンテンツ
- [x] 実践チュートリアル
	- https://ja.reactjs.org/tutorial/tutorial.html
	- 実際に手を動かしながら学びたい人はチュートリアルからはじめましょう。
	- このチュートリアルでは React を使って三目並べゲームを作成します。
	- ゲーム作成に興味が無い方は飛ばそうと思うかもしれませんが、試してみてください。
	- ここで学ぶテクニックは全ての React アプリの基礎となることであり、習得することで React に関する深い理解が得られます。
- [ ] 一歩づつ進めるためのガイド
	- https://ja.reactjs.org/docs/hello-world.html
	- コンセプトからひとつひとつ学んでいきたい人はこちらのガイドからはじめていきましょう。
	- このガイドは章ごとに分かれていて、各章がそれまでに習ったことを上乗せする知識となっているため、余すことなく学ぶことができます。

## 実践チュートリアル

- Reactツールチェイン
	- Create React App
		- 新しいシングルページアプリケーション
	- Next.js
		- Node.jsでサーバーサイドでレンダーされるウェブサイト
	- Gatsby
		- 静的なコンテンツ中心のウェブサイト

### 環境構築 Create React App
- あなたのマシンに Node >= 14.0.0 及び npm >= 5.6 の環境が必要です。
	- brew: 3.5.1
	- nodebrew: 1.2.0
	- node: 18.3.0
	- npm: 8.11.0

```
$ brew update

$ brew --version
Homebrew 3.5.1
Homebrew/homebrew-core (git revision fe410c9e7f7; last commit 2022-06-12)
Homebrew/homebrew-cask (git revision 13eff273c6; last commit 2022-06-12)

$ brew install nodebrew

$ nodebrew -v
nodebrew 1.2.0

$ nodebrew ls-remote
v18.0.0   v18.1.0   v18.2.0   v18.3.0 ...

$ nodebrew install-binary latest

$ nodebrew use v18.3.0

$ nodebrew ls 
v18.3.0
current: v18.3.0

$ echo 'export PATH=$HOME/.nodebrew/current/bin:$PATH' >> ~/.zprofile

$ node -v
v18.3.0

$ npm -v
8.11.0
```

- tips
	- すでにnodeがbinaryなどでinstallしている場合
		- $which node で出てくるファイルを削除する

## プロジェクト作成
```
npx create-react-app my-app
cd my-app
npm start
```
- npxはパッケージランナーツール
- Create React App はフロントエンドのビルドパイプラインを構築する
- 内部では Babel と webpack を利用

```
Success! Created my-app at /Users/takumi/Development/githubIo/kuzu99.github.io/20220612171115/my-app
Inside that directory, you can run several commands:

  npm start
    Starts the development server.

  npm run build
    Bundles the app into static files for production.

  npm test
    Starts the test runner.

  npm run eject
    Removes this tool and copies build dependencies, configuration files
    and scripts into the app directory. If you do this, you can’t go back!

We suggest that you begin by typing:

  cd my-app
  npm start

Happy hacking!
```

## Reactとは
- React はユーザインターフェイスを構築するための、宣言型で効率的で柔軟な JavaScript ライブラリです。
- 複雑な UI を、「コンポーネント」と呼ばれる小さく独立した部品から組み立てることができます。

## 作業
- my-app
	- index.js
	- index.css
	- index.html
- https://codepen.io/gaearon/pen/aWWQOG?editors=0010
- このように配置