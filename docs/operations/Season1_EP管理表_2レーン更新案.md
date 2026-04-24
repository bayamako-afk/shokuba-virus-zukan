# Season1 EP管理表 2レーン更新案

## 1. 目的

本書は、Season 1 の話数管理を **単線進行表から「1EP内にアニメ版 / 実写版の2レーンを持つ管理表」へ更新するための設計案**を示す。今回の方針転換により、進捗確認の単位は「作品1本」ではなく「EP単位の兄弟プロジェクト2本」になるため、管理軸の再設計が必要である。

## 2. 基本構造

管理表は、**1行 = 1EP** を維持したまま、その内部に **共通脚本・アニメ版・実写版・公開結果** を並列で持つ構造へ変える。別表に分けるよりも、同一EPの両レーンが横並びで見える方が、制作判断・公開判断・比較レビューがしやすい。

| 管理単位 | 方針 |
|---|---|
| 行 | EP単位 |
| 列 | 共通脚本、アニメ版、実写版、公開比較 |
| 優先の見方 | まず共通脚本、次に実写版、次にアニメ版、最後に公開反応を見る |

## 3. 推奨列構成

以下の列を基本セットとして採用する。これにより、脚本準備から2レーン生成、公開比較までを1枚で追える。

| 列名 | 役割 |
|---|---|
| `ep_no` | EP番号 |
| `title` | タイトル |
| `virus_name` | ウイルス名 |
| `common_script_status` | 共通脚本の進捗 |
| `anime_project_name` | アニメ版プロジェクト名 |
| `anime_status` | アニメ版進捗 |
| `liveaction_project_name` | 実写版プロジェクト名 |
| `liveaction_asset_status` | 実写版の基準素材準備状況 |
| `liveaction_status` | 実写版進捗 |
| `first_gen_result` | 初回生成の総評 |
| `fix_needed` | 修正要否 |
| `release_status` | 公開状況 |
| `comparison_memo` | 比較視聴・反応メモ |

## 4. ステータス値の考え方

各列の値は自由記述にしすぎず、短い定義済み語でそろえる方がよい。とくにアニメ版・実写版の進捗は、話数が増えるほど表記ゆれが障害になる。

| 列 | 推奨値例 |
|---|---|
| `common_script_status` | `not_started` / `drafted` / `fixed` |
| `anime_status` | `not_started` / `prompt_ready` / `generated` / `fixing` / `ready_to_release` / `released` |
| `liveaction_asset_status` | `not_started` / `base_ready` / `uploaded` / `entity_linked` / `diff_added` |
| `liveaction_status` | `not_started` / `prompt_ready` / `generated` / `fixing` / `ready_to_release` / `released` |
| `first_gen_result` | `good` / `mixed` / `failed` |
| `fix_needed` | `none` / `anime_only` / `liveaction_only` / `both` |
| `release_status` | `not_scheduled` / `paired_release_ready` / `released` |

## 5. EP001〜EP005の初期反映イメージ

現時点の整備状況を前提にすると、初期入力は次のような粒度が扱いやすい。ここでは厳密な完了判定よりも、二層構造へ移行するための見え方を優先している。

| ep_no | title | virus_name | common_script_status | anime_project_name | anime_status | liveaction_project_name | liveaction_asset_status | liveaction_status | first_gen_result | fix_needed | release_status | comparison_memo |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| EP001 | 朝のため息 | ため息ウイルス | fixed | EP001_tameiki_virus_anime | not_started | EP001_tameiki_virus_liveaction | uploaded | prompt_ready | mixed | both | not_scheduled | 実験結果を受けて2レーン運用へ移行 |
| EP002 | 未確定 | 差し戻し確認ウイルス想定 | drafted | EP002_sashimodoshi_confirm_virus_anime | not_started | EP002_sashimodoshi_confirm_virus_liveaction | not_started | not_started | not_started | none | not_scheduled | 命名キー確定後に更新 |
| EP003 | 未確定 | 責任転嫁系候補 | drafted | EP003_placeholder_anime | not_started | EP003_placeholder_liveaction | not_started | not_started | not_started | none | not_scheduled | 仮キー運用中 |
| EP004 | 未確定 | 口頭指示系候補 | drafted | EP004_placeholder_anime | not_started | EP004_placeholder_liveaction | not_started | not_started | not_started | none | not_scheduled | 仮キー運用中 |
| EP005 | 未確定 | 無言差し戻し系候補 | drafted | EP005_placeholder_anime | not_started | EP005_placeholder_liveaction | not_started | not_started | not_started | none | not_scheduled | 仮キー運用中 |

## 6. 実務での使い方

この管理表では、毎回まず `common_script_status` を見て、両レーンの共通核が確定しているかを判断する。そのうえで、実写版では `liveaction_asset_status` と `liveaction_status` を確認し、アニメ版では `anime_status` を追う。最後に `first_gen_result`、`fix_needed`、`comparison_memo` を見れば、同時公開へ進めるかどうかを判断できる。

## 7. 更新ルール

更新は、**EP単位でまとめて触る**のが原則である。たとえばEP001で実写版だけ進んだ場合でも、同時にアニメ版列も確認し、比較公開の準備として空欄や停滞がないかを見る。これにより、片レーンだけが走って全体の企画価値が見えなくなる状態を防げる。

## 8. 次段階の発展余地

将来的には、この管理表をもとに公開日、サムネイル案、反応比較、勝ちパターン分析などの列を追加できる。ただし現段階では、まず **共通脚本 / アニメ版 / 実写版 / 公開比較** の4ブロックを安定運用できることを優先する。

## 9. ひとことでまとめ

話数管理は、**1EPの横にアニメ版と実写版を並べる2レーン表**へ切り替える。別々に追うのではなく、同一EPの兄弟プロジェクトとして横並びで管理することが、今回の方針転換に最も適している。
