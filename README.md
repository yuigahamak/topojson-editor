topojson Editor
====

topojsonから必要な部分だけを切り取るツールです。
geojsonやtopojsonを公開してくれているありがたいプロジェクトがいくつもありますが、ファイルサイズが大きいなあって思ったので、
必要な部分だけを切り抜いてより軽量なtopojsonを作成することを目指します。

必要な機能
----

### topojsonの解析

#### 仕様

https://github.com/topojson/topojson/wiki/Specification.ja

arcsがデータの本体。
objectsにデータの内容が入っているのでこれを読み取る。

### データの切り取り

objectsの内容に従ってarcsから必要な部分だけを取り出す。

### データの表示、ダウンロード

データの表示はD3.jsにて。topojson=>geojsonの変換が必要。
jsonファイルを作成してダウンロード。

### TopoEditor ClassのIF
----

コンストラクタ。データを与える。

    new TopoEditor(topojson)

指定したgeometryを取り出し、objectを返す。

    topo.pickGeometry(index)



