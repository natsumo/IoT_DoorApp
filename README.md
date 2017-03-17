# IoTドア監視アプリ
_2017/03/17 ver1.0.0_

## Overview
* 「IoTドア監視アプリ」は、下記を前提としたアプリです。
 * RaspberryPi とNode-RED を使用して、次の処理が実行されている
   * ドアに設置したセンサーからドアの開閉データを取得し、[ニフティクラウド mobile backend ](http://mb.cloud.nifty.com)上に保存する
   * 開閉データの保存と同時に「IoTドア監視アプリ」にプッシュ通知でお知らせする

## Setting
* [Monaca](https://ja.monaca.io/) アカウントの取得
* [ニフティクラウド mobile backend ](http://mb.cloud.nifty.com) のアカウントの取得
* iOS端末向けにビルドする場合：[APNsとの連携設定](iOS端末向けにビルドする場合：APNsとの連携設定)
* Android端末向けにビルドする場合：[FCMとの連携設定](http://mb.cloud.nifty.com/doc/current/push/basic_usage_android.html)

## How to use
1. Monaca に下記プロジェクトをインポートしてアプリを作成
 * https://github.com/natsumo/IoT_DoorApp/archive/master.zip
1. 「設定」＞「JS/CSS コンポーネントの追加と削除...」で「ncmb」を検索し追加
 * バージョンは最新(デフォルト)を選択
1. index.htmlを開いて、`0. APIキーの設定と初期化`にmobile backend のAPIキーを設定
1. 「設定」＞「Cordova プラグインの管理...」で「Nifty (ncmb-push-monaca-plugin )」を検索し追加
1. 【Android端末利用時のみ】index.htmlを開いて、`3.1. デバイストークンを取得してinstallation に登録する`にmobile backend のAPIキーを設定
1. アプリをビルド
