# shokuba-virus-zukan｜初期リポジトリ構成

## 概要
このリポジトリは、**『職場ウイルス図鑑』Season 1 の制作管制ハブ**として初期構成を整えた。目的は、動画ファイルの保管ではなく、設計書、台帳、テンプレート、各話入力、公開後レビューを一元管理することである。

## 現在の配置
| パス | 内容 |
|---|---|
| `README.md` | リポジトリの目的、運用方針、初期構成、次アクション |
| `docs/design/` | メイン設計書 |
| `docs/operations/` | 初回制作ルール、設計完了宣言、量産整備メモ |
| `registry/` | virus registry、character registry |
| `templates/` | episode sheet、短尺テンプレ、prompt、review、asset台帳 |
| `episodes/season1/` | 各話の記入版を置く場所 |
| `production_logs/` | 公開後レビューと昇格判定メモ |
| `assets/reference/` | 軽量参照素材のメモや管理用プレースホルダ |

## すでに配置した主要ファイル
| 分類 | ファイル |
|---|---|
| 設計 | `docs/design/運用設計書_職場ウイルス図鑑.md` |
| 運用 | `docs/operations/初回制作サイクル運用ルール.md` |
| 運用 | `docs/operations/Season1設計完了宣言_職場ウイルス図鑑.md` |
| 運用 | `docs/operations/season1_量産整備メモ_第1-5話初期入力案.md` |
| 台帳 | `registry/virus_registry.md` |
| 台帳 | `registry/character_registry.md` |
| テンプレ | `templates/season1_episode_sheet_template.md` |
| テンプレ | `templates/short_template_15_30_45.md` |
| テンプレ | `templates/character_base_prompt_template.md` |
| テンプレ | `templates/release_review_template.md` |
| テンプレ | `templates/asset_registry_template.csv` |

## 次に入れるべきもの
| 優先 | 追加内容 |
|---|---|
| 1 | `episodes/season1/EP001.md` 〜 `EP005.md` の記入版 |
| 2 | 各話の30秒版 shotlist 初稿 |
| 3 | 再利用資産キー一覧 |
| 4 | 初期人物固定リスト |
| 5 | 公開後レビューの初回ログ |

## 補足
この状態で、GitHub上の空リポジトリに対して**最初の正本構成をそのまま投入できる準備**は整っている。次工程は、EP001〜EP005 の記入版を置くことが最優先である。
