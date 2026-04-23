# Background Assets Guide

## 目的

このディレクトリは、**職場ウイルス図鑑** の背景参照素材を、キャラクター素材やロゴ素材と同じルール感で管理するための共通置き場である。とくに Season 1 前半のショート動画制作では、同じ職場で起きている連続性を保つため、背景素材を話ごとに散らさず、**共通背景**と**話数固有背景**に分けて整理する。

## 基本配置ルール

背景素材は `assets/reference/backgrounds/` 配下に置き、Season ごと・用途ごとに整理する。現時点では Season 1 用に次の構成を標準とする。

| パス | 用途 |
|---|---|
| `assets/reference/backgrounds/season1/common/` | EP001〜EP005 など複数話で共通利用する背景 |
| `assets/reference/backgrounds/season1/episode_specific/` | 特定話だけで使う背景 |

EP001 試験編集版で使用予定の `office_morning_common`、`desk_row_common`、`manager_desk_common`、`aizawa_desk_common` は、いずれも **共通背景**として `season1/common/` に配置する。

## 命名ルール

背景ファイル名は、**背景ID + バージョン**の形式で統一する。英小文字スネークケースを使用し、拡張子の前に `_v01` のような版番号を付ける。

| 形式 | 例 |
|---|---|
| `{background_id}_v01.png` | `office_morning_common_v01.png` |
| `{background_id}_v02.png` | `desk_row_common_v02.png` |

## 推奨ファイル名

Season 1 前半の初期運用では、以下の4点を最優先で準備する。

| 背景ID | 推奨ファイル名 | 配置先 |
|---|---|---|
| `office_morning_common` | `office_morning_common_v01.png` | `assets/reference/backgrounds/season1/common/` |
| `desk_row_common` | `desk_row_common_v01.png` | `assets/reference/backgrounds/season1/common/` |
| `manager_desk_common` | `manager_desk_common_v01.png` | `assets/reference/backgrounds/season1/common/` |
| `aizawa_desk_common` | `aizawa_desk_common_v01.png` | `assets/reference/backgrounds/season1/common/` |

## 運用メモ

背景は、完成アセットを大量に置く場所というより、**編集・生成・構図検討の基準になる参照素材置き場**として使う。したがって、同一背景の軽微な差分が複数ある場合でも、まずは代表版を `v01` として置き、必要が出た段階で `v02` 以降を追加するのが望ましい。

また、背景の切り出しやトリミングだけで対応できる場合は、毎回別ファイルを増やさず、元背景を基準に編集側で対応する。背景フォルダの肥大化を防ぎつつ、同じ職場感を維持することを優先する。
