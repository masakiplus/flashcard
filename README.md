# SAPIX 漢字フラッシュカード

SAPIX 国語の漢字練習用フラッシュカードアプリ。GitHub Pages で公開中。

**公開URL**: https://masakiplus.github.io/kanji-flashcard/

## 特徴

- ES5 互換・外部依存ゼロの単一 HTML ファイル
- スマートフォン対応（タップ操作）
- 知らない・知ってる の 2 択で学習進捗を管理

## データの追加方法

`index.html` 内の `var CARD_SETS` 配列を編集する。

```javascript
var CARD_SETS = [
  {
    name: "セット名",
    cards: [
      { front: "漢字", back: "読み・意味" },
      // ...
    ]
  }
];
```

追加後は `index.html` を commit して push するだけで自動的に公開される。
