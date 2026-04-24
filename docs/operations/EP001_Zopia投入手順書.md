# Zopia投入手順書（EP001用）

## 対象

| 項目 | 内容 |
|---|---|
| プロジェクト | **職場ウイルス図鑑 Season 1 EP001「ため息ウイルス」** |
| 用途 | **Manus / GeminiCL / zopia-skill 用の実行手順書** |
| 目的 | **Image2 で作成した実写基準画像・背景・UI素材を、Zopia に正しく投入し、実写ショートドラマ風で EP001 を安定生成する** |

## 1. 目的

EP001「ため息ウイルス」を、**日本の職場ショートドラマ風の実写テイスト**で生成する。アニメ調・イラスト調への誤変換を避けるため、**プロジェクト作成直後に基準素材を投入し、Entity として明示的に紐付けた後に脚本具体化・ショット生成へ進む**。

## 2. 重要方針

### 2-1. 実写優先

今回の EP001 は、**実写ショートドラマ風**、**日本の現代オフィスのリアルな空気感**、**再現VTR・スマホドラマのような生っぽさ**を最優先とする。視覚表現は、自然な肌の質感、オフィス蛍光灯の自然なライティング、過剰演出なし、沈黙・視線・ため息による「じわ怖さ」を基準にそろえる。

### 2-2. 禁止事項

以下の方向には寄せない。

| 禁止する方向 | 備考 |
|---|---|
| anime | アニメ調禁止 |
| illustration | イラスト調禁止 |
| manga look | 漫画調禁止 |
| cel shading | セル塗り禁止 |
| cartoon rendering | カートゥーン調禁止 |
| stylized 2D characters | 2Dキャラ化禁止 |
| exaggerated expressions | 誇張表情禁止 |
| 過剰なCG感 | 実写優先 |
| 派手なホラー演出 | 社会怪談寄りに抑える |

## 3. 前提

### 3-1. 仕様前提

GitHub URL 直参照ではなく、**Zopia Web UI への手動アップロード前提**とする。画像投入タイミングは **プロジェクト作成直後** であり、画像はアップロードするだけでなく、**AI Agent に「誰の基準画像か」「何の共通素材か」を認識させる必要がある**。一度 Entity として紐付いた基準画像は、後続ショットでも継続参照される想定とし、表情差分は後から追加可能とする。

### 3-2. 素材管理前提

| 区分 | 役割 |
|---|---|
| `assets/reference/` | 資産庫 |
| `assets/zopia_upload/season1_ep001_ep005/` | 出荷箱 |

Zopia へ投入するのは **zopia_upload 側のみ** とする。

## 4. 投入対象素材

### 4-1. 先行投入（必須）

最初に投入するのは、3キャラの基準全身・基準顔、背景4点、ロゴ、UIである。表情差分はまだ入れない。

| 分類 | 対象 |
|---|---|
| 守屋守 | 全身正面（基準立ち絵）、顔アップ正面（基準顔） |
| 相沢律子 | 全身正面（基準立ち絵）、顔アップ正面（基準顔） |
| クマ課長 | 全身正面（基準立ち絵）、顔アップ正面（基準顔） |
| Backgrounds | `office_morning_common_v01.png` / `desk_row_common_v01.png` / `manager_desk_common_v01.png` / `aizawa_desk_common_v01.png` |
| UI / Brand | `shokuba_virus_zukan_logo_main_v01.png` / `ai_log_overlay_v01.png` |

### 4-2. 後続投入（必要時のみ）

初回生成後、必要に応じて以下の表情差分を追加投入する。

| キャラクター | 追加候補 |
|---|---|
| 守屋守 | `moriya_mamoru_expression_micro_stop_v01.png` / `moriya_mamoru_expression_fatigue_blank_v01.png` |
| クマ課長 | `kuma_kacho_expression_pressure_sigh_v01.png` / `kuma_kacho_expression_soft_recheck_v01.png` |
| 相沢律子 | `aizawa_ritsuko_expression_reinforce_silent_v01.png` / `aizawa_ritsuko_expression_reinforce_soft_justify_v01.png` / `aizawa_ritsuko_expression_reinforce_request_smile_v01.png` |

## 5. 推奨投入順

最初から表情差分を入れすぎると、AI が「何が基準か」「何が差分か」を混乱する可能性がある。したがって、まず **体格・服装・顔の基準** を固定し、その後不足する演技だけ差分追加する。

