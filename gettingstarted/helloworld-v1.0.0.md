---
layout: default-layout
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
title: Dynamsoft Document Viewer Getting Started - Creating HelloWorld
keywords: Documentation, Dynamsoft Document Viewer, Getting Started, Creating HelloWorld
breadcrumbText: Creating HelloWorld
description: Dynamsoft Document Viewer Documentation Getting Started, Creating HelloWorld
permalink: /gettingstarted/helloworld-v1.0.0.html
---

# Creating HelloWorld

In this section, we’ll break down and show all the steps needed to build the HelloWorld.

![Hello World](/assets/imgs/helloWorld.GIF)

We’ll build on this skeleton page:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Dynamsoft Document Viewer - HelloWorld</title>
</head>
<body>
</body>
<script type="module">
// Write your code here
</script>
</html>
```

## Adding the dependency

Please refer to [Adding the dependency]({{ site.gettingstarted }}add_dependency.html).

## Define necessary HTML elements

For HelloWorld, we define below elements.

- Container to hold the viewer

```html
<div id="container"></div>
```

- Container's style

```html
<style>
    html,body {
        width: 100%;
        height: 100%;
        margin:0;
        padding:0;
        overscroll-behavior-y: none;
        overflow: hidden;
    }

    #container {
        width: 100%;
        height: 100%;
    }
</style>
```

## SDK initialization

```javascript
// Initialize DDV
await Dynamsoft.DDV.setConfig({
    // Public trial license which is valid for 24 hours
    // You can request a 30-day trial key from https://www.dynamsoft.com/customer/license/trialLicense/?product=ddv
    license: "DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9", 
    engineResourcePath: "https://cdn.jsdelivr.net/npm/dynamsoft-document-viewer@1.0.0/dist/engine",
});
```

## Create an edit viewer

```javascript
// Configure image filter feature
Dynamsoft.DDV.setProcessingHandler("imageFilter", new Dynamsoft.DDV.ImageFilter());
// Create an edit viewer
const editViewer = new Dynamsoft.DDV.EditViewer({
    container: "container",
});
```

## Review the complete code

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, minimum-scale=1.0, maximum-scale=1.0, user-scalable=no">
    <title>Dynamsoft Document Viewer - HelloWorld</title>
    <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/dynamsoft-document-viewer@1.0.0/dist/ddv.css">
    <script src="https://cdn.jsdelivr.net/npm/dynamsoft-document-viewer@1.0.0/dist/ddv.js"></script>
</head>
<style>
    html,body {
        width: 100%;
        height: 100%;
        margin:0;
        padding:0;
        overscroll-behavior-y: none;
        overflow: hidden;
    }

    #container {
        width: 100%;
        height: 100%;
    }
</style>
<body>
    <div id="container"></div>
</body>
<script type="module">
    (async () => {
        await Dynamsoft.DDV.setConfig({
            // Public trial license which is valid for 24 hours
            //You can request a 30-day trial key from https://www.dynamsoft.com/customer/license/trialLicense/?product=ddv
            license: "DLS2eyJvcmdhbml6YXRpb25JRCI6IjIwMDAwMSJ9",
            engineResourcePath: "https://cdn.jsdelivr.net/npm/dynamsoft-document-viewer@1.0.0/dist/engine",
        });
        Dynamsoft.DDV.setProcessingHandler("imageFilter", new Dynamsoft.DDV.ImageFilter());
        const editViewer = new Dynamsoft.DDV.EditViewer({
            container: "container",
        });
    })();
</script>
</html>
```