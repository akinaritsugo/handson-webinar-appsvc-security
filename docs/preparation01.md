# 事前準備

## 【目次】

1. [開発環境の準備](#開発環境の準備)

## インフラのデプロイ

1. 以下のARMテンプレートを展開

    [![Deploy to Azure](https://aka.ms/deploytoazurebutton)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2Fakinaritsugo%2Fhandson-webinar-appsvc-security%2Fmain%2Finfra%2Farm%2Ftemplate.json)

    (*) ARMテンプレート

    https://github.com/akinaritsugo/handson-webinar-appsvc-security/blob/main/infra/arm/template.json

1. アプリの展開

    1. 以下のリポジトリをダウンロード/クローン

        https://github.com/akinaritsugo/sample-todo-webapp-csharp
    
    1. App Service へデプロイ

    1. 設定にSQLDBへの接続文字列を追加

        |名前|値|種類|
        |---|---|---|
        | `MSSQLDB` | (作成された SQL Database への接続文字列) | `SQL Server` |

1. SQL Database の初期化

    1. ファイアウォール設定の変更
        1. [セキュリティ]-[ネットワーク]を開く
        1. 以下２つからのアクセスを許可

            - 自分自身のクライアントIPアドレス
            - Azureサービスおよびリソース(=チェックボックスを入れる)

    1. スキーマ、データの設定
        1. 展開した SQL Database を開き、「クエリエディター」を開く
        1. 以下にあるDDLを実行

            https://github.com/akinaritsugo/sample-todo-webapp-csharp/blob/main/data/ddl.sql

        1. サンプルデータも投入

            https://github.com/akinaritsugo/sample-todo-webapp-csharp/blob/main/data/sampledata.sql

1. 動作確認

    1. App Service を開くドメイン名を取得

    1. ブラウザを立ち上げて取得したドメインにアクセス

## 開発環境の準備

1. 以下をローカル開発環境にインストールします

    * [Visual Studio Code](https://code.visualstudio.com/download)
    * Visual Studio Code プラグイン
        * [C#](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)
        * [C# DevKit](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csdevkit)
        * [App Service](https://marketplace.visualstudio.com/items?itemName=ms-azuretools.vscode-azureappservice)
    * [.Net 6 SDK](https://dotnet.microsoft.com/ja-jp/download/dotnet/6.0)


