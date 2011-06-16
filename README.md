#太一による太一の為のRiak勉強会

参加希望者は、このREADME.mdに対してPull Requestをして下さい。

資料は[Wiki](https://github.com/taichi/learningRiak/wiki)に順次作成していきます。
参加希望があった時点で、編集権限を付加しますので、出来れば追記して下さい。
一定量資料が貯まったら、日程調整を開始します。

## 参加条件

### 以下に挙げるドキュメントを全て読む事。
但し厳密に理解する必要は無く、どの辺にどんな内容が書かれていたか分かる程度でよいです。

* [An Introduction to Riak](http://wiki.basho.com/An-Introduction-to-Riak.html) 及び、このカテゴリ内のドキュメント
* [How Things Work](http://wiki.basho.com/How-Things-Work.html) 及び、このカテゴリ内のドキュメント

### 太一が説明するRiakの機能不足を修正するパッチを勉強会終了後に作成し、bashoのRiakにpull requestを投げる事。
* REST API と PBC APIの機能差分 
 * REST APIでURLエンコードしてPUT/POSTするとサーバ側でURLデコードが為されない
 * 編集可能なBucketのプロパティがREST API と PBC APIにおいて大きな差分がある
 * PBC APIにおいてエラーコードが1しか存在しない。
* Pythonクライアント
 * Luwakサポートを追加する
 * MapReduce にKeyFilter対応を追加する
* Riakの処理中に原因の例外が発生する(match error等)と、小プロセスのみが死にスーパーバイザがクライアントにエラーを返さずタイムアウトする
 * MapReduce時はデータとの組み合わせ次第でRiak自体に問題が無くとも例外が発生するケースがある。

## 参加者
<table>
<tr><td>名前</td><td>twitter</td><td>GitHub</td></tr>
<tr><td>太一</td><td><a href="http://twitter.com/ryushi">@ryushi</a></td><td><a href="https://github.com/taichi">taichi</a></td></tr>
</table>
