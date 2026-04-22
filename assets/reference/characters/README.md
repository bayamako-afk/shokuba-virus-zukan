# Character Reference Asset Placement Guide

## Purpose
This directory stores the **approved reference images and lightweight variation assets** for the recurring Season 1 characters. For the current first-half production block, the fixed characters are **守屋守**, **クマ課長**, and **相沢律子**.

The goal of this structure is to keep character references stable across EP001〜EP005 so that shotlists, asset lists, and later video generation all point to the same visual identity.

## Folder Layout

| Path | Purpose |
|---|---|
| `assets/reference/characters/moriya_mamoru/` | 守屋守の基準顔・表情差分・姿勢差分 |
| `assets/reference/characters/kuma_kacho/` | クマ課長の基準顔・表情差分・姿勢差分 |
| `assets/reference/characters/aizawa_ritsuko/` | 相沢律子の基準顔・表情差分・姿勢差分 |

## Naming Rule
Use the following filename rule for all approved character images.

> `{character}_{category}_{variant}_v01.png`

If needed, a usage suffix may be inserted before the version.

> `{character}_{category}_{variant}_{use}_v01.png`

## Character Keys

| Character | Key |
|---|---|
| 守屋守 | `moriya_mamoru` |
| クマ課長 | `kuma_kacho` |
| 相沢律子 | `aizawa_ritsuko` |

## Category Keys

| Category | Meaning |
|---|---|
| `base` | 基準顔・基準立ち姿 |
| `expression` | 表情差分 |
| `pose` | 着席・歩行・半身などの姿勢差分 |
| `costume` | 会議用、通常業務用などの衣装差分が必要な場合 |

## Example Filenames

| Use | Example |
|---|---|
| 基準顔 | `moriya_mamoru_base_front_v01.png` |
| 軽い違和感 | `moriya_mamoru_expression_micro_stop_v01.png` |
| 疲労無表情 | `moriya_mamoru_expression_fatigue_blank_v01.png` |
| ため息圧 | `kuma_kacho_expression_pressure_sigh_v01.png` |
| 軽口指示 | `kuma_kacho_expression_pressure_light_order_v01.png` |
| 無言同調 | `aizawa_ritsuko_expression_reinforce_silent_v01.png` |
| 依頼微笑 | `aizawa_ritsuko_expression_reinforce_request_smile_v01.png` |
| 着席姿勢 | `aizawa_ritsuko_pose_seated_v01.png` |

## Operating Notes
Images placed here should be the **approved reference set**, not raw generations in large volumes. Keep only the stable base images and the minimum useful differences for production. When a new file replaces an older approved version, increment the version suffix, such as `v02`.

For Season 1 first-half work, the most important assets to store first are the base images and the cross-episode expression differences listed in the production documents under `docs/operations/`.
