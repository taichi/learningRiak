#太一による太一の為のRiak勉強会
基本的に太一が発表し太一が学習する為の場ですので、**お客様をお呼びする事はありません**。

参加希望者は、このREADME.mdに対してPull Requestをして下さい。

資料は[Wiki](https://github.com/taichi/learningRiak/wiki)に順次作成していきます。<br/>
参加希望があった時点で、編集権限を付加しますので、出来ればWikiに追記して下さい。<br/>
単に疑問をメモ書きするだけでもOKです。<br/>
一定量資料が貯まったら、日程調整を開始します。<br/>

## 参加条件

### 以下に挙げるドキュメントを全て読む事。
厳密に理解する必要は無く、どの辺にどんな内容が書かれていたか分かる程度でよいです。

* [An Introduction to Riak](http://wiki.basho.com/An-Introduction-to-Riak.html) 及び、このカテゴリ内のドキュメント
* [How Things Work](http://wiki.basho.com/How-Things-Work.html) 及び、このカテゴリ内のドキュメント

### riak_kvのmasterブランチを一通り読む事。
厳密に理解する必要は無く、どの様なファイル構成なのかや、どの様な機能がどの様なファイルに含まれているのか把握する程度で良いです。<br/>
Erlangの基本的文法に対する理解があれば読める筈です。<br/>
OTP, MochiWeb, Webmachineに関する理解が不足している事が原因で理解出来ない部分に関しては、[@voluntas](http://twitter.com/#!/voluntas)に勉強会の場で聞けば良いと思います。<br/>
事前にWikiに疑問を書いておくと、より妥当な回答が得られる筈です。<br/>

* https://github.com/basho/riak_kv.git

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
