# Task Board Project

## Overview

タスク管理ボードアプリケーション。

## Git 運用ルール

### 基本方針

コードを変更するたびに、必ず GitHub にプッシュすること。

### ワークフロー

1. コードを変更・編集する
2. 変更内容を確認する: `git diff`
3. 変更をステージング: `git add <files>`
4. コミットを作成する: `git commit -m "<message>"`
5. GitHub にプッシュする: `git push origin <branch>`

### コミットメッセージ規則

- 日本語・英語どちらでも可
- 変更内容を簡潔に記述する
- 例: `feat: タスク追加機能を実装`, `fix: 削除ボタンのバグを修正`

### ブランチ運用

- `main`: 本番相当の安定ブランチ
- 機能追加・バグ修正は `main` に直接コミットしてよい（小規模プロジェクトの場合）

### 注意事項

- `.env` や認証情報を含むファイルは絶対にコミットしない
- コミット前に `git status` で意図しないファイルが含まれていないか確認する
- プッシュは `git push` で毎回実行する（変更を GitHub に反映させること）

## Development Commands

```bash
# 依存関係のインストール
npm install

# 開発サーバー起動
npm run dev

# ビルド
npm run build

# テスト
npm test
```

## Code Style

- コメントは原則不要。変数名・関数名で意図を表現する
- セキュリティ上の懸念（XSS、SQLインジェクション等）がある実装は避ける
- 不要な抽象化・過剰設計はしない
