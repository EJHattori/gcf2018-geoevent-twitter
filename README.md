# gcf2018-geoevent-twitter
GISコミュニティフォーラム2018年GeoEventデモ用

## 概要
SNSにより人、モノ、商品などに対する好感度をリアルタイムに測定して地図上に可視化します。
これにより特定の商品やサービスなどのイメージをビジュアルに地図上で把握することが可能となります。
2018年5月末に開催されましたGISコミュニティフォーラムにてデモ展示しました内容を一部公開します。

### Twitter 上の位置情報タグなしのツィートを拾うには？
ところでTwitter上で位置情報タグ付きのツィートは日本では全体数パーセント程度で非常に少ないのが現実です。
そこで位置情報がないツィートも文章中に地域に関する名称などが含まれていた場合に簡易ジオコード機能にて座標に落とす試みをしてみました。
本レポジトリで公開している簡易ジオコードプロセッサーでは大字レベルまでのジオコードを行っています。

### ArcGIS GeoEvent Server 管理画面イメージ
![ArcGIS GeoEvent Server 管理画面イメージ](https://github.com/EJHattori/gcf2018-geoevent-twitter/blob/master/images/geoevent_manager_sample.PNG)

## lightgeocode-processor
簡易ジオコードプロセッサー

## textanalysis-processor
テキスト解析プロセッサー

## License
MIT
