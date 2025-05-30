
# Week 1 Detailed Task Sheet (Day 1 – Day 7)

**Goal for Week 1**  
MT4 環境を最新ビルドに更新し、MQL4 基礎とストラテジーテスター操作を“手が覚える”ところまで復習する。

---

## Day 1 – MT4 アップデート & ヒストリカル準備

| Step | Action | Tip / Check |
|------|--------|-------------|
| ★1 | **管理者として MT4 を起動** | *Journal* に `terminal started` が出れば OK |
| ★2 | **ビルド番号確認**<br>ヘルプ → バージョン情報 | 2025‑05 現在 **build 1420+** が最新 |
| ★3 | **最速データセンター選択**<br>右下バーを右クリック | 緑バー点滅 & 転送 KB が更新 |
| ★4 | **History Center** → `Forex ▶ USDJPY ▶ H1` を選び **Download** | `H1: xxxx records loaded` が出るまで待機 |
| ☆5 | **データフォルダを ZIP でバックアップ**<br>ファイル → データフォルダを開く | `MQL4` と `profiles` を保存 |

---

## Day 2 – GitHub リポジトリ設定

| Step | Action | Output |
|------|--------|--------|
| ★1 | GitHub で **Private repo `MyStableEA`** を作成 | URL 例: `https://github.com/you/MyStableEA.git` |
| ★2 | データフォルダ直下で `git init` → `git remote add origin` | `.gitignore` に `logs/` 追加 |
| ★3 | `README.md` に目的&完了条件を記述 | commit: `init` |
| ☆4 | `docs/` フォルダ & `今週のメモ.md` 追加 | 週末レビュー用 |

---

## Day 3 – サンプル EA を読み解く

| Step | Action | Focus |
|------|--------|-------|
| ★1 | `Moving Average.mq4` を MetaEditor で開く | 構造を俯瞰 |
| ★2 | **OnInit/OnTick/OnDeinit** を手書きメモ | 流れを掴む |
| ★3 | コンパイル → チャート適用 | *Experts* タブでログ確認 |
| ☆4 | `Print()` 挿入で値を出力 | ログ読み練習 |

---

## Day 4 – 自作 EA 雛形

| Step | Action | Output |
|------|--------|--------|
| ★1 | MetaEditor → 新規 EA テンプレート | `TemplateEA.mq4` |
| ★2 | `#property strict` 追加 | 厳格モード |
| ★3 | 外部入力（Lots, SL, TP）追加 | コンパイル通過 |
| ☆4 | commit: `feat: add template` | - |

---

## Day 5 – RSI クロス EA (≤100行)

| Step | Action | Output |
|------|--------|--------|
| ★1 | `RSICrossEA.mq4` 新規作成 | - |
| ★2 | ロジック: RSI 30↑買い / 70↓売り | - |
| ★3 | `OrderSend` 戻り値チェック & `Print()` | 安定ログ |
| ★4 | H1 チャートで動作確認 | シグナルログ |
| ☆5 | パラメータ化 & 再コンパイル | commit |

---

## Day 6 – 初回バックテスト

| Step | Action | Setting |
|------|--------|---------|
| ★1 | Strategy Tester → Every tick | USDJPY / H1 / 2020‑01‑01〜2024‑12‑31 |
| ★2 | テスト → `Report_RSICross.html` 保存 | PF / DD 確認 |
| ☆3 | エクイティグラフを画像保存 | Git LFS 推奨 |

---

## Day 7 – 週次レビュー

| Step | Action | Deliverable |
|------|--------|-------------|
| ★1 | Notion/Markdown: 成績・改善点まとめ | 週次レポ |
| ★2 | GitHub Issues: 改良タスク登録 | #1, #2 … |
| ☆3 | コードを微リファクタ & commit | Clean commit |

---

### ポモドーロ推奨
25 min 作業 + 5 min 休憩 × 2 セットで 1 h 消化。

### 完了チェック
- `USDJPY H1` データ取得済み  
- `TemplateEA.mq4` & `RSICrossEA.mq4` コンパイル成功  
- 初回バックテストレポート保存  
- 週次レポート & GitHub Issues 登録

---

これで Week 1 の準備は完了です。  
Week 2（戦略設計 & リスク計算）に進む前に、疑問点があればメモしておきましょう。
