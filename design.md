# LOCALIZE JAPAN — デザインシステム

このファイルはLOCALIZE JAPANのデザイン定義です。
新しいページやコンテンツを作る際は、このファイルをCursorに読み込ませてから指示を出してください。

---

## カラーパレット

| 変数名 | HEX | 用途 |
|---|---|---|
| `--main` | `#20c3ff` | メインカラー（ボタン・アクセント） |
| `--sky` | `#40d8ef` | グラデーション・背景 |
| `--yellow` | `#fff2ce` | グラデーション・背景 |
| `--text` | `#5a5a5a` | 本文テキスト |
| `--bg-soft` | `#f8f8f8` | 薄いグレー背景 |
| ピンク | `#ff58c2` | 強調テキスト（解決など） |
| ライトブルー | `#ccf7fe` | フロー背景 |

### グラデーション定義

```css
/* ヒーロー背景 */
background: linear-gradient(150deg, #40d8ef 3%, #fff2ce 98%);

/* サービスカード */
background: linear-gradient(110deg, #c8edfa 1%, #fff 31%, #fff2ce 100%);

/* フロー番号テキスト */
background: linear-gradient(-70deg, #ffd14d 32%, #62d5ff 74%);

/* Aboutセクション背景 */
background: linear-gradient(147deg, #f0f0f0 1%, #fff 45%, #f0f0f0 84%);
```

---

## タイポグラフィ

| 用途 | フォント | ウェイト | サイズ |
|---|---|---|---|
| 本文 | Noto Sans JP | 400 | 15–16px |
| 見出し（セクションタイトル） | Noto Sans JP | 300 | 30px |
| ヒーローコピー大 | Noto Sans JP | 900 | 60px |
| ヒーローコピー中 | Noto Sans JP | 700 | 28–34px |
| ボタン | Noto Sans JP | 700 | 24px |
| フロー番号 | Noto Sans JP | 800 | 32px |
| 注釈・小テキスト | Noto Sans JP | 400 | 12–14px |

```html
<!-- Google Fontsの読み込み -->
<link href="https://fonts.googleapis.com/css2?family=Noto+Sans+JP:wght@300;400;500;700;900&display=swap" rel="stylesheet">
```

---

## レイアウト

```css
/* スマホファーストの固定幅レイアウト */
.lp {
  width: 375px;
  margin: 0 auto;
  background: #fff;
  overflow: hidden;
}

/* セクション共通パディング */
.section {
  padding: 28px 24px;
}
```

- 基本幅：**375px**（スマホ基準）
- セクションパディング：**28px 24px**

---

## コンポーネント

### CTAボタン

```css
.cta-button {
  width: 288px;
  height: 54px;
  border: 2px solid #fff;
  border-radius: 27px;
  background: #20c3ff;
  color: #fff;
  font-weight: 700;
  font-size: 24px;
  letter-spacing: 0.08em;
  box-shadow: 0 6px 0 rgba(0, 0, 0, 0.12);
}
```

### サービスカード

```css
.service-card {
  border-radius: 6px;
  padding: 18px 16px;
  min-height: 127px;
  background: linear-gradient(110deg, #c8edfa 1%, #fff 31%, #fff2ce 100%);
}
```

### フロー番号（グラデーションテキスト）

```css
.flow-num {
  font-weight: 800;
  font-size: 32px;
  background: linear-gradient(-70deg, #ffd14d 32%, #62d5ff 74%);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
}
```

### ケースラベル

```css
.case-label {
  width: 145px;
  height: 24px;
  background: #20c3ff;
  color: #fff;
  font-size: 15px;
  display: grid;
  place-items: center;
}
```

---

## セクション構成

| セクション | 背景 | 備考 |
|---|---|---|
| Hero | グラデーション（スカイ→イエロー） | キャッチコピー＋CTA |
| Problem | `rgba(148,147,147,0.86)` グレー | 白テキスト |
| Solve Banner | グラデーション（スカイ） | 解決メッセージ |
| Capability | `#fff` | サービスカード4枚グリッド |
| Point | `#fffbde` | 3つのポイント |
| Before/After | `#f8f8f8` | 画像スライダー |
| Flow | `#ccf7fe` | 4ステップ |
| About | グラデーション（ライトグレー） | テキスト＋タグ |
| Contact | `#d2d1d1` | Googleフォーム埋め込み |
| Footer | `#626262` | コピーライト |

---

## ボイス＆トーン

- シンプルで直接的な日本語
- ターゲット：中国OEM商品を扱う日本の販売者・中国企業
- 専門的だが親しみやすいトーン
- 「売れる」「高く売れる」など成果を明示する表現を使う

---

## 新しいページを作るときのCursorへの指示例

```
@design.md を参照して、このデザインシステムに沿った
サービス詳細ページを作成してください。
カラーパレット・フォント・コンポーネントはdesign.mdに従ってください。
```
