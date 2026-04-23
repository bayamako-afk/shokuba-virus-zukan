# Zopia手動アップロード順README

## このディレクトリの役割

このディレクトリは、`assets/reference/` を正式な保管庫として維持したまま、**Zopiaへ手動投入する素材だけを一時的に整理する出荷箱**である。したがって、参照元の正式素材は `assets/reference/` に残し、この配下には**今回の投入対象だけをコピーして並べる**。

今回の対象範囲は、Season 1 前半の EP001〜EP005 を想定した共通投入素材である。将来的に Season 2 や別エピソードを追加する場合も、同じ考え方で `assets/zopia_upload/` 配下に別出荷箱を増やせばよい。

## 基本方針

Zopiaは GitHub URL の直接参照ではなく、手動アップロード前提で扱う。そのため、この出荷箱では**アップロード順に迷わないこと**と、**キャラ・背景・UI を即座に選び分けられること**を優先する。`reference` は資産庫、`zopia_upload` は出荷箱、という役割を混同しない。

| 区分 | 役割 | 運用方針 |
|---|---|---|
| `assets/reference/` | 正式素材の保管庫 | 原本を保持し、むやみに構成を変えない |
| `assets/zopia_upload/` | 手動投入用の出荷箱 | 今回投入する素材だけを整理してコピーする |

## フォルダ構成の見方

| パス | 用途 |
|---|---|
| `characters/{character}/01_base/` | そのキャラの基準顔・基準立ち絵 |
| `characters/{character}/02_expression/` | 表情差分。まだ未整備なら後から追加する |
| `characters/{character}/03_pose/` | 姿勢差分・半身・全身など |
| `backgrounds/` | 背景素材をまとめる |
| `ui/` | 観測ログやカードなどのUI素材をまとめる |
| `props/` | 小物・手元・紙・PC画面などを入れる想定枠 |

## 推奨アップロード順

Zopiaでは、最初にキャラクターの基準認識を安定させ、その後に表情差分、姿勢差分、背景、UI の順で投入すると管理しやすい。今回の前半5話では、同じ3人を繰り返し使うため、**人物基準素材から先に上げる**順番が最も実務向きである。

| 手順 | アップロード対象 | 理由 |
|---|---|---|
| 1 | `characters/moriya_mamoru/01_base/` | 主視点キャラであり、最初に基準を安定させたい |
| 2 | `characters/aizawa_ritsuko/01_base/` | 補強役として固定運用するため、早めに基準化する |
| 3 | `characters/kuma_kacho/01_base/` | 圧力源として基準顔を固める |
| 4 | 各キャラの `02_expression/` | EPごとの演技差分を後から追加しやすい |
| 5 | 各キャラの `03_pose/` | 半身・全身・角度違いを補う |
| 6 | `backgrounds/` | 共通背景を後段でまとめて投入する |
| 7 | `ui/` | 命名演出や補助UIを最後に入れる |
| 8 | `props/` | 必要になった小物だけを追加する |

## EP001〜EP005で最初に上げる推奨最小セット

EP001試験編集版と前半5話の共通運用を考えると、まずは以下の最小セットから投入を始めるのがよい。まだ差分が未整備のものは、空フォルダのまま残し、後から追記する。

| 区分 | 優先投入素材 |
|---|---|
| 守屋守 base | `moriya_mamoru_base_face_front_v01.png`、`moriya_mamoru_base_front_v01.png` |
| 守屋守 pose | `moriya_mamoru_pose_bust_45_v01.png`、`moriya_mamoru_pose_full_front_v01.png` |
| 相沢律子 base | `aizawa_ritsuko_base_face_front_v01.png`、`aizawa_ritsuko_base_front_v01.png` |
| 相沢律子 pose | `aizawa_ritsuko_pose_bust_45_v01.png`、`aizawa_ritsuko_pose_full_front_v01.png` |
| クマ課長 base | `kuma_kacho_base_face_front_v01.png`、`kuma_kacho_base_front_v01.png` |
| クマ課長 pose | `kuma_kacho_pose_bust_45_v01.png`、`kuma_kacho_pose_full_front_v01.png` |
| 背景 | `office_morning_common_v01.png`、`desk_row_common_v01.png`、`manager_desk_common_v01.png`、`aizawa_desk_common_v01.png` |
| UI | `ai_log_overlay_v01.png` |

## 命名ルール

この出荷箱でも、命名は `reference` と同じ規則にそろえる。**英小文字、アンダースコア区切り、version付き**を維持し、将来の差し替えや再利用で混乱しないようにする。

| 種別 | 形式 | 例 |
|---|---|---|
| キャラクター | `{character}_{category}_{variant}_v01.png` | `moriya_mamoru_base_face_front_v01.png` |
| 表情差分 | `{character}_expression_{variant}_v01.png` | `aizawa_ritsuko_expression_soft_smile_v01.png` |
| 圧表情 | `{character}_expression_{variant}_v01.png` | `kuma_kacho_expression_sigh_pressure_v01.png` |
| 背景 | `{background_id}_v01.png` | `office_morning_common_v01.png` |
| UI | `{asset_id}_v01.png` | `ai_log_overlay_v01.png` |

## コピー運用メモ

この出荷箱にあるファイルは、原則として `assets/reference/` からの**コピー**であり、原本ではない。差し替えや改訂が起きた場合は、まず `reference` 側を正とし、その後で必要なものだけを `zopia_upload` 側へ再コピーする。

また、現時点では `props/` は将来用の空枠として作成している。EP001〜EP005で小物やPC手元、紙資料などを正式投入する段階になったら、このフォルダへ対象素材を追加する。

## 今回の整理方針まとめ

今回の整備では、`reference` を汚さずに、**Zopia投入のためだけに見通しのよい別系統を作ること**を優先している。運用上は、`reference` を資産庫、`zopia_upload` を出荷箱と見なし、必要素材のみをコピーして投入する流れを固定すると、後続のSeasonや別話数でも再利用しやすい。
