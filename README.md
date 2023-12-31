# 推し乃介

"推し"の"スケ"ジュールを管理できる推し乃介です。

[「球団マスコットの情報。」](https://baseball-mascot.com)を公開するために作成したコードです。

複数の推しのスケジュールをまとめて管理、公開が出来ます。

## ファイルの構成

**index.html**

この場で閲覧できる：本日の予定(今日の予定のみを抽出して表示)

ボタンがある：スケジュールの一覧、推し別スケジュールなど

**profile.html**

推しごとにボタンがあり、推しのプロフィールページに飛ぶ形です。

**schedule.html**

カレンダーが表示されて、登録してあるデータをすべて閲覧できます。

**aboutus.html**

「このサイトについて」で飛びます。適当に使ってください。

**profile/name.html**

推しのプロフィールページは、profile/name.html の形で、サンプルのようなファイルを作れば、あとは data/oshi.json の内容に応じて表示されます。

**data/oshi.json**

推しの簡単なプロフィールをまとめるjsonです。

**data/schedule.json**

推しのスケジュールをまとめるjsonです。



## データの作り方

各種htmlファイルを編集し、jsonファイルを2つ作成することで利用できます。

1. マスコット自体の情報を data/oshi.json に入力する。
2. 各種 html ファイルを編集する。(index,profile,schedule,aboutus とキャラクター別のページ)
3. マスコットのスケジュールを data/schedule.json に入力する。

私は、Excel で json ファイルのもとを作成、変換して使用しています。(後日公開予定)

### oshi.json

**必須の項目**

search: いわゆる「略称」です。スケジュールなどに表示する名前と同じにしてください。

name：「アルファベット表記」です。html ファイルは、${name}.html という形にしてください。

full：「フルネーム」です。

**任意の項目**

team：「フルネーム(チーム名)」といった表示がされます。

url： URL を入力してください。デフォルトでは「公式プロフィール」というテキストで表示されます。

schedule：URL を入力してください。デフォルトでは「公式スケジュール」というテキストで表示されます。

blog：URL を入力してください。デフォルトでは「公式ブログ」というテキストで表示されます。

Twitter：URL を入力してください。デフォルトでは「Twitter」というテキストで表示されます。

Instagram：URL を入力してください。デフォルトでは「Instagram」というテキストで表示されます。

debut：「xxxx 年に登場」と表示されます。

no：「背番号は xx」と表示されます。

### schedule.json

**必須の項目**

date：日付 yyyy/mm/dd の形式

title：タイトル

character：data/oshi.json の"search"に登録した名前を用いると、プロフィールページにリンクされます。スラッシュで区切ることで、複数のキャラクターもプロフィールページにリンクができます。

**任意の項目**

remarks：備考です。デフォルトでは赤字で表示されます。

spot：「場所：xxxx」と表示されます。

lng：経度です。

lat：緯度です。※緯度経度にデータがあると、GoogleMap に接続します。

url1：URL を入力してください。url1 が存在する場合、「参考記事」というテキストでリンクが生成されます。

url2：URL を入力してください。先に url1 に入れてください。url2 は「参考記事 2」となります。

### html ファイル

それぞれ自由に編集が可能です。

### 画像

img ディレクトリに、oshi.json の"name"と同じ名前の name.jpg を入れておくことで、各キャラクターのプロフィールページに画像が表示できます。

## ライセンス

Copyright (c) 2023 geogra-geogra

Released under the MIT license

https://opensource.org/licenses/mit-license.php
