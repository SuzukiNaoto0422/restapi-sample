## RESTful APIの仕様

大きな更新がある場合はSlackチャンネルにてお知らせします!

もしここ改善すべき？という点があれば教えて下さい！

## APIの概要

ユーザーを管理する機能をもったAPIを作成してください。  
仕様書は下記です。  
https://raisetech-for-student.github.io/restapi-sample/

### データベース定義

|カラム名（論理名）|カラム名（物理名）|型・桁|Nullable|その他コメント|
|---|---|---|---|---|
|ID|id|int|NO|primary key|
|名前|name|varchar(255)|NO||
|生年月日|birthdate|date|NO|YYYY-MM-DD形式|
|削除フラグ|deleted|boolean|NO|0:有効、1:削除|
|作成日時|created_at|datetime|NO|YYYY-MM-DD HH:MM:SS形式|
|作成者|created_by|varchar(255)|NO|API経由のときは"api"とする|
|更新日時|updated_at|datetime|NO|YYYY-MM-DD HH:MM:SS形式|
|更新者|updated_by|varchar(255)|NO|API経由のときは"api"とする|
|削除日時|deleted_at|datetime|YES|YYYY-MM-DD HH:MM:SS形式|
|削除者|deleted_by|varchar(255)|YES|API経由のときは"api"とする|
