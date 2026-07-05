# ramen-ai（らぁ麺 玄 -GEN-）

- これは何: L1「AI受付付きHP」事業の業種別営業デモ。架空のラーメン店サイト（index.html 1枚・静的・ルールベースAI店員、英語対応あり）
- 本番URL: https://richend0913.github.io/ramen-ai/
- デプロイ: GitHub Pages。`git push origin main` で自動反映（数分かかる）。Cloudflare/wranglerは使わない
- 触ってはいけないもの:
  - 架空店の明記（title / meta description / footer / AI注記 / 住所・電話の「架空」表記）を弱める・消す変更
  - 実績・レビュー・数字の捏造（「行列のできる」等は架空デモ内の演出。実案件テンプレ流用時は店主提供の事実のみ）
  - `noindex,nofollow` の解除（デモは検索に載せない）
  - AI店員の免責文言（アレルギー断定しない・注文確定しない）
- 修正時に読むスキル: `next-growth-ops` → `ai-employee-site`（references/design-system.md 含む）
- 品質ゲート: `visual-qa` スキルで 375px viewport（iPhone実寸、full-pageスクショ不可）確認。写真の差替は必ず「curlでDL→Readで目視→assets-manifest.md に記録」してから（Phase 2.5）
- 計測: GA4 `G-63VB4HT3T2`（実プロパティか要オーナー確認。差し替えは index.html head の1箇所）。イベント= `ai_open`（AI店員起動）/ `generate_lead {method:'demo'}`（宣伝LPへのリンククリック）
- 導線: footer とAI店員チップ「このHPを自分の店にも」→ https://richend0913.github.io/ai-uketsuke-lp/（utm付き）
- og.png: `og-template.html` を1200x630でスクショして直下に `og.png` を置く（未生成ならogプレビューは出ない）
