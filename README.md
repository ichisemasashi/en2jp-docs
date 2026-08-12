# en2jp — 英語技術書の日本語訳

英語で書かれた技術書リポジトリを日本語に翻訳する作業場です。多くのプロジェクトは
[cloudstreet-dev](https://github.com/cloudstreet-dev) の書籍リポジトリを
`ichisemasashi` にフォークしたもので、`claude/japanese-translation`
ブランチで翻訳し、PRを経て `main` に取り込んでいます。

例外が
[software-design-for-flexibility-ja](https://github.com/ichisemasashi/software-design-for-flexibility-ja)
です。底本が上流リポジトリではなく市販書のPDFなので、フォークではなく新規に
起こしました。詳しくは[底本がPDFのものについて](#底本がpdfのものについて)を
見てください。

## 進捗一覧

| プロジェクト | 内容 | 翻訳 | PR |
|---|---|---|---|
| [Lisp-in-2025](Lisp-in-2025/) | 2025年のLisp — 全10章＋目次・索引・サイトUI | 完了 | [#1](https://github.com/ichisemasashi/Lisp-in-2025/pull/1) [#2](https://github.com/ichisemasashi/Lisp-in-2025/pull/2) [#3](https://github.com/ichisemasashi/Lisp-in-2025/pull/3) [#4](https://github.com/ichisemasashi/Lisp-in-2025/pull/4) [#5](https://github.com/ichisemasashi/Lisp-in-2025/pull/5) マージ済 |
| [Elisp-Tutorial](Elisp-Tutorial/) | Emacs Lisp入門 — README.org と elisp-tutorial.el | 完了 | [#1](https://github.com/ichisemasashi/Elisp-Tutorial/pull/1) マージ済 |
| [Writing-Books-with-Claude-Code](Writing-Books-with-Claude-Code/) | Claude Codeで本を書く — 全11章 | 完了 | [#1](https://github.com/ichisemasashi/Writing-Books-with-Claude-Code/pull/1) マージ済 |
| [Build-Your-Own-AI](Build-Your-Own-AI/) | 自分でAIを作る — 全11章 | 完了 | [#1](https://github.com/ichisemasashi/Build-Your-Own-AI/pull/1) マージ済 |
| [Org-Mode-with-Emacs](Org-Mode-with-Emacs/) | EmacsのOrgモード — 全13章＋目次 | 完了 | [#1](https://github.com/ichisemasashi/Org-Mode-with-Emacs/pull/1) マージ済 |
| [The-Big-Book-of-Compression-Algorithms](The-Big-Book-of-Compression-Algorithms/) | 圧縮アルゴリズム大全 — 全14章＋序論・参考文献 | 完了 | [#1](https://github.com/ichisemasashi/The-Big-Book-of-Compression-Algorithms/pull/1) マージ済 |
| [Database-Internals](Database-Internals/) | データベースの内側 — 全15章＋序文・付録2本 | 完了 | [#1](https://github.com/ichisemasashi/Database-Internals/pull/1) マージ済 |
| [Modern-Go](Modern-Go/) | モダンGo — 全20章＋付録3本 | 完了 | [#1](https://github.com/ichisemasashi/Modern-Go/pull/1) マージ済 |
| [Because-Ruby](Because-Ruby/) | Because Ruby — 全30章＋目次 | 完了 | [#1](https://github.com/ichisemasashi/Because-Ruby/pull/1) マージ済 |
| [The-PERL-Programming-Language](The-PERL-Programming-Language/) | PERLプログラミング言語 — 全22章＋付録3本 | 完了 | [#1](https://github.com/ichisemasashi/The-PERL-Programming-Language/pull/1) マージ済 |
| [paip-lisp](paip-lisp/) | 人工知能プログラミングのパラダイム（Norvig） — 全25章＋まえがき・付録・参考文献 | 完了 | [#1](https://github.com/ichisemasashi/paip-lisp/pull/1) マージ済 |
| [software-design-for-flexibility-ja](software-design-for-flexibility-ja/) | 柔軟性のためのソフトウェア設計（Hanson & Sussman） — 全8章＋前付け・付録2本 | 完了 | フォークではないため直接コミット |

12プロジェクトすべて完了しています。

最後の1つだけ性質が違うので、要点を書いておきます。

- **底本が市販書のPDF**（原著475ページ）。他はすべて上流リポジトリのMarkdown
- **フォークではなく新規リポジトリ。** PRを経ず `main` に直接コミットしています
- **CC BY-SA の継承義務を負う最初の公開物。** 訳文も同じ CC BY-SA 4.0 で公開し、
  帰属表示・ライセンス表示・改変の告知を `LICENSE` と各訳文ファイルの冒頭に
  置いています
- **底本の `src/` は公開していません。** 原著の英文全体にあたるうえ、機械抽出で
  数式が丸ごと落ち記号も化けており、原著を誤って伝えかねないためです。
  いちど含めてコミットしたあと `git filter-branch` で履歴から除きました。
  再生成の手順はリポジトリの README にあります

訳文16,726行、脚注158本、練習問題100問。参考文献と索引は訳出していません。

## これから訳すもの

### 公開するもの

| ディレクトリ | 対象 | 底本の形式 | リポジトリ |
|---|---|---|---|
| `Scheme/MIT Scheme Reference Manual` | 全体（328ページ） | PDF | 新規（未作成） |
| [lisp-1-5](lisp-1-5/) | `README` のみ | 平文（7.7KB） | [ichisemasashi/lisp-1-5](https://github.com/ichisemasashi/lisp-1-5) |
| `Scheme/Scheme 9 from Empty Space` | `README.md`、`s9.1.txt` ほかの文書 | 平文 | [ichisemasashi/S9fES](https://github.com/ichisemasashi/S9fES) |

**次に着手するのは『MIT/GNU Scheme Reference Manual』です。** 訳し終えた SDF が
読者をこの本に差し向けているからです。付録Bは「この体系についての説明書としては
『MIT/GNU Scheme Reference Manual』を見てください」と書き、付録Aは
「ソフトウェアは MIT/GNU Scheme のバージョン10.1.10以降で走る」と書いています。
その参照先が日本語で読めない状態です。

ライセンスは GNU Free Documentation License 1.1 以降で、Invariant Sections も
Front/Back-Cover Texts もありません。継承義務を守れば公開できます。底本はPDFなので、
[底本がPDFのものについて](#底本がpdfのものについて)の段取りとSDFでの反省が
そのまま効きます。

`lisp-1-5` は LISP 1.5 の処理系一式（`lisp15.asm`、`lisp15.lisp`、
IBM 7090アセンブラほか）を収めたフォークです。翻訳対象は `README` のみで、
処理系のソースは対象外です。

**`LISP-1.5-Programmers-Manual.pdf` は翻訳対象から外しました。** 前付け
（4ページ）を確認したところ、記載されている複製の許諾は「合衆国政府の目的の
ためであれば全部または一部の複製を認める」というもので、連邦資金による研究に
付く定型の条項でした。一般向けの許諾も、翻訳を認める文言もありません。
発行は The M.I.T. Press（第2版・1985年第15刷、ISBN 0-262-13011-4）。
手元での閲覧のみとし、訳文は作らず公開もしません。

`Scheme/Scheme 9 from Empty Space` は上流
[reflectionalist/S9fES](https://github.com/reflectionalist/S9fES) の
クローンで、それ自体がgitリポジトリです。パブリックドメインなので
GitHubでも管理します。フォーク [ichisemasashi/S9fES](https://github.com/ichisemasashi/S9fES)
を `origin`、上流を `upstream` に設定済みです。既定ブランチは
`main` ではなく **`master`** なので、PRの `--base` に注意してください。
外側の `Scheme` リポジトリからは参照（gitlink）として記録しているだけなので、
この配下の変更は内側のリポジトリでコミットします。

### ローカルのgitでのみ管理するもの

次は第三者の著作物を底本とするため、**リモートを設定せず、
ローカルのgitでのみ管理します**。GitHubには登録しません。

| ディレクトリ | 内容 | Git |
|---|---|---|
| `COMMON LISP A Gentle Introduction to Symbolic Computation` | Touretzky『COMMON LISP: A Gentle Introduction to Symbolic Computation』のPDF（`book.pdf`） | ローカルのみ（リモートなし） |
| [Scheme](Scheme/) | Scheme・マクロ・コンパイラ実装に関する論文と書籍のPDF、平文の文書、実装のソース | ローカルのみ（リモートなし） |

`Scheme` は、Chez Scheme・nanopassフレームワーク・衛生的マクロ・継続などに関する
論文と書籍を集めた資料置き場です。市販されている書籍のPDFや、学会・著者に
著作権のある論文を多く含みます。訳文も底本と同じ場所に置くため、
リポジトリごと非公開にしています。`Scheme 9 from Empty Space` だけが例外で、
上記のとおり内側のリポジトリを通じて公開します。

**`Scheme/How to Design Programs, Second Edition` は手元で読む用途に限ります。**
CC BY-NC-ND の ND（改変禁止）に該当するため、訳文を公開・再配布しません。
外側の `Scheme` リポジトリの中だけで作業します。

### 底本がPDFのものについて

これまでのプロジェクトは底本がMarkdownだったため、原文の行を1行ずつ
訳文で置き換え、行数・行構造の一致で検証できました。PDFにはこの方法が
使えません。次の段取りが要ります。

1. テキストを抽出する（`pdftotext -layout` など）
2. 抽出結果を見出し・段落・コード・表に整えてMarkdownにする
3. そのMarkdownを原文として、従来どおり1行ずつ訳す
4. 検証は「訳文 対 抽出Markdown」で行う。PDFそのものとは突き合わせられない

2 が事実上の書き起こしになるため、同じ分量のMarkdownより手間がかかります。
数式・図・表・2段組みは抽出が崩れやすく、目視の確認が要ります。

#### 実際にやってみて分かったこと（SDF、原著475ページ）

上の見込みはおおむね当たっていましたが、抽出の壊れ方は想像より広範でした。
`pdftotext -layout` の結果を信じてはいけません。

**表示数式はテキスト層に存在しません。** 式番号 `(3.2)` だけが抽出され、
本体は空白になります。落ちていることに気づかず訳すと、式が丸ごと消えます。
14箇所を見落とし、あとから原著PDFを目で読んで転記しました。転記した式は、
すぐ近くのコードと突き合わせて検算できます（漸化式なら対応する手続きと）。

**記号が別の文字に化けます。** 見つけたものを挙げます。

| 原著 | 抽出結果 | 現れた場所 |
|---|---|---|
| `^` | `∧` | 正規表現の行頭アンカー、`x^2` の冪 |
| `∘` | `◦` | 手続きの合成 |
| `°` | `◦` | 角度 |
| `` ` `` | `‘` | クォート |

`◦` が2つの別々の文字に対応する点に注意してください。文脈で判断するほかありません。
なお **`∧` を機械的に `^` へ戻すのは危険です**。論理式の連言まで壊しました。

**上付き・下付きが失われます。** `fⁿ` は `f` に、`k_exit` は2語に分かれます。
識別子が行の途中で切れることもあります。

**本文中のページ参照は使えません。** 「NNNページ」は印刷版の番号で、電子版とは
対応しません。ずれは一定ですらありませんでした（実測で67・70・70・91）。
SDF では102箇所を、番号（練習問題N.M・脚注N・図N.M）・節番号・手続き名・
「先に」「このあと」に置き換えました。他書を指すページ参照は残します。

**図は訳出しないと決めました。** 説明文だけ訳し、その下に原著の図番号を示す
注を添えています。

### ライセンスの確認状況

底本ごとに権利の状況が違います。実際に前付け・奥付・ソースを見て確認した
結果だけを記録します。推測では書きません。

#### 判断の基準

**配布の許諾と、改変（翻訳）の許諾は別物です。** ここがこの作業でいちばん
効いてくる線引きでした。

翻訳は二次的著作物の作成にあたるので、「自由に配ってよい」だけでは足りず、
**改変を認める文言**が要ります。CC BY-SA、GFDL、パブリックドメイン、BSD系は
これを明示しています。一方「電子形式で配布してよい」「無償で複製してよい」
としか書かれていない文書は、翻訳の対象にできません。

もう1つ。**許諾の表示がないことは、許諾があることを意味しません。** 著作権は
表示がなくても発生するため、表示の見当たらない文書は「許諾を確認できなかった」
として扱い、翻訳しません。

#### 全訳できるもの（改変が明示的に許諾されている）

| 底本 | 分量 | 確認した文言 |
|---|---|---|
| `Scheme/Scheme 9 from Empty Space` | — | `LICENSE` にパブリックドメインと明記 |
| `Scheme/software-design-for-flexibility`（Hanson & Sussman） | 541p | 「Creative Commons Attribution-ShareAlike 4.0 International License」（© 2021 MIT）**→ 訳出・公開済み** |
| `Scheme/MIT Scheme Reference Manual` | 328p | GNU Free Documentation License 1.1 以降。Invariant Sections なし、Front/Back-Cover Texts なし |
| Common Lisp Cookbook（未取得。[現行版](https://github.com/LispCookbook/cl-cookbook)） | 相当量 | [BSD系](https://cl-cookbook.sourceforge.net/license.html)。派生形式・改変ありの再配布を明示的に許可。著作権表示と免責条項の同梱が条件 |

#### 私的使用の範囲で、訳者本人が訳すもの

日本の著作権法では、**第30条**（私的使用のための複製）と**第47条の6**
（複製が認められる場合の翻訳等）により、購入・所持している著作物を、
個人的にまたは家庭内など限られた範囲で使うために自分で翻訳することが
認められています。以下の文書は、この範囲で訳者本人が訳します。

したがってこれらは、

- **公開しません。** 私的使用の範囲を超えるため
- **リモートを持つリポジトリに置きません。** ローカルのgitでのみ管理します
- 作業環境（PDFからの抽出、章分割、行単位の置換と構造検証の道具、
  訳語集の雛形）は用意してあります。[作業環境](#私的使用のための作業環境)を
  見てください

#### 権利者の許諾がないもの（公開を伴う翻訳はしない）

| 底本 | 確認した文言 | 備考 |
|---|---|---|
| `COMMON LISP A Gentle Introduction...`（Touretzky） | © 1990 Symbolic Technology, Ltd. ハードコピーでの教育目的・無償配布のみ可、**電子形式での再配布は禁止**、その他の権利はすべて留保 | 587p |
| `lisp-1-5/LISP-1.5-Programmers-Manual.pdf` | 前付け4ページに「合衆国政府の目的のためであれば複製を認める」とのみ。一般向けの許諾なし | MIT Press 第2版・1985年第15刷。手元での閲覧のみ |
| `Common Lisp the Language, 2nd Edition`（CLtL2） | Butterworth-Heinemann が**電子形式での全文配布**を許諾。ただしソースの `Title-page` に「© 1984, 1989 Guy L. Steele Jr. All rights reserved.」 | **配布の許諾はあるが改変の許諾がない**典型例。LaTeXソースの翻訳も同じ理由で不可 |
| `Scheme/How to Design Programs, 2nd Ed` | CC BY-NC-**ND**（改変禁止） | 48,097行。手元で読む用途に限る |
| `Scheme/Three Implementation Models for Scheme` | ALL RIGHTS RESERVED | 190p |
| `Scheme/ESSENTIALS OF PROGRAMMING LANGUAGES` | All rights reserved | 433p |
| `Scheme/The Scheme Programming Language 4th` | © 2009 The MIT Press | 400p |
| `Scheme/Syntactic Abstraction in Scheme`、`...the Syntax-Case Expander` | MIT Press 収録 | 18p / 23p |
| ACM 著作権の論文4本 | `An Efficient Implementation of Multiple Return Values`(© 1994 ACM)、`Efficient Nondestructive Equality Checking`(© 2008 ACM)、`The Development of Chez Scheme`(© 2006 ACM)、`Compiler and Runtime Support for Continuation Marks`(© owner/author) | |
| 著者著作権の論文5本 | `A Sufficiently Smart Compiler`(© 2012 Keep)、`Enabling Cross-Library Optimization`(© 2010)、`Programming With Hygienic Macros`(© 1992 Dybvig)、`Writing Hygienic Macros`(© 1992)、`Programming Languages and Lambda Calculi`(© 1989, 2003 Felleisen, Flatt) | |

#### 許諾を確認できなかったもの

前付け5ページと末尾3ページを走査しても表示が見つからなかった論文が11本
あります（`A Monadic Framework for Delimited Continuations`、
`A Nanopass Framework for Compiler Education`、
`An Infrastructure for Profile-Driven Dynamic Recompilation`、
`An Introduction to Quantum Computing, Without the Physics`、
`Application and Interpretation`、`Destination-Driven Code Generation`、
`Hygiene-Compatible Macros in an Unhygienic Macro System`、
`Nanopass Framework Users Guide`、`Perf Study on Stack and Register Based VM`、
`Programming with Lambda Calculus`、`Register Allocation via Graph Coloring`）。

多くは著者が個人サイトで配布している preprint です。表示がない以上は翻訳
しませんが、著者に問い合わせれば許諾を得られる可能性はあります。

`lisp_in_small_pieces.pdf`(532p) と
`Three Implementation Models for Scheme-.pdf`(189p) は**テキスト層のない
スキャン画像**なので、この方法では走査できませんでした。後者は重複で、
テキスト層のある版が「ALL RIGHTS RESERVED」と判明しています。

#### 判断が要るもの

**dpANS3**（ANSI Common Lisp 規格の草案、1000ページ超）。CLHS の元になった
文書で、機能としては CLtL2 にいちばん近く、LaTeXソースで章ごとに分かれて
います。

- [CMU AI Repository](https://www.cs.cmu.edu/afs/cs/project/ai-repository/ai/lang/lisp/doc/standard/ansi/0.html)
  は複製条件を「Free use, copying, distribution」と記載
- ただし [ソースの .tex ファイル](https://github.com/Hexstream/dpans) 自体には
  著作権表示も許諾文もなく、リポジトリに LICENSE ファイルもない

標準化委員会が自由な利用を前提に配布した草案であり、コミュニティでは制約なしと
扱われてきた経緯があります。ただ CC BY-SA や GFDL のような明示的な許諾とは
同列に置けないため、着手には判断が要ります。

`paip-lisp` は [norvig/paip-lisp](https://github.com/norvig/paip-lisp) のフォークで、
他とは別系統です。翻訳対象は **`docs/` 配下の文書のみ**とし、`lisp/` 配下のソース、
OCR由来の原文アーカイブ（`PAIP.txt`、`PAIP-safari.md`）、開発用の道具は対象外です。

**ライセンス:** 本書は1992年にMorgan Kaufmannから刊行されたのち、権利が著者
Peter Norvigに返還され、著者がMITライセンスで公開したものです。MITライセンスは
改変と再配布を明示的に許諾しているため、この翻訳は許諾された二次的著作物にあたります。
`LICENSE` と原著の著作権表示はそのまま維持しています。

## 私的使用のための作業環境

権利者の許諾がない文書を、著作権法第30条・第47条の6の範囲で訳者本人が訳す
ための道具立てです。許諾のある文書の翻訳で使ってきたものと同じ一式です。

| 道具 | 役割 |
|---|---|
| `src/` への抽出 | `pdftotext -layout`（1段組み）または `pdftotext`（2段組みの論文）。ページ区切り `\f` を残して原著ページと対応づける |
| 章分割 | ページ範囲を指定して章ごとのファイルに切る |
| `apply.py` / `txt.py` | 行番号または原文の完全一致で置換する。**原文と食い違えば止まる**ので、行のずれを取り逃がさない |
| 構造検証 | 行数・空行の位置・コードフェンス数・リンク数・見出しの並びを原文と突き合わせる |
| 走査 | 訳し残しの英語散文、異言語（キリル文字・ハングル）の混入、見出しと目次の不一致 |
| 訳語集 | `TRANSLATION-GLOSSARY.md` の雛形。章ごとに追記する運用 |

平文を訳すときの注意が1つあります。**空行が段落の切れ目になる**ため、訳文が
原文より短くなった行を空にすると構造が変わります。段落ごとに元の行数へ収まる
よう改行位置を決め、検証は行数だけでなく空行の位置も突き合わせてください。


## 各プロジェクトの構成

翻訳したリポジトリには、いずれも次のファイルを置いています。

- `TRANSLATION-GLOSSARY.md` — そのプロジェクトの訳語表・翻訳方針・原文の不備の扱い
- `.gitignore` — macOSのリソースフォーク（`.DS_Store`、`._*`）ほか

訳語のゆれは記憶ではなく用語集で担保しています。新しい訳語を決めたら、
それを使ったコミットと同じコミットで用語集に追記する運用です。

## 共通の翻訳方針

詳細は各プロジェクトの `TRANSLATION-GLOSSARY.md` にありますが、
全プロジェクトで共通している判断は次のとおりです。

### 訳すもの

本文、見出し、コードブロック内のコメント、frontmatterの `title`、
サイトのUI文言（ナビゲーション、ボタン、`_config.yml` の章タイトル一覧）。

### 訳さないもの

| 対象 | 例 |
|---|---|
| コード本体、識別子、関数名 | `wantarray`、`defrecord`、`make_path` |
| 文字列リテラル、出力例 | `die "Can't open $file: $!"` |
| コマンド、オプション | `cpanm Module::Name`、`go test -race` |
| ライブラリ名、パッケージ名 | `Text::CSV`、`Reagent`、`sqlx` |
| URL、リンク先ファイル名 | `[...](01-introduction.md)` |
| 人名、会議名、書名、企業名 | Larry Wall、RubyKaigi、Booking.com |
| 設定ファイル・テンプレートの見本 | 生成物として提示されている中身 |

設定ファイルやテンプレートの見本を英語のまま残しているのは、
訳すとコードとその生成物の対応が読めなくなるためです。
本文の解説は日本語、生成物の中身は英語、という切り分けにしています。

### 文体

- 本文・説明文は敬体（です・ます調）
- 箇条書きの項目は体言止め、または簡潔な常体
- 英数字・記号は半角。英数と日本語のあいだに空白を入れない
- 日本語文中の括弧は全角（）、引用符は「」

原著の語り口（皮肉、ユーモア、比喩）は日本語でも再現しています。
直訳で調子が死ぬ箇所は意訳し、意訳した箇所はPR本文に記載しています。

## 構造の検証

訳文の良し悪しは人が読むしかありませんが、構造の破壊は機械で検出できます。
翻訳直後に毎回、原文（`main`）と次を突き合わせています。

- **行数** — 1行ずつ置き換えて訳していれば原文と一致する
- **行の種別の並び** — 空行・見出し・コードフェンス・箇条書き・引用・表の並び
- **コードフェンスの数** — 開閉の対応
- **リンク数** — 原文と一致するか
- **翻訳漏れ** — フェンス外の英語散文、英語だけのコメントの走査
- **ハングルの混入** — 日本語入力時の取り違えの検出

行数が原文と異なるのは、意図して行を足した1箇所のみです
（`The-PERL-Programming-Language/06-file-io-and-directory-operations.md`、
不足していた `use` 文2行の追加で624行→626行）。

### 訳文そのものの傷（`tools/lint-ja.py`）

構造の検証は原文と突き合わせますが、**訳文の中だけで完結する傷は捕まりません**。
SDF でこれに手ひどくやられたので、別の道具を用意しました。

```bash
python3 tools/lint-ja.py 'ja/*.md'
python3 tools/lint-ja.py --self-test
```

見るのは4つ。いずれも**一括置換の後始末**で実際に作り込んだ傷です。

- **五段動詞の活用の破壊** — 敬体→常体の一括変換で「働きます」が「働きる」になる
- **サ変の取り違え** — 同じ変換で「返します」が「返する」になる
- **脚注の文体の混在** — 脚注は常体なのに敬体が残る
- **コード span の字間** — ページ参照の削除で「`foo` の定義」が「`foo`の定義」と詰まる

**なぜこれが要るのか。** SDF では、原文由来の問題7件に対して**自分で壊した箇所が
25件**ありました。自損のほうが多かったのです。しかも第5章では同じ取りこぼしを
2回繰り返しています。原因は、壊れ方の型を**想像で列挙して**確認していたこと。
1回目は「働きる」「使いる」など思いついた語幹を探し、8件を取りこぼしました。
2回目に文法の形（五段連用形＋る）で網羅的に走査して、ようやく残存0を確認できました。

そこでこの道具は語彙ではなく**文法の形**で走査します。書いたあと SDF 全体に
かけたところ、通し読みで見落としていた3件（脚注の敬体1件、字間2件）が出ました。

**誤検出を出さないことを優先しています。** 練習問題の文体は検査していません。
始まりは見出しで分かるものの終わりに印がなく、本文が見出しなしで再開するため、
区切りを機械で決められないからです。試作では練習問題の直後の本文を巻き込んで
10件の誤検出を出しました。誤検出の多い検査は読み飛ばされます。それが25件を
見逃した原因そのものなので、確実に区切れるものだけを見ます。

一段動詞（起きる・足りる）や「〜できる」「〜すぎる」を除く判定は、実際の訳文で
この形が83種あることを数えてから決めました。想定ではなく実測です。
`--self-test` に、実際に作り込んだ傷から取った10件の標本を入れてあります。

## 原文のコードの不備について

翻訳中に動かないコードが見つかることがあります。扱いは全プロジェクト共通です。

1. **手元の処理系で実際に走らせて再現を確認する。**
   構文チェックだけでは足りません。たとえば `perl -c` は構文しか見ないので、
   未定義サブルーチンの呼び出しは実行しないと出ません
2. 再現したら修正し、**修正後のコードも走らせて確認する**
3. 実行して確認できないもの（外部サービス依存など）は推測で直さず、
   用語集に観察として記録するにとどめる
4. 修正はコミットメッセージ・用語集・PR本文の3箇所に記録する

「誤用に見えたが実際は動いた」ため原文のまま残した箇所もあります
（例: `XML::LibXML::Schema->new(string => ...)`）。
直す前に確かめる、を徹底しています。

## 作業の進め方

`japanese-translation` スキルの手順に沿っています。

```
1. 対象の棚卸し  → 何が翻訳対象で、何が対象外かを先に確定させる
2. 用語集の用意  → 訳語の単一の情報源を作る
3. 翻訳          → 1ファイルずつ。用語集に従う
4. 構造の検証    → 行数・フェンス・リンク・翻訳漏れ
5. 用語集に追記  → 新しく決めた訳語を必ず記録
6. コミット/PR   → 判断の理由を残す
```

PR本文には訳文全体ではなく、**判断が分かれる箇所**を書きます。
意訳した箇所とその理由、一般語と意味がずれる訳語の判断、
原文の不整合をどう扱ったか、翻訳対象外にしたものとその理由、構造検証の結果です。
