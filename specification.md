# 仕様書  
2018/11/03更新

開発を進めていく上での大まかな方向性を示した仕様書です。詳細については別途ファイルを作り、Trelloなどのコミュニティで検討してから文章化します。

1. 開発の方針  
オープンソースかつ中央集権型(非連合型)のSNS。Google+の機能を包括し、マテリアルデザインベースのデザインを採用。

2. 開発の優先順位  
    1. ユーザーの利便性、ニーズ
	2. 軽量さ(クライアント)
	3. 軽量さ(サーバー)
	4. デザイン
	5. 開発速度
	6. 新機能

3. バックエンド  
Javascriptで記述  
フレームワーク:Node.js

4. データベース  
プロフィールと個人情報を別ファイルで格納、関連付け
    1. データ構造  
    検討中

1. エンドポイント  
<details><summary>バックエンド一覧(表示の乱れあり)<p><a href="https://plus.google.com/u/0/105503903949965673965/posts/4zFAec12Vcy">参考先(外部リンク)</a></summary>
/people/me
/people/me/edit
/people/userId
/people?query=
/people/userId/posts
/people/userId/collections  
/people/userId/communities  

/circle/list  
/circle/create  
/circle/circleId/add
/circle/circleId/delete
/circle/circleId/list
/circle/edit
/circle/delete

/post/create
/post/edit
/post/delete
/post/comment
/post/comment/commentId/edit
/post/comment/commentId/delete
/post?query=

/community/create
/community/edit
/community/join
/community/leave
/community/delete
/community/list
/community?query=

/collection/create
/collection/edit
/collection/delete
/collection/list
/collection?query=

/notifications/unreadlist
/notifications/list
/notifications/dismiss
</details>

6. Webフロントエンド  
Javascriptで記述  
フレームワーク(検討中):React.js, Redux.js

7. API  
未定

8. 詳細な仕様  
* スコープ  
	一般投稿(グローバル)、カテゴリー投稿、リスト投稿、コミュニティ内投稿、ダイレクト投稿(会話形式も検討)
* ユーザーリスト  
	ユーザーをカテゴライズする機能
* コミュニティ  
* コレクション  
    投稿をカテゴライズする機能、スコープを指定可能
    一つの投稿に対し複数のコレクションに収載可能
* タイムライン  
    + ホームタイムライン
    + リストタイムライン
    + タグタイムライン
    + ランダムタイムライン
    + メディアタイムライン

9. クライアント  
フレームワーク:React Native  
Android、iOS向け