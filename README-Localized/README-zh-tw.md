---
topic: sample
products:
- Excel
- PowerPoint
- Word
- Office 365
languages:
- JavaScript
- ASP.NET
extensions:
  contentType: samples
  technologies:
  - Add-ins
  - Microsoft Graph
  services:
  - Excel
  - Office 365
  createdDate: 5/1/2017 2:09:09 PM
---
# <a name="office-add-in-that-that-supports-single-sign-on-to-office-the-add-in-and-microsoft-graph"></a>Office 增益集支援 Office 的單一登入功能、增益集與 Microsoft Graph

Office.js 中的 `getAccessTokenAsync` API 可讓已登入 Office 的使用者存取受 AAD 保護的增益集和 Microsoft Graph，而不需要重新登入。 本範例建立在 ASP.NET 和 Microsoft Identity Library (MSAL)。 

 > 注意：此 `getAccessTokenAsync` API 是預覽版本。

## <a name="table-of-contents"></a>目錄
* [變更歷程記錄](#change-history)
* [必要條件](#prerequisites)
* [使用專案](#to-use-the-project)
* [問題和建議](#questions-and-comments)
* [其他資源](#additional-resources)

## <a name="change-history"></a>變更歷程記錄

* 2017 年 5 月 10 日：初始版本。
* 2017 年 9 月 15 日：針對 2AF 新增支援。
* 2017 年 12 月 8 日：新增大量的錯誤處理。
* 2019 年 1 月 7 日：新增有關 Web 應用程式安全性做法的詳細資訊。

## <a name="prerequisites"></a>必要條件

* Office 365 帳戶。
* 在預覽版本階段，SSO 需要使用 Office 365 (Office 的訂閱版本，也稱為「隨選即用」)。 您應該使用來自測試人員通道的每月最新版本和組建。 您必須是 Office 測試人員才能取得這個版本。 如需詳細資訊，請參閱[成為 Office 測試人員](https://products.office.com/office-insider?tab=tab-1)。 請注意，當組建進展到生產環境半年通道時，即會關閉對該組建的預覽版功能的支援，包含 SSO。
* Visual Studio 2017 15.4.0 版預覽版 1 或更新版本。

## <a name="deviations-from-best-practices"></a>與最佳作法間的差異

此存放庫中的範例主要著重於示範 SSO API 的使用方式。 為求簡易，將不遵循某些最佳作法，包括 Web 應用程式安全性最佳作法。 *除非您準備進行實質性變更，否則不應使用這些範本作為生產環境增益集的建立起點。* 我們建議您使用 Visual Studio 中其中一個 Office 增益集來開始建立生產環境增益集，或者使用 [Yeoman Generator for Office 增益集](https://github.com/OfficeDev/generator-office)來產生新專案。

需謹記的_一個_範例重點：

* 範例會使用 Microsoft Graph REST API 將硬式編碼的查詢參數傳送到 URL。 如果您在生產環境增益集中及來自使用者輸入的查詢參數的任何部分修改此程式碼，請務必清理此程式碼，以便回應標頭插入式攻擊無法使用此程式碼。

## <a name="to-use-the-project"></a>使用專案

這個範例是用來輔助說明以下的逐步解說：[建立使用單一登入的 ASP.NET Office 增益集 (預覽)](https://dev.office.com/docs/add-ins/develop/create-sso-office-add-ins-aspnet) (英文)

範本有兩個版本，分別在 [Before] 和 [Completed] 資料夾中。

若要使用 Before 版本，並手動新增重要的 SSO 相關程式碼，請遵照上述連結文章中的所有程序。

若要使用 Completed 版本，請遵照上述連結文章中的所有程序，除了 "Code the client-side" (為用戶端編碼) 和 "Code the server-side" (為伺服器端編碼) 這兩節之外。

## <a name="questions-and-comments"></a>問題和建議

我們很樂於收到您對於此範例的意見反應。您可以在此存放庫的 [問題]** 區段中，將您的意見反應傳送給我們。

請在 [Stack Overflow](http://stackoverflow.com/questions/tagged/office-js+API) 提出有關 Microsoft Office 365 開發的一般問題。如果您的問題是關於 Office JavaScript API，請確定您的問題標記有 [office js] 與 [API]。

## <a name="additional-resources"></a>其他資源

* [Office 增益集文件](https://msdn.microsoft.com/zh-tw/library/office/jj220060.aspx)
* [Office 開發人員中心](http://dev.office.com/)
* 在 [Github 上的 OfficeDev](https://github.com/officedev) 中有更多 Office 增益集範例

此專案已採用 [Microsoft 開放原始碼執行](https://opensource.microsoft.com/codeofconduct/)。如需詳細資訊，請參閱[程式碼執行常見問題集](https://opensource.microsoft.com/codeofconduct/faq/)，如果有其他問題或意見，請連絡 [opencode@microsoft.com](mailto:opencode@microsoft.com)。

## <a name="copyright"></a>著作權
Copyright (c) 2017 Microsoft Corporation.著作權所有，並保留一切權利。

