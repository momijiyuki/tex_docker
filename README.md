# tex_docker
devcontainer for texlive

## Getting Started

```sh
cd /root/workspace/
./install-tl/install-tl --profile texlive.profile
rm -r install-tl install-tl-unx.tar.gz
```

## 使用したコレクション

- `a, b, c, f, g, m, x, D, F, J, K`
  - 必須プログラムとファイル
  - BibTeXの追加スタイル
    - ref.bibが使えるようになる
  - TeX外部プログラム
    - latexmk
  - 推奨フォント
  - 画像およびフォントのユーティリティ
  - 日中韓(base)
  - 日本語
  - LaTeX基本パッケージ
  - LaTeX推奨パッケージ
  - 画像と図表
  - Plain(La)TeXパッケージ
- ドキュメントとソースツリーの除外


## TeX Live コレクション対応

|    |terminal                                                  | 日本語gui版                                 |
|:--:|----------------------------------------------------------|:-------------------------------------------|
| a  | Essential programs and files                             | 必須プログラムとファイル                     |
| b  | BibTeX additional styles                                 | BibTeXの追加スタイル                        |
| c  | TeX auxiliary programs                                   | TeX外部プログラム                           |
| d  | ConTeXt and packages                                     | ConTeXtとパッケージ                         |
| e  | Additional fonts                                         | 追加フォント                                |
| f  | Recommended fonts                                        | 推奨フォント                                |
| g  | Graphics and font utilities                              | 画像およびフォントのユーティリティ           |
| h  | Additional formats                                       | 追加フォーマット                            |
| i  | Games typesetting                                        | ゲーム組版                                  |
| j  | Humanities packages                                      | 人文科学パッケージ                           |
| k  | Arabic                                                   | アラビア語                                  |
| l  | Chinese                                                  | 中国語                                      |
| m  | Chinese/Japanese/Korean (base)                           | 日中韓(base)                                |
| n  | Cyrillic                                                 | キリル文字                                  |
| o  | Czech/Slovak                                             | チェコ・スロバキア語                         |
| p  | US and UK English                                        | 英語・米語                                   |
| s  | Other European languages                                 | その他の欧州言語                             |
| t  | French                                                   | フランス語                                   |
| u  | German                                                   | ドイツ語                                     |
| v  | Greek                                                    | ギリシア語                                   |
| w  | Italian                                                  | イタリア語                                   |
| x  | Japanese                                                 | 日本語                                       |
| y  | Korean                                                   | 韓国語                                       |
| z  | Other languages                                          | 他の言語                                     |
| A  | Polish                                                   | ポーランド語                                 |
| B  | Portuguese                                               | ポルトガル語                                 |
| C  | Spanish                                                  | スペイン語                                   |
| D  | LaTeX fundamental packages                               | LaTeX基本パッケージ                          |
| E  | LaTeX additional packages                                | LaTeX追加パッケージ                          |
| F  | LaTeX recommended packages                               | LaTeX推奨パッケージ                          |
| G  | LuaTeX packages                                          | LuaTeXパッケージ                             |
| H  | MetaPost and Metafont packages                           | MetaPostおよびMetafontパッケージ             |
| I  | Music packages                                           | 音楽パッケージ                               |
| J  | Graphics, pictures, diagrams                             | 画像と図表                                   |
| K  | Plain (La)TeX packages                                   | Plain(La)TeXパッケージ                       |
| L  | PSTricks                                                 | PSTricks                                    |
| M  | Publisher styles, theses, etc.                           | 出版社スタイルや学位論文                      |
| N  | Windows-only support programs                            | Windows専用プログラム                        |
| O  | XeTeX and packages                                       | XeTeXとパッケージ                            |
| P  | Mathematics, natural sciences, computer science packages | 数学、自然科学、計算機科学パッケージ           |
| S  | TeXworks editor; TL includes only the Windows binary     | TeXworks(Windows版のみ)                      |

## 参考元

- [TEX Live ガイド 2023](https://www.tug.org/texlive/doc/texlive-ja/texlive-ja.pdf)
- [インストーラプロファイルを用いてTeX Liveをインストールしよう](https://qiita.com/munepi/items/f2eaa30f0cd00a9a68f8)
- [TeX Live ドキュメント #PROFILES](https://tug.org/texlive/doc/install-tl.html#PROFILES)
- [VSCode で最高の LaTeX 環境を作る](https://qiita.com/rainbartown/items/d7718f12d71e688f3573)
  - `settings.json`や`.latexmkrc`を参考
- [Tex Liveのクソデカ容量を削減したい！](https://blog.loliver.net/archive/texlive_minimal_install/)
  - コレクションの選定の参考に
- [texliveの最強環境を作ったよ](https://zenn.dev/tbistr/articles/texlive-devcontainer-repost)
  - `Dockerfileの記法等を参考

<!-- [LaTeXで作るA0poster](http://www.math.kobe-u.ac.jp/a0poster/) -->
