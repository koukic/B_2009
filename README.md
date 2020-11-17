# 画像分析で忘れ物を防ぐアプリ 「Laff」
<img src="https://i.gyazo.com/1021cc3205920cf8a2ab83856dc8e956.png">

## 製品概要
#### 忘れ物 × Tech

## 紹介動画
 https://www.youtube.com/watch?v=mVvbSJA8qvQ&feature=youtu.be

### 背景(製品開発のきっかけ、課題等）
旅行にいく時、友達と遊びにいく時、デートをする時『持ってくるの忘れた！』という経験は誰にでもありますよね。
最近で言えばコロナのためマスクが必須アイテムになりましたが忘れてしまって無駄な出費をする事が多々あります。
そうならないために何回もチャックリストを確認して多くの時間を浪費したり、めんどくさくて確認をしないと忘れ物をしてしまいます。

そんな時簡単にかつ一瞬で正確に忘れ物を判定してくれるようなアプリがあればとても便利だなと思い開発をはじめました！
### 製品説明（具体的な製品の説明）
|1. 新規登録/ログイン|2. 持ち物を登録|3. ホーム画面|4. 写真を撮る|5. 忘れ物を表示| 6. 行ってらっしゃい！！
|---|---|---|---|---|---|
|<img src="https://i.gyazo.com/d278b6d261cfebdf9cf2b3b46d1e1e8e.png" width="200x45">|<img src="https://i.gyazo.com/998d46620fd51dd1e6d0f90e7926f3b5.png" width="200x45">|<img src="https://i.gyazo.com/9b16b762388d01580295d9750ef1e5bc.png" width="200x45">|<img src="https://i.gyazo.com/c92e3c1132b36ab10bc29f3bcc3bf8a1.png" width="200x45">|<img src="https://i.gyazo.com/2c9aae8b48cecf02410c6bf6f88a459a.png" width="200x45">|<img src="https://i.gyazo.com/88cd8f8d0ea3ea936d854099a898aa1b.png" width="200x50">


### 特長
#### 1. 画像認識の機械学習を使っているため写真を撮るだけで簡単に忘れ物を表示してくれます
#### 2. 翻訳apiを使っているので英語/日本語に対応しています
#### 3. 独自の技術によって、より正確な判定を実現しています
#### 4. ios/Andoridのクロスプラットフォームに対応しています

### 解決出来ること
* 既存のアプリで忘れ物チェックすると手動であるため多くの時間を浪費するがこのアプリだと自動で忘れ物を表示してくれる
* 主観的な判断ではなく機械を通した客観的な判断ができるため思い込みによる忘れ物をなくすことができる

以上の理由により
#### 簡単かつ一瞬で正確に忘れ物がわかりユーザーの出かける時の心配事をなくすことができる

### 今後の展望
* 持ち物リストの登録のテンプレートを作れるようにする
* 用途ごとにリストを作れるようにする
* チェックリスト的な役割を果たせるようにする
ex)買い物時に買い忘れがないかなどを写真を撮るだけでわかるようにしたり
* 忘れ物を探す際の機械学習の精度をあげる
* UIをカッコよくする

### 注力したこと（こだわり等）
* 画像認識の機械学習などを使うことで従来とは違うアプローチの仕方をすることで簡単かつ一瞬で正確に忘れ物を出せるようにしたこと
* 誰でも使えるようにシンプルにかつ使いやすくしたこと
* 画像認識で検知したラベルに同義語apiを使うことで精度をあげた。翻訳apiで英語も日本語も対応させた
* 当初はVue.jsでWeb版の開発を進めていたが、  
  ①カメラの画質を上げて分析の精度も上げる  
  ②よりスムーズなユーザー体験
  これらの理由によってReact Nativeでのモバイル開発へ変更した。
* また、ReactNativeで開発する事でiOS/Android対応のクロスプラットフォームを実現した

## 開発技術
### 活用した技術
#### システム構成図
<img src="https://user-images.githubusercontent.com/41990509/98366943-1f67e900-2078-11eb-904b-6cafd83e1e19.png" width="800" height="600"/>

#### API・データ
* Google Cloud Vision Api：画像認識
* Google Cloud Translation Api：翻訳
* Words Api：類義語

#### フレームワーク・ライブラリ・モジュール
##### フロントエンド
* フロントエンド：React Native(Expo) 
* バックエンド：Ruby on Rails(Ruby), Heroku, Google Cloud Platform, Rapid API

#### デバイス
* iPhone/Android

### 独自技術
#### ハッカソンで開発した独自機能・技術
* マルチプラットフォームでのカメラアプリ開発
* ユーザー管理, アイテム管理機能のバックエンドAPI
* 画像認識, 翻訳, 同義語を組み合わせた持ち物照合機能 

### プレゼン
https://docs.google.com/presentation/d/1x56RnSUM8XT5Q-hmNnLFchycf73qw6giE5C7PAi2bq4/edit#slide=id.ga88b9b5b42_1_2
 
 
 
## ダウンロード方法 
### ⚠️初回カメラ起動時に画面が黒くなってしまう事があります。一旦ホーム画面に戻って「カメラを開く」ボタンを再度押してみてください。
1. expoアプリをダウンロードします 

  * iOS: https://apps.apple.com/jp/app/expo-client/id982107779 
   
  * android: https://play.google.com/store/apps/details?id=host.exp.exponent&hl=ja 
  
2. アプリを開いたら「Sugn in to your account」ボタンを押して、以下のログイン情報でログインします 
   
  * E-mail/username: NoSalary 
   
  * Password: nosalary$0 
  
3. 「Laff」というProjectがあるのでそれを開きます
 <img src="https://user-images.githubusercontent.com/46051957/98431517-5af6c780-20f9-11eb-9029-3f1c44e7aad8.PNG" width="200x45">
 
## 備考
  当初はwebアプリを検討していて、フロントでvercel、バックエンドはherokuでデプロイする為にリポジトリを分けました。(この提出用リポジトリのような構成にするとherokuのデプロイが失敗しました)
   
  各々のリポジトリをclone/submoduleしております。
   
* フロント: https://github.com/ikkei12/scanhack_front_native
* バックエンド: https://github.com/loadmap/scanhack_api
