# Zopia出荷箱 コピー整理メモ

## 方針

今回の整備では、`assets/reference/` を正式保管庫としてそのまま維持し、Zopiaへ手動アップロードしやすいように、必要素材だけを `assets/zopia_upload/season1_ep001_ep005/` へ**コピー**した。元ファイルの移動や改名は行っていない。

## 今回コピーした素材

| 出荷先 | コピー元 |
|---|---|
| `characters/moriya_mamoru/01_base/` | `assets/reference/characters/moriya_mamoru/moriya_mamoru_base_face_front_v01.png` |
| `characters/moriya_mamoru/01_base/` | `assets/reference/characters/moriya_mamoru/moriya_mamoru_base_front_v01.png` |
| `characters/moriya_mamoru/03_pose/` | `assets/reference/characters/moriya_mamoru/moriya_mamoru_pose_bust_45_v01.png` |
| `characters/moriya_mamoru/03_pose/` | `assets/reference/characters/moriya_mamoru/moriya_mamoru_pose_full_front_v01.png` |
| `characters/aizawa_ritsuko/01_base/` | `assets/reference/characters/aizawa_ritsuko/aizawa_ritsuko_base_face_front_v01.png` |
| `characters/aizawa_ritsuko/01_base/` | `assets/reference/characters/aizawa_ritsuko/aizawa_ritsuko_base_front_v01.png` |
| `characters/aizawa_ritsuko/03_pose/` | `assets/reference/characters/aizawa_ritsuko/aizawa_ritsuko_pose_bust_45_v01.png` |
| `characters/aizawa_ritsuko/03_pose/` | `assets/reference/characters/aizawa_ritsuko/aizawa_ritsuko_pose_full_front_v01.png` |
| `characters/kuma_kacho/01_base/` | `assets/reference/characters/kuma_kacho/kuma_kacho_base_face_front_v01.png` |
| `characters/kuma_kacho/01_base/` | `assets/reference/characters/kuma_kacho/kuma_kacho_base_front_v01.png` |
| `characters/kuma_kacho/03_pose/` | `assets/reference/characters/kuma_kacho/kuma_kacho_pose_bust_45_v01.png` |
| `characters/kuma_kacho/03_pose/` | `assets/reference/characters/kuma_kacho/kuma_kacho_pose_full_front_v01.png` |
| `backgrounds/` | `assets/reference/backgrounds/season1/common/office_morning_common_v01.png` |
| `backgrounds/` | `assets/reference/backgrounds/season1/common/desk_row_common_v01.png` |
| `backgrounds/` | `assets/reference/backgrounds/season1/common/manager_desk_common_v01.png` |
| `backgrounds/` | `assets/reference/backgrounds/season1/common/aizawa_desk_common_v01.png` |
| `ui/` | `assets/reference/ui/overlays/ai_log_overlay_v01.png` |

## 今回は空のまま残した場所

現時点では、表情差分や小物素材の正式ファイルがまだ揃っていないため、以下は**投入待ちの空フォルダ**として維持している。

| フォルダ | 理由 |
|---|---|
| 各キャラの `02_expression/` | 本番用の表情差分が未整備のため |
| `props/` | 小物・手元・紙資料の正式投入前のため |

## 更新ルール

今後、表情差分や小物素材が `assets/reference/` に追加されたら、まず保管庫側を正として確定し、その後に必要分のみをこの出荷箱へ追加コピーする。
