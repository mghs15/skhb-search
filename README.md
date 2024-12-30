# skhb-search
指定緊急避難場所の簡易検索用ツール

国土地理院が提供している[指定緊急避難場所等の CSV データ](https://www.gsi.go.jp/bousaichiri/hinanbasho.html)の中身を簡易的に検索するためのツールです。

まだ実装が甘い部分があるかもしれませんので、使用するときは**自己責任**でお願いいたします。

## 使い方
新バージョン（新形式データ・指定避難所データに対応）
* Maplibre 版 https://mghs15.github.io/skhb-search/index-maplibre-v2.html

1. まずは手元に指定緊急避難場所等の CSV データ（国土地理院提供の CSV と同形式）を準備する。
2. ツール（index.html 等）を開いて、CSV データをアップロード。
3. 各種条件を調整して、「絞り込み」ボタンを押す。

旧来バージョン
* Maplibre 版 https://mghs15.github.io/skhb-search/index-maplibre.html
* Leaflet 版 https://mghs15.github.io/skhb-search/

※旧来バージョンでは、新形式データ・指定避難所データには対応していません。

## 特長
* CSV の行全体と一部（施設・場所名 or 住所）を対象として文字列検索（正規表現利用可）
* 種別ごとの絞り込みも可
* CSV （ヘッダー付き）で出力可能
* 地図への表示・範囲での絞り込みも可能

## Reference
* 指定緊急避難場所（国土地理院）https://www.gsi.go.jp/bousaichiri/hinanbasho.html
 * サンプルデータは以下のものをホストしています。
   * 新バージョンについては 2024/12/23 公開のもの（指定緊急避難場所・指定避難所）
   * 旧来バージョンについては 2023/12/13 公開のもの（指定緊急避難場所）

### Leaflet 版
* Leaflet https://leafletjs.com/
* Leaflet.markercluster https://github.com/Leaflet/Leaflet.markercluster
* Leaflet.heat https://github.com/Leaflet/Leaflet.heat
* 地理院タイル https://maps.gsi.go.jp/development/ichiran.html

### Maplibre 版
* MapLibre GL JS https://github.com/maplibre/maplibre-gl-js
  * https://maplibre.org/maplibre-gl-js-docs/example/cluster/
  * https://maplibre.org/maplibre-gl-js-docs/example/heatmap-layer/
* 国土地理院最適化ベクトルタイル https://github.com/gsi-cyberjapan/optimal_bvmap
