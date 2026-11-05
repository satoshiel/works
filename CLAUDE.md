# CLAUDE.md

## プロジェクト概要

`works` は汎用Pythonワークスペースリポジトリです。
スクリプト、ツール、実験コードを格納します。

## 主要技術スタック

- **言語**: Python 3.x
- **パッケージ管理**: pip / uv / poetry（プロジェクト毎に選択）
- **コード品質**: Ruff（lint + format）
- **型チェック**: mypy / pytype
- **テスト**: pytest
- **仮想環境**: venv / .venv

## コーディング規約

- インデント: スペース4つ
- 最大行長: 88文字（Ruff デフォルト）
- 型アノテーションを積極的に使用する
- docstring は必要な関数・クラスにのみ記載（自明なものは省略）
- コメントは「なぜ」を書く（「何を」はコード自体で表現）

## よく使うコマンド

```bash
# 仮想環境の作成・有効化
python -m venv .venv
source .venv/bin/activate

# 依存パッケージのインストール
pip install -r requirements.txt

# Ruff でコードチェック
ruff check .

# Ruff で自動フォーマット
ruff format .

# テスト実行
pytest

# 型チェック
mypy .
```

## ディレクトリ構成

```
works/
├── CLAUDE.md          # このファイル
├── .claude/
│   ├── settings.json  # Claude Code 設定
│   ├── rules/         # Claude への指示ルール
│   └── skills/        # 再利用可能なワークフロー
└── docs/              # アドホック参照ドキュメント
```

## 参照ドキュメント

詳細なドキュメントは `@docs/ファイル名` で参照してください。