| Step | 内容 |
|---|---|
| A | 基準キャラを投入する。順番は **全身正面 → 顔アップ正面**。 |
| B | 背景4点、ロゴ、UIを投入する。 |
| C | AI Agent に「この画像は誰か / 何か」を明示し、Entity 紐付けする。 |
| D | base だけで EP001 のコンテ・ショット生成を試行する。 |
| E | 表情が足りないショットだけ差分投入し、再生成する。 |

## 6. 実作業フロー

### Phase 1：プロジェクト作成

生成の器を先に作る。`create_project.py` を実行して新規プロジェクトを作成し、Base ID / Project ID を取得し、Zopia Web UI で当該プロジェクトを開く。この段階ではまだ脚本の具体化を進めすぎず、**先に基準素材を投入すること** を優先する。

### Phase 2：スタイル設定

アニメ化を防ぐため、可能であれば **`photographic` → `live_action` → `realistic_3d_cg`（fallback）** の優先順で設定する。`anime_japanese_korean` は使わない。「実写ドラマ風」が本文に書いてあっても、上位 style が anime だとアニメ化されるリスクが高い。`realistic_3d_cg` を使う場合も、「CG感不要」「実写優先」を本文で必ず補強する。

### Phase 3：素材アップロード（手動）

Zopia Web UI を開き、`assets/zopia_upload/season1_ep001_ep005/` を参照し、まず **3キャラの基準全身、3キャラの基準顔、背景4点、ロゴ、UI** をアップロードする。可能なら、アップロード後にアセット名が分かるようスクリーンショットまたはメモを残す。

### Phase 4：AI Agent への基準認識指示

アップロードした画像を Entity として意味づけするため、GeminiCL、zopia-skill、または Manus からの送信文で以下のように指示する。

> アップロード済み画像を使って、このプロジェクトの基準ビジュアルを定義してください。  
> 1. 守屋守：30代後半の日本人男性社員。疲労感のある中堅会社員。白シャツ中心の現代的オフィス服。  
> 2. 相沢律子：40代の日本人女性。知的で落ち着いた雰囲気。静かに空気を補強する人物。  
> 3. クマ課長：50代の大柄な日本人男性管理職。怒鳴らず、ため息と空気圧で場を止める人物。  
> 4. 背景画像は、日本の現代オフィスの共通背景として使用してください。  
> 5. タイトルロゴとAIログUIは、EP001演出における共通素材として使用してください。  
> 以降の全ショットで、これらのビジュアル特徴を厳密に維持してください。

### Phase 5：EP001 初回生成

まずは base だけで実写ショットの骨格を確認する。最初は表情差分を入れすぎず、まず構図・空気感・キャラ固定ができるかを見る。実写ショートドラマ風を優先し、初回生成プロンプト内には **No anime style / No illustration / No manga look / No cel shading / Real human skin texture / Natural Japanese office lighting / Live-action office drama realism / Documentary-like realism / No exaggerated expressions** を明示する。

## 7. EP001 構成方針

EP001 は、朝の静かなオフィスでクマ課長のため息が空気を止め、守屋守の反応は大げさでなく「止まる」ことを中心に見せる。相沢律子は静かに空気へ同調し、最後に「これは、ため息ウイルスである。」で締める。演出は派手なホラーではなく、視線・沈黙・息づかい重視の**じわ怖**へ寄せる。

## 8. 差分投入の判断基準

以下のような不足が出た場合のみ差分を後から入れる。

| キャラクター | 差分追加の判断 |
|---|---|
| 守屋守 | 反応が弱い、「止まる感じ」が足りない、疲労感が薄い |
| クマ課長 | ため息圧が足りない、`pressure_sigh` と `soft_recheck` の差が弱い |
| 相沢律子 | 補強の無言圧が足りない、正当化の柔らかさが足りない、依頼笑顔が怖すぎる / 弱すぎる |

## 9. 差分投入手順

必要な差分画像だけを追加アップロードし、AI Agent に「既存キャラの表情差分として追加」と指示し、特定ショットに対して「このショットはこの表情に寄せる」と指定して再生成する。

> 守屋守の既存 Entity に対して、新しい表情リファレンスを追加してください。  
> `moriya_mamoru_expression_micro_stop_v01.png` は、異変を感じて反応が一瞬止まる微表情です。  
> EP001 の守屋守反応カットでは、この表情差分を優先参照してください。

## 10. 実写固定のための推奨プロンプト断片

以下の断片は、EP001生成時の本文に入れてよい。

```text
This project must be rendered as a realistic Japanese live-action office drama.
No anime style.
No illustration.
No manga look.
No cel shading.
No stylized 2D character rendering.
Use real human skin texture, natural office fluorescent lighting, and documentary-like realism.
The tone should be subtle, tense, and quietly unsettling, not exaggerated horror.
```
