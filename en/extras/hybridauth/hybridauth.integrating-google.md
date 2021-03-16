---
title: "Integrating Google"
_old_id: "899"
_old_uri: "revo/hybridauth/hybridauth.integrating-google"
---

Integration of any service is very simple. So, you can read about [Facebook](extras/hybridauth/hybridauth.integrating-facebook), first, then look to screenshots and everything must be clear.

#### Registering application

**1**. Go to <https://code.google.com/apis/console/> and create a new project.

**2**. Go to **API Access** under **API Project**. After that click on **Create an OAuth 2.0 client ID** to **create a new application**.

**3**. A pop-up named **"Create Client ID"** will appear, fill out any required fields such as the application name and description.

**4**. Click on **Next**.

**5**. On the popup set **Application type** to **Web application** and switch to advanced settings by clicking on **(more options)**.

**6**. Provide this URL as the Callback URL for your application: <http://example.com/assets/components/hybridauth/action.php?hauth.done=Google>

![](ha_gg1.png)

![](ha_gg2.png)

![](ha_gg3.png)

![](ha_gg4.png)

![](ha_gg5.png)

![](ha_gg6.png)
