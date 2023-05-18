# Hyperledger DLT Landscape

[![Netlify Status](https://api.netlify.com/api/v1/badges/78ae7ad4-157c-421d-97ea-f3fca9136a05/deploy-status)](https://app.netlify.com/sites/dltlandscape/deploys)

![DLT Landscape Logo](https://github.com/dltlandscape/dlt-landscape/raw/main/images/left-logo.svg?sanitize=true)

- [Hyperledger DLT Landscape](#cloud-native-landscape)
  * [Current Version](#current-version)
  * [Interactive Version](#interactive-version)
  * [New Entries](#new-entries)
  * [Commit Sign-off](#commit-sign-off)
  * [Logos](#logos)
  * [Proper SVGs](#proper-svgs)
  * [Corrections](#corrections)
  * [External Data](#external-data)
  * [Best Practices Badge](#best-practices-badge)
  * [Non-Updated Items](#non-updated-items)
  * [License](#license)
  * [Formats](#formats)
  * [Installation](#installation)
  * [Vulnerability reporting](#vulnerability-reporting)
  * [Adjusting the Landscape View](#adjusting-the-landscape-view)

Welcome to a living segmentation of the evolving DLT market! Hyperledger DLT Landscape is a business stack with a technology foundation. BTP has created the DLT Landscape for the whole blockchain/DLT community to benefit from and contribute to. The DLT Landscape is open source, curated and hosted by BTP, but independent of the company. It is modeled after the Cloud Native Computing Foundation (CNCF) [landscape](https://landscape.cncf.io) and based on the same open source code.

## Current Version

[![DLT Landscape](https://dltlandscape.org/images/landscape.png)](https://dltlandscape.org/images/landscape.png)

## Interactive Version

Please see [dltlandscape.hyperledger.org/]([https://dltlandscape.org](https://dltlandscape.hyperledger.org/)).

## New Entries

* Your project or company needs a logo and the logo needs to include the name.
* Crunchbase organization should be the company or organization that controls the software. That is normally the owner of the trademark, whether or not a trademark has been formally filed.

If you think your project should be included, please open a pull request to add it to [landscape.yml](landscape.yml). For the logo, you can either upload an SVG to the `hosted_logos` directory or put a URL as the value, and it will be fetched.

Netlify will generate a staging server for you to preview your updates. Please check that the logo and information appear correctly and then add `LGTM` to the pull request confirming your review and requesting a merge.

## Commit Sign-off
All commits should be signed off confirming the [Developer Certificate of Origin](https://developercertificate.org)

You can do this by adding a line to your commit message: 
```
This is my commit message

Signed-off-by: Random Developer <random@developer.example.org>
```
Or via cli:

```
$ git commit -s -m 'This is my commit message'
```

We use the [Github DCO app](https://github.com/apps/dco) to check all commits in a pull request are signed off.

## Logos

The following rules will produce the most readable and attractive logos:

1. We require SVGs, as they are smaller, display correctly at any scale, and work on all modern browsers. If you only have the logo in another vector format (like AI or EPS), please open an issue and we'll convert it to an SVG for you, or you can often do it yourself at https://cloudconvert.com/. Note that you may need to zip your file to attach it to a GitHub issue. Please note that we require pure SVGs and will reject SVGs that contain embedded PNGs since they have the same problems of being bigger and not scaling seamlessly. We also require that SVGs convert fonts to outlines so that they will render correctly whether or not a font is installed. See [Proper SVGs](#proper-svgs) below.
1. Don't use reversed logos (i.e., with a non-white, non-transparent background color). If you only have a reversed logo, create an issue with it attached and we'll produce a non-reversed version for you.
1. Logos must include the company, product or project name in English. It's fine to also include words from another language. If you don't have a version of your logo with the name in it, please open an issue and we'll create one for you (and please specify the font).
1. Match the item name to the English words in the logos. So an Acme Rocket logo that shows "Rocket" should have product name "Rocket", while if the logo shows "Acme Rocket", the product name should be "Acme Rocket". Otherwise, logos look out of place when you sort alphabetically.
1. Google images is often the best way to find a good version of the logo (but ensure it's the up-to-date version). Search for [grpc logo filetype:svg](https://www.google.com/search?q=grpc+logo&tbs=ift:svg,imgo:1&tbm=isch) but substitute your project or product name for grpc.
1. You can either upload an SVG to the `hosted_logos` directory or put a URL as the value, and it will be fetched.

## Proper SVGs

SVGs need to not rely on external fonts so that they will render correctly in any web browser, whether or not the correct fonts are installed. If you have the original AI file, here are the steps in Illustrator to create a proper SVG:

1. Open file in Illustrator
1. Select all text
1. With the text selected, go to Object > Expand in the top menu
1. Export file by going to File > Export > Export As in top menu
1. Select SVG from the format drop down and make sure that "Use Artboards" is checked
1. This will open a SVG options box, make sure to set Decimal to 5 (that is the highest possible, so to ensure that sufficient detail is preserved)
1. Click Okay to export

## Corrections

Please open a pull request with edits to [landscape.yml](landscape.yml). The file [processed_landscape.yml](processed_landscape.yml) is generated and so should never be edited directly.

If the error is with data from [Crunchbase](https://www.crunchbase.com/) you should open an account there and edit the data. If you don't like a project description, edit it in GitHub. If your project isn't showing the license correctly, you may need to paste the unmodified text of the license into a LICENSE file at the root of your project in GitHub, in order for GitHub to serve the license information correctly.

## External Data

The canonical source for all data is [landscape.yml](landscape.yml). Once a day, we download data for projects and companies from the following sources:

* Project info from GitHub
* Funding info from [Crunchbase](https://www.crunchbase.com/)
* Market cap data from Yahoo Finance
* CII Best Practices Badge [data](https://bestpractices.coreinfrastructure.org/)

The update server enhances the source data with the fetched data and saves the result in [processed_landscape.yml](processed_landscape.yml). The app loads a JSON representation of processed_landscape.yml to display data.

## License

This repository contains data received from [Crunchbase](http://www.crunchbase.com). This data is not licensed pursuant to the Apache License. It is subject to Crunchbase’s Data Access Terms, available at [https://data.crunchbase.com/v3.1/docs/terms](https://data.crunchbase.com/v3.1/docs/terms), and is only permitted to be used with this Landscape Project which is hosted by the Linux Foundation.

Everything else is under the Apache License, Version 2.0, except for project and product logos, which are generally copyrighted by the company that created them, and are simply cached here for reliability. The trail map, static landscape, serverless landscape, and [landscape.yml](landscape.yml) file are alternatively available under the [Creative Commons Attribution 4.0 license](https://creativecommons.org/licenses/by/4.0/).

## Formats

The Hyperledger DLT Landscape is available in these formats:

* [PNG](landscape.png)
* [PDF](landscape.pdf)

## Installation

You can install and run locally with the [install directions](INSTALL.md). It's not necessary to install locally if you just want to edit [landscape.yml](landscape.yml). You can do so via the GitHub web interface.

## Issue and Vulnerability reporting

Please open an [issue](https://github.com/dltlandscape/dlt-landscape/issues/new) or, for sensitive information, email  Original source code inquiries: info@cncf.io

## Adjusting the Landscape View
The file src/components/MainContent2.js describes the key elements of a
landscape big picture. It specifies where to put these sections: App Definition
and Development, Orchestration & Management, Runtime,  Provisioning, Cloud, 
Platform, Observability and Analysis, Special. Also it specifies where to
locate the link to the serverless preview and an info with a QR code.

All these elements should have `top`, `left`, `width` and `height` properties to
position them. `rows` and `cols` specify how much columns or rows we expect in a
given horizontal or vertical section.

When we see that those elements can not fit the sections, we need to either increase
the width of all the horizontal sections, or increase height and amount of rows
in a single horizontal section and adjust the position of sections below.

Beside that, we have to adjust the width of a parent div (1620), the width in a
`src/components/BigPicture/FullscreenLandscape.js` (1640) and the width in a
`tools/renderLandscape.js` (6560, because of x4 zoom and margins)

Sometimes the total height is changed too, then we need to adjust the height the
same way as we adjust the width.

We have an experimental `fitWidth` property, it is good when you want to get rid of
extra space on the right of a section.

The best way to test that layout is ok, is to visit `/landscape`, and if it looks ok, run `PORT=3000 babel-node
tools/renderLandscape` and see the rendered png files, they are in src/images folder.
