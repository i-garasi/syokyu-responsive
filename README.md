### レスポンシブ対応、Sassの学習ステップ
- [ ]  メディアクエリの学習（Progate HTML/CSS 上級コース）
- [ ]  Sassの学習（Progate Sass 学習コース）
- [ ]  VScode上でSassを使用するために新たな拡張機能「Live Sass Compiler」を導入する
    - Sass形式(.scss)ではブラウザ上で読み込めないためCSS形式に変換（コンパイル）する必要がある
    - Sass形式(.scss)で書いたファイルをcss形式に変換して所定のディレクトリに適宜配置してくれる機能を持つ
- [ ]  [デザインコーディング課題初級](https://note.com/samuraibrass/n/n2108f5f03dd8) のレスポンシブ化

### 参考リンク
[Progate HTML & CSS 上級編](https://prog-8.com/lessons/html/study/3)

[Progate Sass I](https://prog-8.com/lessons/sass/study/1)

- Sassに関する概要とVSCode拡張機能Live Sass Compilerの導入に関する動画（導入解説は10:00~あたりから）
[Sassではじめる CSSプリプロセッサー #01：VS Codeの拡張機能で手軽にコンパイルしよう](https://www.youtube.com/watch?v=s9Z-kOzqwTw)

### Live Sass Compilerの初期設定
Live Sass Compilerは初期設定の状態だとsassディレクトリの直下にコンパイル後のCSSファイルとCSSとSassを結びつけるmapファイルを吐き出すように設定されているため以下の手順でcssディレクトリ配下にCSSファイルを吐き出すよう設定してください。

1. VSCode上で Command + Shift + P を入力
2. コマンドパレットにフォーカスが当たるので、検索欄で「setting.json」と入力してenter
3. プロジェクト常に.vscodeというディレクトリが作られ、中にsetting.jsonという空のファイルが生成される
4. setting.json内の { } の間に以下をコピペ

```
"liveSassCompile.settings.formats": [ //Sassの出力内容の設定
    {
      "format": "expanded", //nested、compact、compressedのどれかを選ぶ
      "extensionName": ".css", //style.cssとして出力
      "savePath": "/css" //cssフォルダの中にstyle.cssを出力
    }
  ],
  "liveSassCompile.settings.excludeList": [ //対象外とするフォルダを指定
    "**/node_modules/**",
    ".vscode/**",
    ".history/**"
  ],
  "liveSassCompile.settings.autoprefix": [ //ベンダープレフィックスの指定
    "last 2 versions",
    "ie >= 11",
    "Android >= 4",
    "ios_saf >= 8"
  ],
  ```

  5. watch sass でcssディレクトリ配下にstyle.cssとreset.cssが吐き出されることを確認

### ノーコードツールSTUDIOの学習ステップ
- [ ]  STUDIOの基本的な使い方を学習
- [ ]  STUDIOで初級・初級Exコーディング課題の再現

### 参考リンク
[ノーコードで超速WEB制作　STUDIO超入門コース](https://www.udemy.com/course/studio-for-beginners/)

- 下記は有料だが修了まででSTUDIOでのリッチなサイト制作手法を一通り網羅可能。またSTUDIOのUI上HTML・CSSを視覚的に捉えることができるため、HTMLとCSSの復習にもなる部分がある。
[ノーコードで超速WEB制作　STUDIO学習完全パック（初級〜上級編）](https://www.udemy.com/course/studio-complete-pack/)
