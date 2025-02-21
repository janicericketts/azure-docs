---
services: cognitive-services
author: aahill
manager: nitinme
ms.service: cognitive-services
ms.subservice: language-service
ms.topic: include
ms.date: 05/19/2022
ms.author: aahi
---

Use the following **GET** request to get your project details. You can use the URL you received from the previous step, or replace the placeholder values below with your own values. 

```rest
{ENDPOINT}/language/analyze-conversations/projects/{PROJECT-NAME}?api-version=2021-11-01-preview
```

|Placeholder  |Value  | Example |
|---------|---------|---------|
|`{ENDPOINT}`     | The endpoint for authenticating your API request.   | `https://<your-custom-subdomain>.cognitiveservices.azure.com` |
|`{PROJECT-NAME}`     | The name for your project. This value is case-sensitive.  | `myProject` |
|`{API-VERSION}`     | The version of the API you are calling. The value referenced here is for the latest released [model version](../../../concepts/model-lifecycle.md#choose-the-model-version-used-on-your-data). | `2022-03-01-preview` |

#### Headers

Use the following header to authenticate your request. 

|Key|Description|Value|
|--|--|--|
|`Ocp-Apim-Subscription-Key`| The key to your resource. Used for authenticating your API requests.| `{YOUR-PRIMARY-RESOURCE-KEY}` |

#### Response body

```json
    {
        "createdDateTime": "2021-10-19T23:24:41.572Z",
        "lastModifiedDateTime": "2021-10-19T23:24:41.572Z",
        "lastTrainedDateTime": "2021-10-19T23:24:41.572Z",
        "lastDeployedDateTime": "2021-10-19T23:24:41.572Z",
        "type": "orchestration",
        "name": "myProject",
        "multiLingual": true,
        "description": "string",
        "language": "en-us",
        "settings": {}
    }
```
