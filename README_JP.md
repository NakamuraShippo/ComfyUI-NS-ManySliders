# ComfyUI-NS-ManySliders
ComfyUIで動作する、たくさんのスライダーで値を操作するノード

## 概要
ComfyUI-NS-ManySlidersは、ComfyUI用に開発されたカスタムノードで、複数のスライダーを用いて値を操作することができます。このノードを使用することで、簡単に多くの数値パラメータを直感的に調整でき、様々な用途に利用できます。

## 特徴
- 複数のスライダーを使用してパラメータの調整が可能。
- スライダーの数や範囲は設定ファイルで柔軟にカスタマイズ可能。
- 最低1個から最大設定数までスライダーを動的に追加できます。
- スライダー数が1の場合はシンプルな出力（1つの値のみ）を提供。

## ファイル構成
- nodes.py: ノードのメインロジックが実装されています。
- settings.yaml: スライダーの数、最小値、最大値、デフォルト値などの設定を管理するファイル。
- README.md: 本ファイル（ドキュメント）。
- __init__.py: NS_ManySlidersノードをComfyUIに登録するための初期化ファイル。

## インストール
1. このリポジトリをローカルにクローンします。
2. ComfyUIのカスタムノードディレクトリに配置してください。
3. 必要に応じてsettings.yamlファイルを編集し、スライダーの数や各種パラメータを設定します。

## 設定
- settings.yamlで以下の設定が可能です。
- count: スライダーの数（デフォルトは15）
- min_value: 各スライダーの最小値（例: -1.0）
- max_value: 各スライダーの最大値（例: 1.0）
- default_value: 各スライダーの初期値（例: 0.0）

## 使用方法
1. ComfyUI内で「NS_ManySliders」ノードを追加します。
2. slider_countパラメータで使用したいスライダーの数を指定します。
3. 各スライダーの値を調整することで、出力に反映されます。
4. slider_countが1の場合、単一の値が出力されます。それ以外の場合、スライダーの値がカンマで結合された形式で出力されます。

## 注意点
- slider_countが設定されたスライダーの最大数を超えないようにしてください。
- settings.yamlファイルの変更後はComfyUIを再起動する必要があります。

## 例
- slider_count = 1 の場合、出力は単一の値（例: "0.0"）になります。
- slider_count = 3 の場合、出力はカンマ区切りの文字列（例: "0.0,0.0,0.0"）になります。