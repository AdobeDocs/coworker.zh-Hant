---
source-git-commit: e5bf2a0a2ee55513b32442f70d01dc5825ac9d6a
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 5%
---
# CX Enterprise Coworker 文件

適用於Adobe CX Enterprise Coworker檔案集的Source。

## 發佈設定

在`.github/workflows/`中使用共用文章驗證和映象工作流程。
驗證工作流程會針對提取要求執行並推送至`main`。
當您推送至`main`時，映象工作流程便會執行。

使用`markdownlint_custom.json`進行Markdown規則覆寫，並使用`linkcheckexclude.json`進行URL排除範例。
`pipeline.opts`檔案遵循`cx-enterprise-ai.en`中的連結檢查組態。
使用`source,dest`欄新增URL重新導向至`redirects.csv`。
