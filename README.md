# SAPIX フラッシュカード

SAPIX の学習用フラッシュカードアプリ。GitHub Pages で公開中。

**公開URL**: https://masakiplus.github.io/flashcard/

## 科目

| 科目 | URL | 内容 |
|------|-----|------|
| 国語 | `/kokugo/` | 漢字フラッシュカード（SM-2忘却曲線） |
| 算数 | `/sansu/` | 計算フラッシュカード（SM-2忘却曲線） |

## 特徴

- 外部依存ゼロの単一 HTML ファイル（科目ごと）
- スマートフォン対応（タップ操作）
- キャラクター「ハナちゃん」がクイズを出す
- SM-2アルゴリズムによる忘却曲線スケジューリング
- 「今日の復習」で期限到来カードをまとめて出題
- 学習データは localStorage に永続保存

## 問題の追加方法

各科目の `index.html` 内の `CARD_SETS` 配列にオブジェクトを追加する。

```javascript
// 国語（kokugo/index.html）
{
  name: "セット名",
  isReview: false,
  cards: [
    { sentence: "____に役立つ人になりたい", reading: "よ", answer: "世" },
  ]
}

// 算数（sansu/index.html）
{
  name: "セット名",
  isReview: false,
  cards: [
    { sentence: "640 − 158 + 36 = ____", reading: "3項→筆算2段", answer: "518" },
  ]
}
```

追加後は commit して push するだけで自動的に公開される。
