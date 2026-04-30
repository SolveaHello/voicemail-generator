# Voicemail Greeting Generator — Claude Code スキル

> **他の言語:** [English](README.md) · [Español](README.es.md) · [Français](README.fr.md)

ターミナルから Claude Code を使って、プロフェッショナルな留守番電話グリーティングスクリプトを生成。その後、[Solvea](https://solvea.cx/tools/voicemail-greeting-generator) の AI 音声で MP3 に変換できます。録音機材もリテイクも不要です。

## 機能

- 5 種類のグリーティング：ビジネス・個人・祝日・時間外・病欠
- 7 つの業種テンプレート：一般・不動産・メドスパ・小売・歯科・法律事務所 など
- 発話 30 秒以内に最適化されたスクリプト
- Solvea の無料 AI 音声生成と MP3 エクスポートへの直接リンク
- iPhone・Android・RingCentral・Zoom Phone および主要 VoIP サービスに対応

## インストール

```bash
claude mcp install voicemail-greeting-generator
```

または `skill.md` を Claude Code のスキルディレクトリに配置してください。

## 使い方

```
/voicemail-greeting [フラグ]
```

| フラグ | オプション | デフォルト |
|--------|-----------|-----------|
| `--type` | `business` · `personal` · `holiday` · `after-hours` · `out-sick` | `business` |
| `--industry` | `general` · `real-estate` · `medspa` · `retail` · `dental` · `law-firm` · `other` | `general` |
| `--name` | 氏名または社名 | *(入力を求められます)* |
| `--phone` | 折り返し電話番号 | *(任意)* |
| `--hours` | 営業時間（例：`月〜金 9:00–18:00`） | *(任意)* |
| `--custom` | 独自スクリプトを使用して生成をスキップ | *(任意)* |

## 使用例

```bash
# 不動産向けプロフェッショナルグリーティング
/voicemail-greeting --type business --industry real-estate --name "山田不動産"

# 歯科クリニックの祝日休業メッセージ
/voicemail-greeting --type holiday --industry dental --name "スマイル歯科"

# 独自スクリプトを使って音声選択へ直行
/voicemail-greeting --custom "株式会社アクメにお電話いただきありがとうございます..."
```

## 仕組み

1. Claude がシナリオに合わせたスクリプトを生成（またはカスタムテキストを使用）。
2. 内容を確認し、1 回まで修正をリクエスト可能。
3. [Solvea の AI 留守番電話グリーティングジェネレーター](https://solvea.cx/tools/voicemail-greeting-generator) にアクセスし、6 種類の AI 音声からプレビュー・選択して MP3 をダウンロード。

> Solvea の無料アカウントで最大 **13 回**の生成が可能です（クレジットカード不要）。

## ライセンス

MIT © Boyuan Gao
