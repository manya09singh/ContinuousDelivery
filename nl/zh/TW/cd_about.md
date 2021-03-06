---

Copyright:
  years: 2015, 2019
lastupdated: "2019-03-27"

keywords: IBM Cloud Public, Use Developer Insights, US South

subcollection: ContinuousDelivery

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}


# 工具鏈可用性、範本及指導教學  
{: #cd_about}  

{{site.data.keyword.Bluemix_notm}} Public 及 Dedicated 上都提供工具鏈。您可以使用範本作為起點來建立工具鏈。
{:shortdesc}

## {{site.data.keyword.Bluemix_notm}} Public 與 {{site.data.keyword.Bluemix_notm}} Dedicated 的工具鏈可用性比較
{: #public_and_dedicated}

{{site.data.keyword.Bluemix_notm}} Public 是一種開放式標準雲端型平台，您可以在其中建置、執行及管理 [http://cloud.ibm.com ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://cloud.ibm.com){:new_window} 所存取的應用程式。{{site.data.keyword.Bluemix_notm}} Dedicated 在專用 SoftLayer 環境中提供 {{site.data.keyword.Bluemix_notm}} 功能，該環境可安全地連接至 {{site.data.keyword.Bluemix_notm}} Public 環境及網路。您公司的 {{site.data.keyword.Bluemix_notm}} Dedicated 環境可能未包含與 {{site.data.keyword.Bluemix_notm}} Public 網站相同的工具整合。

對於原始碼管理及問題追蹤，{{site.data.keyword.Bluemix_notm}} Public 一般會使用 {{site.data.keyword.gitrepos}}（由 IBM 所管理並以 [GitLab Community Edition ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://about.gitlab.com/){:new_window} 為建置基礎）或 GitHub (github.com)。{{site.data.keyword.Bluemix_notm}} Dedicated 也可以使用 github.com，但一般會使用公司所安裝或 IBM 所管理的 {{site.data.keyword.ghe_short}}。

在所選取地區的 {{site.data.keyword.Bluemix_notm}} Public 上以及 {{site.data.keyword.Bluemix_notm}} Dedicated 上可以使用 {{site.data.keyword.contdelivery_short}}。視您是在 {{site.data.keyword.Bluemix_notm}} Public 還是 {{site.data.keyword.Bluemix_notm}} Dedicated 上使用 {{site.data.keyword.contdelivery_short}} 而定，工具鏈會有所不同。

雖然工具鏈目前無法在所有地區中使用，但是您可以配置工具鏈將應用程式部署至所有地區。若要進一步瞭解，請嘗試[將安全 Web 應用程式部署至多個地區指導教學](/docs/tutorials?topic=solution-tutorials-multi-region-webapp){: new_window}。
{: tip}

|工具鏈|{{site.data.keyword.Bluemix_notm}} Public	|{{site.data.keyword.Bluemix_notm}} Dedicated |
|:----------|:------------------------------|:------------------|
|工具整合|如需所支援工具整合的清單，請參閱[配置工具整合](/docs/services/ContinuousDelivery?topic=ContinuousDelivery-integrations){: new_window}。|可用的工具整合取決於 {{site.data.keyword.contdelivery_short}} 在您環境中的設定方式。|
|從範本建立工具鏈|登入 [{{site.data.keyword.Bluemix_notm}} ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://cloud.ibm.com/devops){:new_window}|登入 {{site.data.keyword.Bluemix_notm}} 的「專用」環境。|
|從應用程式建立工具鏈|應用程式會配置成從已移入應用程式入門範本程式碼的新 GitHub 儲存庫進行持續交付。|應用程式會配置成從已移入應用程式入門範本程式碼的新 GitHub 或 GitHub Enterprise 儲存庫進行持續交付。|  
|交付管線部署地區|Cloud Foundry 部署工作可以使用所有 {{site.data.keyword.Bluemix_notm}} Public 地區。|{{site.data.keyword.Bluemix_notm}} Dedicated 地區可供使用。視 {{site.data.keyword.contdelivery_short}} 在您特定環境中的設定方式而定，也可使用相同客戶帳戶內的其他「專用」或「本端」地區。|
|交付管線部署工作|所有[工作類型](/docs/services/ContinuousDelivery?topic=ContinuousDelivery-deliverypipeline_about#deliverypipeline_jobs)都可供使用。|可能無法使用與「專用」環境中未安裝之 {{site.data.keyword.Bluemix_notm}} 服務相依的工作類型。例如，在沒有 {{site.data.keyword.containerlong_notm}} 的環境中，可能無法使用容器建置及部署工作類型。|
{: caption="表 1. {{site.data.keyword.Bluemix_notm}} Dedicated 及 {{site.data.keyword.Bluemix_notm}} Public 上的工具鏈差異" caption-side="top"}


## 工具鏈範本
{: #templates}

您可以使用範本作為起點來[建立工具鏈 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://cloud.ibm.com/devops/create){: new_window}。工具鏈範本包含可支援開發、部署及操作作業的特定工具整合集。

您公司的 {{site.data.keyword.Bluemix_notm}} Dedicated 環境可能未包含與 {{site.data.keyword.Bluemix_notm}} Public 網站相同的工具鏈範本。{{site.data.keyword.Bluemix_notm}} Public 及 {{site.data.keyword.Bluemix_notm}} Dedicated 上可用的工具鏈範本可能包含 {{site.data.keyword.Bluemix_notm}} Dedicated 上的不同工具整合集。
{: note}

部分工具鏈範本包含 {{site.data.keyword.contdelivery_short}} 服務所屬的工具整合。如果資源群組或組織中還沒有該服務的實例，則在按一下**建立**以建立工具鏈時，會使用所選取的免費「精簡」方案自動新增服務。如需相關資訊及術語，請參閱 [{{site.data.keyword.Bluemix_notm}} 型錄 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://cloud.ibm.com/catalog/services/continuous-delivery/){:new_window}。

「在 Cloud Foundry 上開發及測試微服務」工具鏈會部署具有 Cloudant 儲存庫所支援之型錄及訂單 API 的應用程式。部署應用程式時，會建立不需要成本的 Cloudant 服務實例。如需相關資訊及術語，請參閱 [{{site.data.keyword.Bluemix_notm}} 型錄 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://cloud.ibm.com/catalog/services/cloudant-nosql-db/){:new_window}。

預先定義的 DevOps 工具鏈範本是解決真實情境的建議範例，而且各包含一個範例應用程式。從範本建立工具鏈時，指定 git 儲存庫即可使用自己的應用程式。

<table valign="top" padding="2px">
  <caption>表 2. 工具鏈範本</caption>
  <tr>
    <th style="width:25%; text-align:left; vertical-align:top">範本及可用的地區</th>
    <th style="width:50%; text-align:left; vertical-align:top">說明及可用的指導教學</th>
    <th style="text-align:left; vertical-align:top">包含的工具</th>
  </tr>
  <tr><td>
  <a href="https://cloud.ibm.com/devops/setup/deploy?repository=https%3A%2F%2Fgithub.com%2Fopen-toolchain%2Fsimple-toolchain" target="_blank">「開發 Cloud Foundry 應用程式」工具鏈 <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a> <br><br>

  可以在美國南部、美國東部、德國、東京及英國使用

  </td><td>
運用此工具鏈，您可以開發及部署 Cloud Foundry 應用程式。根據預設值，此工具鏈會使用範例 Node.js "Hello world" 應用程式，但您可以改為鏈結至自己的 GitHub 儲存庫。已預先配置此工具鏈，以進行持續交付、來源控制、問題追蹤及線上編輯。<br><br>

  嘗試指導教學：<a href="https://www.ibm.com/cloud/garage/tutorials/introduce-develop-cloud-foundry-app-toolchain" target="_blank">使用「開發 Cloud Foundry 應用程式」工具鏈介紹工具鏈 <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a> <br><br>
  </td><td><ul><li>
  {{site.data.keyword.deliverypipeline}}
  </li><li>Eclipse Orion {{site.data.keyword.webide}}</li><li>GitHub 及 GitHub Issues</li><li>{{site.data.keyword.Bluemix_notm}}
  </li></ul>
  </td></tr>

  <tr><td>
  <a href="https://cloud.ibm.com/devops/setup/deploy?repository=https%3A%2F%2Fgithub.com%2Fopen-toolchain%2Fsecure-kube-toolchain" target="_blank">「開發 Kubernetes 應用程式」工具鏈 <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a> <br><br>

  可以在美國南部、美國東部、德國、東京及英國使用

  </td><td>
  使用此工具鏈，您可以安全地開發應用程式並將其部署至 {{site.data.keyword.containerlong_notm}} 所管理的 Kubernetes 叢集。依預設，工具鏈會使用範例 Node.js "Hello World" 應用程式，但您可以改為鏈結至自己的 GitHub 儲存庫。已預先配置此工具鏈，以進行「漏洞警告器」的持續交付、來源控制、問題追蹤及線上編輯。<br><br>
  嘗試指導教學：<a href="https://www.ibm.com/cloud/garage/tutorials/use-develop-kubernetes-app-toolchain" target="_blank">使用「開發 Kubernetes 應用程式」工具鏈 <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a>  
  <br><br>
  </td><td><ul><li>{{site.data.keyword.deliverypipeline}}
  </li><li>Eclipse Orion {{site.data.keyword.webide}}</li><li>GitHub 及 GitHub Issues</li><li>{{site.data.keyword.containerlong_notm}}（Kubernetes 叢集）
  </li></ul>
  </td></tr>

  <tr><td>
  <a href="https://cloud.ibm.com/devops/setup/deploy?repository=https%3A%2F%2Fgithub.com%2Fopen-toolchain%2Fsimple-helm-toolchain" target="_blank">「使用 Helm 開發 Kubernetes 應用程式」工具鏈
   <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a> <br><br>

  可以在美國南部、美國東部、德國、東京及英國使用

  </td><td>
  使用此工具鏈，您可以在來源控制中一起開發 Docker 應用程式及其 Helm 圖表，並自動將它建置及部署至 Kubernetes 叢集。此工具鏈會在建置或部署之前執行煙霧測試，並使用專用容器登錄以及容器登錄和 Kubernetes 叢集的名稱空間來確定隱私權。此工具鏈也使用「漏洞警告器」來確定僅部署安全映像檔。<br><br>
嘗試指導教學：<a href="https://www.ibm.com/cloud/garage/tutorials/use-develop-kubernetes-app-with-helm-toolchain" target="_blank">使用「使用 Helm 開發 Kubernetes 應用程式」工具鏈 <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a>	 <br><br>
  </td><td><ul>
  <li>{{site.data.keyword.deliverypipeline}}
  </li><li>Eclipse Orion {{site.data.keyword.webide}}</li><li>Git Repos and Issue Tracking</li><li>搭配 Helm 圖表的 {{site.data.keyword.containerlong_notm}}（Kurbernetes 叢集）
  </li></ul>
  </td></tr>

  <tr><td>
  <a href="https://cloud.ibm.com/devops/setup/deploy?repository=https%3A%2F%2Fgithub.com%2Fopen-toolchain%2Fdra-toolchain-demo" target="_blank">「開發及測試 Cloud Foundry 應用程式」工具鏈
   <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a> <br><br>

  可以在美國南部、德國及英國使用

  </td><td>
  使用此雲端原生工具鏈，您可以使用 DevOps Insights 來限制簡單 Cloud Foundry 應用程式的部署。依預設，此工具鏈會使用簡單 Node.js 天氣應用程式，或者您可以鏈結至自己的 GitHub 儲存庫。此工具鏈會使用 Mocha 來執行單元測試，並使用 Istanbul 來檢查程式碼涵蓋面。<br><br>
嘗試指導教學：<a href="https://www.ibm.com/cloud/garage/tutorials/use-develop-test-cloud-foundry-app-toolchain" target="_blank">使用「開發及測試 Cloud Foundry 應用程式」工具鏈 <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a>  <br><br>
  </td><td><ul>
  <li>{{site.data.keyword.deliverypipeline}}
  </li><li>Eclipse Orion {{site.data.keyword.webide}}</li><li>Git Repos and Issue Tracking</li><li>{{site.data.keyword.DRA_full}}
  </li></ul>
  </td></tr>


  <tr><td>
  <a href="https://cloud.ibm.com/devops/setup/deploy?repository=https%3A%2F%2Fgithub.com%2Fopen-toolchain%2Fmicroservices-toolchain-hosted" target="_blank">
  「在 Cloud Foundry 上開發及測試微服務」工具鏈 <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a> <br><br>

  可以在美國南部、德國及英國使用

  </td><td>
使用此雲端原生工具鏈，您可以使用範例來建立包含三個微服務的線上商店：Catalog API、Orders API 以及呼叫這兩個 API 的使用者介面。已預先配置此工具鏈，以進行持續交付、來源控制、功能測試、問題追蹤、線上編輯及警示通知。<br><br>
  嘗試指導教學：<a href="https://www.ibm.com/cloud/garage/tutorials/use-develop-test-microservices-on-cloud-foundry-toolchain" target="_blank">使用「在 Cloud Foundry 上開發及測試微服務」工具鏈 <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a><br><br>
  </td><td>
  <ul>
  <li>{{site.data.keyword.deliverypipeline}}
  </li><li>Eclipse Orion {{site.data.keyword.webide}}</li><li>GitHub 及 GitHub Issues</li><li>{{site.data.keyword.Bluemix_notm}}
  </li><li>{{site.data.keyword.DRA_full}}
  </li><li>PagerDuty</li><li>Sauce Labs		</li><li>Slack</li></ul>
 </td>
</tr>

  <tr>
  <td><a href="https://cloud.ibm.com/devops/setup/deploy?repository=https%3A%2F%2Fgithub.com%2Fopen-toolchain%2Fcloud-native-toolchain-tutorial" targe="_blank">
「搭配 Cloud Foundry 的 Garage Method 指導教學」工具鏈 <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a> <br><br>

  可以在美國南部、美國東部、德國、東京及英國使用

</td><td>
此工具鏈示範 Garage Method 中所具備的 DevOps 作法。已預先配置此工具鏈，以進行持續交付、來源控制、測試自動化，以及自動化監視和作業。它會隨附以 Node.js Express 4 撰寫的範例應用程式，而且您可以進一步予以擴充。<br><br>嘗試課程：<a href="https://www.ibm.com/cloud/garage/content/course/gm_advocate" target="_blank">Become a Garage Method advocate <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a>
</td><td>
<ul>
<li>{{site.data.keyword.deliverypipeline}}
</li><li>Eclipse Orion {{site.data.keyword.webide}}</li><li>GitHub 及 GitHub Issues</li><li>Google Analytics
</li><li>{{site.data.keyword.Bluemix_notm}}
</li><li>New Relic
</li><li>PagerDuty</li><li>Sauce Labs		</li><li>Slack</li></ul>
</td></tr>

<tr><td>
<a href="https://cloud.ibm.com/devops/setup/deploy?repository=https%3A%2F%2Fgithub.com%2Fdevops-insights%2FDevOpsInsights_Demo_Toolchain_Template" target="_blank">"DevOps Insights Quick Start Demo" toolchain <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a> <br><br>

  可以在美國南部、德國及英國使用

</td><td>
運用此工具鏈，您可以探索 {{site.data.keyword.DRA_short}}，而不需要進行設定。若要開始，請登入 {{site.data.keyword.Bluemix}}。此示範包含一個參照工具鏈及三個 GitHub 儲存庫的資料。探索如何在「品質儀表板」內組織、測試、建置及部署所有團隊的所有應用程式的資料。評估趨勢，並瞭解需要改善的區域，以便得知應該將資源聚焦在何處。在 Team Dynamics 內，檢閱團隊成員在每個版本如何分工合作。<br><br>
嘗試指導教學：<a href="https://www.ibm.com/cloud/garage/tutorials/explore-ibm-cloud-devops-insights" target="_blank">Explore {{site.data.keyword.DRA_full}} <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a> <br><br>
</td><td><ul><li>
GitHub 及 GitHub Issues</li><li>{{site.data.keyword.DRA_full}}
</li></ul>
</td></tr>

<tr><td>
<a href="https://cloud.ibm.com/devops/setup/deploy?repository=https%3A%2F%2Fgithub.com%2Fopen-toolchain%2Fempty-toolchain" target="_blank">建置您自己的工具鏈 <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a> <br><br>

  可以在美國南部、美國東部、德國、東京及英國使用

</td><td>
此工具鏈沒有預先配置的工具。如果您已熟悉工具鏈，則可以設定自己的工具鏈。<br><br>
嘗試指導教學：<a href="https://www.ibm.com/cloud/garage/tutorials/create-a-custom-toolchain" target="_blank">建立自訂工具鏈 <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a>
</td><td> &nbsp;&nbsp; 無
</td></tr>

<tr><td>Continuous Delivery 工具鏈<br><br>

 可以在美國南部、美國東部、德國、東京及英國使用

</td><td>
當您啟用應用程式的持續交付時，就會使用此工具鏈。<br><br>
嘗試指導教學：

<ul><li><a href="https://www.ibm.com/cloud/garage/tutorials/add-a-toolchain-to-an-app" target="_blank">將工具鏈新增至應用程式 <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a></li>
<li><a href="https://www.ibm.com/cloud/garage/tutorials/create-a-custom-toolchain" target="_blank">建立自訂工具鏈 <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a></li>
</ul></td>
<td><ul><li>{{site.data.keyword.deliverypipeline}}
</li><li>Eclipse Orion {{site.data.keyword.webide}}</li><li>
GitHub 及 GitHub Issues</li>
<li>{{site.data.keyword.Bluemix_notm}}</li></ul>
</td></tr>

<tr><td>自訂工具鏈範本<br><br>

 可以在美國南部、美國東部、德國、東京及英國使用

</td><td>
<br><br>
您可以建立可供其他人使用的自訂工具鏈範本。<br><br>

請參閱文件：
<a href="https://github.com/open-toolchain/sdk/wiki" target="_blank">建立自訂工具鏈範本 <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a>
<br><br>
嘗試指導教學：<a href="https://www.ibm.com/cloud/garage/tutorials/create-a-template-for-a-custom-toolchain" target="_blank">建立自訂工具鏈的範本 <img src="../../icons/launch-glyph.svg" alt="外部鏈結圖示"></a></td>
<td>無
</td></tr>

</table>
