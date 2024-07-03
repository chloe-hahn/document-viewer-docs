---
layout: default-layout
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
title: Dynamsoft Document Viewer - Release Notes
keywords: Documentation, Dynamsoft Document Viewer, Release Notes
breadcrumbText: Release Notes
description: Dynamsoft Document Viewer Documentation Release Notes
permalink: /releasenotes/index.html
---

# Release Notes

## 1.1 (01/12/2024)

### Improved

- Optimized compatibility with browsers. [>> Detail]({{ site.gettingstarted }}sys_requirement.html#supported-browsers)

### Added

- Added the namespace [`Dynamsoft.DDV.Core`]({{ site.api }}namespace/ddv_core.html).

- Added the property [`license`]({{ site.api }}namespace/ddv_core.html#license) to specify the license string.

- Added the property [`engineResourcePath`]({{ site.api }}namespace/ddv_core.html#engineresourcepath) to specify the path leading to a folder containing the distributed WASM files.

- Added the property [`deviceFriendlyName`]({{ site.api }}namespace/ddv_core.html#devicefriendlyname) to specify a human-readable name for the device which corresponds to its UUID.

- Added the method [`loadWasm()`]({{ site.api }}namespace/ddv_core.html#loadwasm) to load WASM modules before initializing.

- Added the method [`init()`]({{ site.api }}namespace/ddv_core.html#init) to initialize DDV.

- Added the method [`insertBlankPage()`]({{ site.api }}interface/idocument/index.html#insertblankpage) to insert a blank page to the document.

### Removed

The following API is removed.

| API Name                  | Notes                                                        |
| ------------------------- | ------------------------------------------------------------ |
| `Dynamsoft.DDV.setConfig()` | Use [`Dynamsoft.DDV.Core.license`]({{ site.api }}namespace/ddv_core.html#license),  [`Dynamsoft.DDV.Core.engineResource`]({{ site.api }}namespace/ddv_core.html#engineresourcepath), [`Dynamsoft.DDV.Core.deviceFriendlyName`]({{ site.api }}namespace/ddv_core.html#devicefriendlyname), [`Dynamsoft.DDV.Core.init()`]({{ site.api }}namespace/ddv_core.html#init) instead. |

## 1.0.0 (12/26/2023)

Dynamsoft Document Viewer (DDV) is a versatile SDK designed to offer a range of viewers for configuring and executing various document processing workflows.

### Highlights

#### Efficient Data Management

Organize, retrieve, and manage documents and pages efficiently: 
- Document Management: Document creation/deletion/merging, etc.
- Page management: Pages in documents loading/saving/deleting/moving, etc.

#### Various Viewers 

Various kinds of viewers implement different document processing flows:
- Edit Viewer: Edit the pages in document, such as, rotating, cropping, filtering, etc. and adjust the layout of the display.
- Capture Viewer: Control camera, play video stream, and capture the images from camera.
- Perspective Viewer: Do page boundaries manual adjustment & perspective transformation.
- Browse Viewer: Display pages in multiple-mode, pages can be multiple selected.
- Custom Viewer: No built-in UI or functionality, which is used for creating your own viewer.

#### Flexible Customization

Besides using the default user interface and viewer directly, developers can easily and flexibly customize them:
- [User Interface](https://www.dynamsoft.com/document-viewer/docs/ui/index.html): Layout, elements
- [Viewer](https://www.dynamsoft.com/document-viewer/docs/viewer/index.html): Styles, viewer properties

#### Advanced Features

Dynamsoft Document Viewer provides methods to access document boundaries detection and image filter algorithms.
- [Image filter](https://www.dynamsoft.com/document-viewer/docs/features/advanced/imagefilter.html): Image filter algorithm which is used by Filter element in Edit Viewer.
- [Document detection](https://www.dynamsoft.com/document-viewer/docs/features/advanced/documentdetect.html): Document boundaries detection algorithm which is used during capturing images. Recommend using [Dynamsoft Document Normalizer](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/).
