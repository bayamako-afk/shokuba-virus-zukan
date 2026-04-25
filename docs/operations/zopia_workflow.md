# 職場ウイルス図鑑 - Zopia Workflow

## 役割
Zopiaは主にアニメ版・実写風素材・シーンカット生成に使う。最終的な番組化はFlexClipで行う。

## 基本フロー
1. 脚本から必要カットを抽出する。
2. キャラクター固定要素を確認する。
3. 背景、表情、ポーズ、小物をリスト化する。
4. Zopia用英語プロンプトを作る。
5. 出力画像を確認し、必要なら差分を追加生成する。
6. FlexClip用にファイル名と配置を整理する。

## キャラクター固定
- 守谷守：中堅の日本人男性、情報システム担当寄り、カジュアル寄りオフィス服、疲労と困惑が出やすい。
- 相沢律子：スマートな女性管理職、冷静、政治力、一見デキる雰囲気。
- クマ課長：圧のある管理職、威圧感、ため息・丸投げに使いやすい。

## 推奨ファイルパス
```text
assets/ep001/characters/moriya_mamoru/base.png
assets/ep001/characters/aizawa_ritsuko/base.png
assets/ep001/characters/kuma_kacho/base.png
assets/ep001/backgrounds/office_morning.png
assets/ep001/effects/virus_aura.png
assets/ep001/title_cards/virus_title.png
```

## 注意
- 1話ごとにキャラが変わらないよう、基準画像・基準プロンプトを残す。
- Zopiaだけで完結させず、FlexClipで字幕・BGM・テロップを整える前提にする。
- 実写版は過度なCG感を避ける。
