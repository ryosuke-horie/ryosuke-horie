# Repository Guidelines

このリポジトリは GitHub プロフィールの README と静的アセットを管理します。変更は最小限に、Markdown に適した構成で、秘密情報は含めないでください。

## プロジェクト構成
- `README.md`: プロフィールページに表示される本体コンテンツ。
- `picture/`: 画像アセット。PNG/SVG 推奨、サイズは小さく保つ。
- 新規フォルダは `README.md` から参照が必要な場合に限定。

## ビルド・テスト・開発コマンド
- ローカルプレビュー: エディタで `README.md` を Markdown プレビュー（VS Code: 「Open Preview」）。
- Markdown Lint（任意）: `npx markdownlint-cli README.md` — 一般的なスタイル違反を検出。
- リンクチェック（任意）: `npx linkinator README.md` — 外部リンクの死活を検証。

## コーディング規約・命名
- Markdown: ATX 見出し（`#`, `##`）、Sentence case、簡潔な段落。バッジやリンクはリスト化。
- 画像: `picture/` 配下に配置し、`topic-descriptor.ext` で命名（例: `cloud-architecture.png`）。代替テキスト必須。
- 行: ソフトラップ推奨。長い URL はリンク化して可読性を確保。
- リンク/バッジ: HTTPS と安定ソースを使用。レイアウト目的のインライン HTML は最小限。

## テスト指針
- 実行時テストはありません。以下を確認:
  - `markdownlint` によるスタイル整合性（任意）。
  - プレビューでリンクと画像が正しく表示されること。
  - 外部ウィジェット（例: GitHub Stats カード）が崩れないこと。

## コミット・PR ガイドライン
- コミットは可能であれば Conventional Commits:
  - `docs:` README/コンテンツの更新
  - `chore:` アセットの移動/改名などの保守
  - `fix:` リンク切れ、タイポ、画像差し替え
- PR には以下を含める:
  - 目的と変更範囲の要約
  - レンダリング結果のスクリーンショット（必要に応じて Before/After）
  - 関連 Issue や背景コンテキスト

## セキュリティ・運用の注意
- 秘密情報や非公開 URL をコミットしない。
- 画像は `picture/` か信頼できる CDN に配置。脆弱なホットリンクは避ける。
- 画像は 1 枚あたり 300 KB 目安で軽量化し、プロフィール表示を高速に。

## エージェント向けメモ
- 原則として変更対象は `README.md` と `picture/` のみ。
- 既存セクションやバッジの順序は、明確な意図がある場合のみ変更する。
