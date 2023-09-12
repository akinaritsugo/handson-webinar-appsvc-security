# Exercise6: Defender for Cloud の設定

## 【目次】

![](images/ex01-0000-sqldb-create.png)

1. [Defender for Cloud の有効化](#defender-for-cloud-の有効化)
1. [動作確認](#動作確認画面確認のみ)


## Defender for Cloud の有効化

1. Azureポータルにて「Microsoft Defender for Cloud」を開き、[管理]-[環境設定] を開く

1. [Expand all] を選択して展開し、ハンズオン利用中のサブスクリプションを選択

1. CWPにある「App Service」と「データベース」を有効化して「保存」

    * Cloud Workload Protection (CWP)
        * App Service
        * データベース


## 動作確認（画面確認のみ）

1. Azureポータルから「Microsoft Defender for Cloud」を開く

1. [全般]-[セキュリティ警告] を開く

    * 検出されたインシデントが表示される

1. [全般]-[推奨事項] を開く

    * 設定など見直した方が良い内容が表示される



# すべて完了 🎉

不要なリソースグループは削除して終わりになります。

* [クリーンアップ](exercise99.md)
