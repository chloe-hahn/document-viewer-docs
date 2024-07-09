---
layout: default-layout
needAutoGenerateSidebar: true
needGenerateH3Content: true
noTitleIndex: true
title: Dynamsoft Document Viewer - Introduction
keywords: Documentation, Dynamsoft Document Viewer, Introduction
breadcrumbText: Introduction
description: Dynamsoft Document Viewer Documentation Introduction
permalink: /introduction/index.html
---

# Introduction to Dynamsoft Document Viewer

Dynamsoft Document Viewer is a browser-based JavaScript SDK designed for viewing and editing images and PDFs. It provides a wide range of functionalities, including PDF annotation, page manipulation, image quality enhancement, and document saving. 

## Security

Dynamsoft Document Viewer is independently developed and does not rely on any external third-party open-source software. All processing, such as rendering and editing, is securely performed within the browser using a web assembly module. This architecture eliminates the need for a server-side backend, ensuring security compliance and scalability. 





## Browser and Platform Compatibility

Dynamsoft Document Viewer is designed to work seamlessly across different browsers and platforms. It is compatible with major browsers like Chrome, Firefox, Safari, and Edge, ensuring a consistent user experience. Additionally, it supports various operating systems, including Windows, macOS, Linux, iOS, and Android, allowing users to access documents from any device.

## Supported File Types

Users can open, edit, and save PDFs, as well as various image formats such as JPEG, PNG, BMP, TIFF, and GIF. 


## Annotation Types

Dynamsoft Document Viewer supports a variety of annotation types to enhance document interaction and collaboration. Users can add, edit, and delete annotations such as: 

* text
* images
* signature
* shapes 
* stamps 
* freehand drawings

## Data Management Concepts

Dynamsoft Document Viewer organizes data using two main concepts: "document" and "page." A document can contain one or multiple pages, and each page must belong to a single document.

* Page: The smallest unit of data management, currently represented as an image. Each page has a unique pageUid.
* Document: A collection of pages, each with a unique docUid. Documents collectively make up the entire data set.

Managing data, therefore, involves managing documents and pages.

* [Document Management]({{ site.features }}datamanagement/docmanagement.html)
* [Page Management]({{ site.features }}datamanagement/pagemanagement.html)

If you are using the default UI of DDV, data processing and management are handled internally.

## UI Customization

The SDK offers extensive customization options, enabling developers to tailor the interface, toolbar, and annotation tools to meet specific application needs and branding requirements.

## Designed with Camera Capture in Mind

Dynamsoft Document Viewer is designed for seamless integration with camera capture. It features five built-in viewer types, with the first three optimized for camera capture scenarios:

* Edit Viewer: Provides image quality enhancement filters.
* Capture Viewer: Includes built-in camera control for continuous capture.
* Perspective Viewer: Equipped with document cropping features; for document detection, using Dynamsoft Document Normalizer is recommended.
* Browse Viewer
* Custom Viewer

As part of the Mobile Web Capture solution, this viewer helps developers create efficient, accurate, and user-friendly workflows, from camera capture to document finalization.







