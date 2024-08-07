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

## 2.0 (15/08/2024)

**We are excited to introduce version 2.0, which focuses on adding a powerful new annotation feature. This release includes comprehensive support for various types of annotations, new APIs for managing annotations, and advanced UI capabilities for seamless interaction.**

### Annotation Support

- **Annotation Types:**

    - [Rectangle]({{ site.api }}class/annotation/rectangle.html)
    - [Ellipse]({{ site.api }}class/annotation/ellipse.html)
    - [Polygon]({{ site.api }}class/annotation/polygon.html)
    - [Polyline]({{ site.api }}class/annotation/polyline.html)
    - [Line]({{ site.api }}class/annotation/line.html)
    - [Ink]({{ site.api }}class/annotation/ink.html)
    - [TextBox]({{ site.api }}class/annotation/textbox.html)
    - [TextTypewriter]({{ site.api }}class/annotation/texttypewriter.html)
    - [Stamp]({{ site.api }}class/annotation/stamp.html)

- **New APIs for Annotation Management:**

    - Load and save annotations
    - Create, delete, and retrieve annotations based on various conditions
    - Adjust annotation hierarchy
    - Handle events triggered by annotation operations

- **Direct Annotation Operations in the UI:**
    - Add, select, and delete annotations
    - Drag, resize, and rotate selected annotations
    - Real-time editing of annotation styles using the palette

- **Annotation Configuration:**

    Configure annotation UI through `EditViewerConstructorOptions.annotationConfig`, including the toolbar, palette, and default annotation style:

    - [annotationSelectionStyle]({{ site.api }}interface/annotationconfig.html#annotationSelectionStyle): Defines the style of annotation selection.
    - [inkCreateDelay]({{ site.api }}interface/annotationconfig.html#inkCreateDelay): Specifies the delay for ink creation to support annotations created in multiple strokes.
    - [showOnTopWhenSelected]({{ site.api }}interface/annotationconfig.html#showOnTopWhenSelected): Determines whether the selected annotation should be displayed on the top layer.

- **New Built-in Elements**
    - Added built-in elements to enhance UI configuration flexibility.

### New APIs for Annotation

- Added the namespace [`Dynamsoft.DDV.annotationManager`]({{ site.api }}class/annotationmanager.html).

- Added the method [`selectAnnotations()`]({{ site.api }}class/editviewer.html#selectannotations) to select the specified annotation(s) on the current page.
- Added the method [`getSelectedAnnotations()`]({{ site.api }}class/editviewer.html#getselectedannotations) to retrieve selected annotation(s).
- Added properties [`mediaBox`]({{ site.api }}interface/idocument/pagedata.html#mediaBox) and [`cropBox`]({{ site.api }}interface/idocument/pagedata.html#cropBox) to `PageData` for accurate annotation position calculation.
- Added the property [`annotationConfig`]({{ site.api }}interface/editviewerconstructoroptions.html#annotationConfig) to `EditViewerConstructorOptions` for configuring the annotation part in the viewer.
- Added the property [`annotationMode`]({{ site.api }}class/editviewer.html#annotationmode) to specify or return the annotation mode of the viewer.
- Added the parameter [`defaultUiConfigOptions`]({{ site.api }}namespace/ddv.html#static-getdefaultuiconfig) to `getDefaultUiConfig()` to retrieve configurations, including annotations.
- Added the parameter [`printSettings`]({{ site.api }}interface/idocument/printsettings.html#printSettings) to the [`document.print()`]({{ site.api }}interface/idocument/index.html#print) to specify whether printable annotations should be included in the print.
- Added the type `annotation` to [`ToolMode`]({{ site.api }}class/editviewer.html#toolMode) to enable a mode that allows annotations to be manipulated via the UI.
- Added the type `annotationSelectionStyle` to [`EditViewerStyleName`]({{ site.api }}class/editviewer.html#getStyle) for retrieving or updating the annotation selection style.
- Added the attribute `saveAnnotation` to the interfaces [`SavePngSettings`]({{ site.api }}interface/idocument/savepngsettings.html#saveAnnotation), [`SaveJpegSettings`]({{ site.api }}interface/idocument/savejpegsettings.html#saveAnnotation), or [`SaveTiffSettings`]({{ site.api }}interface/idocument/savetiffsettings.html#saveAnnotation) to determine whether annotations are saved as part of the image when calling [`saveToPng()`]({{ site.api }}interface/idocument/index.html#saveToPng), [`saveToJpeg()`]({{ site.api }}interface/idocument/index.html#saveToJpeg), or [`saveToTiff()`]({{ site.api }}interface/idocument/index.html#saveToTiff).
- Added [`saveAnnotation`]({{ site.api }}interface/idocument/savepdfsettings.html#saveAnnotation) to the interface `SavePdfSettings` to configure whether annotations should be saved when `document.saveToPdf()` is called.


**Additionally, we've optimized performance and added several new features to enhance the overall user experience.**

### Added APIs

- Added the method [`<static> addFonts()`]({{ site.api }}namespace/ddv.html#static-addfonts) to add fonts to the library.
- Added [`password`]({{ site.api }}interface/idocument/savepdfsettings.html#password) to the interface `SavePdfSettings` for configuring the password of the PDF file to save when `document.saveToPdf()` is called.
- Added [`imageScaleFactor`]({{ site.api }}interface/idocument/savepdfsettings.html#imageScaleFactor) to the interface `SavePdfSettings` for configuring the image scale factor of the PDF file to be saved when `document.saveToPdf()` is called.


### Improved

- Optimized image display (图片显示效果优化)
- Optimized the interactive experience of scaling.
- Modified the type of [`PdfSource.renderOptions.renderAnnotations`]({{ site.api }}interface/idocument/pdfsource.html#renderAnnotations) to support reading annotations.
- The method `openDocument()` now supports the UID or the document object. This affects the `openDocument()` method in the [`EditViewer`]({{ site.api }}class/editviewer.html#openDocument), [`PerspectiveViewer`]({{ site.api }}class/perspectiveviewer.html#openDocument), [`CaptureViewer`]({{ site.api }}class/captureviewer.html#openDocument), and [`BrowseViewer`]({{ site.api }}class/browseviewer.html#openDocument) classes.
- Built-in elements now include a hover effect.

### Changed

- Changed the length unit from pixels to points for crop-related functions, for example, [`crop()`]({{ site.api }}class/editviewer.html#crop), [`getCropRect()`]({{ site.api }}class/editviewer.html#getCropRect), [`setCropRect()`]({{ site.api }}class/editviewer.html#setCropRect).
- Changed the units of the parameters `pageWidth` and `pageHeight` in the method [`insertBlankPage`]({{ site.api }}interface/idocument/index.html#insertblankpage) from inches to points.
- Changed the related date string format from D:YYYYMMDDHHmmSS to D:YYYYMMDDHHmmSSOHH'mm'.


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

DDV provides methods to access document boundaries detection and image filter algorithms.
- [Image filter](https://www.dynamsoft.com/document-viewer/docs/features/advanced/imagefilter.html): Image filter algorithm which is used by Filter element in Edit Viewer.
- [Document detection](https://www.dynamsoft.com/document-viewer/docs/features/advanced/documentdetect.html): Document boundaries detection algorithm which is used during capturing images. Recommend using [Dynamsoft Document Normalizer](https://www.dynamsoft.com/document-normalizer/docs/web/programming/javascript/).
