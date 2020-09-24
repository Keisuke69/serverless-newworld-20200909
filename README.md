# serverless-newworld-20200909
2020年9月9日開催のイベントでの説明用に利用するサンプルアプリです。

サーバーレスアンチパターン今昔物語 第四夜 - 夏の残り香 - <br>
https://serverless-newworld.connpass.com/event/187317/ <br>


Nuxt.jsベースのアプリケーションをAmazon API GatewayとAWS Lambdaを使ってServer Side Renderingをしています。<br>
AWSへのデプロイはServerless Frameworkを利用しています。<br>
時間のない人はlambda.jsとserverless.xmlを見てもらえるだけで十分です。

なお、このサンプルではAPI Gatewayでカスタムドメインを利用する前提となっています。利用しない場合は`nuxt.config.js`を修正してベースディレクトリにAPI Gatewayで設定されるステージ名のパス（デフォルトでは/dev）を設定しておく必要があります。

# 簡単なセットアップ方法
まず、`.devcontainer`というフォルダとDockerfileはVS CodeのRemote Containers用のファイル群です。この環境で実行しない方は削除しても大丈夫です。もし、このRemote Containersを使う場合はVS Codeをインストールした上で、Remote Containersという拡張をインストールしてください。また、Docker Desktopも必要となるのでこちらもインストールしてください。

Dockerを使わない場合はNode.jsをインストールしておく必要があります。

リポジトリをクローンした後、`npm install`を実行しておいてください。Nuxt.jsおよびNuxt.jsが依存するライブラリがインストールされます。

また、今回はデプロイにServerless Frameworkを利用していますので、`npm install -g serverless`でこちらもインストールしておいてください。

## ビルド
npm run build

## デプロイ
sls deploy



