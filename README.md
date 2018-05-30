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

### テキスト解析
テキスト解析では日本語の文章を形態素解析により分割して地域に関する名称、文章中のポジティブやネガティブ度合いをスコアに落としています。
ツィート文をこのテキスト解析プロセッサーに通せば、地域名称、好感度スコアなどを取得できます。
※ポジティブやネガティブ判定は研究用の辞書を利用しておりますがGithub上では公開しておりません。一応、辞書なしでも動作できるようにしておりますがスコアはすべて100と判定されます。

### コーヒーに関するSNS好感度リアルタイムエリア判定イメージ
上記のテキスト解析、位置情報なしのツィートを地図上へ落とす簡易ジオコードプロセッサーなどを利用して、リアルタイムに特定の人、モノ、商品などに対する好感度をエリア別に表示することが可能となります。ここではコーヒーに関するツィートの好感度判定の平均値をエリア別に表示している例になります。青いエリアほど好感度が高い、という判定です。
![コーヒーに関するSNS好感度リアルタイムエリア判定イメージ](https://github.com/EJHattori/gcf2018-geoevent-twitter/blob/master/images/sns_area_coffee_tokyo.JPG)

### 必要な資材などは？
Portal for ArcGIS, ArcGIS GeoEvent Processor, ArcGIS DataStore のセットアップが必要となります。
セットアップ方法は以下のサイトをご覧ください。
* http://enterprise.arcgis.com/ja/portal/latest/install/windows/welcome-to-the-portal-for-arcgis-installation-guide.htm
* http://enterprise.arcgis.com/ja/geoevent/latest/install/windows/installing-geoevent.htm
* http://enterprise.arcgis.com/ja/portal/latest/administer/windows/install-data-store.htm

### ArcGIS GeoEvent Server 管理画面イメージ
![ArcGIS GeoEvent Server 管理画面イメージ](https://github.com/EJHattori/gcf2018-geoevent-twitter/blob/master/images/geoevent_manager_sample.PNG)

## lightgeocode-processor
簡易ジオコードプロセッサー

## textanalysis-processor
テキスト解析プロセッサー

## License
MIT
