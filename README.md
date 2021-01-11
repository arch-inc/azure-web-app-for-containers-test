azure-web-app-for-containers-test
---

「[研究プロジェクトのWebアプリを気軽にデプロイする方法](https://zenn.dev/junkato/books/how-to-deploy-research-web-apps)」 Chapter 03 Azure Web App for Containers のサンプルコードを含むリポジトリです。

## Directory structure

- `src/` TypeScript で書かれたWebサーバ
- `dist/` npm run build でトランスパイルされたWebサーバのコード置き場
- `.github/workflows/` Azure Web App for Containers へ自動デプロイを行う GitHub Actions の設定

## How to use

このリポジトリを fork して動作させる場合、以下の設定が必要です。

- `.github/workflows/deploy.yml > env.AZURE_WEBAPP_NAME` を自分の環境に合わせて書き換える（cf. [App Serviceの作り方](https://zenn.dev/junkato/books/how-to-deploy-research-web-apps/viewer/azure-web-app-for-containers#app-service-%E3%81%AE%E4%BD%9C%E6%88%90)）
- GitHub secret `AZURE_CREDENTIALS` をセットする（cf. [Service Principalの作り方](https://zenn.dev/junkato/books/how-to-deploy-research-web-apps/viewer/azure-web-app-for-containers#service-principal-%E3%81%AE%E4%BD%9C%E6%88%90)）
- GitHub secret `GCR_USERNAME` `GCR_TOKEN` をセットする（cf. [GitHub Personal Access Tokenの作り方](https://zenn.dev/junkato/books/how-to-deploy-research-web-apps/viewer/azure-web-app-for-containers#github-personal-access-token-%E3%81%AE%E4%BD%9C%E6%88%90)）

## Demo site

Microsoft Azure App Service の F1 tier のプラン（月額料金: 無料）で動いています。予告なく落ちることがあります。

- http://azure-web-app-for-containers-test.azurewebsites.net/
- http://azure-web-app-for-containers-test.azurewebsites.net/hoge

---
https://github.com/arch-inc/azure-web-app-for-containers-test