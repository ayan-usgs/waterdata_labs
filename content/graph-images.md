---
slug: about-graph-image-api
title: Graph Image API
description: Information about the Graph Image API.
keywords:
  - Graph
  - Image
  - API
image: /static/graph-images/api_graph_image.png
---

Recently, the Water Data for the Nation (WDFN) development [released a new real-time site page](https://waterdata.usgs.gov/blog/wdfn-tng/). One of the[ most common pieces of feedback](https://waterdata.usgs.gov/blog/wdfn-firstlook/)[ ](https://waterdata.usgs.gov/blog/wdfn-firstlook/)that we received about the hydrograph on[ the new monitoring location pages](https://waterdata.usgs.gov/monitoring-location/09380000/) was that users need a way to save an image of a given hydrograph. In the [classic pages](https://waterdata.usgs.gov/nwis/uv?site_no=09380000)[,](https://waterdata.usgs.gov/nwis/uv?site_no=09380000) these graphs are already images, and it was easy enough to expose the endpoint that generated those images:

[https://waterdata.usgs.gov/nwisweb/graph?agency_cd=USGS&site_no=09380000&parm_cd=00060&period=7](https://waterdata.usgs.gov/nwisweb/graph?agency_cd=USGS&site_no=09380000&parm_cd=00060&period=7)
![Legacy Graph Image](/static/graph-images/legacy_graph_image.png)

However, the new graphs are not easy to generate, as they are dynamically generated in the web browser using a tool called D3. Replicating the environment of a browser was a non-trivial task, but with the major advances in automated browser testing with tools like [puppeteer](https://developers.google.com/web/tools/puppeteer/), we were able to generate a reasonable solution.
![Graph API Image](/static/graph-images/api_graph_image.png)


https://labs.waterdata.usgs.gov/graph-images/monitoring-location/09380000/?parameterCode=00060

The graph image project is a work in progress and this is a first step to meeting users’ requests for easy image downloads. Try it out and [let us know](https://water.usgs.gov/contact/gsanswers?pemail=gs-w-ks_NWISWeb_Data_Inquiries&subject=Site+Number%3A+07144100&viewnote=%3CH1%3EUSGS+NWIS+Feedback+Request%3C%2FH1%3E%3Cp%3E%3Cb%3EPlease+enter+a+subject+in+the+form+below+that+briefly+summarizes+your+request%3C%2Fb%3E%3C%2Fp%3E)[ ](https://water.usgs.gov/contact/gsanswers?pemail=gs-w-ks_NWISWeb_Data_Inquiries&subject=Site+Number%3A+07144100&viewnote=%3CH1%3EUSGS+NWIS+Feedback+Request%3C%2FH1%3E%3Cp%3E%3Cb%3EPlease+enter+a+subject+in+the+form+below+that+briefly+summarizes+your+request%3C%2Fb%3E%3C%2Fp%3E)how it works for you!
