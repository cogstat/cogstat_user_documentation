---
title: Displaying the data and results graphically
---
CogStat creates charts for various aspects of the data and results automatically. There are specific considerations on how these charts are created:

* [Individual data](Displaying-individual-data) are displayed in the raw data charts and the sample charts
* For [repeated measures data](Displaying-individual-data-in-repeated-measures-variables), the connection between the same case's values are also displayed
* [Ordinal and nominal variables](Displaying-ordinal-and-nominal-data) are handled distinctively
* [Within-subject and between-subject information](Display-within-subject-and-between-subject-information-when-comparing-variables) can be displayed flexibly
* Box plots display the minimum and maximum values, too
    * In CogStat, whiskers of [box plots](https://en.wikipedia.org/wiki/Box_plot) represent the minimum and maximum values. Up to v1.7, in line with some other analysis software, CogStat used the [Tukey boxplot](https://en.wikipedia.org/wiki/Box_plot#Variations) where the whiskers cannot be larger than the than 1.5 times the [interquartile range](https://en.wikipedia.org/wiki/Interquartile_range). The minimum-maximum solution is more in line with the idea that the charts should show the information the analysis relies on.

## Axes of the charts

In CogStat, in most cases, the [axes style](Displaying-ordinal-and-nominal-data) reflects the measurement level of that variable:

* For interval variables, the axes are solid.
* For ordinal variables, the axes are dashed.
* For nominal variables, the axes are dotted.

## Modifying the charts

### Display options

In some analyses, some fundamental parts of the charts can be changed (e.g., click the `Display options...` button in several analysis dialogs).

#### Range of the axes

In some analyses, in the `Display options...` dialog, the minimum and maximum of the x and/or y axes can be set. This is useful if the results of several analyses should be presented together, but the independent analyses would produce different axis ranges, which would make the comparison of the charts more difficult.

#### Displaying factors and groups in the x-axis, colors, and panels

(New in v2.4)

In some analyses, in the `Display options...` dialog, the (between-subject) groups and (within-subject or repeated measures) factors can be set flexibly, whether displayed on separate panels, on the x-axis, or with different colors.

* By default, all factors and groups are displayed on the x-axis.
* Move the appropriate factors and groups to the x-axis, color, or panel list.
    * Only groups (but not factors) can be used in panels.
* You can use several factors/groups in the display categories.
    * The order of the factors/groups within a display category matters: lower factors/groups change the "fastest".
* Related tables (e.g., descriptives or parameter estimations) follow the order of the factors/groups, with a panel – x-axis – color order.

### Chart theme

The look of the charts can be changed: color themes, font sizes, etc. You can choose from preset themes.

The image format of the charts can be set in the [`CogStat > Preferences...`](Preferences#chart-theme) menu. Analyses after setting the new theme will be displayed with the new theme (i.e., the charts already visible on the Results pane will not be modified).

See some examples of how those themes may look [here](https://matplotlib.org/gallery/style_sheets/style_sheets_reference.html). Note that some features of the themes may be overwritten by CogStat to have a reasonable output. In other words, some details of the chart will not look like in the theme list above. These features include how dashed and dotted lines look, a few colors (to make sure that [the axes look fine](Displaying-ordinal-and-nominal-data)) some of the font sizes (to make sure that some fonts are not too large).

### Customizing further details

If you're not satisfied with the given themes or want to modify further elements of the charts, then you may use the svg image format (see below), and then your chart can be edited in image manipulation software packages, such as [LibreOffice Draw](https://www.libreoffice.org/) or [Inkscape](https://inkscape.org/).

For example, in [LibreOffice](https://www.libreoffice.org/), 
* after you copied the chart from CogStat to Writer to your report, 
* copy the chart again from Writer, open a Draw window (`File > New > Drawing`), and paste your chart, 
* right-click on the chart, choose `Break`,
* modify the required components and properties of the chart,
* and when you're satisfied with the result, select the whole chart (e.g., if you don't have anything else in the Draw document, then `Edit > Select all`), copy from Draw, and paste to Writer.

## Image format

(New in v2.4)

The image format of the charts can be set in the [`CogStat > Preferences...`](Preferences#image-format) menu.

The charts can be displayed in [png](https://en.wikipedia.org/wiki/PNG) and [svg](https://en.wikipedia.org/wiki/SVG) format. The svg format is always sharp, no matter what zooming one uses, while the png format may require less memory when there are many details in the images (mostly for large sample sizes when the individual data are displayed). The svg format later can be reformatted (e.g., changing the colors) in other image manipulation software - see below.

Currently, the svg format may not work with all word processors when you want to copy and paste the results. For example, the svg format is not supported (as of 2023 September) in Google Docs, and it is only partly supported in OnlyOffice (where various parts of the image are not displayed).
