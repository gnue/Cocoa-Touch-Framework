### 概要

XcodeでiOS用のFrameworkプロジェクト（ただし静的ライブラリ）をつくるテンプレート

* Xcode 3 でのみテンプレートとして使用できます

### 使い方

1. ~/"Library/Application Support/Developer/Shared/Xcode/Project Templates" に適当なディレクトリ（例 iOS）をつくってこのテンプレートをコピー
2. Xcodeのファイルメニューから新規プロジェクトを選択、User TemplateでCocoa Touch Frameworkが表示されるので選択
3. lib〜ターゲットにコンパイルするライブラリのソースコードを登録
4. 赤い標的マークのターゲットの「ファイルをコピー」フェーズに Framework の Headers に追加するヘッダファイルを追加
5. 赤い標的マークでビルドするとデバイスとシミュレータのユニバーサルバイナリの Framework が作成されます

### ビルド設定

既に静的ライブラリをビルドするプロジェクトがある場合は次のビルド設定を変更することにより Framework の生成だけこのテンプレートでビルドすることができます

* SOURCE_PROJECT_NAME　… 静的ライブラリをビルドするプロジェクトファイルの名前（拡張子は不要）
* SOURCE_TARGET_NAME　… 静的ライブラリをビルドするターゲットの名前
* SOURCE_LIB_NAME　… ビルドされた静的ライブラリの名前

なお、対象となるプロジェクトファイルとは同じフォルダに置く必要があります
