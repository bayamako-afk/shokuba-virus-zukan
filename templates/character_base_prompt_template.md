# Character Base Prompt Template

## 1. Purpose
このテンプレートは、**Zopiaに渡す前段階のキャラクター基準画像を ChatGPT image2 で固定するためのもの**である。顔、衣装、生活感、職場感の基準を少数の生成で安定させることを目的とする。

## 2. Master Prompt Structure
> A realistic Japanese office worker in contemporary Japan, natural live-action feel, grounded and relatable, not glamorous, subtle facial details, everyday clothing, believable office environment, restrained dramatic tone, black comedy atmosphere, realistic lighting, minimal stylization.

このベースに、下の各欄を埋めて人物ごとに調整する。

| Prompt Block | Content |
|---|---|
| Role | 例: junior office worker, systems administrator, mid-level manager |
| Age Impression | 例: late 20s, early 40s |
| Face Impression | 例: slightly tired eyes, polite but guarded expression |
| Hair | 例: neat short black hair, practical office hairstyle |
| Wardrobe | 例: affordable office casual, muted navy shirt, plain slacks |
| Physical Presence | 例: slightly hunched shoulders from daily stress |
| Mood | 例: quietly tense, enduring discomfort |
| Environment | 例: ordinary Japanese office desk area, fluorescent lighting |
| Realism Guardrail | 例: avoid fashion-magazine beauty, avoid anime style |

## 3. Office Base Prompt
> Create a realistic base portrait of a Japanese office worker for live-action drama preproduction. The person should look ordinary, believable, and slightly worn by workplace stress. Keep the visual tone grounded, realistic, and contemporary. Avoid glamour, fantasy, anime, exaggerated beauty, or stylized fashion aesthetics. Use a neutral office background with practical lighting.

## 4. Home Self-Defense Mode Prompt
> Create a realistic reference image of the same character at home after work, sitting at a small desk in a modest apartment room, opening a laptop and beginning to record an incident log. The mood should feel quiet, observant, and slightly uncanny, but still realistic and grounded in everyday life. Avoid sci-fi excess.

## 5. Expression Variation Prompt
> Generate expression variations for the same character while preserving face identity, hairstyle, wardrobe logic, and realism. Required expressions: neutral working face, slight discomfort, silent shock, suppressed frustration, analytical focus, quiet resolve.

## 6. Costume Variation Prompt
> Generate wardrobe variations for the same character with consistent identity. Include standard office look, slightly more formal meeting look, and casual at-home look. Keep colors muted and realistic for contemporary Japan.

## 7. Negative Guidance
| Avoid | Reason |
|---|---|
| Anime look | Breaks live-action realism |
| Fashion editorial beauty | Makes character feel less ordinary |
| Excessively cinematic lighting | Reduces office realism |
| Futuristic room design | Weakens the everyday setting |
| Extreme emotional acting | Hurts black-comedy subtlety |

## 8. Approval Criteria
採用する基準画像は、**実在しそうか、職場にいそうか、別カットでも再現しやすいか、Zopiaの参照素材としてブレが少ないか**を満たしている必要がある。さらに、**基準顔1、必要表情2〜3、必要なら帰宅後1**の範囲で足りるかを確認し、保険で差分を増やしすぎない。
