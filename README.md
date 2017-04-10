# Liftim用教科定義データ

Liftim用教科定義データは、Liftim時間割の教科一覧や教科ごとのテーマ色を設定するもので、[JSON](http://json.org/)で記述されています。
定義データは`subjects.json`です。まだ色を決めていないものは一時的に`COLOR_DEF`という文字列を入れてあります。
また、`material_color.json`はマテリアルデザインガイドラインの[Color palette](https://material.io/guidelines/style/color.html#color-color-palette)で示された色と`RGB`の対応をJsonArrayのデータとして保存しています（このファイルは`MaterialDesignLite`から生成しました）。

## 教科定義を追加するにあたって
教科定義を追加するにあたって、`subjects.json`のフォーマットを示しておきます。
次のコードをご覧ください：
```
[
  {
    "subject": "国語",
    "shortSubject": "国語",
    "color": "red"
  },
  {
    "subject": "現代社会",
    "shortSubject": "現社",
    "color": "yellow-800"
  }
]

```
これは`subjects.json`の内容の一部を取り出したものです。ルートはJSONArrayです。その中にJSONObjectが列挙されているフォーマットになっています。`subject`、`shortSubject`、`color`の要素がありますが、それぞれの内容は次の表をご覧ください。

キー | 概要 | 型
---- | ---- | ----
`subject` | 教科の正式な名称 | `String`
`shortSubject` | 教科の略名 | `String`
`color` | ColorPaletteで定義されている色 | `String`

※キーの順番はデータの読み取りに全く影響がありません。
もしColorPalleteにない定義をした場合はLiftimは未定義の色として内部的に決められた色を使用します。
