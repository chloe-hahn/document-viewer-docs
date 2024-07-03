---
layout: default-layout
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
title: Dynamsoft Document Viewer Viewer Style - Customize
keywords: Documentation, Dynamsoft Document Viewer, Viewer Style, Customize 
breadcrumbText: How to Customize UI
description: Dynamsoft Document Viewer Documentation Viewer Configuration How to Customize Viewer Style
permalink: /viewer/customize.html
--- 

# How to customize viewer 

Although Dynamsoft Document Viewer has provided the default ViewerConfig for each type of viewer, developer can also customize it as needed.

ViewerConfig contains two parts of configuration, one is the configuration on the viewer style and the other is the configuration on the viewer properties.

## Viewer Style

### Customize styles while creating a viewer

Take the edit viewer as example, according to the structure [`EditViewerConfig`]({{ site.api }}interface/editviewerconfig.html), there are three styles which can be configured, [`canvasStyle`]({{ site.api }}interface/editviewerconfig.html#canvasstyle), [`pageStyle`]({{ site.api }}interface/editviewerconfig.html#pagestyle) and [`quadSelectionStyle`]({{ site.api }}interface/editviewerconfig.html#quadselectionstyle).

**Use case**

Customize `pageStyle` while creating an edit viewer.
 
 - Step one: Create a `BaseStyle` object which meets the page style you want.
    ```typescript
    const newPageStyle = {
        border: "2px dashed red",
        background: "grey",
    };
    ```

 - Step two: Create the customized viewer config.
    ```typescript
    const newViewerConfig = {
        pageStyle: newPageStyle,
    };
    ```

 - Step three: Configure the customized viewer config while creating the edit viewer.
    ```typescript
    const editViewer = new Dynamsoft.DDV.EditViewer({
        container: "viewer",
        viewerConfig: newViewerConfig,
    });
    ```

Please notice that only the customized style will be modified, and the remaining styles will remain in their default state.

### Update styles dynamically

Besides customize the initial viewer style, Dynamsoft Document Viewer also allows update the styles dynamically after the viewer is created by using [`getStyle()`]({{ site.api }}class/editviewer.html#getstyle) & [`updateStyle()`]({{ site.api }}class/editviewer.html#updatestyle).

**Use case**

Update the `CanvasStyle` after the edit viewer is created.

```typescript
const editViewer = new Dynamsoft.DDV.EditViewer({
    container: "viewer",
});

const newCanvasStyle = editViewer.getStyle("canvasStyle");
newCanvasStyle.border = "2px dashed green";
newCanvasStyle.background = "white";
newCanvasStyle.cursor = "pointer";

editViewer.updateStyle("canvasStyle", newCanvasStyle);
```

## Viewer properties

Some properties can also customized, for example, the values of [`minZoom`]({{ site.api }}interface/editviewerconfig.html#minzoom) and [`maxZoom`]({{ site.api }}interface/editviewerconfig.html#maxzoom) can be customized for a edit viewer.

**Use case**

Customize the `minZoom` and `maxZoom` while creating an edit viewer.

```typescript
const newViewerConfig = {
    minZoom: 0.1, // Set the minimum zoom value to 10%
    maxZoom: 32,  // Set the maximum zoom value to 3200%
};

const editViewer = new Dynamsoft.DDV.EditViewer({
    container: "viewer",
    viewerConfig: newViewerConfig,
});
```

Please notice that only the customized properties will be modified, and the remaining properties will remain in their default state.