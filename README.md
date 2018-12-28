# Angular - overview
ここではAngularに関する歴史にも軽く触れます。
誕生当初AngularJSとして作成されましたが、そのバージョンのものはアーキテクチャがAngularとは違う為（互換性もない）、Angularの情報だけを取り違えずに仕入れる事ができるようにする為の予備知識が必要な為です。

## 歴史
- 2012年 `AngularJS`として誕生。ver.1
- 2016年 `Angular`に名称変更。アーキテクチャが一新された。ver.2
  - 以降、Angular/AngularJSで情報が混在している、Angularの情報を調べる際は以下に留意する
    - `Angular`/`Angular 2`と表記されている情報を確認する
    - `$scope`, `ng-`（ハイフン有り）などの記述はAngularJSの方
- 2017年 ver.4（ver.3はスキップされた）
- 2018年 ver.5

## 特徴
- Google社製のフレームワーク
- ライセンスはMIT、商用利用可能
- SPA（Single Page Application）を実現するJavaScriptフレームワークの1つ
- MVW(Model View Whatever)アーキテクチャなので以下のようなアーキテクチャの実現も可能
  - MVC(Model Veiw Controller)
  - MVVM（Model View ViewModel）
- MEAN（MongoDB, Express, Angular, Node.js）のスタックの一角
- WEBアプリケーション開発でフルスタック
  - データバインディング、ルーティング、テンプレート機能など必要なものが一通り揃っている
  - 標準機能だけで十分開発できる
  - 学習コストは高い

## 仕様
- TypeScript（JavaScriptに型定義やES6文法などを加えた言語）を使用する
  - TypeScriptで作成したスクリプトをES5のJavaScriptに変換してブラウザで表示させる
- 入力フィールド/表示フィールド/モデルの双方向バインディングに対応
- Ajaxなどの非同期イベント処理ライブラリとして[RxJS](https://rxjs-dev.firebaseapp.com/)を採用
- UI部品をサポートする[Angular Material](https://material.angular.io/)が公開されている

# Angular環境作成

nodejsなどなどが必要なので先にインストールする
## node.jsインストール
複数バージョンの切り替えができるように以下の順でインストール
1. Homebrew
2. nodebrew
3. nodejs

### Homebrewインストール
[公式サイト](https://brew.sh/index_ja)
> /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
> このスクリプトをターミナルに貼り付け実行して下さい。

### nodebrew
```sh
# インストール
$ brew install nodebrew
# 確認
$ nodebrew -v
# 設定
$ nodebrew setup
```
表示されるPATH（`export PATH=$PATH:$HOME/.nodebrew/current/bin`)を`~/.zshrc`に登録する。

### node.js
```sh
# 安定版インストール
$ nodebrew install-binary stable
# インストールされている一覧表示
$ nodebrew ls
# current: が古い場合は使用バージョン入れ替え
$ nodebrew use 10.15.0
# 確認
$ node -v
```

## Angular CLI
[公式](https://cli.angular.io/)
どのIntelliJ IDEAプロジェクトでも使用できるように、グローバルにインストールする必要がある
```sh
$ npm install -g @angular/cli
```

## Angular プロジェクト作成
```sh
# プロジェクトフォルダを作成するディレクトリに移動
$ cd ~/project
# プロジェクト作成
$ ng new test-app
```

## IntelliJ でAngularプロジェクトを更新する
別にエディタは何でもいいけどIntelliJ慣れてるのでそれで開く。
### アプリケーション起動
```sh
# アプリケーションディレクトリに移動
$ cd ~/project/test-app
# アプリケーション起動
$ ng serve
```

### ブラウザで表示
[http://localhost:4200](http://localhost:4200)

後はhtmlファイルなどを更新すると保存したタイミングで自動リコンパイルされて表示も自動更新される

## このプロジェクトのベース
以下サイトの前半に従いAngular CLIで作成したアプリケーションを更新すると当該プロジェクトが出来上がる
[Angular入門](http://www.tohoho-web.com/ex/angular.html)


# 元からついてたREADMEは以下

This project was generated with [Angular CLI](https://github.com/angular/angular-cli) version 7.1.4.

## Development server

Run `ng serve` for a dev server. Navigate to `http://localhost:4200/`. The app will automatically reload if you change any of the source files.

## Code scaffolding

Run `ng generate component component-name` to generate a new component. You can also use `ng generate directive|pipe|service|class|guard|interface|enum|module`.

## Build

Run `ng build` to build the project. The build artifacts will be stored in the `dist/` directory. Use the `--prod` flag for a production build.

## Running unit tests

Run `ng test` to execute the unit tests via [Karma](https://karma-runner.github.io).

## Running end-to-end tests

Run `ng e2e` to execute the end-to-end tests via [Protractor](http://www.protractortest.org/).

## Further help

To get more help on the Angular CLI use `ng help` or go check out the [Angular CLI README](https://github.com/angular/angular-cli/blob/master/README.md).
