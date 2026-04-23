# 02_expression 想定ファイル名一覧

## 目的

本書は、`assets/zopia_upload/season1_ep001_ep005/characters/*/02_expression/` に今後配置していく**表情差分の想定ファイル名**を、Season 1前半 EP001〜EP005 の運用前提に合わせて整理した一覧である。ここでの目的は、まだ未生成または未確定の差分素材について、Zopia手動アップロード時に**どの名前で揃えるかを先に固定**し、後工程で命名がぶれないようにすることにある。

今回の一覧は、既存の命名規則である `{character}_expression_{variant}_v01.png` を前提にしており、3名の固定キャラクターで必要になる差分だけを、最小運用に寄せてまとめている。`reference` 側の正式保管庫を汚さず、まずは `zopia_upload` 側で投入計画を立てやすくするための基準表として使う。

## 命名の基本ルール

表情差分はすべて `02_expression/` に配置し、キャラクターキー、`expression`、差分名、バージョン番号の順で命名する。差分名は、shotlistと運用資料で使っている意味をなるべくそのまま反映しつつ、ファイル名として扱いやすい英小文字スネークケースへ統一する。

| 項目 | ルール |
|---|---|
| 配置先 | `characters/{character}/02_expression/` |
| 形式 | `{character}_expression_{variant}_v01.png` |
| 文字種 | 英小文字 |
| 単語区切り | アンダースコア |
| 版管理 | 初版は `v01`、差し替え時のみ `v02` 以降 |

## 守屋守｜想定ファイル名

守屋守は、前半5話を通して**観測者としての微細な変化**を最も多く担う。したがって、怒りや大きなリアクションではなく、停止、飲み込み、疲労、遅れて理解する感覚を中心に整理する。

| 用途 | 想定ファイル名 | 主な使用話 |
|---|---|---|
| 通常業務顔 | `moriya_mamoru_expression_base_work_v01.png` | EP001〜EP005 |
| 視線停止 | `moriya_mamoru_expression_micro_stop_v01.png` | EP001, EP002 |
| 口元硬化 | `moriya_mamoru_expression_micro_mouth_tense_v01.png` | EP001 |
| 軽い停止 | `moriya_mamoru_expression_micro_light_stop_v01.png` | EP002 |
| 理解の瞬間 | `moriya_mamoru_expression_micro_realize_v01.png` | EP002, EP003, EP004 |
| 目泳ぎ | `moriya_mamoru_expression_micro_eye_dart_v01.png` | EP003 |
| 足止まり | `moriya_mamoru_expression_micro_step_stop_v01.png` | EP004 |
| 記憶あいまい | `moriya_mamoru_expression_micro_memory_blur_v01.png` | EP004 |
| 愛想笑い | `moriya_mamoru_expression_micro_polite_smile_v01.png` | EP005 |
| 遅れて気づく | `moriya_mamoru_expression_micro_late_realize_v01.png` | EP005 |
| 薄い疲労 | `moriya_mamoru_expression_fatigue_light_v01.png` | EP002, EP004 |
| 飲み込み疲労 | `moriya_mamoru_expression_fatigue_swallow_v01.png` | EP003 |
| 残務疲労 | `moriya_mamoru_expression_fatigue_backlog_v01.png` | EP005 |
| 無表情疲労 | `moriya_mamoru_expression_fatigue_blank_v01.png` | EP005 |

## クマ課長｜想定ファイル名

クマ課長は、前半5話で一貫して**大きく怒らずに空気を固定する圧力源**として機能する。そのため、表情差分も感情の激しさより、圧の種類の違いが分かる名前で揃える方が実務上わかりやすい。

