# God-s-View-AI-War-Visualizer
God-s-View-AI-War-Visualizer | 神の視点・AI-War-Visualizer

# AI War Visualizer | Civilization OS

**Civilization OS Calculator: AI War Visualizer**

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-red)](https://choiizuka.github.io/God-s-View-AI-War-Visualizer/)

> スライダーを右に動かすと、世界が壊れていく。
> これはゲームではない。AI軍事利用の危険を「見て感じる」ためのビジュアライザーだ。

---

## デモ / Live Demo

**https://choiizuka.github.io/God-s-View-AI-War-Visualizer/**

---

## 概要 / Overview

AI軍事利用率を1本のスライダーで操作すると、世界地図上で警告ノードの点滅・爆発・波紋・汚染の拡大がリアルタイムで変化し、同時にカウントダウンが加速する。

難しいパラメーターを読む必要はない。スライダーを動かすだけで「AIが戦争に使われる世界がどうなるか」が直感的に体感できる。

[神の視点 — Civilization OS Calculator](https://choiizuka.github.io/God-s-View-Civilization-OS-Calculator/) の視覚特化版。

---

## 操作方法 / How to Use

1. ページを開く
2. **AI Military Use** スライダーを右に動かす
3. 世界地図の上で何が起きるかを見る
4. 100% まで上げると何が起きるか確認する

---

## 入力 / Input

| パラメータ | 説明 |
|---|---|
| AI Military Use（0–100%） | AIが軍事・兵器に利用される度合い。唯一の入力変数。 |

---

## 出力 / Output

| 表示 | 説明 |
|---|---|
| Escalation Risk | 軍事エスカレーションの確率指標 |
| System Entropy | システムの無秩序・崩壊圧力 |
| Collapse Speed | カウントダウンの加速倍率 |
| Time Remaining | 現在の利用率が続いた場合の推計残存時間 |
| System Status | STABLE / CRITICAL / ESCALATION / COLLAPSE |

---

## 状態遷移 / System Status

| 状態 | 条件 | 意味 |
|---|---|---|
| **STABLE** | AI利用率 < 20% | AIが管理・制御された範囲内にある |
| **CRITICAL** | AI利用率 < 50% | 危険な領域に入り始めている |
| **ESCALATION** | AI利用率 < 80% | 制御を超えたエスカレーションが発生中 |
| **COLLAPSE** | AI利用率 ≥ 80% | システム全損。人間の介入では間に合わない |

---

## 計算ロジック / Calculation Logic

```
EscalationRisk   = (M/100)^1.4 × 100
SystemEntropy    = (M/100)^1.2 × 100
CountdownSpeed   = 0.1 + (M/100)^2 × 9.9
ExplosionRate/s  = 0.3 + M × 0.18
WarningNodeRate/s = 0.5 + M × 0.10
```

M = AI Military Use (0–100)

---

## 技術仕様 / Technical Specs

| 項目 | 内容 |
|---|---|
| 構成 | HTML + CSS + JavaScript（単一ファイル） |
| アニメーション | Canvas API（requestAnimationFrame） |
| 世界地図 | インラインSVG（外部依存なし） |
| 外部ライブラリ | なし |
| 対応環境 | モダンブラウザ全般 |
| ホスティング | GitHub Pages |

---

## このプロジェクトの位置づけ / Project Series

| バージョン | 内容 |
|---|---|
| [Civilization OS Calculator](https://choiizuka.github.io/God-s-View-Civilization-OS-Calculator/) | 6変数を操作して文明の状態を計算するエンジン版 |
| **AI War Visualizer（本作）** | AI軍事利用の危険を世界地図アニメで可視化した版 |
| Civilization OS Simulator（予定） | 時間発展・連鎖反応・複数変数の本格アニメーション版 |
| AI War Decision Simulator（予定） | 人間承認・誤爆率・エスカレーション連鎖を扱う拡張版 |

---

## 関連レポート・書籍 / Related Reports & Books

このVisualizerは以下の著作・レポートの思想に基づいている。

### 書籍
- **イランAI戦争 2026** — JP: https://amzn.to/4aYlXKL / EN: https://amzn.to/4rhrv7W
- **人類は必ず絶滅する 2026** — JP: https://amzn.to/4ryj2Nz / EN: https://amzn.to/4b7Vt9x
- **侵略の21世紀 2026** — JP: https://amzn.to/4sdzGU5 / EN: https://amzn.to/4bkJVPa

### GitHubレポート
- [The Paradox of Intelligence（イラン紛争AI軍事分析）](https://github.com/choiizuka/The-Paradox-of-Intelligence)
- [Eden Protocols — 反戦科学](https://github.com/choiizuka/Eden_Protocols-Anti-War_Scientific_Report)
- [人類絶滅の確率の超シンプルな証明](https://github.com/choiizuka/The-Simple-Proof-of-Human-Extinction-Probability)
- [AI Scheming 構造解析](https://github.com/choiizuka/Structural-Analysis-of-AI-Scheming)
- [全レポート一覧 (reports-index)](https://github.com/choiizuka/reports-index)

### 2026年宣言
- JP: https://choappceo.wordpress.com/2026/03/10/2026-manifesto-intelligence-ai-and-human-responsibility/
- EN: https://choiizuka.wordpress.com/2026/03/10/2026-manifesto-intelligence-ai-and-human-responsibility/

---

## 注記 / Note

このVisualizerは教育的デモであり、予言・予測・特定国家への攻撃意図を持つものではない。AI軍事利用のリスクを直感的に理解するための概念モデルである。

---

## 作者 / Author

**CHOIIZUKA (Toshihide Choiizuka)**

- Web JP: https://choappceo.wordpress.com/
- Web EN: https://choiizuka.wordpress.com/
- GitHub: https://github.com/choiizuka
- X: https://x.com/choiizuka
- Instagram: https://www.instagram.com/choiizuka/
- YouTube: https://youtube.com/@choiizuka/

---

*AI War Visualizer v1.0 — CHOIIZUKA 2026*
