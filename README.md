# Minify images tool

[Squooshが開発終了したので、sharpを使って画像を一括最適化、ついでにSVGにも対応した](https://qiita.com/bananacoffee/items/d7a4b5cb4afff7efd162) を流用

## 導入方法

### 前提条件
- Node.js v18 up

### インストール方法
```bash
npm install
```

## 利用方法

- 画像圧縮

1. `images`ディレクトリに変換したい画像ファイルを配置する

2. run.batをダブルクリックする (Windows only)

    または、コマンドを実行する

    ```bash
    npm run image
    ```

    実行後、`outputs`ディレクトリに圧縮された画像が出力される

- ヘルプを表示

  ```bash
  $ node convertImage.mjs -h
  ```

## オプション

```bash
Options:
    -i, --input <string>   ソースディレクトリ（必須）
    -o, --out <string>     出力先ディレクトリ（必須）
    -m, --minify           画像の最適化を行う（同一拡張子での変換） (default: false)
    -w, --webp             webp化を行う (default: false)
    -a, --webp-suffix-add  webp化の際、拡張子を書き換え（false）するか追加（true）するか (default: false)
    -v, --svg              svgの最適化を行う (default: false)
    -z, --svgz             svgzを出力する (default: false)
    -n, --nosvg            svgzを出力した場合、svgは出力しない (default: false)
    -t, --truncate         出力先のディレクトリを空にする (default: false)
    -h, --help             display help for command
```

# Release Notes

| バージョン | リリース日   | 主な変更点       |
|----------|------------|-----------------|
| 1.0.0    | 2024-01-14 | 初回リリース      |
