# joseg-skills

[English](README.en.md)

実際の仕事で検証してきたワークフローを、幅広い人が再利用できる形へ一般化したエージェントスキル集です。

## 公開中のスキル

### 022｜`dev-log-to-article` — 開発ログを解説記事に変換

開発ログ、チャット履歴、作業メモ、Gitの変更履歴などを読み取り、単なる時系列の記録ではなく、第三者が学びに使える解説記事へ再構成します。

1. 実際に確認できた事実と、推測・未確認事項を分けます。
2. 読者が理解しやすいように、背景、課題、試したこと、解決方法、結果、学びの順に整理します。
3. 秘密情報、個人情報、環境固有のパスなど、公開に不要な情報を除去します。
4. タイトル、導入、見出し、手順、注意点を含むMarkdown記事として出力します。

開発の振り返り、技術ブログ、社内ナレッジ、トラブル解決記事の下書き作成に向いています。

### 009｜`summarize-work-session` — 長時間作業を引き継ぎ要約

長いチャットや複数工程にわたる作業を、次の担当者や別のエージェントがそのまま再開できる引き継ぎ文書へ変換します。

1. 作業目的と、最後に合意された対象範囲を特定します。
2. 「完了して実物確認済み」「実行したが未確認」「未着手」を明確に分けます。
3. 変更したファイル、URL、ブランチ、コミット、判断事項など、再開に必要な情報を残します。
4. 未解決事項と次に行う作業を、安全に実行できる順番で整理します。

長時間セッションの終了時、担当者交代、別AIへの引き継ぎ、翌日の作業再開前の状況整理に向いています。

## インストール

互換性のあるAgent Skillsインストーラーから、必要なスキルを指定して導入できます。

```bash
npx skills add takuhirokosa/joseg-skills --skill dev-log-to-article
```

```bash
npx skills add takuhirokosa/joseg-skills --skill summarize-work-session
```

## リポジトリ構成

各スキルは`skills/`配下の独立したフォルダにあり、必須ファイルとして`SKILL.md`を含みます。

```text
skills/
├── dev-log-to-article/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    └── references/
        └── article-structure.md
└── summarize-work-session/
    ├── SKILL.md
    └── agents/
        └── openai.yaml
```

## コントリビューション

新しいスキルの提案、既存スキルの改善、不具合修正、使用例や業種別知見の追加など、実際に利用者の役に立つIssue・プルリクエストを歓迎します。

## ライセンス

このリポジトリはGNU General Public License v3.0 only（`GPL-3.0-only`）で提供します。詳細は[LICENSE](LICENSE)をご確認ください。
