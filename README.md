# SAPIX 漢字フラッシュカード

SAPIX 国語の漢字練習用フラッシュカードアプリ。GitHub Pages で公開中。

**公開URL**: https://masakiplus.github.io/kanji-flashcard/

## 特徴

- 外部依存ゼロの単一 HTML ファイル
- スマートフォン対応（タップ操作）
- キャラクター「ハナちゃん」がクイズを出す
- 覚えた・もう一回 の 2 択で学習進捗を管理
- 間違えたカードはデッキに戻って繰り返し出題

## カードセット

| セット | 問数 | 内容 |
|--------|------|------|
| 2026年4月 第3週 | 12問 | 通常の週次カード |
| 復習：まちがえた問題 | 15問 | うでだめし1・3で間違えた問題 |

## 問題の追加方法

`index.html` 内の `CARD_SETS` 配列にオブジェクトを追加する。

```javascript
{
  name: "セット名",
  isReview: false,   // 復習セットなら true
  cards: [
    { sentence: "____に役立つ人になりたい", reading: "よ", answer: "世" },
    // sentence: ____ が空欄になる問題文
    // reading:  ひらがなのヒント
    // answer:   正解の漢字
  ]
}
```

追加後は `index.html` を commit して push するだけで自動的に公開される。
