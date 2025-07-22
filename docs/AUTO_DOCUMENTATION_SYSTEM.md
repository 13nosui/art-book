# 🤖 自動ドキュメント読み込みシステム

## 概要

指示内容から関連ドキュメントを自動判定し、実装前に必要なガイドラインを自動読み込みするシステム。

## 📋 ドキュメント分類とマッピングルール

### 🎨 UI/デザイン関連
**判定キーワード:** `UI`, `コンポーネント`, `デザイン`, `HeroUI`, `Button`, `Input`, `Card`, `Form`, `レイアウト`, `スタイル`

**自動読み込みドキュメント:**
- `DESIGN_GUIDELINE.md` - HeroUI使用ルール・デザイントークン
- `docs/AI_IMPLEMENTATION_RULES.md` - AI実装時の絶対禁止事項
- `docs/components/component-catalog.md` - 利用可能コンポーネント一覧
- `.cursorrules` - Cursor開発ガイドライン

### 🔒 セキュリティ関連
**判定キーワード:** `認証`, `auth`, `セキュリティ`, `バリデーション`, `XSS`, `CSRF`, `Firebase Auth`, `NextAuth`

**自動読み込みドキュメント:**
- `docs/SECURITY_IMPLEMENTATION.md` - セキュリティ実装ガイド
- `docs/SECURITY_OPERATIONS.md` - セキュリティ運用ルール
- `SECURITY.md` - 全般的なセキュリティポリシー
- `src/lib/validation.ts` - バリデーション実装例

### 🛠️ API/バックエンド関連
**判定キーワード:** `API`, `Firebase`, `Firestore`, `Storage`, `サーバー`, `データベース`, `CORS`

**自動読み込みドキュメント:**
- `docs/api/README.md` - API実装ガイド
- `docs/generated/api-endpoints.md` - API仕様書
- `src/lib/firebase.ts` - Firebase設定例
- `src/lib/api-client.ts` - API クライアント実装

### 🔄 リファクタリング関連
**判定キーワード:** `リファクタリング`, `修正`, `最適化`, `改善`, `変更`, `更新`

**自動読み込みドキュメント:**
- `docs/REFACTORING_GUIDE.md` - リファクタリング手順
- `docs/AI_IMPLEMENTATION_RULES.md` - 実装ルール
- `DESIGN_GUIDELINE.md` - デザイン準拠ルール

### 📝 新機能開発関連
**判定キーワード:** `新機能`, `追加`, `作成`, `実装`, `開発`, `機能`

**自動読み込みドキュメント:**
- `docs/AI_IMPLEMENTATION_RULES.md` - 実装ルール
- `DESIGN_GUIDELINE.md` - デザインガイドライン
- `.cursorrules` - 開発フロー
- `docs/project-overview.md` - プロジェクト全体像

### 🐛 バグ修正関連
**判定キーワード:** `バグ`, `エラー`, `修正`, `問題`, `不具合`, `fix`

**自動読み込みドキュメント:**
- `docs/AI_IMPLEMENTATION_RULES.md` - 実装ルール
- `docs/REFACTORING_GUIDE.md` - 修正手順
- `.cursorrules` - デバッグフロー

## 🔄 自動実行フロー

### 1. 指示解析
```
指示内容を解析 → キーワード抽出 → 関連カテゴリ判定
```

### 2. ドキュメント自動読み込み
```
カテゴリに応じた必須ドキュメントを並列読み込み
```

### 3. 実装前確認
```
読み込んだガイドラインに基づく実装計画の作成
```

### 4. 実装実行
```
ガイドライン準拠の実装実行
```

## 📚 優先度別ドキュメント

### 🔴 高優先度（必ず読み込み）
- `docs/AI_IMPLEMENTATION_RULES.md` - **全実装で必須**
- `DESIGN_GUIDELINE.md` - **UI関連で必須**
- `.cursorrules` - **開発フロー必須**

### 🟡 中優先度（カテゴリ該当時）
- `docs/SECURITY_IMPLEMENTATION.md`
- `docs/REFACTORING_GUIDE.md`
- `docs/api/README.md`

### 🔵 低優先度（補完情報）
- `docs/project-overview.md`
- `docs/generated/` 配下の自動生成ドキュメント

## 💡 実装例

### 指示例1: "HeroUIのButtonコンポーネントを使ってログインフォームを作成"

**自動読み込み:**
- `DESIGN_GUIDELINE.md` (HeroUI使用ルール)
- `docs/AI_IMPLEMENTATION_RULES.md` (実装ルール)
- `docs/SECURITY_IMPLEMENTATION.md` (認証セキュリティ)
- `docs/components/component-catalog.md` (Button仕様)

### 指示例2: "APIの入力値バリデーションを強化"

**自動読み込み:**
- `docs/SECURITY_IMPLEMENTATION.md` (バリデーション実装)
- `docs/AI_IMPLEMENTATION_RULES.md` (実装ルール)
- `docs/api/README.md` (API実装ガイド)
- `src/lib/validation.ts` (実装例)

## ⚙️ 設定

このシステムは Claude AI による自動判定で動作し、指示を受けた際に関連ドキュメントを自動的に読み込んでから実装を開始します。

**メリット:**
- 🎯 ガイドライン準拠の確実性向上
- ⚡ 指示の簡素化（"〇〇ドキュメントに従って"が不要）
- 🔄 一貫性のある実装品質
- 📚 ドキュメント活用率の向上