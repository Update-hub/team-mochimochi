﻿# life-card
人の人生を簡易的にビジュアライズするジェネレータ

## Demo

https://update-hub.github.io/team-mochimochi/

### 開発メンバー向け

#### ■ファイルの保存場所
開発中のファイルは  
ejsは「src/ejs/core/」または「src/ejs/component/」  
sassは「src/sass/core/」または「src/sass/component/」  
jsは「src/js/」  
画像は「src/image/」  
に保存すること

#### ■Gulpタスク


##### `gulp`
ローカルサーバーを立ち上げ、同時にブラウザ上に新しいタブを開き、ページを表示する。  
src内のファイルの変更を監視し、変更があった場合コンパイルや結合、圧縮をしつつdocsにコピーする。

##### `gulp reloadDocs`
docsディレクトリが強制的に更新される。src内のファイルをコンパイルや結合、圧縮をしつつdocsにコピーする。

#### ■JSの記述の統一

今回のチーム制作では以下のルールを採用する。

##### ・.jsファイル内の記述を即時関数```(function(){  ～  })();```で囲む。
変数の競合が怖いので即時関数を使う。  
ただし、output～()関数はグローバルに定義したいので、即時関数で囲まない。

##### ・jsファイル内の記述の末尾には```;(セミコロン)```をつける
ESLintエラーは無視する、エラーの予防のためなので最終的に適宜削除されます。

##### ・文字列リテラルを表すのは'シングルクォート'

##### ・必ず一度formatをかける

##### ・ESLintエラーが出ないように気を配る

ESLintに従った結果、index.jsに結合した際に問題が発生するなら、結合時の整合性を優先してエラーは無視する  
$やgoogleなどが定義されていない問題は下記参照https://docs.update.jp/dokyumento/ji-chu-zhi-shi/eslint

##### ・なるべくjQuery の DOM キャッシュでelementを指定して処理を行う

##### ・```'use strict'```は記述しない

**---このJSの記述の統一は暫定的なものです。問題・ご意見があれば、随時募集中です。---**

