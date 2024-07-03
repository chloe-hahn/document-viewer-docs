---
layout: default-layout
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
title: Dynamsoft Document Viewer API Reference - Class
keywords: Documentation, Dynamsoft Document Viewer, API Reference, Class
breadcrumbText: EditViewer Class
description: Dynamsoft Document Viewer Documentation API Reference Class Index Page
permalink: /api/class/index.html
---


# Dynamsoft Document Viewer Class

Dynamsoft Document Viewer Javascript library comes with six primary classes:

<div class="multi-panel-switching-prefix"></div>

- [DocumentManager](#documentmanager)
- [EditViewer](#editviewer)
- [CaptureViewer](#captureviewer)
- [PerspectiveViewer](#perspectiveviewer)
- [BrowseViewer](#browseviewer)
- [CustomViewer](#customviewer)

<div class="multi-panel-start"></div>

## [DocumentManager Class]({{ site.api }}class/documentmanager.html)

The `Dynamsoft.DDV.documentManager` instance will be created automatically as soon as Dynamsoft Document Viewer is initialized. Please refer to [`documentManager`]({{ site.api }}namespace/ddv.html#static-documentmanager).

**Methods**

| API Name              | Description                                               |
| --------------------- | --------------------------------------------------------- |
| [`createDocument()`]({{ site.api }}class/documentmanager.html#createdocument)     | Create an empty document.                                 |
| [`deleteDocuments()`]({{ site.api }}class/documentmanager.html#deletedocuments)     | Delete the specified document(s) by the document uid(s).  |
| [`deleteAllDocuments()`]({{ site.api }}class/documentmanager.html#deletealldocuments)  | Delete all documents.                                     |
| [`getDocument()`]({{ site.api }}class/documentmanager.html#getdocument)         | Get the specified document object with the document uid.  |
| [`getAllDocuments()`]({{ site.api }}class/documentmanager.html#getalldocuments)     | Get all documents' objects.                               |
| [`mergeDocuments()`]({{ site.api }}class/documentmanager.html#mergedocuments)      | Merge specified documents to a new document.              |
| [`copyPagesToDocument()`]({{ site.api }}class/documentmanager.html#copypagestodocument) | Copy pages from a specified document to another document. |
| [`movePagesToDocument()`]({{ site.api }}class/documentmanager.html#movepagestodocument) | Move pages from a specified document to another document. |

**Events**

| API Name | Description                                        |
| -------- | -------------------------------------------------- |
| [`on()`]({{ site.api }}class/documentmanager.html#on)     | Bind a listener to the specified event.            |
| [`off()`]({{ site.api }}class/documentmanager.html#off)    | Unbind event listener(s) from the specified event. |

***Integrated Events***

| Event Name      | Description                               |
| --------------- | ----------------------------------------- |
| [`documentCreated`]({{ site.api }}class/documentmanager.html#documentcreated) | Triggered when a new document is created. |
| [`documentDeleted`]({{ site.api }}class/documentmanager.html#documentdeleted) | Triggered when a document is deleted.     |


<div class="multi-panel-end"></div>

<div class="multi-panel-start"></div>

## [EditViewer Class]({{ site.api }}class/editviewer.html)

**Create and Destroy Instances** 

| API Name       | Description                                   |
| ------------ | --------------------------------------------- |
| [`EditViewer()`]({{ site.api }}class/editviewer.html#editviewer) | Default constructor of an `EditViewer` instance. |
| [`destroy()`]({{ site.api }}class/editviewer.html#destroy)             | Destroy the `EditViewer` instance.                             |

**Viewer Control**

| API Name              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [`bindContainer()`]({{ site.api }}class/editviewer.html#bindcontainer)     | Bind the viewer to the specified container.                  |
| [`unbindContainer()`]({{ site.api }}class/editviewer.html#unbindcontainer) | Unbind the viewer from the specified container.              |
| [`isBoundContainer`]({{ site.api }}class/editviewer.html#isboundcontainer) | Return whether the viewer is bound to a container. |
| [`getStyle()`]({{ site.api }}class/editviewer.html#getstyle)            | Get the style object of `EditViewer`.                        |
| [`updateStyle()`]({{ site.api }}class/editviewer.html#updatestyle)        | Update the style object of `EditViewer`.                     |
| [`getUiConfig()`]({{ site.api }}class/editviewer.html#getuiconfig)         | Get current `UiConfig` object.                               |
| [`updateUiConfig()`]({{ site.api }}class/editviewer.html#updateuiconfig)     | Update `UiConfig` object.                                    |
| [`show()`]({{ site.api }}class/editviewer.html#show)                | Show the viewer.                                             |
| [`hide()`]({{ site.api }}class/editviewer.html#hide)                | Hide the viewer.                                             |
| [`isVisible`]({{ site.api }}class/editviewer.html#isvisible)        | Return whether the viewer is shown or hidden.      |
| [`toolMode`]({{ site.api }}class/editviewer.html#toolmode)              | Specify or return the tool mode of the viewer.     |

**Document and Page Control**

| API Name              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [`openDocument()`]({{ site.api }}class/editviewer.html#opendocument)        | Open the specified document by document uid.                 |
| [`closeDocument()`]({{ site.api }}class/editviewer.html#closedocument)       | Close current document.                                      |
| [`currentDocument`]({{ site.api }}class/editviewer.html#currentdocument)   | Return the object of the current document.         |
| [`getPageCount()`]({{ site.api }}class/editviewer.html#getpagecount)        | Get the page count in the viewer.                            |
| [`goToPage()`]({{ site.api }}class/editviewer.html#gotopage)            | Navigate to the specified page by index.                     |
| [`getCurrentPageIndex()`]({{ site.api }}class/editviewer.html#getcurrentpageindex) | Get the index of current page.                               |
| [`getCurrentPageUid()`]({{ site.api }}class/editviewer.html#getcurrentpageuid)   | Get the uid of the current page.                             |
| [`indexToUid()`]({{ site.api }}class/editviewer.html#indextouid)          | Get the uid of the specified page by its index.                      |
| [`uidToIndex()`]({{ site.api }}class/editviewer.html#uidtoindex)          | Get the index of the specified page by its uid. |


**Display Control**

| API Name              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [`displayMode`]({{ site.api }}class/editviewer.html#displaymode)                 | Specify or return the display mode of the viewer.  |
| [`setParallelScrollCount()`]({{ site.api }}class/editviewer.html#setparallelscrollcount)     | Specify the number of pages to scroll in parallel.    |
| [`fitMode`]({{ site.api }}class/editviewer.html#fitmode)                     | Specify or return the fit mode of the viewer.      |
| [`zoom`]({{ site.api }}class/editviewer.html#zoom)                        | Specify or return zoom ratio.                      |
| [`zoomOrigin`]({{ site.api }}class/editviewer.html#zoomorigin)                  | Specify or return the zoom origin of the viewer.   |

**Edit Operations**

| API Name              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [`rotate()`]({{ site.api }}class/editviewer.html#rotate)              | Rotate the specified pages.                                  |
| [`crop()`]({{ site.api }}class/editviewer.html#crop)                | Crop the specified page(s) with the specified rectangle.     |
| [`getCropRect()`]({{ site.api }}class/editviewer.html#getcroprect)         | Get the crop rectangular selection.                            |
| [`setCropRect()`]({{ site.api }}class/editviewer.html#setcroprect)         | Set a crop rectangular selection on the current page. *This method is only available when [`toolMode`]({{ site.api }}class/editviewer.html#toolmode) is `crop` mode.* |
| [`undo()`]({{ site.api }}class/editviewer.html#undo)                | Undo the last editing operation.                             |
| [`redo()`]({{ site.api }}class/editviewer.html#redo)                | Redo the last undo operation.                                |
| [`saveOperations()`]({{ site.api }}class/editviewer.html#saveoperations)      | Save the edit operations in pages to document.               |

**Events**

| API Name | Description                                        |
| -------- | -------------------------------------------------- |
| [`on()`]({{ site.api }}class/editviewer.html#on)     | Bind a listener to the specified event.            |
| [`off()`]({{ site.api }}class/editviewer.html#off)    | Unbind event listener(s) from the specified event. |

***Integrated Events***

| Event Name          | Description                                                  |
| ------------------- | ------------------------------------------------------------ |
| [`resized`]({{ site.api }}class/editviewer.html#resized)             | Triggered when the viewer is resized.                        |
| [`pageRendered`]({{ site.api }}class/editviewer.html#pagerendered)        | Triggered when a page has been completely rendered.          |
| [`currentIndexChanged`]({{ site.api }}class/editviewer.html#currentindexchanged) | Triggered when currentIndex is changed.                      |
| [`currentPageChanged`]({{ site.api }}class/editviewer.html#currentpagechanged)  | Triggered when current page is changed.                      |
| [`displayModeChanged`]({{ site.api }}class/editviewer.html#displaymodechanged)  | Triggered when the display mode is changed.                  |
| [`fitModeChanged`]({{ site.api }}class/editviewer.html#fitmodechanged)      | Triggered when the fit mode has changed.                     |
| [`zoomChanged`]({{ site.api }}class/editviewer.html#zoomchanged)         | Triggered when the zoom ratio has been changed.              |
| [`toolModeChanged`]({{ site.api }}class/editviewer.html#toolmodechanged)     | Triggered when the tool mode has changed.                    |
| [`cropRectDrawn`]({{ site.api }}class/editviewer.html#croprectdrawn)       | Triggered when a rectangular selection is drawn.               |
| [`cropRectDeleted`]({{ site.api }}class/editviewer.html#croprectdeleted)     | Triggered when the rectangular selection is deleted.           |
| [`cropRectModified`]({{ site.api }}class/editviewer.html#croprectmodified)    | Triggered when the crop rectangular selection is modified.     |
| [`click`]({{ site.api }}class/editviewer.html#click)               | Triggered when click in the viewer's viewing area.           |
| [`dblclick`]({{ site.api }}class/editviewer.html#dbclick)            | Triggered when double click in the viewer's viewing area.    |
| [`rightclick`]({{ site.api }}class/editviewer.html#rightclick)          | Triggered when right click in the viewer's viewing area.     |

<div class="multi-panel-end"></div>

<div class="multi-panel-start"></div>

## [CaptureViewer Class]({{ site.api }}class/captureviewer.html)

**Create and Destroy Instances** 

| API Name       | Description                                   |
| ------------ | --------------------------------------------- |
| [`CaptureViewer()`]({{ site.api }}class/captureviewer.html#captureviewer) | Default constructor of a `CaptureViewer` instance. |
| [`destroy()`]({{ site.api }}class/captureviewer.html#destroy)             | Destroy the `CaptureViewer` instance.                             |

**Viewer Control**

| API Name              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [`bindContainer()`]({{ site.api }}class/captureviewer.html#bindcontainer)     | Bind the viewer to the specified container.                  |
| [`unbindContainer()`]({{ site.api }}class/captureviewer.html#unbindcontainer) | Unbind the viewer from the specified container.              |
| [`isBoundContainer`]({{ site.api }}class/captureviewer.html#isboundcontainer) | Return whether the viewer is bound to a container. |
| [`getStyle()`]({{ site.api }}class/captureviewer.html#getstyle)            | Get the style object of `CaptureViewer`.                        |
| [`updateStyle()`]({{ site.api }}class/captureviewer.html#updatestyle)        | Update the style object of `CaptureViewer`.                     |
| [`getUiConfig()`]({{ site.api }}class/captureviewer.html#getuiconfig)         | Get current `UiConfig` object.                               |
| [`updateUiConfig()`]({{ site.api }}class/captureviewer.html#updateuiconfig)     | Update `UiConfig` object.                                    |
| [`show()`]({{ site.api }}class/captureviewer.html#show)                | Show the viewer.                                             |
| [`hide()`]({{ site.api }}class/captureviewer.html#hide)                | Hide the viewer.                                             |
| [`isVisible`]({{ site.api }}class/captureviewer.html#isvisible)        | Return whether the viewer is shown or hidden.      |

**Document Control**

| API Name              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [`openDocument()`]({{ site.api }}class/captureviewer.html#opendocument)        | Open the specified document by document uid.                 |
| [`closeDocument()`]({{ site.api }}class/captureviewer.html#closedocument)       | Close current document.                                      |
| [`currentDocument`]({{ site.api }}class/captureviewer.html#currentdocument)   | Return the object of the current document.         |

**Camera Control**

| API Name              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [`play()`]({{ site.api }}class/captureviewer.html#play)                 | Play the camera video stream.                                |
| [`stop()`]({{ site.api }}class/captureviewer.html#stop)                 | Stop the camera video stream.                                |
| [`capture()`]({{ site.api }}class/captureviewer.html#capture)              | Capture a frame from video stream.                           |
| [`getAllCameras()`]({{ site.api }}class/captureviewer.html#getallcameras)        | Return information of all available cameras on the device.   |
| [`selectCamera()`]({{ site.api }}class/captureviewer.html#selectcamera)         | Select a camera as the video source.                         |
| [`getCurrentCamera()`]({{ site.api }}class/captureviewer.html#getcurrentcamera)     | Return information about the current camera.                 |
| [`getCurrentResolution()`]({{ site.api }}class/captureviewer.html#getcurrentresolution) | Return the resolution of the current video input.            |
| [`turnOnTorch()`]({{ site.api }}class/captureviewer.html#turnontorch)          | Turn on the torch/flashlight if the current camera supports it. |
| [`turnOffTorch()`]({{ site.api }}class/captureviewer.html#turnofftorch)         | Turn off the torch/flashlight.                               |
| [`enableAutoCapture`]({{ site.api }}class/captureviewer.html#enableautocapture)           | Specify or return whether to enable automatic capture.       |
| [`enableAutoDetect`]({{ site.api }}class/captureviewer.html#enableautodetect)            | Specify or return whether to enable automatic border detection in video stream. |
| [`acceptedPolygonConfidence`]({{ site.api }}class/captureviewer.html#acceptedpolygonconfidence)   | Specify or return the confidence when detecting the border.  |
| [`maxFrameNumber`]({{ site.api }}class/captureviewer.html#maxframenumber)              | Specify or return the maximum number of frames detected per second. |

**Events**

| API Name | Description                                        |
| -------- | -------------------------------------------------- |
| [`on()`]({{ site.api }}class/captureviewer.html#on)     | Bind a listener to the specified event.            |
| [`off()`]({{ site.api }}class/captureviewer.html#off)    | Unbind event listener(s) from the specified event. |

***Integrated Events***

| Event Name    | Description                                                  |
| ------------- | ------------------------------------------------------------ |
| [`resized`]({{ site.api }}class/captureviewer.html#resized)       | Triggered when the viewer is resized.                        |
| [`played`]({{ site.api }}class/captureviewer.html#played)        | Triggered when the camera video stream is played.            |
| [`stopped`]({{ site.api }}class/captureviewer.html#stopped)       | Triggered when the camera video stream is stopped.           |
| [`captured`]({{ site.api }}class/captureviewer.html#captured)      | Triggered when a frame is captured.                          |
| [`cameraChanged`]({{ site.api }}class/captureviewer.html#camerachanged) | Triggered when the used camera is changed.                   |
| [`click`]({{ site.api }}class/captureviewer.html#click)         | Triggered when click in the viewer's viewing area.           |
| [`dblclick`]({{ site.api }}class/captureviewer.html#dblclick)      | Triggered when double click in the viewer's viewing area.    |
| [`rightclick`]({{ site.api }}class/captureviewer.html#rightclick)    | Triggered when right click in the viewer's viewing area.     |

<div class="multi-panel-end"></div>

<div class="multi-panel-start"></div>

## [PerspectiveViewer Class]({{ site.api }}class/perspectiveviewer.html)

**Create and Destroy Instances** 

| API Name       | Description                                   |
| ------------ | --------------------------------------------- |
| [`PerspectiveViewer()`]({{ site.api }}class/perspectiveviewer.html#perspectiveviewer) | Default constructor of a `PerspectiveViewer` instance. |
| [`destroy()`]({{ site.api }}class/perspectiveviewer.html#destroy)             | Destroy the `PerspectiveViewer` instance.                             |

**Viewer Control**

| API Name              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [`bindContainer()`]({{ site.api }}class/perspectiveviewer.html#bindcontainer)     | Bind the viewer to the specified container.                  |
| [`unbindContainer()`]({{ site.api }}class/perspectiveviewer.html#unbindcontainer) | Unbind the viewer from the specified container.              |
| [`isBoundContainer`]({{ site.api }}class/perspectiveviewer.html#isboundcontainer) | Return whether the viewer is bound to a container. |
| [`getStyle()`]({{ site.api }}class/perspectiveviewer.html#getstyle)            | Get the style object of `PerspectiveViewer`.                        |
| [`updateStyle()`]({{ site.api }}class/perspectiveviewer.html#updatestyle)        | Update the style object of `PerspectiveViewer`.                     |
| [`getUiConfig()`]({{ site.api }}class/perspectiveviewer.html#getuiconfig)         | Get current `UiConfig` object.                               |
| [`updateUiConfig()`]({{ site.api }}class/perspectiveviewer.html#updateuiconfig)     | Update `UiConfig` object.                                    |
| [`show()`]({{ site.api }}class/perspectiveviewer.html#show)                | Show the viewer.                                             |
| [`hide()`]({{ site.api }}class/perspectiveviewer.html#hide)                | Hide the viewer.                                             |
| [`isVisible`]({{ site.api }}class/perspectiveviewer.html#isvisible)        | Return whether the viewer is shown or hidden.      |

**Document and Page Control**

| API Name              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [`openDocument()`]({{ site.api }}class/perspectiveviewer.html#opendocument)        | Open the specified document by document uid.                 |
| [`closeDocument()`]({{ site.api }}class/perspectiveviewer.html#closedocument)       | Close current document.                                      |
| [`currentDocument`]({{ site.api }}class/perspectiveviewer.html#currentdocument)   | Return the object of the current document.         |
| [`getPageCount()`]({{ site.api }}class/perspectiveviewer.html#getpagecount)        | Get the page count in the viewer.                            |
| [`goToPage()`]({{ site.api }}class/perspectiveviewer.html#gotopage)            | Navigate to the specified page by index.                     |
| [`getCurrentPageIndex()`]({{ site.api }}class/perspectiveviewer.html#getcurrentpageindex) | Get the index of current page.                               |
| [`getCurrentPageUid()`]({{ site.api }}class/perspectiveviewer.html#getcurrentpageuid)   | Get the uid of the current page.                             |
| [`indexToUid()`]({{ site.api }}class/perspectiveviewer.html#indextouid)          | Get the uid of the specified page by its index.                      |
| [`uidToIndex()`]({{ site.api }}class/perspectiveviewer.html#uidtoindex)          | Get the index of the specified page by its uid. |

**Perspective Transformation**

| API Name              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [`setQuadSelection()`]({{ site.api }}class/perspectiveviewer.html#setquadselection)    | Set a quadrilateral selection on the current page.              |
| [`getQuadSelection()`]({{ site.api }}class/perspectiveviewer.html#getquadselection)    | Get the quadrilateral selection.                                |
| [`resetQuadSelection()`]({{ site.api }}class/perspectiveviewer.html#resetquadselection)  | Reset the quadrilateral selection to the original one.          |
| [`applyPerspective()`]({{ site.api }}class/perspectiveviewer.html#applyperspective)         | Performs a perspective transformation in current page based on the specified quadrangle. |

**Edit Operations**

| API Name              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [`rotate()`]({{ site.api }}class/perspectiveviewer.html#rotate)              | Rotate the specified pages.                                  |
| [`saveOperations()`]({{ site.api }}class/perspectiveviewer.html#saveoperations)      | Save the edit operations in pages to document.               |

**Events**

| API Name | Description                                        |
| -------- | -------------------------------------------------- |
| [`on()`]({{ site.api }}class/perspectiveviewer.html#on)     | Bind a listener to the specified event.            |
| [`off()`]({{ site.api }}class/perspectiveviewer.html#off)    | Unbind event listener(s) from the specified event. |

***Integrated Events***

| Event Name          | Description                                                  |
| ------------------- | ------------------------------------------------------------ |
| [`resized`]({{ site.api }}class/perspectiveviewer.html#resized)             | Triggered when the viewer is resized.                        |
| [`pageRendered`]({{ site.api }}class/perspectiveviewer.html#pagerendered)        | Triggered when a page has been completely rendered.          |
| [`currentIndexChanged`]({{ site.api }}class/perspectiveviewer.html#currentindexchanged) | Triggered when currentIndex is changed.                      |
| [`currentPageChanged`]({{ site.api }}class/perspectiveviewer.html#currentpagechanged)  | Triggered when current page is changed.                      |
| [`quadModifiedModified`]({{ site.api }}class/perspectiveviewer.html#quadmodified)    | Triggered when the quadrilateral selection is modified.     |
| [`click`]({{ site.api }}class/perspectiveviewer.html#click)               | Triggered when click in the viewer's viewing area.           |
| [`dblclick`]({{ site.api }}class/perspectiveviewer.html#dbclick)            | Triggered when double click in the viewer's viewing area.    |
| [`rightclick`]({{ site.api }}class/perspectiveviewer.html#rightclick)          | Triggered when right click in the viewer's viewing area.     |

<div class="multi-panel-end"></div>

<div class="multi-panel-start"></div>

## [BrowseViewer Class]({{ site.api }}class/browseviewer.html)

**Create and Destroy Instances** 

| API Name       | Description                                   |
| ------------ | --------------------------------------------- |
| [`BrowseViewer()`]({{ site.api }}class/browseviewer.html#browseviewer) | Default constructor of a `BrowseViewer` instance. |
| [`destroy()`]({{ site.api }}class/browseviewer.html#destroy)             | Destroy the `BrowseViewer` instance.                             |

**Viewer Control**

| API Name              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [`bindContainer()`]({{ site.api }}class/browseviewer.html#bindcontainer)     | Bind the viewer to the specified container.                  |
| [`unbindContainer()`]({{ site.api }}class/browseviewer.html#unbindcontainer) | Unbind the viewer from the specified container.              |
| [`isBoundContainer`]({{ site.api }}class/browseviewer.html#isboundcontainer) | Return whether the viewer is bound to a container. |
| [`getStyle()`]({{ site.api }}class/browseviewer.html#getstyle)            | Get the style object of `BrowseViewer`.                        |
| [`updateStyle()`]({{ site.api }}class/browseviewer.html#updatestyle)        | Update the style object of `BrowseViewer`.                     |
| [`getUiConfig()`]({{ site.api }}class/browseviewer.html#getuiconfig)         | Get current `UiConfig` object.                               |
| [`updateUiConfig()`]({{ site.api }}class/browseviewer.html#updateuiconfig)     | Update `UiConfig` object.                                    |
| [`show()`]({{ site.api }}class/browseviewer.html#show)                | Show the viewer.                                             |
| [`hide()`]({{ site.api }}class/browseviewer.html#hide)                | Hide the viewer.                                             |
| [`isVisible`]({{ site.api }}class/browseviewer.html#isvisible)        | Return whether the viewer is shown or hidden.      |
| [`multiselectMode`]({{ site.api }}class/browseviewer.html#multiselectmode) | Specify or return whether to allow multiple pages to be selected at once. |

**Document and Page Control**

| API Name              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [`openDocument()`]({{ site.api }}class/browseviewer.html#opendocument)        | Open the specified document by document uid.                 |
| [`closeDocument()`]({{ site.api }}class/browseviewer.html#closedocument)       | Close current document.                                      |
| [`currentDocument`]({{ site.api }}class/browseviewer.html#currentdocument)   | Return the object of the current document.         |
| [`getPageCount()`]({{ site.api }}class/browseviewer.html#getpagecount)        | Get the page count in the viewer.                            |
| [`goToPage()`]({{ site.api }}class/browseviewer.html#gotopage)            | Navigate to the specified page by index.                     |
| [`getCurrentPageIndex()`]({{ site.api }}class/browseviewer.html#getcurrentpageindex) | Get the index of current page.                               |
| [`getCurrentPageUid()`]({{ site.api }}class/browseviewer.html#getcurrentpageuid)   | Get the uid of the current page.                             |
| [`indexToUid()`]({{ site.api }}class/browseviewer.html#indextouid)          | Get the uid of the specified page by its index.                      |
| [`uidToIndex()`]({{ site.api }}class/browseviewer.html#uidtoindex)          | Get the index of the specified page by its uid. |
| [`getSelectedPageIndices()`]({{ site.api }}class/browseviewer.html#getselectedpageindices) | Get indices of selected pages.                               |
| [`selectPages()`]({{ site.api }}class/browseviewer.html#selectpages)            | Select pages by specified indices.                           |
| [`selectAllPages()`]({{ site.api }}class/browseviewer.html#selectallpages)         | Select all pages.                                            |


**Display Control**

| API Name              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [`setRowAndColumn()`]({{ site.api }}class/browseviewer.html#setrowandcolumn)        | Set rows and columns of displayed pages.                     |

**Edit Operations**

| API Name              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [`rotate()`]({{ site.api }}class/browseviewer.html#rotate)              | Rotate the specified pages.                                  |
| [`saveOperations()`]({{ site.api }}class/browseviewer.html#saveoperations)      | Save the edit operations in pages to document.               |

**Events**

| API Name | Description                                        |
| -------- | -------------------------------------------------- |
| [`on()`]({{ site.api }}class/browseviewer.html#on)     | Bind a listener to the specified event.            |
| [`off()`]({{ site.api }}class/browseviewer.html#off)    | Unbind event listener(s) from the specified event. |

***Integrated Events***

| Event Name          | Description                                                  |
| ------------------- | ------------------------------------------------------------ |
| [`resized`]({{ site.api }}class/browseviewer.html#resized)             | Triggered when the viewer is resized.                        |
| [`pageRendered`]({{ site.api }}class/browseviewer.html#pagerendered)        | Triggered when a page has been completely rendered.          |
| [`currentIndexChanged`]({{ site.api }}class/browseviewer.html#currentindexchanged) | Triggered when currentIndex is changed.                      |
| [`currentPageChanged`]({{ site.api }}class/browseviewer.html#currentpagechanged)  | Triggered when current page is changed.                      |
| [`selectedPagesChanged`]({{ site.api }}class/browseviewer.html#selectedpageschanged) | Trigeered when the page(s) is selected.                      |
| [`pagesDragged`]({{ site.api }}class/browseviewer.html#pagesdragged)         | Triggered when page(s) is dragged.                           |
| [`pagesDropped`]({{ site.api }}class/browseviewer.html#pagesdropped)         | Triggered when page(s) is dropped.                           |
| [`click`]({{ site.api }}class/browseviewer.html#click)               | Triggered when click in the viewer's viewing area.           |
| [`dblclick`]({{ site.api }}class/browseviewer.html#dbclick)            | Triggered when double click in the viewer's viewing area.    |
| [`rightclick`]({{ site.api }}class/browseviewer.html#rightclick)          | Triggered when right click in the viewer's viewing area.     |

<div class="multi-panel-end"></div>

<div class="multi-panel-start"></div>

## [CustomViewer Class]({{ site.api }}class/customviewer.html)

**Create and Destroy Instances** 

| API Name       | Description                                   |
| ------------ | --------------------------------------------- |
| [`CustomViewer()`]({{ site.api }}class/customviewer.html#customviewer) | Default constructor of a `CustomViewer` instance. |
| [`destroy()`]({{ site.api }}class/customviewer.html#destroy)             | Destroy the `CustomViewer` instance.                             |

**Viewer Control**

| API Name              | Description                                                  |
| --------------------- | ------------------------------------------------------------ |
| [`bindContainer()`]({{ site.api }}class/customviewer.html#bindcontainer)     | Bind the viewer to the specified container.                  |
| [`unbindContainer()`]({{ site.api }}class/customviewer.html#unbindcontainer) | Unbind the viewer from the specified container.              |
| [`isBoundContainer`]({{ site.api }}class/customviewer.html#isboundcontainer) | Return whether the viewer is bound to a container. |
| [`getUiConfig()`]({{ site.api }}class/customviewer.html#getuiconfig)         | Get current `UiConfig` object.                               |
| [`updateUiConfig()`]({{ site.api }}class/customviewer.html#updateuiconfig)     | Update `UiConfig` object.                                    |
| [`show()`]({{ site.api }}class/customviewer.html#show)                | Show the viewer.                                             |
| [`hide()`]({{ site.api }}class/customviewer.html#hide)                | Hide the viewer.                                             |
| [`isVisible`]({{ site.api }}class/customviewer.html#isvisible)        | Return whether the viewer is shown or hidden.      |

**Events**

| API Name | Description                                        |
| -------- | -------------------------------------------------- |
| [`on()`]({{ site.api }}class/customviewer.html#on)     | Bind a listener to the specified event.            |
| [`off()`]({{ site.api }}class/customviewer.html#off)    | Unbind event listener(s) from the specified event. |

<div class="multi-panel-end"></div>

<div class="multi-panel-switching-end"></div>

Besides, there are two advanced classes.

- [ImageFilter]({{ site.api }}class/advanced/imagefilter.html)
- [DocumentDetect]({{ site.api }}class/advanced/documentdetect.html)