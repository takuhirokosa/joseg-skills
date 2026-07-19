# joseg-skills

[English](README.en.md)

実際の仕事で検証してきたワークフローを、幅広い人が再利用できる形へ一般化したエージェントスキル集です。

## 公開中のスキル

| スキル | 内容 |
| --- | --- |
| `dev-log-to-article` | 開発ログや作業記録を、読者に役立つ再利用可能な解説記事へ変換します。 |
| `summarize-work-session` | 長時間の作業を、完了・変更成果物・未確認・次の作業に分けて引き継ぎ要約します。 |

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
