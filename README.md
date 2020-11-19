# NLP2021 文書クラス（v0.4.0 2020-11-19）

## 概要

[言語処理学会第27回年次大会 (NLP2021)](https://www.anlp.jp/nlp2021/) 予稿集用 LaTeX 文書クラスです．[W3C 日本語組版の要件 (JLREQ)](https://www.w3.org/TR/jlreq/) に準拠することを目指した jlreq クラスをベースにしており，LaTeX による日本語組版で一般によく用いられる pLaTeX, upLaTeX, LuaLaTeX をサポートしています．

## 動作要件

* TeX フォーマット：LaTeX2e
* TeX エンジン：pLaTeX, upLaTeX, LuaTeX
* 依存クラス：[jlreq](https://www.ctan.org/pkg/jlreq)

推奨環境は **TeX Live 2017 以降**です．推奨環境であれば，追加でインストールする必要なものはありません．（それより古い環境では別途 jlreq を入手・インストールする必要があるかもしれません．いずれにせよ TeX Live 2017 以前のものには深刻な脆弱性が知られていますので，そのような環境をお使いの場合はアップデートを強く推奨します．）

## サンプル文書

本文書クラスには，仕上がりを確認するためのサンプル文書が付属しています．同文書は，そのままテンプレートとして用いられることも想定しています．

* ソース：[nlp2021-sample.tex](./nlp2021-sample.tex)
* PDF：[nlp2021-sample.pdf](./nlp2021-sample.pdf)

## 使い方

本文書クラスは，基本的に jlreq クラスの仕様をそのまま引き継いでいます．そのため，仕様の詳細は [jlreq のマニュアル](http://mirrors.ctan.org/language/japanese/jlreq/jlreq-ja.pdf)を参照してください．ただし，一般的なユーザ用コマンドや環境に関しては，pLaTeX の標準クラス (jclasses) や新ドキュメントクラス (jsclasses) とほぼ同様なので，基本的には何かを新しく学ぶ必要はないはずです．

### 文書クラス宣言とクラスオプション

LaTeX 標準の通り `\documentclass` により行います．その際，使用するワークフロー（使用エンジン，DVI ウェア）を必ず明示的に指定してください．こうすることにより，各種パッケージを `\usepackage` で読み込む際に個別にドライバオプションを指定する必要はなくなります．

* pLaTeX + dvipdfmx を使用する場合

```tex
%#!platex
\documentclass[platex,dvipdfmx]{nlp2021}
```

* upLaTeX + dvipdfmx を使用する場合

```tex
%#!uplatex
\documentclass[uplatex,dvipdfmx]{nlp2021}
```

* LuaLaTeX を使用する場合

```tex
%#!lualatex
\documentclass[lualatex]{nlp2021}
```

またワークフロー指定以外のクラスオプションも利用可能で，そのまま jlreq クラスに渡されます．ただし，基本版面設計に関わるようなオプション（例えば紙面サイズ，フォントサイズ，段組み数に関わるもの）は無効化されています．使わないでください．

### 体裁に関して

予稿集全体を通して体裁を揃えるという趣旨に則り，本文の文字サイズを変更したり，`\setlength` 等により版面設計に関わる寸法値を大域的に変更したりすることはお控えください．また，図表中を含め，文字サイズが小さくなり過ぎないようにご留意ください．

## バグ報告

本文書クラスに関するバグや不具合，あるいは改善提案等は GitHub 上の開発リポジトリまでご報告ください．

* <https://github.com/wtsnjp/nlproceedings/issues>

## ライセンス

本文書クラスは [MIT ライセンス](./LICENSE)の下で配布します．

---

Takuto ASAKURA