| 用途 | 想定ファイル名 | 主な使用話 |
|---|---|---|
| 管理職基準圧 | `kuma_kacho_expression_base_manager_v01.png` | EP001〜EP005 |
| ため息圧 | `kuma_kacho_expression_pressure_sigh_v01.png` | EP001 |
| 無言支配 | `kuma_kacho_expression_pressure_silent_control_v01.png` | EP001 |
| 静かな差し戻し | `kuma_kacho_expression_pressure_soft_recheck_v01.png` | EP002 |
| 会議支配 | `kuma_kacho_expression_pressure_meeting_control_v01.png` | EP003 |
| 軽口指示 | `kuma_kacho_expression_pressure_light_order_v01.png` | EP004 |
| 遠景圧 | `kuma_kacho_expression_base_distant_pressure_v01.png` | EP005 |
| 残留圧 | `kuma_kacho_expression_pressure_lingering_v01.png` | EP005 |

## 相沢律子｜想定ファイル名

相沢律子は、前半5話で**静かな同調・補強役**として作用する。露骨な悪役顔ではなく、感じの良さや理性を保ったまま、場の異常を止めない差分名に寄せるのが適切である。

| 用途 | 想定ファイル名 | 主な使用話 |
|---|---|---|
| 有能基準顔 | `aizawa_ritsuko_expression_base_capable_v01.png` | EP001〜EP005 |
| 感じの良い基準顔 | `aizawa_ritsuko_expression_base_kind_v01.png` | EP001〜EP005 |
| 無言同調 | `aizawa_ritsuko_expression_reinforce_silent_v01.png` | EP001 |
| 視線落とし | `aizawa_ritsuko_expression_reinforce_gaze_down_v01.png` | EP001 |
| 柔らかい正当化 | `aizawa_ritsuko_expression_reinforce_soft_justify_v01.png` | EP002 |
| 理性的補強 | `aizawa_ritsuko_expression_reinforce_logical_v01.png` | EP003 |
| 穏やか圧 | `aizawa_ritsuko_expression_reinforce_gentle_pressure_v01.png` | EP003 |
| 流し顔 | `aizawa_ritsuko_expression_reinforce_pass_through_v01.png` | EP004 |
| 軽いうなずき | `aizawa_ritsuko_expression_reinforce_light_nod_v01.png` | EP004 |
| 依頼微笑 | `aizawa_ritsuko_expression_reinforce_request_smile_v01.png` | EP005 |
| 申し訳なさ風 | `aizawa_ritsuko_expression_reinforce_apologetic_v01.png` | EP005 |

## 先に入れるべき優先セット

すべてを一度に用意するより、まずはEP001試験編集版と前半5話の再利用効率が高いものから埋める方がよい。とくに、守屋守の観測系差分、クマ課長の圧差分、相沢律子の補強差分は、シリーズ前半の核になるため優先度が高い。

| 優先 | 先に揃えるファイル |
|---|---|
| 1 | `moriya_mamoru_expression_micro_stop_v01.png` |
| 2 | `moriya_mamoru_expression_fatigue_blank_v01.png` |
| 3 | `kuma_kacho_expression_pressure_sigh_v01.png` |
| 4 | `kuma_kacho_expression_pressure_soft_recheck_v01.png` |
| 5 | `aizawa_ritsuko_expression_reinforce_silent_v01.png` |
| 6 | `aizawa_ritsuko_expression_reinforce_soft_justify_v01.png` |
| 7 | `aizawa_ritsuko_expression_reinforce_request_smile_v01.png` |

## 運用メモ

この一覧は、あくまで `02_expression/` に入れる**想定ファイル名の基準表**である。実際に生成・採用した差分がこの一覧より少ない場合は、未使用の名前を無理に埋める必要はない。一方で、新規差分を追加する場合は、ここにある命名の粒度と語彙にそろえると、`reference` 側へ正式採用する際も整理しやすい。

また、`base` に近い意味を持つ差分でも、Zopia投入上は表情差分として扱う方が都合がよいものがあるため、本一覧では `02_expression/` 側に置く前提で整理している。基準立ち絵や基準顔そのものは従来どおり `01_base/` に置き、**感情やニュアンスの違いがあるものだけを `02_expression/` に入れる**運用で問題ない。
