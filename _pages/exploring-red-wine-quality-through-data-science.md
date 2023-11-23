---
permalink: /projects/exploring-red-wine-quality-through-data-science
title: "Exploring Red Wine Quality Through Data Science"
author_profile: true
---

**Supervisor:** Prof. Garg  
**Type:** Academic Project (Data Science, Machine Learning)

## Overview
This project, led by Prof. Garg, aimed to explore the quality of red wine using data science techniques. The objective was to analyze the physicochemical properties of red wine and to determine the best indicators of quality using Regression and Classification Models.

## Methodology
The methodology included:
1. **Exploratory Data Analysis (EDA):** Conducting an initial analysis to understand the dataset and identify potential relationships.
2. **Data Preparation:** Addressing missing values, handling outliers, and implementing feature scaling.
3. **Regression Model Implementation:** Employing Random Forest and Gradient Boosting models to predict wine quality.
4. **Classification Model Development:** Utilizing a Neural Network using TensorFlow and Keras for quality classification.

## Evaluation
The evaluation of the models involved:
- **Regression Model Assessment:** Using metrics like R-squared, RMSE, and MAE for performance evaluation.
- **Classification Model Analysis:** Tracking training and validation loss and accuracy, along with Precision, Recall, and Accuracy metrics.

## Key Findings
- Identified key physicochemical properties that significantly influence wine quality.
- Random Forest and Gradient Boosting models provided insights into the wine quality, with Random Forest showing slightly better performance.
- The Neural Network model demonstrated a promising ability to classify wine quality, though constrained by the dataset size.

## Personal Contributions
- **Complete Project Leadership:** Oversaw all aspects of the project from data collection to model development and evaluation.
- **Data Analysis and Preprocessing:** Conducted thorough EDA, data cleaning, and preparation for modeling.
- **Model Development and Optimization:** Developed both regression and classification models, focusing on fine-tuning and optimization.
- **Performance Evaluation:** Assessed the models using various metrics and interpreted the results to draw meaningful conclusions.

## Conclusion
This project showcased the effectiveness of data science techniques in analyzing and predicting red wine quality. The use of advanced modeling approaches provided valuable insights into the factors influencing wine quality and demonstrated the potential of machine learning in the food and beverage industry.

## Project Jupyter Notebook
Project's jupyter notebook can be viewed via this <a href="https://github.com/razaviah/Exploring-Red-Wine-Quality-Through-Data-Science/blob/main/Exploring-Red-Wine-Quality-Through-Data-Science.ipynb" target="_blank">link</a>

Or, you can view the text representation of it as follows:

<details>
  <summary>Click to expand!</summary>

<!DOCTYPE html>

<html lang="en">
<head><meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>Exploring-Red-Wine-Quality-Through-Data-Science</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
<style type="text/css">
    pre { line-height: 125%; }
td.linenos .normal { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
span.linenos { color: inherit; background-color: transparent; padding-left: 5px; padding-right: 5px; }
td.linenos .special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
span.linenos.special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
.highlight .hll { background-color: var(--jp-cell-editor-active-background) }
.highlight { background: var(--jp-cell-editor-background); color: var(--jp-mirror-editor-variable-color) }
.highlight .c { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment */
.highlight .err { color: var(--jp-mirror-editor-error-color) } /* Error */
.highlight .k { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword */
.highlight .o { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator */
.highlight .p { color: var(--jp-mirror-editor-punctuation-color) } /* Punctuation */
.highlight .ch { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Hashbang */
.highlight .cm { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Multiline */
.highlight .cp { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Preproc */
.highlight .cpf { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.PreprocFile */
.highlight .c1 { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Single */
.highlight .cs { color: var(--jp-mirror-editor-comment-color); font-style: italic } /* Comment.Special */
.highlight .kc { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Constant */
.highlight .kd { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Declaration */
.highlight .kn { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Namespace */
.highlight .kp { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Pseudo */
.highlight .kr { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Reserved */
.highlight .kt { color: var(--jp-mirror-editor-keyword-color); font-weight: bold } /* Keyword.Type */
.highlight .m { color: var(--jp-mirror-editor-number-color) } /* Literal.Number */
.highlight .s { color: var(--jp-mirror-editor-string-color) } /* Literal.String */
.highlight .ow { color: var(--jp-mirror-editor-operator-color); font-weight: bold } /* Operator.Word */
.highlight .pm { color: var(--jp-mirror-editor-punctuation-color) } /* Punctuation.Marker */
.highlight .w { color: var(--jp-mirror-editor-variable-color) } /* Text.Whitespace */
.highlight .mb { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Bin */
.highlight .mf { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Float */
.highlight .mh { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Hex */
.highlight .mi { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer */
.highlight .mo { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Oct */
.highlight .sa { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Affix */
.highlight .sb { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Backtick */
.highlight .sc { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Char */
.highlight .dl { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Delimiter */
.highlight .sd { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Doc */
.highlight .s2 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Double */
.highlight .se { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Escape */
.highlight .sh { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Heredoc */
.highlight .si { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Interpol */
.highlight .sx { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Other */
.highlight .sr { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Regex */
.highlight .s1 { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Single */
.highlight .ss { color: var(--jp-mirror-editor-string-color) } /* Literal.String.Symbol */
.highlight .il { color: var(--jp-mirror-editor-number-color) } /* Literal.Number.Integer.Long */
  </style>
<style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
 * Mozilla scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */
[data-jp-theme-scrollbars='true'] {
  scrollbar-color: rgb(var(--jp-scrollbar-thumb-color))
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar. These selectors
 * will match lower in the tree, and so will override the above */
[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
}

/* tiny scrollbar */

.jp-scrollbar-tiny {
  scrollbar-color: rgba(var(--jp-scrollbar-thumb-color), 0.5) transparent;
  scrollbar-width: thin;
}

/* tiny scrollbar */

.jp-scrollbar-tiny::-webkit-scrollbar,
.jp-scrollbar-tiny::-webkit-scrollbar-corner {
  background-color: transparent;
  height: 4px;
  width: 4px;
}

.jp-scrollbar-tiny::-webkit-scrollbar-thumb {
  background: rgba(var(--jp-scrollbar-thumb-color), 0.5);
}

.jp-scrollbar-tiny::-webkit-scrollbar-track:horizontal {
  border-left: 0 solid transparent;
  border-right: 0 solid transparent;
}

.jp-scrollbar-tiny::-webkit-scrollbar-track:vertical {
  border-top: 0 solid transparent;
  border-bottom: 0 solid transparent;
}

/*
 * Lumino
 */

.lm-ScrollBar[data-orientation='horizontal'] {
  min-height: 16px;
  max-height: 16px;
  min-width: 45px;
  border-top: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] {
  min-width: 16px;
  max-width: 16px;
  min-height: 45px;
  border-left: 1px solid #a0a0a0;
}

.lm-ScrollBar-button {
  background-color: #f0f0f0;
  background-position: center center;
  min-height: 15px;
  max-height: 15px;
  min-width: 15px;
  max-width: 15px;
}

.lm-ScrollBar-button:hover {
  background-color: #dadada;
}

.lm-ScrollBar-button.lm-mod-active {
  background-color: #cdcdcd;
}

.lm-ScrollBar-track {
  background: #f0f0f0;
}

.lm-ScrollBar-thumb {
  background: #cdcdcd;
}

.lm-ScrollBar-thumb:hover {
  background: #bababa;
}

.lm-ScrollBar-thumb.lm-mod-active {
  background: #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal'] .lm-ScrollBar-thumb {
  height: 100%;
  min-width: 15px;
  border-left: 1px solid #a0a0a0;
  border-right: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='vertical'] .lm-ScrollBar-thumb {
  width: 100%;
  min-height: 15px;
  border-top: 1px solid #a0a0a0;
  border-bottom: 1px solid #a0a0a0;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-left);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='horizontal']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-right);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='decrement'] {
  background-image: var(--jp-icon-caret-up);
  background-size: 17px;
}

.lm-ScrollBar[data-orientation='vertical']
  .lm-ScrollBar-button[data-action='increment'] {
  background-image: var(--jp-icon-caret-down);
  background-size: 17px;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-Widget {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
}

.lm-Widget.lm-mod-hidden {
  display: none !important;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

.lm-AccordionPanel[data-orientation='horizontal'] > .lm-AccordionPanel-title {
  /* Title is rotated for horizontal accordion panel using CSS */
  display: block;
  transform-origin: top left;
  transform: rotate(-90deg) translate(-100%);
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-CommandPalette {
  display: flex;
  flex-direction: column;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.lm-CommandPalette-search {
  flex: 0 0 auto;
}

.lm-CommandPalette-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  min-height: 0;
  overflow: auto;
  list-style-type: none;
}

.lm-CommandPalette-header {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.lm-CommandPalette-item {
  display: flex;
  flex-direction: row;
}

.lm-CommandPalette-itemIcon {
  flex: 0 0 auto;
}

.lm-CommandPalette-itemContent {
  flex: 1 1 auto;
  overflow: hidden;
}

.lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}

.lm-CommandPalette-itemLabel {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.lm-close-icon {
  border: 1px solid transparent;
  background-color: transparent;
  position: absolute;
  z-index: 1;
  right: 3%;
  top: 0;
  bottom: 0;
  margin: auto;
  padding: 7px 0;
  display: none;
  vertical-align: middle;
  outline: 0;
  cursor: pointer;
}
.lm-close-icon:after {
  content: 'X';
  display: block;
  width: 15px;
  height: 15px;
  text-align: center;
  color: #000;
  font-weight: normal;
  font-size: 12px;
  cursor: pointer;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-DockPanel {
  z-index: 0;
}

.lm-DockPanel-widget {
  z-index: 0;
}

.lm-DockPanel-tabBar {
  z-index: 1;
}

.lm-DockPanel-handle {
  z-index: 2;
}

.lm-DockPanel-handle.lm-mod-hidden {
  display: none !important;
}

.lm-DockPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}

.lm-DockPanel-handle[data-orientation='horizontal'] {
  cursor: ew-resize;
}

.lm-DockPanel-handle[data-orientation='vertical'] {
  cursor: ns-resize;
}

.lm-DockPanel-handle[data-orientation='horizontal']:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}

.lm-DockPanel-handle[data-orientation='vertical']:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}

.lm-DockPanel-overlay {
  z-index: 3;
  box-sizing: border-box;
  pointer-events: none;
}

.lm-DockPanel-overlay.lm-mod-hidden {
  display: none !important;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-Menu {
  z-index: 10000;
  position: absolute;
  white-space: nowrap;
  overflow-x: hidden;
  overflow-y: auto;
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.lm-Menu-content {
  margin: 0;
  padding: 0;
  display: table;
  list-style-type: none;
}

.lm-Menu-item {
  display: table-row;
}

.lm-Menu-item.lm-mod-hidden,
.lm-Menu-item.lm-mod-collapsed {
  display: none !important;
}

.lm-Menu-itemIcon,
.lm-Menu-itemSubmenuIcon {
  display: table-cell;
  text-align: center;
}

.lm-Menu-itemLabel {
  display: table-cell;
  text-align: left;
}

.lm-Menu-itemShortcut {
  display: table-cell;
  text-align: right;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-MenuBar {
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.lm-MenuBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: row;
  list-style-type: none;
}

.lm-MenuBar-item {
  box-sizing: border-box;
}

.lm-MenuBar-itemIcon,
.lm-MenuBar-itemLabel {
  display: inline-block;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-ScrollBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.lm-ScrollBar[data-orientation='horizontal'] {
  flex-direction: row;
}

.lm-ScrollBar[data-orientation='vertical'] {
  flex-direction: column;
}

.lm-ScrollBar-button {
  box-sizing: border-box;
  flex: 0 0 auto;
}

.lm-ScrollBar-track {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  flex: 1 1 auto;
}

.lm-ScrollBar-thumb {
  box-sizing: border-box;
  position: absolute;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-SplitPanel-child {
  z-index: 0;
}

.lm-SplitPanel-handle {
  z-index: 1;
}

.lm-SplitPanel-handle.lm-mod-hidden {
  display: none !important;
}

.lm-SplitPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}

.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle {
  cursor: ew-resize;
}

.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle {
  cursor: ns-resize;
}

.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}

.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-TabBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.lm-TabBar[data-orientation='horizontal'] {
  flex-direction: row;
  align-items: flex-end;
}

.lm-TabBar[data-orientation='vertical'] {
  flex-direction: column;
  align-items: flex-end;
}

.lm-TabBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex: 1 1 auto;
  list-style-type: none;
}

.lm-TabBar[data-orientation='horizontal'] > .lm-TabBar-content {
  flex-direction: row;
}

.lm-TabBar[data-orientation='vertical'] > .lm-TabBar-content {
  flex-direction: column;
}

.lm-TabBar-tab {
  display: flex;
  flex-direction: row;
  box-sizing: border-box;
  overflow: hidden;
  touch-action: none; /* Disable native Drag/Drop */
}

.lm-TabBar-tabIcon,
.lm-TabBar-tabCloseIcon {
  flex: 0 0 auto;
}

.lm-TabBar-tabLabel {
  flex: 1 1 auto;
  overflow: hidden;
  white-space: nowrap;
}

.lm-TabBar-tabInput {
  user-select: all;
  width: 100%;
  box-sizing: border-box;
}

.lm-TabBar-tab.lm-mod-hidden {
  display: none !important;
}

.lm-TabBar-addButton.lm-mod-hidden {
  display: none !important;
}

.lm-TabBar.lm-mod-dragging .lm-TabBar-tab {
  position: relative;
}

.lm-TabBar.lm-mod-dragging[data-orientation='horizontal'] .lm-TabBar-tab {
  left: 0;
  transition: left 150ms ease;
}

.lm-TabBar.lm-mod-dragging[data-orientation='vertical'] .lm-TabBar-tab {
  top: 0;
  transition: top 150ms ease;
}

.lm-TabBar.lm-mod-dragging .lm-TabBar-tab.lm-mod-dragging {
  transition: none;
}

.lm-TabBar-tabLabel .lm-TabBar-tabInput {
  user-select: all;
  width: 100%;
  box-sizing: border-box;
  background: inherit;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-TabPanel-tabBar {
  z-index: 1;
}

.lm-TabPanel-stackedPanel {
  z-index: 0;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapse {
  display: flex;
  flex-direction: column;
  align-items: stretch;
}

.jp-Collapse-header {
  padding: 1px 12px;
  background-color: var(--jp-layout-color1);
  border-bottom: solid var(--jp-border-width) var(--jp-border-color2);
  color: var(--jp-ui-font-color1);
  cursor: pointer;
  display: flex;
  align-items: center;
  font-size: var(--jp-ui-font-size0);
  font-weight: 600;
  text-transform: uppercase;
  user-select: none;
}

.jp-Collapser-icon {
  height: 16px;
}

.jp-Collapse-header-collapsed .jp-Collapser-icon {
  transform: rotate(-90deg);
  margin: auto 0;
}

.jp-Collapser-title {
  line-height: 25px;
}

.jp-Collapse-contents {
  padding: 0 12px;
  background-color: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  overflow: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensureUiComponents() in @jupyterlab/buildutils */

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

/* Icons urls */

:root {
  --jp-icon-add-above: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTQiIGhlaWdodD0iMTQiIHZpZXdCb3g9IjAgMCAxNCAxNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPGcgY2xpcC1wYXRoPSJ1cmwoI2NsaXAwXzEzN18xOTQ5MikiPgo8cGF0aCBjbGFzcz0ianAtaWNvbjMiIGQ9Ik00Ljc1IDQuOTMwNjZINi42MjVWNi44MDU2NkM2LjYyNSA3LjAxMTkxIDYuNzkzNzUgNy4xODA2NiA3IDcuMTgwNjZDNy4yMDYyNSA3LjE4MDY2IDcuMzc1IDcuMDExOTEgNy4zNzUgNi44MDU2NlY0LjkzMDY2SDkuMjVDOS40NTYyNSA0LjkzMDY2IDkuNjI1IDQuNzYxOTEgOS42MjUgNC41NTU2NkM5LjYyNSA0LjM0OTQxIDkuNDU2MjUgNC4xODA2NiA5LjI1IDQuMTgwNjZINy4zNzVWMi4zMDU2NkM3LjM3NSAyLjA5OTQxIDcuMjA2MjUgMS45MzA2NiA3IDEuOTMwNjZDNi43OTM3NSAxLjkzMDY2IDYuNjI1IDIuMDk5NDEgNi42MjUgMi4zMDU2NlY0LjE4MDY2SDQuNzVDNC41NDM3NSA0LjE4MDY2IDQuMzc1IDQuMzQ5NDEgNC4zNzUgNC41NTU2NkM0LjM3NSA0Ljc2MTkxIDQuNTQzNzUgNC45MzA2NiA0Ljc1IDQuOTMwNjZaIiBmaWxsPSIjNjE2MTYxIiBzdHJva2U9IiM2MTYxNjEiIHN0cm9rZS13aWR0aD0iMC43Ii8+CjwvZz4KPHBhdGggY2xhc3M9ImpwLWljb24zIiBmaWxsLXJ1bGU9ImV2ZW5vZGQiIGNsaXAtcnVsZT0iZXZlbm9kZCIgZD0iTTExLjUgOS41VjExLjVMMi41IDExLjVWOS41TDExLjUgOS41Wk0xMiA4QzEyLjU1MjMgOCAxMyA4LjQ0NzcyIDEzIDlWMTJDMTMgMTIuNTUyMyAxMi41NTIzIDEzIDEyIDEzTDIgMTNDMS40NDc3MiAxMyAxIDEyLjU1MjMgMSAxMlY5QzEgOC40NDc3MiAxLjQ0NzcxIDggMiA4TDEyIDhaIiBmaWxsPSIjNjE2MTYxIi8+CjxkZWZzPgo8Y2xpcFBhdGggaWQ9ImNsaXAwXzEzN18xOTQ5MiI+CjxyZWN0IGNsYXNzPSJqcC1pY29uMyIgd2lkdGg9IjYiIGhlaWdodD0iNiIgZmlsbD0id2hpdGUiIHRyYW5zZm9ybT0ibWF0cml4KC0xIDAgMCAxIDEwIDEuNTU1NjYpIi8+CjwvY2xpcFBhdGg+CjwvZGVmcz4KPC9zdmc+Cg==);
  --jp-icon-add-below: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTQiIGhlaWdodD0iMTQiIHZpZXdCb3g9IjAgMCAxNCAxNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPGcgY2xpcC1wYXRoPSJ1cmwoI2NsaXAwXzEzN18xOTQ5OCkiPgo8cGF0aCBjbGFzcz0ianAtaWNvbjMiIGQ9Ik05LjI1IDEwLjA2OTNMNy4zNzUgMTAuMDY5M0w3LjM3NSA4LjE5NDM0QzcuMzc1IDcuOTg4MDkgNy4yMDYyNSA3LjgxOTM0IDcgNy44MTkzNEM2Ljc5Mzc1IDcuODE5MzQgNi42MjUgNy45ODgwOSA2LjYyNSA4LjE5NDM0TDYuNjI1IDEwLjA2OTNMNC43NSAxMC4wNjkzQzQuNTQzNzUgMTAuMDY5MyA0LjM3NSAxMC4yMzgxIDQuMzc1IDEwLjQ0NDNDNC4zNzUgMTAuNjUwNiA0LjU0Mzc1IDEwLjgxOTMgNC43NSAxMC44MTkzTDYuNjI1IDEwLjgxOTNMNi42MjUgMTIuNjk0M0M2LjYyNSAxMi45MDA2IDYuNzkzNzUgMTMuMDY5MyA3IDEzLjA2OTNDNy4yMDYyNSAxMy4wNjkzIDcuMzc1IDEyLjkwMDYgNy4zNzUgMTIuNjk0M0w3LjM3NSAxMC44MTkzTDkuMjUgMTAuODE5M0M5LjQ1NjI1IDEwLjgxOTMgOS42MjUgMTAuNjUwNiA5LjYyNSAxMC40NDQzQzkuNjI1IDEwLjIzODEgOS40NTYyNSAxMC4wNjkzIDkuMjUgMTAuMDY5M1oiIGZpbGw9IiM2MTYxNjEiIHN0cm9rZT0iIzYxNjE2MSIgc3Ryb2tlLXdpZHRoPSIwLjciLz4KPC9nPgo8cGF0aCBjbGFzcz0ianAtaWNvbjMiIGZpbGwtcnVsZT0iZXZlbm9kZCIgY2xpcC1ydWxlPSJldmVub2RkIiBkPSJNMi41IDUuNUwyLjUgMy41TDExLjUgMy41TDExLjUgNS41TDIuNSA1LjVaTTIgN0MxLjQ0NzcyIDcgMSA2LjU1MjI4IDEgNkwxIDNDMSAyLjQ0NzcyIDEuNDQ3NzIgMiAyIDJMMTIgMkMxMi41NTIzIDIgMTMgMi40NDc3MiAxMyAzTDEzIDZDMTMgNi41NTIyOSAxMi41NTIzIDcgMTIgN0wyIDdaIiBmaWxsPSIjNjE2MTYxIi8+CjxkZWZzPgo8Y2xpcFBhdGggaWQ9ImNsaXAwXzEzN18xOTQ5OCI+CjxyZWN0IGNsYXNzPSJqcC1pY29uMyIgd2lkdGg9IjYiIGhlaWdodD0iNiIgZmlsbD0id2hpdGUiIHRyYW5zZm9ybT0ibWF0cml4KDEgMS43NDg0NmUtMDcgMS43NDg0NmUtMDcgLTEgNCAxMy40NDQzKSIvPgo8L2NsaXBQYXRoPgo8L2RlZnM+Cjwvc3ZnPgo=);
  --jp-icon-add: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDEzaC02djZoLTJ2LTZINXYtMmg2VjVoMnY2aDZ2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-bell: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE2IDE2IiB2ZXJzaW9uPSIxLjEiPgogICA8cGF0aCBjbGFzcz0ianAtaWNvbjIganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMzMzMzMzIgogICAgICBkPSJtOCAwLjI5Yy0xLjQgMC0yLjcgMC43My0zLjYgMS44LTEuMiAxLjUtMS40IDMuNC0xLjUgNS4yLTAuMTggMi4yLTAuNDQgNC0yLjMgNS4zbDAuMjggMS4zaDVjMC4wMjYgMC42NiAwLjMyIDEuMSAwLjcxIDEuNSAwLjg0IDAuNjEgMiAwLjYxIDIuOCAwIDAuNTItMC40IDAuNi0xIDAuNzEtMS41aDVsMC4yOC0xLjNjLTEuOS0wLjk3LTIuMi0zLjMtMi4zLTUuMy0wLjEzLTEuOC0wLjI2LTMuNy0xLjUtNS4yLTAuODUtMS0yLjItMS44LTMuNi0xLjh6bTAgMS40YzAuODggMCAxLjkgMC41NSAyLjUgMS4zIDAuODggMS4xIDEuMSAyLjcgMS4yIDQuNCAwLjEzIDEuNyAwLjIzIDMuNiAxLjMgNS4yaC0xMGMxLjEtMS42IDEuMi0zLjQgMS4zLTUuMiAwLjEzLTEuNyAwLjMtMy4zIDEuMi00LjQgMC41OS0wLjcyIDEuNi0xLjMgMi41LTEuM3ptLTAuNzQgMTJoMS41Yy0wLjAwMTUgMC4yOCAwLjAxNSAwLjc5LTAuNzQgMC43OS0wLjczIDAuMDAxNi0wLjcyLTAuNTMtMC43NC0wLjc5eiIgLz4KPC9zdmc+Cg==);
  --jp-icon-bug-dot: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiPgogICAgICAgIDxwYXRoIGZpbGwtcnVsZT0iZXZlbm9kZCIgY2xpcC1ydWxlPSJldmVub2RkIiBkPSJNMTcuMTkgOEgyMFYxMEgxNy45MUMxNy45NiAxMC4zMyAxOCAxMC42NiAxOCAxMVYxMkgyMFYxNEgxOC41SDE4VjE0LjAyNzVDMTUuNzUgMTQuMjc2MiAxNCAxNi4xODM3IDE0IDE4LjVDMTQgMTkuMjA4IDE0LjE2MzUgMTkuODc3OSAxNC40NTQ5IDIwLjQ3MzlDMTMuNzA2MyAyMC44MTE3IDEyLjg3NTcgMjEgMTIgMjFDOS43OCAyMSA3Ljg1IDE5Ljc5IDYuODEgMThINFYxNkg2LjA5QzYuMDQgMTUuNjcgNiAxNS4zNCA2IDE1VjE0SDRWMTJINlYxMUM2IDEwLjY2IDYuMDQgMTAuMzMgNi4wOSAxMEg0VjhINi44MUM3LjI2IDcuMjIgNy44OCA2LjU1IDguNjIgNi4wNEw3IDQuNDFMOC40MSAzTDEwLjU5IDUuMTdDMTEuMDQgNS4wNiAxMS41MSA1IDEyIDVDMTIuNDkgNSAxMi45NiA1LjA2IDEzLjQyIDUuMTdMMTUuNTkgM0wxNyA0LjQxTDE1LjM3IDYuMDRDMTYuMTIgNi41NSAxNi43NCA3LjIyIDE3LjE5IDhaTTEwIDE2SDE0VjE0SDEwVjE2Wk0xMCAxMkgxNFYxMEgxMFYxMloiIGZpbGw9IiM2MTYxNjEiLz4KICAgICAgICA8cGF0aCBkPSJNMjIgMTguNUMyMiAyMC40MzMgMjAuNDMzIDIyIDE4LjUgMjJDMTYuNTY3IDIyIDE1IDIwLjQzMyAxNSAxOC41QzE1IDE2LjU2NyAxNi41NjcgMTUgMTguNSAxNUMyMC40MzMgMTUgMjIgMTYuNTY3IDIyIDE4LjVaIiBmaWxsPSIjNjE2MTYxIi8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-bug: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik0yMCA4aC0yLjgxYy0uNDUtLjc4LTEuMDctMS40NS0xLjgyLTEuOTZMMTcgNC40MSAxNS41OSAzbC0yLjE3IDIuMTdDMTIuOTYgNS4wNiAxMi40OSA1IDEyIDVjLS40OSAwLS45Ni4wNi0xLjQxLjE3TDguNDEgMyA3IDQuNDFsMS42MiAxLjYzQzcuODggNi41NSA3LjI2IDcuMjIgNi44MSA4SDR2MmgyLjA5Yy0uMDUuMzMtLjA5LjY2LS4wOSAxdjFINHYyaDJ2MWMwIC4zNC4wNC42Ny4wOSAxSDR2MmgyLjgxYzEuMDQgMS43OSAyLjk3IDMgNS4xOSAzczQuMTUtMS4yMSA1LjE5LTNIMjB2LTJoLTIuMDljLjA1LS4zMy4wOS0uNjYuMDktMXYtMWgydi0yaC0ydi0xYzAtLjM0LS4wNC0uNjctLjA5LTFIMjBWOHptLTYgOGgtNHYtMmg0djJ6bTAtNGgtNHYtMmg0djJ6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-build: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE0LjkgMTcuNDVDMTYuMjUgMTcuNDUgMTcuMzUgMTYuMzUgMTcuMzUgMTVDMTcuMzUgMTMuNjUgMTYuMjUgMTIuNTUgMTQuOSAxMi41NUMxMy41NCAxMi41NSAxMi40NSAxMy42NSAxMi40NSAxNUMxMi40NSAxNi4zNSAxMy41NCAxNy40NSAxNC45IDE3LjQ1Wk0yMC4xIDE1LjY4TDIxLjU4IDE2Ljg0QzIxLjcxIDE2Ljk1IDIxLjc1IDE3LjEzIDIxLjY2IDE3LjI5TDIwLjI2IDE5LjcxQzIwLjE3IDE5Ljg2IDIwIDE5LjkyIDE5LjgzIDE5Ljg2TDE4LjA5IDE5LjE2QzE3LjczIDE5LjQ0IDE3LjMzIDE5LjY3IDE2LjkxIDE5Ljg1TDE2LjY0IDIxLjdDMTYuNjIgMjEuODcgMTYuNDcgMjIgMTYuMyAyMkgxMy41QzEzLjMyIDIyIDEzLjE4IDIxLjg3IDEzLjE1IDIxLjdMMTIuODkgMTkuODVDMTIuNDYgMTkuNjcgMTIuMDcgMTkuNDQgMTEuNzEgMTkuMTZMOS45NjAwMiAxOS44NkM5LjgxMDAyIDE5LjkyIDkuNjIwMDIgMTkuODYgOS41NDAwMiAxOS43MUw4LjE0MDAyIDE3LjI5QzguMDUwMDIgMTcuMTMgOC4wOTAwMiAxNi45NSA4LjIyMDAyIDE2Ljg0TDkuNzAwMDIgMTUuNjhMOS42NTAwMSAxNUw5LjcwMDAyIDE0LjMxTDguMjIwMDIgMTMuMTZDOC4wOTAwMiAxMy4wNSA4LjA1MDAyIDEyLjg2IDguMTQwMDIgMTIuNzFMOS41NDAwMiAxMC4yOUM5LjYyMDAyIDEwLjEzIDkuODEwMDIgMTAuMDcgOS45NjAwMiAxMC4xM0wxMS43MSAxMC44NEMxMi4wNyAxMC41NiAxMi40NiAxMC4zMiAxMi44OSAxMC4xNUwxMy4xNSA4LjI4OTk4QzEzLjE4IDguMTI5OTggMTMuMzIgNy45OTk5OCAxMy41IDcuOTk5OThIMTYuM0MxNi40NyA3Ljk5OTk4IDE2LjYyIDguMTI5OTggMTYuNjQgOC4yODk5OEwxNi45MSAxMC4xNUMxNy4zMyAxMC4zMiAxNy43MyAxMC41NiAxOC4wOSAxMC44NEwxOS44MyAxMC4xM0MyMCAxMC4wNyAyMC4xNyAxMC4xMyAyMC4yNiAxMC4yOUwyMS42NiAxMi43MUMyMS43NSAxMi44NiAyMS43MSAxMy4wNSAyMS41OCAxMy4xNkwyMC4xIDE0LjMxTDIwLjE1IDE1TDIwLjEgMTUuNjhaIi8+CiAgICA8cGF0aCBkPSJNNy4zMjk2NiA3LjQ0NDU0QzguMDgzMSA3LjAwOTU0IDguMzM5MzIgNi4wNTMzMiA3LjkwNDMyIDUuMjk5ODhDNy40NjkzMiA0LjU0NjQzIDYuNTA4MSA0LjI4MTU2IDUuNzU0NjYgNC43MTY1NkM1LjM5MTc2IDQuOTI2MDggNS4xMjY5NSA1LjI3MTE4IDUuMDE4NDkgNS42NzU5NEM0LjkxMDA0IDYuMDgwNzEgNC45NjY4MiA2LjUxMTk4IDUuMTc2MzQgNi44NzQ4OEM1LjYxMTM0IDcuNjI4MzIgNi41NzYyMiA3Ljg3OTU0IDcuMzI5NjYgNy40NDQ1NFpNOS42NTcxOCA0Ljc5NTkzTDEwLjg2NzIgNC45NTE3OUMxMC45NjI4IDQuOTc3NDEgMTEuMDQwMiA1LjA3MTMzIDExLjAzODIgNS4xODc5M0wxMS4wMzg4IDYuOTg4OTNDMTEuMDQ1NSA3LjEwMDU0IDEwLjk2MTYgNy4xOTUxOCAxMC44NTUgNy4yMTA1NEw5LjY2MDAxIDcuMzgwODNMOS4yMzkxNSA4LjEzMTg4TDkuNjY5NjEgOS4yNTc0NUM5LjcwNzI5IDkuMzYyNzEgOS42NjkzNCA5LjQ3Njk5IDkuNTc0MDggOS41MzE5OUw4LjAxNTIzIDEwLjQzMkM3LjkxMTMxIDEwLjQ5MiA3Ljc5MzM3IDEwLjQ2NzcgNy43MjEwNSAxMC4zODI0TDYuOTg3NDggOS40MzE4OEw2LjEwOTMxIDkuNDMwODNMNS4zNDcwNCAxMC4zOTA1QzUuMjg5MDkgMTAuNDcwMiA1LjE3MzgzIDEwLjQ5MDUgNS4wNzE4NyAxMC40MzM5TDMuNTEyNDUgOS41MzI5M0MzLjQxMDQ5IDkuNDc2MzMgMy4zNzY0NyA5LjM1NzQxIDMuNDEwNzUgOS4yNTY3OUwzLjg2MzQ3IDguMTQwOTNMMy42MTc0OSA3Ljc3NDg4TDMuNDIzNDcgNy4zNzg4M0wyLjIzMDc1IDcuMjEyOTdDMi4xMjY0NyA3LjE5MjM1IDIuMDQwNDkgNy4xMDM0MiAyLjA0MjQ1IDYuOTg2ODJMMi4wNDE4NyA1LjE4NTgyQzIuMDQzODMgNS4wNjkyMiAyLjExOTA5IDQuOTc5NTggMi4yMTcwNCA0Ljk2OTIyTDMuNDIwNjUgNC43OTM5M0wzLjg2NzQ5IDQuMDI3ODhMMy40MTEwNSAyLjkxNzMxQzMuMzczMzcgMi44MTIwNCAzLjQxMTMxIDIuNjk3NzYgMy41MTUyMyAyLjYzNzc2TDUuMDc0MDggMS43Mzc3NkM1LjE2OTM0IDEuNjgyNzYgNS4yODcyOSAxLjcwNzA0IDUuMzU5NjEgMS43OTIzMUw2LjExOTE1IDIuNzI3ODhMNi45ODAwMSAyLjczODkzTDcuNzI0OTYgMS43ODkyMkM3Ljc5MTU2IDEuNzA0NTggNy45MTU0OCAxLjY3OTIyIDguMDA4NzkgMS43NDA4Mkw5LjU2ODIxIDIuNjQxODJDOS42NzAxNyAyLjY5ODQyIDkuNzEyODUgMi44MTIzNCA5LjY4NzIzIDIuOTA3OTdMOS4yMTcxOCA0LjAzMzgzTDkuNDYzMTYgNC4zOTk4OEw5LjY1NzE4IDQuNzk1OTNaIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iOS45LDEzLjYgMy42LDcuNCA0LjQsNi42IDkuOSwxMi4yIDE1LjQsNi43IDE2LjEsNy40ICIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNS45TDksOS43bDMuOC0zLjhsMS4yLDEuMmwtNC45LDVsLTQuOS01TDUuMiw1Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNy41TDksMTEuMmwzLjgtMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-left: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik0xMC44LDEyLjhMNy4xLDlsMy44LTMuOGwwLDcuNkgxMC44eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-right: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik03LjIsNS4yTDEwLjksOWwtMy44LDMuOFY1LjJINy4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-up-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iMTUuNCwxMy4zIDkuOSw3LjcgNC40LDEzLjIgMy42LDEyLjUgOS45LDYuMyAxNi4xLDEyLjYgIi8+Cgk8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-up: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik01LjIsMTAuNUw5LDYuOGwzLjgsMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-case-sensitive: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgogIDxnIGNsYXNzPSJqcC1pY29uLWFjY2VudDIiIGZpbGw9IiNGRkYiPgogICAgPHBhdGggZD0iTTcuNiw4aDAuOWwzLjUsOGgtMS4xTDEwLDE0SDZsLTAuOSwySDRMNy42LDh6IE04LDkuMUw2LjQsMTNoMy4yTDgsOS4xeiIvPgogICAgPHBhdGggZD0iTTE2LjYsOS44Yy0wLjIsMC4xLTAuNCwwLjEtMC43LDAuMWMtMC4yLDAtMC40LTAuMS0wLjYtMC4yYy0wLjEtMC4xLTAuMi0wLjQtMC4yLTAuNyBjLTAuMywwLjMtMC42LDAuNS0wLjksMC43Yy0wLjMsMC4xLTAuNywwLjItMS4xLDAuMmMtMC4zLDAtMC41LDAtMC43LTAuMWMtMC4yLTAuMS0wLjQtMC4yLTAuNi0wLjNjLTAuMi0wLjEtMC4zLTAuMy0wLjQtMC41IGMtMC4xLTAuMi0wLjEtMC40LTAuMS0wLjdjMC0wLjMsMC4xLTAuNiwwLjItMC44YzAuMS0wLjIsMC4zLTAuNCwwLjQtMC41QzEyLDcsMTIuMiw2LjksMTIuNSw2LjhjMC4yLTAuMSwwLjUtMC4xLDAuNy0wLjIgYzAuMy0wLjEsMC41LTAuMSwwLjctMC4xYzAuMiwwLDAuNC0wLjEsMC42LTAuMWMwLjIsMCwwLjMtMC4xLDAuNC0wLjJjMC4xLTAuMSwwLjItMC4yLDAuMi0wLjRjMC0xLTEuMS0xLTEuMy0xIGMtMC40LDAtMS40LDAtMS40LDEuMmgtMC45YzAtMC40LDAuMS0wLjcsMC4yLTFjMC4xLTAuMiwwLjMtMC40LDAuNS0wLjZjMC4yLTAuMiwwLjUtMC4zLDAuOC0wLjNDMTMuMyw0LDEzLjYsNCwxMy45LDQgYzAuMywwLDAuNSwwLDAuOCwwLjFjMC4zLDAsMC41LDAuMSwwLjcsMC4yYzAuMiwwLjEsMC40LDAuMywwLjUsMC41QzE2LDUsMTYsNS4yLDE2LDUuNnYyLjljMCwwLjIsMCwwLjQsMCwwLjUgYzAsMC4xLDAuMSwwLjIsMC4zLDAuMmMwLjEsMCwwLjIsMCwwLjMsMFY5Ljh6IE0xNS4yLDYuOWMtMS4yLDAuNi0zLjEsMC4yLTMuMSwxLjRjMCwxLjQsMy4xLDEsMy4xLTAuNVY2Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-check: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik05IDE2LjE3TDQuODMgMTJsLTEuNDIgMS40MUw5IDE5IDIxIDdsLTEuNDEtMS40MXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-circle-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDJDNi40NyAyIDIgNi40NyAyIDEyczQuNDcgMTAgMTAgMTAgMTAtNC40NyAxMC0xMFMxNy41MyAyIDEyIDJ6bTAgMThjLTQuNDEgMC04LTMuNTktOC04czMuNTktOCA4LTggOCAzLjU5IDggOC0zLjU5IDgtOCA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-circle: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iOSIgY3k9IjkiIHI9IjgiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-clear: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8bWFzayBpZD0iZG9udXRIb2xlIj4KICAgIDxyZWN0IHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgZmlsbD0id2hpdGUiIC8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSI4IiBmaWxsPSJibGFjayIvPgogIDwvbWFzaz4KCiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxyZWN0IGhlaWdodD0iMTgiIHdpZHRoPSIyIiB4PSIxMSIgeT0iMyIgdHJhbnNmb3JtPSJyb3RhdGUoMzE1LCAxMiwgMTIpIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIxMCIgbWFzaz0idXJsKCNkb251dEhvbGUpIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-close: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1ub25lIGpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIGpwLWljb24zLWhvdmVyIiBmaWxsPSJub25lIj4KICAgIDxjaXJjbGUgY3g9IjEyIiBjeT0iMTIiIHI9IjExIi8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIGpwLWljb24tYWNjZW50Mi1ob3ZlciIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMTkgNi40MUwxNy41OSA1IDEyIDEwLjU5IDYuNDEgNSA1IDYuNDEgMTAuNTkgMTIgNSAxNy41OSA2LjQxIDE5IDEyIDEzLjQxIDE3LjU5IDE5IDE5IDE3LjU5IDEzLjQxIDEyeiIvPgogIDwvZz4KCiAgPGcgY2xhc3M9ImpwLWljb24tbm9uZSBqcC1pY29uLWJ1c3kiIGZpbGw9Im5vbmUiPgogICAgPGNpcmNsZSBjeD0iMTIiIGN5PSIxMiIgcj0iNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-code-check: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBzaGFwZS1yZW5kZXJpbmc9Imdlb21ldHJpY1ByZWNpc2lvbiI+CiAgICA8cGF0aCBkPSJNNi41OSwzLjQxTDIsOEw2LjU5LDEyLjZMOCwxMS4xOEw0LjgyLDhMOCw0LjgyTDYuNTksMy40MU0xMi40MSwzLjQxTDExLDQuODJMMTQuMTgsOEwxMSwxMS4xOEwxMi40MSwxMi42TDE3LDhMMTIuNDEsMy40MU0yMS41OSwxMS41OUwxMy41LDE5LjY4TDkuODMsMTZMOC40MiwxNy40MUwxMy41LDIyLjVMMjMsMTNMMjEuNTksMTEuNTlaIiAvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-code: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjIiIGhlaWdodD0iMjIiIHZpZXdCb3g9IjAgMCAyOCAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTExLjQgMTguNkw2LjggMTRMMTEuNCA5LjRMMTAgOEw0IDE0TDEwIDIwTDExLjQgMTguNlpNMTYuNiAxOC42TDIxLjIgMTRMMTYuNiA5LjRMMTggOEwyNCAxNEwxOCAyMEwxNi42IDE4LjZWMTguNloiLz4KCTwvZz4KPC9zdmc+Cg==);
  --jp-icon-collapse-all: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGgKICAgICAgICAgICAgZD0iTTggMmMxIDAgMTEgMCAxMiAwczIgMSAyIDJjMCAxIDAgMTEgMCAxMnMwIDItMiAyQzIwIDE0IDIwIDQgMjAgNFMxMCA0IDYgNGMwLTIgMS0yIDItMnoiIC8+CiAgICAgICAgPHBhdGgKICAgICAgICAgICAgZD0iTTE4IDhjMC0xLTEtMi0yLTJTNSA2IDQgNnMtMiAxLTIgMmMwIDEgMCAxMSAwIDEyczEgMiAyIDJjMSAwIDExIDAgMTIgMHMyLTEgMi0yYzAtMSAwLTExIDAtMTJ6bS0yIDB2MTJINFY4eiIgLz4KICAgICAgICA8cGF0aCBkPSJNNiAxM3YyaDh2LTJ6IiAvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-console: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwMCAyMDAiPgogIDxnIGNsYXNzPSJqcC1jb25zb2xlLWljb24tYmFja2dyb3VuZC1jb2xvciBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMjg4RDEiPgogICAgPHBhdGggZD0iTTIwIDE5LjhoMTYwdjE1OS45SDIweiIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtY29uc29sZS1pY29uLWNvbG9yIGpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIiBmaWxsPSIjZmZmIj4KICAgIDxwYXRoIGQ9Ik0xMDUgMTI3LjNoNDB2MTIuOGgtNDB6TTUxLjEgNzdMNzQgOTkuOWwtMjMuMyAyMy4zIDEwLjUgMTAuNSAyMy4zLTIzLjNMOTUgOTkuOSA4NC41IDg5LjQgNjEuNiA2Ni41eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-copy: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTExLjksMUgzLjJDMi40LDEsMS43LDEuNywxLjcsMi41djEwLjJoMS41VjIuNWg4LjdWMXogTTE0LjEsMy45aC04Yy0wLjgsMC0xLjUsMC43LTEuNSwxLjV2MTAuMmMwLDAuOCwwLjcsMS41LDEuNSwxLjVoOCBjMC44LDAsMS41LTAuNywxLjUtMS41VjUuNEMxNS41LDQuNiwxNC45LDMuOSwxNC4xLDMuOXogTTE0LjEsMTUuNWgtOFY1LjRoOFYxNS41eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-copyright: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGVuYWJsZS1iYWNrZ3JvdW5kPSJuZXcgMCAwIDI0IDI0IiBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCI+CiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik0xMS44OCw5LjE0YzEuMjgsMC4wNiwxLjYxLDEuMTUsMS42MywxLjY2aDEuNzljLTAuMDgtMS45OC0xLjQ5LTMuMTktMy40NS0zLjE5QzkuNjQsNy42MSw4LDksOCwxMi4xNCBjMCwxLjk0LDAuOTMsNC4yNCwzLjg0LDQuMjRjMi4yMiwwLDMuNDEtMS42NSwzLjQ0LTIuOTVoLTEuNzljLTAuMDMsMC41OS0wLjQ1LDEuMzgtMS42MywxLjQ0QzEwLjU1LDE0LjgzLDEwLDEzLjgxLDEwLDEyLjE0IEMxMCw5LjI1LDExLjI4LDkuMTYsMTEuODgsOS4xNHogTTEyLDJDNi40OCwyLDIsNi40OCwyLDEyczQuNDgsMTAsMTAsMTBzMTAtNC40OCwxMC0xMFMxNy41MiwyLDEyLDJ6IE0xMiwyMGMtNC40MSwwLTgtMy41OS04LTggczMuNTktOCw4LThzOCwzLjU5LDgsOFMxNi40MSwyMCwxMiwyMHoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-cut: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkuNjQgNy42NGMuMjMtLjUuMzYtMS4wNS4zNi0xLjY0IDAtMi4yMS0xLjc5LTQtNC00UzIgMy43OSAyIDZzMS43OSA0IDQgNGMuNTkgMCAxLjE0LS4xMyAxLjY0LS4zNkwxMCAxMmwtMi4zNiAyLjM2QzcuMTQgMTQuMTMgNi41OSAxNCA2IDE0Yy0yLjIxIDAtNCAxLjc5LTQgNHMxLjc5IDQgNCA0IDQtMS43OSA0LTRjMC0uNTktLjEzLTEuMTQtLjM2LTEuNjRMMTIgMTRsNyA3aDN2LTFMOS42NCA3LjY0ek02IDhjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTAgMTJjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTYtNy41Yy0uMjggMC0uNS0uMjItLjUtLjVzLjIyLS41LjUtLjUuNS4yMi41LjUtLjIyLjUtLjUuNXpNMTkgM2wtNiA2IDIgMiA3LTdWM3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-delete: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2cHgiIGhlaWdodD0iMTZweCI+CiAgICA8cGF0aCBkPSJNMCAwaDI0djI0SDB6IiBmaWxsPSJub25lIiAvPgogICAgPHBhdGggY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjI2MjYyIiBkPSJNNiAxOWMwIDEuMS45IDIgMiAyaDhjMS4xIDAgMi0uOSAyLTJWN0g2djEyek0xOSA0aC0zLjVsLTEtMWgtNWwtMSAxSDV2MmgxNFY0eiIgLz4KPC9zdmc+Cg==);
  --jp-icon-download: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDloLTRWM0g5djZINWw3IDcgNy03ek01IDE4djJoMTR2LTJINXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-duplicate: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTQiIGhlaWdodD0iMTQiIHZpZXdCb3g9IjAgMCAxNCAxNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggY2xhc3M9ImpwLWljb24zIiBmaWxsLXJ1bGU9ImV2ZW5vZGQiIGNsaXAtcnVsZT0iZXZlbm9kZCIgZD0iTTIuNzk5OTggMC44NzVIOC44OTU4MkM5LjIwMDYxIDAuODc1IDkuNDQ5OTggMS4xMzkxNCA5LjQ0OTk4IDEuNDYxOThDOS40NDk5OCAxLjc4NDgyIDkuMjAwNjEgMi4wNDg5NiA4Ljg5NTgyIDIuMDQ4OTZIMy4zNTQxNUMzLjA0OTM2IDIuMDQ4OTYgMi43OTk5OCAyLjMxMzEgMi43OTk5OCAyLjYzNTk0VjkuNjc5NjlDMi43OTk5OCAxMC4wMDI1IDIuNTUwNjEgMTAuMjY2NyAyLjI0NTgyIDEwLjI2NjdDMS45NDEwMyAxMC4yNjY3IDEuNjkxNjUgMTAuMDAyNSAxLjY5MTY1IDkuNjc5NjlWMi4wNDg5NkMxLjY5MTY1IDEuNDAzMjggMi4xOTA0IDAuODc1IDIuNzk5OTggMC44NzVaTTUuMzY2NjUgMTEuOVY0LjU1SDExLjA4MzNWMTEuOUg1LjM2NjY1Wk00LjE0MTY1IDQuMTQxNjdDNC4xNDE2NSAzLjY5MDYzIDQuNTA3MjggMy4zMjUgNC45NTgzMiAzLjMyNUgxMS40OTE3QzExLjk0MjcgMy4zMjUgMTIuMzA4MyAzLjY5MDYzIDEyLjMwODMgNC4xNDE2N1YxMi4zMDgzQzEyLjMwODMgMTIuNzU5NCAxMS45NDI3IDEzLjEyNSAxMS40OTE3IDEzLjEyNUg0Ljk1ODMyQzQuNTA3MjggMTMuMTI1IDQuMTQxNjUgMTIuNzU5NCA0LjE0MTY1IDEyLjMwODNWNC4xNDE2N1oiIGZpbGw9IiM2MTYxNjEiLz4KPHBhdGggY2xhc3M9ImpwLWljb24zIiBkPSJNOS40MzU3NCA4LjI2NTA3SDguMzY0MzFWOS4zMzY1QzguMzY0MzEgOS40NTQzNSA4LjI2Nzg4IDkuNTUwNzggOC4xNTAwMiA5LjU1MDc4QzguMDMyMTcgOS41NTA3OCA3LjkzNTc0IDkuNDU0MzUgNy45MzU3NCA5LjMzNjVWOC4yNjUwN0g2Ljg2NDMxQzYuNzQ2NDUgOC4yNjUwNyA2LjY1MDAyIDguMTY4NjQgNi42NTAwMiA4LjA1MDc4QzYuNjUwMDIgNy45MzI5MiA2Ljc0NjQ1IDcuODM2NSA2Ljg2NDMxIDcuODM2NUg3LjkzNTc0VjYuNzY1MDdDNy45MzU3NCA2LjY0NzIxIDguMDMyMTcgNi41NTA3OCA4LjE1MDAyIDYuNTUwNzhDOC4yNjc4OCA2LjU1MDc4IDguMzY0MzEgNi42NDcyMSA4LjM2NDMxIDYuNzY1MDdWNy44MzY1SDkuNDM1NzRDOS41NTM2IDcuODM2NSA5LjY1MDAyIDcuOTMyOTIgOS42NTAwMiA4LjA1MDc4QzkuNjUwMDIgOC4xNjg2NCA5LjU1MzYgOC4yNjUwNyA5LjQzNTc0IDguMjY1MDdaIiBmaWxsPSIjNjE2MTYxIiBzdHJva2U9IiM2MTYxNjEiIHN0cm9rZS13aWR0aD0iMC41Ii8+Cjwvc3ZnPgo=);
  --jp-icon-edit: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMgMTcuMjVWMjFoMy43NUwxNy44MSA5Ljk0bC0zLjc1LTMuNzVMMyAxNy4yNXpNMjAuNzEgNy4wNGMuMzktLjM5LjM5LTEuMDIgMC0xLjQxbC0yLjM0LTIuMzRjLS4zOS0uMzktMS4wMi0uMzktMS40MSAwbC0xLjgzIDEuODMgMy43NSAzLjc1IDEuODMtMS44M3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-ellipses: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iNSIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxOSIgY3k9IjEyIiByPSIyIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-error: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj48Y2lyY2xlIGN4PSIxMiIgY3k9IjE5IiByPSIyIi8+PHBhdGggZD0iTTEwIDNoNHYxMmgtNHoiLz48L2c+CjxwYXRoIGZpbGw9Im5vbmUiIGQ9Ik0wIDBoMjR2MjRIMHoiLz4KPC9zdmc+Cg==);
  --jp-icon-expand-all: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGgKICAgICAgICAgICAgZD0iTTggMmMxIDAgMTEgMCAxMiAwczIgMSAyIDJjMCAxIDAgMTEgMCAxMnMwIDItMiAyQzIwIDE0IDIwIDQgMjAgNFMxMCA0IDYgNGMwLTIgMS0yIDItMnoiIC8+CiAgICAgICAgPHBhdGgKICAgICAgICAgICAgZD0iTTE4IDhjMC0xLTEtMi0yLTJTNSA2IDQgNnMtMiAxLTIgMmMwIDEgMCAxMSAwIDEyczEgMiAyIDJjMSAwIDExIDAgMTIgMHMyLTEgMi0yYzAtMSAwLTExIDAtMTJ6bS0yIDB2MTJINFY4eiIgLz4KICAgICAgICA8cGF0aCBkPSJNMTEgMTBIOXYzSDZ2MmgzdjNoMnYtM2gzdi0yaC0zeiIgLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-extension: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwLjUgMTFIMTlWN2MwLTEuMS0uOS0yLTItMmgtNFYzLjVDMTMgMi4xMiAxMS44OCAxIDEwLjUgMVM4IDIuMTIgOCAzLjVWNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAydjMuOEgzLjVjMS40OSAwIDIuNyAxLjIxIDIuNyAyLjdzLTEuMjEgMi43LTIuNyAyLjdIMlYyMGMwIDEuMS45IDIgMiAyaDMuOHYtMS41YzAtMS40OSAxLjIxLTIuNyAyLjctMi43IDEuNDkgMCAyLjcgMS4yMSAyLjcgMi43VjIySDE3YzEuMSAwIDItLjkgMi0ydi00aDEuNWMxLjM4IDAgMi41LTEuMTIgMi41LTIuNVMyMS44OCAxMSAyMC41IDExeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-fast-forward: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTQgMThsOC41LTZMNCA2djEyem05LTEydjEybDguNS02TDEzIDZ6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-file-upload: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkgMTZoNnYtNmg0bC03LTctNyA3aDR6bS00IDJoMTR2Mkg1eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-file: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuMyA4LjJsLTUuNS01LjVjLS4zLS4zLS43LS41LTEuMi0uNUgzLjljLS44LjEtMS42LjktMS42IDEuOHYxNC4xYzAgLjkuNyAxLjYgMS42IDEuNmgxNC4yYy45IDAgMS42LS43IDEuNi0xLjZWOS40Yy4xLS41LS4xLS45LS40LTEuMnptLTUuOC0zLjNsMy40IDMuNmgtMy40VjQuOXptMy45IDEyLjdINC43Yy0uMSAwLS4yIDAtLjItLjJWNC43YzAtLjIuMS0uMy4yLS4zaDcuMnY0LjRzMCAuOC4zIDEuMWMuMy4zIDEuMS4zIDEuMS4zaDQuM3Y3LjJzLS4xLjItLjIuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-filter-dot: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiNGRkYiPgogICAgPHBhdGggZD0iTTE0LDEyVjE5Ljg4QzE0LjA0LDIwLjE4IDEzLjk0LDIwLjUgMTMuNzEsMjAuNzFDMTMuMzIsMjEuMSAxMi42OSwyMS4xIDEyLjMsMjAuNzFMMTAuMjksMTguN0MxMC4wNiwxOC40NyA5Ljk2LDE4LjE2IDEwLDE3Ljg3VjEySDkuOTdMNC4yMSw0LjYyQzMuODcsNC4xOSAzLjk1LDMuNTYgNC4zOCwzLjIyQzQuNTcsMy4wOCA0Ljc4LDMgNSwzVjNIMTlWM0MxOS4yMiwzIDE5LjQzLDMuMDggMTkuNjIsMy4yMkMyMC4wNSwzLjU2IDIwLjEzLDQuMTkgMTkuNzksNC42MkwxNC4wMywxMkgxNFoiIC8+CiAgPC9nPgogIDxnIGNsYXNzPSJqcC1pY29uLWRvdCIgZmlsbD0iI0ZGRiI+CiAgICA8Y2lyY2xlIGN4PSIxOCIgY3k9IjE3IiByPSIzIj48L2NpcmNsZT4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-filter-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEwIDE4aDR2LTJoLTR2MnpNMyA2djJoMThWNkgzem0zIDdoMTJ2LTJINnYyeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-filter: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiNGRkYiPgogICAgPHBhdGggZD0iTTE0LDEyVjE5Ljg4QzE0LjA0LDIwLjE4IDEzLjk0LDIwLjUgMTMuNzEsMjAuNzFDMTMuMzIsMjEuMSAxMi42OSwyMS4xIDEyLjMsMjAuNzFMMTAuMjksMTguN0MxMC4wNiwxOC40NyA5Ljk2LDE4LjE2IDEwLDE3Ljg3VjEySDkuOTdMNC4yMSw0LjYyQzMuODcsNC4xOSAzLjk1LDMuNTYgNC4zOCwzLjIyQzQuNTcsMy4wOCA0Ljc4LDMgNSwzVjNIMTlWM0MxOS4yMiwzIDE5LjQzLDMuMDggMTkuNjIsMy4yMkMyMC4wNSwzLjU2IDIwLjEzLDQuMTkgMTkuNzksNC42MkwxNC4wMywxMkgxNFoiIC8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-folder-favorite: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGhlaWdodD0iMjRweCIgdmlld0JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjRweCIgZmlsbD0iIzAwMDAwMCI+CiAgPHBhdGggZD0iTTAgMGgyNHYyNEgwVjB6IiBmaWxsPSJub25lIi8+PHBhdGggY2xhc3M9ImpwLWljb24zIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzYxNjE2MSIgZD0iTTIwIDZoLThsLTItMkg0Yy0xLjEgMC0yIC45LTIgMnYxMmMwIDEuMS45IDIgMiAyaDE2YzEuMSAwIDItLjkgMi0yVjhjMC0xLjEtLjktMi0yLTJ6bS0yLjA2IDExTDE1IDE1LjI4IDEyLjA2IDE3bC43OC0zLjMzLTIuNTktMi4yNCAzLjQxLS4yOUwxNSA4bDEuMzQgMy4xNCAzLjQxLjI5LTIuNTkgMi4yNC43OCAzLjMzeiIvPgo8L3N2Zz4K);
  --jp-icon-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY4YzAtMS4xLS45LTItMi0yaC04bC0yLTJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-home: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGhlaWdodD0iMjRweCIgdmlld0JveD0iMCAwIDI0IDI0IiB3aWR0aD0iMjRweCIgZmlsbD0iIzAwMDAwMCI+CiAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPjxwYXRoIGNsYXNzPSJqcC1pY29uMyBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiIGQ9Ik0xMCAyMHYtNmg0djZoNXYtOGgzTDEyIDMgMiAxMmgzdjh6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-html5: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMDAiIGQ9Ik0xMDguNCAwaDIzdjIyLjhoMjEuMlYwaDIzdjY5aC0yM1Y0NmgtMjF2MjNoLTIzLjJNMjA2IDIzaC0yMC4zVjBoNjMuN3YyM0gyMjl2NDZoLTIzbTUzLjUtNjloMjQuMWwxNC44IDI0LjNMMzEzLjIgMGgyNC4xdjY5aC0yM1YzNC44bC0xNi4xIDI0LjgtMTYuMS0yNC44VjY5aC0yMi42bTg5LjItNjloMjN2NDYuMmgzMi42VjY5aC01NS42Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI2U0NGQyNiIgZD0iTTEwNy42IDQ3MWwtMzMtMzcwLjRoMzYyLjhsLTMzIDM3MC4yTDI1NS43IDUxMiIvPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNmMTY1MjkiIGQ9Ik0yNTYgNDgwLjVWMTMxaDE0OC4zTDM3NiA0NDciLz4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNlYmViZWIiIGQ9Ik0xNDIgMTc2LjNoMTE0djQ1LjRoLTY0LjJsNC4yIDQ2LjVoNjB2NDUuM0gxNTQuNG0yIDIyLjhIMjAybDMuMiAzNi4zIDUwLjggMTMuNnY0Ny40bC05My4yLTI2Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIiBmaWxsPSIjZmZmIiBkPSJNMzY5LjYgMTc2LjNIMjU1Ljh2NDUuNGgxMDkuNm0tNC4xIDQ2LjVIMjU1Ljh2NDUuNGg1NmwtNS4zIDU5LTUwLjcgMTMuNnY0Ny4ybDkzLTI1LjgiLz4KPC9zdmc+Cg==);
  --jp-icon-image: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1icmFuZDQganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNGRkYiIGQ9Ik0yLjIgMi4yaDE3LjV2MTcuNUgyLjJ6Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzNGNTFCNSIgZD0iTTIuMiAyLjJ2MTcuNWgxNy41bC4xLTE3LjVIMi4yem0xMi4xIDIuMmMxLjIgMCAyLjIgMSAyLjIgMi4ycy0xIDIuMi0yLjIgMi4yLTIuMi0xLTIuMi0yLjIgMS0yLjIgMi4yLTIuMnpNNC40IDE3LjZsMy4zLTguOCAzLjMgNi42IDIuMi0zLjIgNC40IDUuNEg0LjR6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-info: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUwLjk3OCA1MC45NzgiPgoJPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KCQk8cGF0aCBkPSJNNDMuNTIsNy40NThDMzguNzExLDIuNjQ4LDMyLjMwNywwLDI1LjQ4OSwwQzE4LjY3LDAsMTIuMjY2LDIuNjQ4LDcuNDU4LDcuNDU4CgkJCWMtOS45NDMsOS45NDEtOS45NDMsMjYuMTE5LDAsMzYuMDYyYzQuODA5LDQuODA5LDExLjIxMiw3LjQ1NiwxOC4wMzEsNy40NThjMCwwLDAuMDAxLDAsMC4wMDIsMAoJCQljNi44MTYsMCwxMy4yMjEtMi42NDgsMTguMDI5LTcuNDU4YzQuODA5LTQuODA5LDcuNDU3LTExLjIxMiw3LjQ1Ny0xOC4wM0M1MC45NzcsMTguNjcsNDguMzI4LDEyLjI2Niw0My41Miw3LjQ1OHoKCQkJIE00Mi4xMDYsNDIuMTA1Yy00LjQzMiw0LjQzMS0xMC4zMzIsNi44NzItMTYuNjE1LDYuODcyaC0wLjAwMmMtNi4yODUtMC4wMDEtMTIuMTg3LTIuNDQxLTE2LjYxNy02Ljg3MgoJCQljLTkuMTYyLTkuMTYzLTkuMTYyLTI0LjA3MSwwLTMzLjIzM0MxMy4zMDMsNC40NCwxOS4yMDQsMiwyNS40ODksMmM2LjI4NCwwLDEyLjE4NiwyLjQ0LDE2LjYxNyw2Ljg3MgoJCQljNC40MzEsNC40MzEsNi44NzEsMTAuMzMyLDYuODcxLDE2LjYxN0M0OC45NzcsMzEuNzcyLDQ2LjUzNiwzNy42NzUsNDIuMTA2LDQyLjEwNXoiLz4KCQk8cGF0aCBkPSJNMjMuNTc4LDMyLjIxOGMtMC4wMjMtMS43MzQsMC4xNDMtMy4wNTksMC40OTYtMy45NzJjMC4zNTMtMC45MTMsMS4xMS0xLjk5NywyLjI3Mi0zLjI1MwoJCQljMC40NjgtMC41MzYsMC45MjMtMS4wNjIsMS4zNjctMS41NzVjMC42MjYtMC43NTMsMS4xMDQtMS40NzgsMS40MzYtMi4xNzVjMC4zMzEtMC43MDcsMC40OTUtMS41NDEsMC40OTUtMi41CgkJCWMwLTEuMDk2LTAuMjYtMi4wODgtMC43NzktMi45NzljLTAuNTY1LTAuODc5LTEuNTAxLTEuMzM2LTIuODA2LTEuMzY5Yy0xLjgwMiwwLjA1Ny0yLjk4NSwwLjY2Ny0zLjU1LDEuODMyCgkJCWMtMC4zMDEsMC41MzUtMC41MDMsMS4xNDEtMC42MDcsMS44MTRjLTAuMTM5LDAuNzA3LTAuMjA3LDEuNDMyLTAuMjA3LDIuMTc0aC0yLjkzN2MtMC4wOTEtMi4yMDgsMC40MDctNC4xMTQsMS40OTMtNS43MTkKCQkJYzEuMDYyLTEuNjQsMi44NTUtMi40ODEsNS4zNzgtMi41MjdjMi4xNiwwLjAyMywzLjg3NCwwLjYwOCw1LjE0MSwxLjc1OGMxLjI3OCwxLjE2LDEuOTI5LDIuNzY0LDEuOTUsNC44MTEKCQkJYzAsMS4xNDItMC4xMzcsMi4xMTEtMC40MSwyLjkxMWMtMC4zMDksMC44NDUtMC43MzEsMS41OTMtMS4yNjgsMi4yNDNjLTAuNDkyLDAuNjUtMS4wNjgsMS4zMTgtMS43MywyLjAwMgoJCQljLTAuNjUsMC42OTctMS4zMTMsMS40NzktMS45ODcsMi4zNDZjLTAuMjM5LDAuMzc3LTAuNDI5LDAuNzc3LTAuNTY1LDEuMTk5Yy0wLjE2LDAuOTU5LTAuMjE3LDEuOTUxLTAuMTcxLDIuOTc5CgkJCUMyNi41ODksMzIuMjE4LDIzLjU3OCwzMi4yMTgsMjMuNTc4LDMyLjIxOHogTTIzLjU3OCwzOC4yMnYtMy40ODRoMy4wNzZ2My40ODRIMjMuNTc4eiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-inspector: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaW5zcGVjdG9yLWljb24tY29sb3IganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY2YzAtMS4xLS45LTItMi0yem0tNSAxNEg0di00aDExdjR6bTAtNUg0VjloMTF2NHptNSA1aC00VjloNHY5eiIvPgo8L3N2Zz4K);
  --jp-icon-json: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtanNvbi1pY29uLWNvbG9yIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI0Y5QTgyNSI+CiAgICA8cGF0aCBkPSJNMjAuMiAxMS44Yy0xLjYgMC0xLjcuNS0xLjcgMSAwIC40LjEuOS4xIDEuMy4xLjUuMS45LjEgMS4zIDAgMS43LTEuNCAyLjMtMy41IDIuM2gtLjl2LTEuOWguNWMxLjEgMCAxLjQgMCAxLjQtLjggMC0uMyAwLS42LS4xLTEgMC0uNC0uMS0uOC0uMS0xLjIgMC0xLjMgMC0xLjggMS4zLTItMS4zLS4yLTEuMy0uNy0xLjMtMiAwLS40LjEtLjguMS0xLjIuMS0uNC4xLS43LjEtMSAwLS44LS40LS43LTEuNC0uOGgtLjVWNC4xaC45YzIuMiAwIDMuNS43IDMuNSAyLjMgMCAuNC0uMS45LS4xIDEuMy0uMS41LS4xLjktLjEgMS4zIDAgLjUuMiAxIDEuNyAxdjEuOHpNMS44IDEwLjFjMS42IDAgMS43LS41IDEuNy0xIDAtLjQtLjEtLjktLjEtMS4zLS4xLS41LS4xLS45LS4xLTEuMyAwLTEuNiAxLjQtMi4zIDMuNS0yLjNoLjl2MS45aC0uNWMtMSAwLTEuNCAwLTEuNC44IDAgLjMgMCAuNi4xIDEgMCAuMi4xLjYuMSAxIDAgMS4zIDAgMS44LTEuMyAyQzYgMTEuMiA2IDExLjcgNiAxM2MwIC40LS4xLjgtLjEgMS4yLS4xLjMtLjEuNy0uMSAxIDAgLjguMy44IDEuNC44aC41djEuOWgtLjljLTIuMSAwLTMuNS0uNi0zLjUtMi4zIDAtLjQuMS0uOS4xLTEuMy4xLS41LjEtLjkuMS0xLjMgMC0uNS0uMi0xLTEuNy0xdi0xLjl6Ii8+CiAgICA8Y2lyY2xlIGN4PSIxMSIgY3k9IjEzLjgiIHI9IjIuMSIvPgogICAgPGNpcmNsZSBjeD0iMTEiIGN5PSI4LjIiIHI9IjIuMSIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-julia: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDMyNSAzMDAiPgogIDxnIGNsYXNzPSJqcC1icmFuZDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjY2IzYzMzIj4KICAgIDxwYXRoIGQ9Ik0gMTUwLjg5ODQzOCAyMjUgQyAxNTAuODk4NDM4IDI2Ni40MjE4NzUgMTE3LjMyMDMxMiAzMDAgNzUuODk4NDM4IDMwMCBDIDM0LjQ3NjU2MiAzMDAgMC44OTg0MzggMjY2LjQyMTg3NSAwLjg5ODQzOCAyMjUgQyAwLjg5ODQzOCAxODMuNTc4MTI1IDM0LjQ3NjU2MiAxNTAgNzUuODk4NDM4IDE1MCBDIDExNy4zMjAzMTIgMTUwIDE1MC44OTg0MzggMTgzLjU3ODEyNSAxNTAuODk4NDM4IDIyNSIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzM4OTgyNiI+CiAgICA8cGF0aCBkPSJNIDIzNy41IDc1IEMgMjM3LjUgMTE2LjQyMTg3NSAyMDMuOTIxODc1IDE1MCAxNjIuNSAxNTAgQyAxMjEuMDc4MTI1IDE1MCA4Ny41IDExNi40MjE4NzUgODcuNSA3NSBDIDg3LjUgMzMuNTc4MTI1IDEyMS4wNzgxMjUgMCAxNjIuNSAwIEMgMjAzLjkyMTg3NSAwIDIzNy41IDMzLjU3ODEyNSAyMzcuNSA3NSIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzk1NThiMiI+CiAgICA8cGF0aCBkPSJNIDMyNC4xMDE1NjIgMjI1IEMgMzI0LjEwMTU2MiAyNjYuNDIxODc1IDI5MC41MjM0MzggMzAwIDI0OS4xMDE1NjIgMzAwIEMgMjA3LjY3OTY4OCAzMDAgMTc0LjEwMTU2MiAyNjYuNDIxODc1IDE3NC4xMDE1NjIgMjI1IEMgMTc0LjEwMTU2MiAxODMuNTc4MTI1IDIwNy42Nzk2ODggMTUwIDI0OS4xMDE1NjIgMTUwIEMgMjkwLjUyMzQzOCAxNTAgMzI0LjEwMTU2MiAxODMuNTc4MTI1IDMyNC4xMDE1NjIgMjI1Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-jupyter-favicon: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTUyIiBoZWlnaHQ9IjE2NSIgdmlld0JveD0iMCAwIDE1MiAxNjUiIHZlcnNpb249IjEuMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgPGcgY2xhc3M9ImpwLWp1cHl0ZXItaWNvbi1jb2xvciIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA3ODk0NywgMTEwLjU4MjkyNykiIGQ9Ik03NS45NDIyODQyLDI5LjU4MDQ1NjEgQzQzLjMwMjM5NDcsMjkuNTgwNDU2MSAxNC43OTY3ODMyLDE3LjY1MzQ2MzQgMCwwIEM1LjUxMDgzMjExLDE1Ljg0MDY4MjkgMTUuNzgxNTM4OSwyOS41NjY3NzMyIDI5LjM5MDQ5NDcsMzkuMjc4NDE3MSBDNDIuOTk5Nyw0OC45ODk4NTM3IDU5LjI3MzcsNTQuMjA2NzgwNSA3NS45NjA1Nzg5LDU0LjIwNjc4MDUgQzkyLjY0NzQ1NzksNTQuMjA2NzgwNSAxMDguOTIxNDU4LDQ4Ljk4OTg1MzcgMTIyLjUzMDY2MywzOS4yNzg0MTcxIEMxMzYuMTM5NDUzLDI5LjU2Njc3MzIgMTQ2LjQxMDI4NCwxNS44NDA2ODI5IDE1MS45MjExNTgsMCBDMTM3LjA4Nzg2OCwxNy42NTM0NjM0IDEwOC41ODI1ODksMjkuNTgwNDU2MSA3NS45NDIyODQyLDI5LjU4MDQ1NjEgTDc1Ljk0MjI4NDIsMjkuNTgwNDU2MSBaIiAvPgogICAgPHBhdGggdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMzczNjgsIDAuNzA0ODc4KSIgZD0iTTc1Ljk3ODQ1NzksMjQuNjI2NDA3MyBDMTA4LjYxODc2MywyNC42MjY0MDczIDEzNy4xMjQ0NTgsMzYuNTUzNDQxNSAxNTEuOTIxMTU4LDU0LjIwNjc4MDUgQzE0Ni40MTAyODQsMzguMzY2MjIyIDEzNi4xMzk0NTMsMjQuNjQwMTMxNyAxMjIuNTMwNjYzLDE0LjkyODQ4NzggQzEwOC45MjE0NTgsNS4yMTY4NDM5IDkyLjY0NzQ1NzksMCA3NS45NjA1Nzg5LDAgQzU5LjI3MzcsMCA0Mi45OTk3LDUuMjE2ODQzOSAyOS4zOTA0OTQ3LDE0LjkyODQ4NzggQzE1Ljc4MTUzODksMjQuNjQwMTMxNyA1LjUxMDgzMjExLDM4LjM2NjIyMiAwLDU0LjIwNjc4MDUgQzE0LjgzMzA4MTYsMzYuNTg5OTI5MyA0My4zMzg1Njg0LDI0LjYyNjQwNzMgNzUuOTc4NDU3OSwyNC42MjY0MDczIEw3NS45Nzg0NTc5LDI0LjYyNjQwNzMgWiIgLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-jupyter: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzkiIGhlaWdodD0iNTEiIHZpZXdCb3g9IjAgMCAzOSA1MSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMTYzOCAtMjI4MSkiPgogICAgIDxnIGNsYXNzPSJqcC1qdXB5dGVyLWljb24tY29sb3IiIGZpbGw9IiNGMzc3MjYiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5Ljc0IDIzMTEuOTgpIiBkPSJNIDE4LjI2NDYgNy4xMzQxMUMgMTAuNDE0NSA3LjEzNDExIDMuNTU4NzIgNC4yNTc2IDAgMEMgMS4zMjUzOSAzLjgyMDQgMy43OTU1NiA3LjEzMDgxIDcuMDY4NiA5LjQ3MzAzQyAxMC4zNDE3IDExLjgxNTIgMTQuMjU1NyAxMy4wNzM0IDE4LjI2OSAxMy4wNzM0QyAyMi4yODIzIDEzLjA3MzQgMjYuMTk2MyAxMS44MTUyIDI5LjQ2OTQgOS40NzMwM0MgMzIuNzQyNCA3LjEzMDgxIDM1LjIxMjYgMy44MjA0IDM2LjUzOCAwQyAzMi45NzA1IDQuMjU3NiAyNi4xMTQ4IDcuMTM0MTEgMTguMjY0NiA3LjEzNDExWiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5LjczIDIyODUuNDgpIiBkPSJNIDE4LjI3MzMgNS45MzkzMUMgMjYuMTIzNSA1LjkzOTMxIDMyLjk3OTMgOC44MTU4MyAzNi41MzggMTMuMDczNEMgMzUuMjEyNiA5LjI1MzAzIDMyLjc0MjQgNS45NDI2MiAyOS40Njk0IDMuNjAwNEMgMjYuMTk2MyAxLjI1ODE4IDIyLjI4MjMgMCAxOC4yNjkgMEMgMTQuMjU1NyAwIDEwLjM0MTcgMS4yNTgxOCA3LjA2ODYgMy42MDA0QyAzLjc5NTU2IDUuOTQyNjIgMS4zMjUzOSA5LjI1MzAzIDAgMTMuMDczNEMgMy41Njc0NSA4LjgyNDYzIDEwLjQyMzIgNS45MzkzMSAxOC4yNzMzIDUuOTM5MzFaIi8+CiAgICA8L2c+CiAgICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjY5LjMgMjI4MS4zMSkiIGQ9Ik0gNS44OTM1MyAyLjg0NEMgNS45MTg4OSAzLjQzMTY1IDUuNzcwODUgNC4wMTM2NyA1LjQ2ODE1IDQuNTE2NDVDIDUuMTY1NDUgNS4wMTkyMiA0LjcyMTY4IDUuNDIwMTUgNC4xOTI5OSA1LjY2ODUxQyAzLjY2NDMgNS45MTY4OCAzLjA3NDQ0IDYuMDAxNTEgMi40OTgwNSA1LjkxMTcxQyAxLjkyMTY2IDUuODIxOSAxLjM4NDYzIDUuNTYxNyAwLjk1NDg5OCA1LjE2NDAxQyAwLjUyNTE3IDQuNzY2MzMgMC4yMjIwNTYgNC4yNDkwMyAwLjA4MzkwMzcgMy42Nzc1N0MgLTAuMDU0MjQ4MyAzLjEwNjExIC0wLjAyMTIzIDIuNTA2MTcgMC4xNzg3ODEgMS45NTM2NEMgMC4zNzg3OTMgMS40MDExIDAuNzM2ODA5IDAuOTIwODE3IDEuMjA3NTQgMC41NzM1MzhDIDEuNjc4MjYgMC4yMjYyNTkgMi4yNDA1NSAwLjAyNzU5MTkgMi44MjMyNiAwLjAwMjY3MjI5QyAzLjYwMzg5IC0wLjAzMDcxMTUgNC4zNjU3MyAwLjI0OTc4OSA0Ljk0MTQyIDAuNzgyNTUxQyA1LjUxNzExIDEuMzE1MzEgNS44NTk1NiAyLjA1Njc2IDUuODkzNTMgMi44NDRaIi8+CiAgICAgIDxwYXRoIHRyYW5zZm9ybT0idHJhbnNsYXRlKDE2MzkuOCAyMzIzLjgxKSIgZD0iTSA3LjQyNzg5IDMuNTgzMzhDIDcuNDYwMDggNC4zMjQzIDcuMjczNTUgNS4wNTgxOSA2Ljg5MTkzIDUuNjkyMTNDIDYuNTEwMzEgNi4zMjYwNyA1Ljk1MDc1IDYuODMxNTYgNS4yODQxMSA3LjE0NDZDIDQuNjE3NDcgNy40NTc2MyAzLjg3MzcxIDcuNTY0MTQgMy4xNDcwMiA3LjQ1MDYzQyAyLjQyMDMyIDcuMzM3MTIgMS43NDMzNiA3LjAwODcgMS4yMDE4NCA2LjUwNjk1QyAwLjY2MDMyOCA2LjAwNTIgMC4yNzg2MSA1LjM1MjY4IDAuMTA1MDE3IDQuNjMyMDJDIC0wLjA2ODU3NTcgMy45MTEzNSAtMC4wMjYyMzYxIDMuMTU0OTQgMC4yMjY2NzUgMi40NTg1NkMgMC40Nzk1ODcgMS43NjIxNyAwLjkzMTY5NyAxLjE1NzEzIDEuNTI1NzYgMC43MjAwMzNDIDIuMTE5ODMgMC4yODI5MzUgMi44MjkxNCAwLjAzMzQzOTUgMy41NjM4OSAwLjAwMzEzMzQ0QyA0LjU0NjY3IC0wLjAzNzQwMzMgNS41MDUyOSAwLjMxNjcwNiA2LjIyOTYxIDAuOTg3ODM1QyA2Ljk1MzkzIDEuNjU4OTYgNy4zODQ4NCAyLjU5MjM1IDcuNDI3ODkgMy41ODMzOEwgNy40Mjc4OSAzLjU4MzM4WiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM4LjM2IDIyODYuMDYpIiBkPSJNIDIuMjc0NzEgNC4zOTYyOUMgMS44NDM2MyA0LjQxNTA4IDEuNDE2NzEgNC4zMDQ0NSAxLjA0Nzk5IDQuMDc4NDNDIDAuNjc5MjY4IDMuODUyNCAwLjM4NTMyOCAzLjUyMTE0IDAuMjAzMzcxIDMuMTI2NTZDIDAuMDIxNDEzNiAyLjczMTk4IC0wLjA0MDM3OTggMi4yOTE4MyAwLjAyNTgxMTYgMS44NjE4MUMgMC4wOTIwMDMxIDEuNDMxOCAwLjI4MzIwNCAxLjAzMTI2IDAuNTc1MjEzIDAuNzEwODgzQyAwLjg2NzIyMiAwLjM5MDUxIDEuMjQ2OTEgMC4xNjQ3MDggMS42NjYyMiAwLjA2MjA1OTJDIDIuMDg1NTMgLTAuMDQwNTg5NyAyLjUyNTYxIC0wLjAxNTQ3MTQgMi45MzA3NiAwLjEzNDIzNUMgMy4zMzU5MSAwLjI4Mzk0MSAzLjY4NzkyIDAuNTUxNTA1IDMuOTQyMjIgMC45MDMwNkMgNC4xOTY1MiAxLjI1NDYyIDQuMzQxNjkgMS42NzQzNiA0LjM1OTM1IDIuMTA5MTZDIDQuMzgyOTkgMi42OTEwNyA0LjE3Njc4IDMuMjU4NjkgMy43ODU5NyAzLjY4NzQ2QyAzLjM5NTE2IDQuMTE2MjQgMi44NTE2NiA0LjM3MTE2IDIuMjc0NzEgNC4zOTYyOUwgMi4yNzQ3MSA0LjM5NjI5WiIvPgogICAgPC9nPgogIDwvZz4+Cjwvc3ZnPgo=);
  --jp-icon-jupyterlab-wordmark: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyMDAiIHZpZXdCb3g9IjAgMCAxODYwLjggNDc1Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0RTRFNEUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ4MC4xMzY0MDEsIDY0LjI3MTQ5MykiPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMDAwMDAsIDU4Ljg3NTU2NikiPgogICAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA4NzYwMywgMC4xNDAyOTQpIj4KICAgICAgICA8cGF0aCBkPSJNLTQyNi45LDE2OS44YzAsNDguNy0zLjcsNjQuNy0xMy42LDc2LjRjLTEwLjgsMTAtMjUsMTUuNS0zOS43LDE1LjVsMy43LDI5IGMyMi44LDAuMyw0NC44LTcuOSw2MS45LTIzLjFjMTcuOC0xOC41LDI0LTQ0LjEsMjQtODMuM1YwSC00Mjd2MTcwLjFMLTQyNi45LDE2OS44TC00MjYuOSwxNjkuOHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTU1LjA0NTI5NiwgNTYuODM3MTA0KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuNTYyNDUzLCAxLjc5OTg0MikiPgogICAgICAgIDxwYXRoIGQ9Ik0tMzEyLDE0OGMwLDIxLDAsMzkuNSwxLjcsNTUuNGgtMzEuOGwtMi4xLTMzLjNoLTAuOGMtNi43LDExLjYtMTYuNCwyMS4zLTI4LDI3LjkgYy0xMS42LDYuNi0yNC44LDEwLTM4LjIsOS44Yy0zMS40LDAtNjktMTcuNy02OS04OVYwaDM2LjR2MTEyLjdjMCwzOC43LDExLjYsNjQuNyw0NC42LDY0LjdjMTAuMy0wLjIsMjAuNC0zLjUsMjguOS05LjQgYzguNS01LjksMTUuMS0xNC4zLDE4LjktMjMuOWMyLjItNi4xLDMuMy0xMi41LDMuMy0xOC45VjAuMmgzNi40VjE0OEgtMzEyTC0zMTIsMTQ4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzOTAuMDEzMzIyLCA1My40Nzk2MzgpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS43MDY0NTgsIDAuMjMxNDI1KSI+CiAgICAgICAgPHBhdGggZD0iTS00NzguNiw3MS40YzAtMjYtMC44LTQ3LTEuNy02Ni43aDMyLjdsMS43LDM0LjhoMC44YzcuMS0xMi41LDE3LjUtMjIuOCwzMC4xLTI5LjcgYzEyLjUtNywyNi43LTEwLjMsNDEtOS44YzQ4LjMsMCw4NC43LDQxLjcsODQuNywxMDMuM2MwLDczLjEtNDMuNywxMDkuMi05MSwxMDkuMmMtMTIuMSwwLjUtMjQuMi0yLjItMzUtNy44IGMtMTAuOC01LjYtMTkuOS0xMy45LTI2LjYtMjQuMmgtMC44VjI5MWgtMzZ2LTIyMEwtNDc4LjYsNzEuNEwtNDc4LjYsNzEuNHogTS00NDIuNiwxMjUuNmMwLjEsNS4xLDAuNiwxMC4xLDEuNywxNS4xIGMzLDEyLjMsOS45LDIzLjMsMTkuOCwzMS4xYzkuOSw3LjgsMjIuMSwxMi4xLDM0LjcsMTIuMWMzOC41LDAsNjAuNy0zMS45LDYwLjctNzguNWMwLTQwLjctMjEuMS03NS42LTU5LjUtNzUuNiBjLTEyLjksMC40LTI1LjMsNS4xLTM1LjMsMTMuNGMtOS45LDguMy0xNi45LDE5LjctMTkuNiwzMi40Yy0xLjUsNC45LTIuMywxMC0yLjUsMTUuMVYxMjUuNkwtNDQyLjYsMTI1LjZMLTQ0Mi42LDEyNS42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSg2MDYuNzQwNzI2LCA1Ni44MzcxMDQpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC43NTEyMjYsIDEuOTg5Mjk5KSI+CiAgICAgICAgPHBhdGggZD0iTS00NDAuOCwwbDQzLjcsMTIwLjFjNC41LDEzLjQsOS41LDI5LjQsMTIuOCw0MS43aDAuOGMzLjctMTIuMiw3LjktMjcuNywxMi44LTQyLjQgbDM5LjctMTE5LjJoMzguNUwtMzQ2LjksMTQ1Yy0yNiw2OS43LTQzLjcsMTA1LjQtNjguNiwxMjcuMmMtMTIuNSwxMS43LTI3LjksMjAtNDQuNiwyMy45bC05LjEtMzEuMSBjMTEuNy0zLjksMjIuNS0xMC4xLDMxLjgtMTguMWMxMy4yLTExLjEsMjMuNy0yNS4yLDMwLjYtNDEuMmMxLjUtMi44LDIuNS01LjcsMi45LTguOGMtMC4zLTMuMy0xLjItNi42LTIuNS05LjdMLTQ4MC4yLDAuMSBoMzkuN0wtNDQwLjgsMEwtNDQwLjgsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoODIyLjc0ODEwNCwgMC4wMDAwMDApIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS40NjQwNTAsIDAuMzc4OTE0KSI+CiAgICAgICAgPHBhdGggZD0iTS00MTMuNywwdjU4LjNoNTJ2MjguMmgtNTJWMTk2YzAsMjUsNywzOS41LDI3LjMsMzkuNWM3LjEsMC4xLDE0LjItMC43LDIxLjEtMi41IGwxLjcsMjcuN2MtMTAuMywzLjctMjEuMyw1LjQtMzIuMiw1Yy03LjMsMC40LTE0LjYtMC43LTIxLjMtMy40Yy02LjgtMi43LTEyLjktNi44LTE3LjktMTIuMWMtMTAuMy0xMC45LTE0LjEtMjktMTQuMS01Mi45IFY4Ni41aC0zMVY1OC4zaDMxVjkuNkwtNDEzLjcsMEwtNDEzLjcsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOTc0LjQzMzI4NiwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuOTkwMDM0LCAwLjYxMDMzOSkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDQ1LjgsMTEzYzAuOCw1MCwzMi4yLDcwLjYsNjguNiw3MC42YzE5LDAuNiwzNy45LTMsNTUuMy0xMC41bDYuMiwyNi40IGMtMjAuOSw4LjktNDMuNSwxMy4xLTY2LjIsMTIuNmMtNjEuNSwwLTk4LjMtNDEuMi05OC4zLTEwMi41Qy00ODAuMiw0OC4yLTQ0NC43LDAtMzg2LjUsMGM2NS4yLDAsODIuNyw1OC4zLDgyLjcsOTUuNyBjLTAuMSw1LjgtMC41LDExLjUtMS4yLDE3LjJoLTE0MC42SC00NDUuOEwtNDQ1LjgsMTEzeiBNLTMzOS4yLDg2LjZjMC40LTIzLjUtOS41LTYwLjEtNTAuNC02MC4xIGMtMzYuOCwwLTUyLjgsMzQuNC01NS43LDYwLjFILTMzOS4yTC0zMzkuMiw4Ni42TC0zMzkuMiw4Ni42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxMjAxLjk2MTA1OCwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuMTc5NjQwLCAwLjcwNTA2OCkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDc4LjYsNjhjMC0yMy45LTAuNC00NC41LTEuNy02My40aDMxLjhsMS4yLDM5LjloMS43YzkuMS0yNy4zLDMxLTQ0LjUsNTUuMy00NC41IGMzLjUtMC4xLDcsMC40LDEwLjMsMS4ydjM0LjhjLTQuMS0wLjktOC4yLTEuMy0xMi40LTEuMmMtMjUuNiwwLTQzLjcsMTkuNy00OC43LDQ3LjRjLTEsNS43LTEuNiwxMS41LTEuNywxNy4ydjEwOC4zaC0zNlY2OCBMLTQ3OC42LDY4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCBkPSJNMTM1Mi4zLDMyNi4yaDM3VjI4aC0zN1YzMjYuMnogTTE2MDQuOCwzMjYuMmMtMi41LTEzLjktMy40LTMxLjEtMy40LTQ4Ljd2LTc2IGMwLTQwLjctMTUuMS04My4xLTc3LjMtODMuMWMtMjUuNiwwLTUwLDcuMS02Ni44LDE4LjFsOC40LDI0LjRjMTQuMy05LjIsMzQtMTUuMSw1My0xNS4xYzQxLjYsMCw0Ni4yLDMwLjIsNDYuMiw0N3Y0LjIgYy03OC42LTAuNC0xMjIuMywyNi41LTEyMi4zLDc1LjZjMCwyOS40LDIxLDU4LjQsNjIuMiw1OC40YzI5LDAsNTAuOS0xNC4zLDYyLjItMzAuMmgxLjNsMi45LDI1LjZIMTYwNC44eiBNMTU2NS43LDI1Ny43IGMwLDMuOC0wLjgsOC0yLjEsMTEuOGMtNS45LDE3LjItMjIuNywzNC00OS4yLDM0Yy0xOC45LDAtMzQuOS0xMS4zLTM0LjktMzUuM2MwLTM5LjUsNDUuOC00Ni42LDg2LjItNDUuOFYyNTcuN3ogTTE2OTguNSwzMjYuMiBsMS43LTMzLjZoMS4zYzE1LjEsMjYuOSwzOC43LDM4LjIsNjguMSwzOC4yYzQ1LjQsMCw5MS4yLTM2LjEsOTEuMi0xMDguOGMwLjQtNjEuNy0zNS4zLTEwMy43LTg1LjctMTAzLjcgYy0zMi44LDAtNTYuMywxNC43LTY5LjMsMzcuNGgtMC44VjI4aC0zNi42djI0NS43YzAsMTguMS0wLjgsMzguNi0xLjcsNTIuNUgxNjk4LjV6IE0xNzA0LjgsMjA4LjJjMC01LjksMS4zLTEwLjksMi4xLTE1LjEgYzcuNi0yOC4xLDMxLjEtNDUuNCw1Ni4zLTQ1LjRjMzkuNSwwLDYwLjUsMzQuOSw2MC41LDc1LjZjMCw0Ni42LTIzLjEsNzguMS02MS44LDc4LjFjLTI2LjksMC00OC4zLTE3LjYtNTUuNS00My4zIGMtMC44LTQuMi0xLjctOC44LTEuNy0xMy40VjIwOC4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgZmlsbD0iIzYxNjE2MSIgZD0iTTE1IDlIOXY2aDZWOXptLTIgNGgtMnYtMmgydjJ6bTgtMlY5aC0yVjdjMC0xLjEtLjktMi0yLTJoLTJWM2gtMnYyaC0yVjNIOXYySDdjLTEuMSAwLTIgLjktMiAydjJIM3YyaDJ2MkgzdjJoMnYyYzAgMS4xLjkgMiAyIDJoMnYyaDJ2LTJoMnYyaDJ2LTJoMmMxLjEgMCAyLS45IDItMnYtMmgydi0yaC0ydi0yaDJ6bS00IDZIN1Y3aDEwdjEweiIvPgo8L3N2Zz4K);
  --jp-icon-keyboard: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMTdjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY3YzAtMS4xLS45LTItMi0yem0tOSAzaDJ2MmgtMlY4em0wIDNoMnYyaC0ydi0yek04IDhoMnYySDhWOHptMCAzaDJ2Mkg4di0yem0tMSAySDV2LTJoMnYyem0wLTNINVY4aDJ2MnptOSA3SDh2LTJoOHYyem0wLTRoLTJ2LTJoMnYyem0wLTNoLTJWOGgydjJ6bTMgM2gtMnYtMmgydjJ6bTAtM2gtMlY4aDJ2MnoiLz4KPC9zdmc+Cg==);
  --jp-icon-launch: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMzIgMzIiIHdpZHRoPSIzMiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik0yNiwyOEg2YTIuMDAyNywyLjAwMjcsMCwwLDEtMi0yVjZBMi4wMDI3LDIuMDAyNywwLDAsMSw2LDRIMTZWNkg2VjI2SDI2VjE2aDJWMjZBMi4wMDI3LDIuMDAyNywwLDAsMSwyNiwyOFoiLz4KICAgIDxwb2x5Z29uIHBvaW50cz0iMjAgMiAyMCA0IDI2LjU4NiA0IDE4IDEyLjU4NiAxOS40MTQgMTQgMjggNS40MTQgMjggMTIgMzAgMTIgMzAgMiAyMCAyIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-launcher: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkgMTlINVY1aDdWM0g1YTIgMiAwIDAwLTIgMnYxNGEyIDIgMCAwMDIgMmgxNGMxLjEgMCAyLS45IDItMnYtN2gtMnY3ek0xNCAzdjJoMy41OWwtOS44MyA5LjgzIDEuNDEgMS40MUwxOSA2LjQxVjEwaDJWM2gtN3oiLz4KPC9zdmc+Cg==);
  --jp-icon-line-form: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGZpbGw9IndoaXRlIiBkPSJNNS44OCA0LjEyTDEzLjc2IDEybC03Ljg4IDcuODhMOCAyMmwxMC0xMEw4IDJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-link: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMuOSAxMmMwLTEuNzEgMS4zOS0zLjEgMy4xLTMuMWg0VjdIN2MtMi43NiAwLTUgMi4yNC01IDVzMi4yNCA1IDUgNWg0di0xLjlIN2MtMS43MSAwLTMuMS0xLjM5LTMuMS0zLjF6TTggMTNoOHYtMkg4djJ6bTktNmgtNHYxLjloNGMxLjcxIDAgMy4xIDEuMzkgMy4xIDMuMXMtMS4zOSAzLjEtMy4xIDMuMWgtNFYxN2g0YzIuNzYgMCA1LTIuMjQgNS01cy0yLjI0LTUtNS01eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiIGQ9Ik0xOSA1djE0SDVWNWgxNG0xLjEtMkgzLjljLS41IDAtLjkuNC0uOS45djE2LjJjMCAuNC40LjkuOS45aDE2LjJjLjQgMCAuOS0uNS45LS45VjMuOWMwLS41LS41LS45LS45LS45ek0xMSA3aDZ2MmgtNlY3em0wIDRoNnYyaC02di0yem0wIDRoNnYyaC02ek03IDdoMnYySDd6bTAgNGgydjJIN3ptMCA0aDJ2Mkg3eiIvPgo8L3N2Zz4K);
  --jp-icon-markdown: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjN0IxRkEyIiBkPSJNNSAxNC45aDEybC02LjEgNnptOS40LTYuOGMwLTEuMy0uMS0yLjktLjEtNC41LS40IDEuNC0uOSAyLjktMS4zIDQuM2wtMS4zIDQuM2gtMkw4LjUgNy45Yy0uNC0xLjMtLjctMi45LTEtNC4zLS4xIDEuNi0uMSAzLjItLjIgNC42TDcgMTIuNEg0LjhsLjctMTFoMy4zTDEwIDVjLjQgMS4yLjcgMi43IDEgMy45LjMtMS4yLjctMi42IDEtMy45bDEuMi0zLjdoMy4zbC42IDExaC0yLjRsLS4zLTQuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-move-down: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTQiIGhlaWdodD0iMTQiIHZpZXdCb3g9IjAgMCAxNCAxNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggY2xhc3M9ImpwLWljb24zIiBkPSJNMTIuNDcxIDcuNTI4OTlDMTIuNzYzMiA3LjIzNjg0IDEyLjc2MzIgNi43NjMxNiAxMi40NzEgNi40NzEwMVY2LjQ3MTAxQzEyLjE3OSA2LjE3OTA1IDExLjcwNTcgNi4xNzg4NCAxMS40MTM1IDYuNDcwNTRMNy43NSAxMC4xMjc1VjEuNzVDNy43NSAxLjMzNTc5IDcuNDE0MjEgMSA3IDFWMUM2LjU4NTc5IDEgNi4yNSAxLjMzNTc5IDYuMjUgMS43NVYxMC4xMjc1TDIuNTk3MjYgNi40NjgyMkMyLjMwMzM4IDYuMTczODEgMS44MjY0MSA2LjE3MzU5IDEuNTMyMjYgNi40Njc3NFY2LjQ2Nzc0QzEuMjM4MyA2Ljc2MTcgMS4yMzgzIDcuMjM4MyAxLjUzMjI2IDcuNTMyMjZMNi4yOTI4OSAxMi4yOTI5QzYuNjgzNDIgMTIuNjgzNCA3LjMxNjU4IDEyLjY4MzQgNy43MDcxMSAxMi4yOTI5TDEyLjQ3MSA3LjUyODk5WiIgZmlsbD0iIzYxNjE2MSIvPgo8L3N2Zz4K);
  --jp-icon-move-up: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTQiIGhlaWdodD0iMTQiIHZpZXdCb3g9IjAgMCAxNCAxNCIgZmlsbD0ibm9uZSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KPHBhdGggY2xhc3M9ImpwLWljb24zIiBkPSJNMS41Mjg5OSA2LjQ3MTAxQzEuMjM2ODQgNi43NjMxNiAxLjIzNjg0IDcuMjM2ODQgMS41Mjg5OSA3LjUyODk5VjcuNTI4OTlDMS44MjA5NSA3LjgyMDk1IDIuMjk0MjYgNy44MjExNiAyLjU4NjQ5IDcuNTI5NDZMNi4yNSAzLjg3MjVWMTIuMjVDNi4yNSAxMi42NjQyIDYuNTg1NzkgMTMgNyAxM1YxM0M3LjQxNDIxIDEzIDcuNzUgMTIuNjY0MiA3Ljc1IDEyLjI1VjMuODcyNUwxMS40MDI3IDcuNTMxNzhDMTEuNjk2NiA3LjgyNjE5IDEyLjE3MzYgNy44MjY0MSAxMi40Njc3IDcuNTMyMjZWNy41MzIyNkMxMi43NjE3IDcuMjM4MyAxMi43NjE3IDYuNzYxNyAxMi40Njc3IDYuNDY3NzRMNy43MDcxMSAxLjcwNzExQzcuMzE2NTggMS4zMTY1OCA2LjY4MzQyIDEuMzE2NTggNi4yOTI4OSAxLjcwNzExTDEuNTI4OTkgNi40NzEwMVoiIGZpbGw9IiM2MTYxNjEiLz4KPC9zdmc+Cg==);
  --jp-icon-new-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwIDZoLThsLTItMkg0Yy0xLjExIDAtMS45OS44OS0xLjk5IDJMMiAxOGMwIDEuMTEuODkgMiAyIDJoMTZjMS4xMSAwIDItLjg5IDItMlY4YzAtMS4xMS0uODktMi0yLTJ6bS0xIDhoLTN2M2gtMnYtM2gtM3YtMmgzVjloMnYzaDN2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-not-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI1IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDMgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMTkgMTcuMTg0NCAyLjk2OTY4IDE0LjMwMzIgMS44NjA5NCAxMS40NDA5WiIvPgogICAgPHBhdGggY2xhc3M9ImpwLWljb24yIiBzdHJva2U9IiMzMzMzMzMiIHN0cm9rZS13aWR0aD0iMiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOS4zMTU5MiA5LjMyMDMxKSIgZD0iTTcuMzY4NDIgMEwwIDcuMzY0NzkiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDkuMzE1OTIgMTYuNjgzNikgc2NhbGUoMSAtMSkiIGQ9Ik03LjM2ODQyIDBMMCA3LjM2NDc5Ii8+Cjwvc3ZnPgo=);
  --jp-icon-notebook: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtbm90ZWJvb2staWNvbi1jb2xvciBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNFRjZDMDAiPgogICAgPHBhdGggZD0iTTE4LjcgMy4zdjE1LjRIMy4zVjMuM2gxNS40bTEuNS0xLjVIMS44djE4LjNoMTguM2wuMS0xOC4zeiIvPgogICAgPHBhdGggZD0iTTE2LjUgMTYuNWwtNS40LTQuMy01LjYgNC4zdi0xMWgxMXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-numbering: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjIiIGhlaWdodD0iMjIiIHZpZXdCb3g9IjAgMCAyOCAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTQgMTlINlYxOS41SDVWMjAuNUg2VjIxSDRWMjJIN1YxOEg0VjE5Wk01IDEwSDZWNkg0VjdINVYxMFpNNCAxM0g1LjhMNCAxNS4xVjE2SDdWMTVINS4yTDcgMTIuOVYxMkg0VjEzWk05IDdWOUgyM1Y3SDlaTTkgMjFIMjNWMTlIOVYyMVpNOSAxNUgyM1YxM0g5VjE1WiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-offline-bolt: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDIuMDJjLTUuNTEgMC05Ljk4IDQuNDctOS45OCA5Ljk4czQuNDcgOS45OCA5Ljk4IDkuOTggOS45OC00LjQ3IDkuOTgtOS45OFMxNy41MSAyLjAyIDEyIDIuMDJ6TTExLjQ4IDIwdi02LjI2SDhMMTMgNHY2LjI2aDMuMzVMMTEuNDggMjB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-palette: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE4IDEzVjIwSDRWNkg5LjAyQzkuMDcgNS4yOSA5LjI0IDQuNjIgOS41IDRINEMyLjkgNCAyIDQuOSAyIDZWMjBDMiAyMS4xIDIuOSAyMiA0IDIySDE4QzE5LjEgMjIgMjAgMjEuMSAyMCAyMFYxNUwxOCAxM1pNMTkuMyA4Ljg5QzE5Ljc0IDguMTkgMjAgNy4zOCAyMCA2LjVDMjAgNC4wMSAxNy45OSAyIDE1LjUgMkMxMy4wMSAyIDExIDQuMDEgMTEgNi41QzExIDguOTkgMTMuMDEgMTEgMTUuNDkgMTFDMTYuMzcgMTEgMTcuMTkgMTAuNzQgMTcuODggMTAuM0wyMSAxMy40MkwyMi40MiAxMkwxOS4zIDguODlaTTE1LjUgOUMxNC4xMiA5IDEzIDcuODggMTMgNi41QzEzIDUuMTIgMTQuMTIgNCAxNS41IDRDMTYuODggNCAxOCA1LjEyIDE4IDYuNUMxOCA3Ljg4IDE2Ljg4IDkgMTUuNSA5WiIvPgogICAgPHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik00IDZIOS4wMTg5NEM5LjAwNjM5IDYuMTY1MDIgOSA2LjMzMTc2IDkgNi41QzkgOC44MTU3NyAxMC4yMTEgMTAuODQ4NyAxMi4wMzQzIDEySDlWMTRIMTZWMTIuOTgxMUMxNi41NzAzIDEyLjkzNzcgMTcuMTIgMTIuODIwNyAxNy42Mzk2IDEyLjYzOTZMMTggMTNWMjBINFY2Wk04IDhINlYxMEg4VjhaTTYgMTJIOFYxNEg2VjEyWk04IDE2SDZWMThIOFYxNlpNOSAxNkgxNlYxOEg5VjE2WiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-paste: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE5IDJoLTQuMThDMTQuNC44NCAxMy4zIDAgMTIgMGMtMS4zIDAtMi40Ljg0LTIuODIgMkg1Yy0xLjEgMC0yIC45LTIgMnYxNmMwIDEuMS45IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjRjMC0xLjEtLjktMi0yLTJ6bS03IDBjLjU1IDAgMSAuNDUgMSAxcy0uNDUgMS0xIDEtMS0uNDUtMS0xIC40NS0xIDEtMXptNyAxOEg1VjRoMnYzaDEwVjRoMnYxNnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-pdf: url(data:image/svg+xml;base64,PHN2ZwogICB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyMiAyMiIgd2lkdGg9IjE2Ij4KICAgIDxwYXRoIHRyYW5zZm9ybT0icm90YXRlKDQ1KSIgY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI0ZGMkEyQSIKICAgICAgIGQ9Im0gMjIuMzQ0MzY5LC0zLjAxNjM2NDIgaCA1LjYzODYwNCB2IDEuNTc5MjQzMyBoIC0zLjU0OTIyNyB2IDEuNTA4NjkyOTkgaCAzLjMzNzU3NiBWIDEuNjUwODE1NCBoIC0zLjMzNzU3NiB2IDMuNDM1MjYxMyBoIC0yLjA4OTM3NyB6IG0gLTcuMTM2NDQ0LDEuNTc5MjQzMyB2IDQuOTQzOTU0MyBoIDAuNzQ4OTIgcSAxLjI4MDc2MSwwIDEuOTUzNzAzLC0wLjYzNDk1MzUgMC42NzgzNjksLTAuNjM0OTUzNSAwLjY3ODM2OSwtMS44NDUxNjQxIDAsLTEuMjA0NzgzNTUgLTAuNjcyOTQyLC0xLjgzNDMxMDExIC0wLjY3Mjk0MiwtMC42Mjk1MjY1OSAtMS45NTkxMywtMC42Mjk1MjY1OSB6IG0gLTIuMDg5Mzc3LC0xLjU3OTI0MzMgaCAyLjIwMzM0MyBxIDEuODQ1MTY0LDAgMi43NDYwMzksMC4yNjU5MjA3IDAuOTA2MzAxLDAuMjYwNDkzNyAxLjU1MjEwOCwwLjg5MDAyMDMgMC41Njk4MywwLjU0ODEyMjMgMC44NDY2MDUsMS4yNjQ0ODAwNiAwLjI3Njc3NCwwLjcxNjM1NzgxIDAuMjc2Nzc0LDEuNjIyNjU4OTQgMCwwLjkxNzE1NTEgLTAuMjc2Nzc0LDEuNjM4OTM5OSAtMC4yNzY3NzUsMC43MTYzNTc4IC0wLjg0NjYwNSwxLjI2NDQ4IC0wLjY1MTIzNCwwLjYyOTUyNjYgLTEuNTYyOTYyLDAuODk1NDQ3MyAtMC45MTE3MjgsMC4yNjA0OTM3IC0yLjczNTE4NSwwLjI2MDQ5MzcgaCAtMi4yMDMzNDMgeiBtIC04LjE0NTg1NjUsMCBoIDMuNDY3ODIzIHEgMS41NDY2ODE2LDAgMi4zNzE1Nzg1LDAuNjg5MjIzIDAuODMwMzI0LDAuNjgzNzk2MSAwLjgzMDMyNCwxLjk1MzcwMzE0IDAsMS4yNzUzMzM5NyAtMC44MzAzMjQsMS45NjQ1NTcwNiBRIDkuOTg3MTk2MSwyLjI3NDkxNSA4LjQ0MDUxNDUsMi4yNzQ5MTUgSCA3LjA2MjA2ODQgViA1LjA4NjA3NjcgSCA0Ljk3MjY5MTUgWiBtIDIuMDg5Mzc2OSwxLjUxNDExOTkgdiAyLjI2MzAzOTQzIGggMS4xNTU5NDEgcSAwLjYwNzgxODgsMCAwLjkzODg2MjksLTAuMjkzMDU1NDcgMC4zMzEwNDQxLC0wLjI5ODQ4MjQxIDAuMzMxMDQ0MSwtMC44NDExNzc3MiAwLC0wLjU0MjY5NTMxIC0wLjMzMTA0NDEsLTAuODM1NzUwNzQgLTAuMzMxMDQ0MSwtMC4yOTMwNTU1IC0wLjkzODg2MjksLTAuMjkzMDU1NSB6IgovPgo8L3N2Zz4K);
  --jp-icon-python: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iLTEwIC0xMCAxMzEuMTYxMzYxNjk0MzM1OTQgMTMyLjM4ODk5OTkzODk2NDg0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMzA2OTk4IiBkPSJNIDU0LjkxODc4NSw5LjE5Mjc0MjFlLTQgQyA1MC4zMzUxMzIsMC4wMjIyMTcyNyA0NS45NTc4NDYsMC40MTMxMzY5NyA0Mi4xMDYyODUsMS4wOTQ2NjkzIDMwLjc2MDA2OSwzLjA5OTE3MzEgMjguNzAwMDM2LDcuMjk0NzcxNCAyOC43MDAwMzUsMTUuMDMyMTY5IHYgMTAuMjE4NzUgaCAyNi44MTI1IHYgMy40MDYyNSBoIC0yNi44MTI1IC0xMC4wNjI1IGMgLTcuNzkyNDU5LDAgLTE0LjYxNTc1ODgsNC42ODM3MTcgLTE2Ljc0OTk5OTgsMTMuNTkzNzUgLTIuNDYxODE5OTgsMTAuMjEyOTY2IC0yLjU3MTAxNTA4LDE2LjU4NjAyMyAwLDI3LjI1IDEuOTA1OTI4Myw3LjkzNzg1MiA2LjQ1NzU0MzIsMTMuNTkzNzQ4IDE0LjI0OTk5OTgsMTMuNTkzNzUgaCA5LjIxODc1IHYgLTEyLjI1IGMgMCwtOC44NDk5MDIgNy42NTcxNDQsLTE2LjY1NjI0OCAxNi43NSwtMTYuNjU2MjUgaCAyNi43ODEyNSBjIDcuNDU0OTUxLDAgMTMuNDA2MjUzLC02LjEzODE2NCAxMy40MDYyNSwtMTMuNjI1IHYgLTI1LjUzMTI1IGMgMCwtNy4yNjYzMzg2IC02LjEyOTk4LC0xMi43MjQ3NzcxIC0xMy40MDYyNSwtMTMuOTM3NDk5NyBDIDY0LjI4MTU0OCwwLjMyNzk0Mzk3IDU5LjUwMjQzOCwtMC4wMjAzNzkwMyA1NC45MTg3ODUsOS4xOTI3NDIxZS00IFogbSAtMTQuNSw4LjIxODc1MDEyNTc5IGMgMi43Njk1NDcsMCA1LjAzMTI1LDIuMjk4NjQ1NiA1LjAzMTI1LDUuMTI0OTk5NiAtMmUtNiwyLjgxNjMzNiAtMi4yNjE3MDMsNS4wOTM3NSAtNS4wMzEyNSw1LjA5Mzc1IC0yLjc3OTQ3NiwtMWUtNiAtNS4wMzEyNSwtMi4yNzc0MTUgLTUuMDMxMjUsLTUuMDkzNzUgLTEwZS03LC0yLjgyNjM1MyAyLjI1MTc3NCwtNS4xMjQ5OTk2IDUuMDMxMjUsLTUuMTI0OTk5NiB6Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI2ZmZDQzYiIgZD0ibSA4NS42Mzc1MzUsMjguNjU3MTY5IHYgMTEuOTA2MjUgYyAwLDkuMjMwNzU1IC03LjgyNTg5NSwxNi45OTk5OTkgLTE2Ljc1LDE3IGggLTI2Ljc4MTI1IGMgLTcuMzM1ODMzLDAgLTEzLjQwNjI0OSw2LjI3ODQ4MyAtMTMuNDA2MjUsMTMuNjI1IHYgMjUuNTMxMjQ3IGMgMCw3LjI2NjM0NCA2LjMxODU4OCwxMS41NDAzMjQgMTMuNDA2MjUsMTMuNjI1MDA0IDguNDg3MzMxLDIuNDk1NjEgMTYuNjI2MjM3LDIuOTQ2NjMgMjYuNzgxMjUsMCA2Ljc1MDE1NSwtMS45NTQzOSAxMy40MDYyNTMsLTUuODg3NjEgMTMuNDA2MjUsLTEzLjYyNTAwNCBWIDg2LjUwMDkxOSBoIC0yNi43ODEyNSB2IC0zLjQwNjI1IGggMjYuNzgxMjUgMTMuNDA2MjU0IGMgNy43OTI0NjEsMCAxMC42OTYyNTEsLTUuNDM1NDA4IDEzLjQwNjI0MSwtMTMuNTkzNzUgMi43OTkzMywtOC4zOTg4ODYgMi42ODAyMiwtMTYuNDc1Nzc2IDAsLTI3LjI1IC0xLjkyNTc4LC03Ljc1NzQ0MSAtNS42MDM4NywtMTMuNTkzNzUgLTEzLjQwNjI0MSwtMTMuNTkzNzUgeiBtIC0xNS4wNjI1LDY0LjY1NjI1IGMgMi43Nzk0NzgsM2UtNiA1LjAzMTI1LDIuMjc3NDE3IDUuMDMxMjUsNS4wOTM3NDcgLTJlLTYsMi44MjYzNTQgLTIuMjUxNzc1LDUuMTI1MDA0IC01LjAzMTI1LDUuMTI1MDA0IC0yLjc2OTU1LDAgLTUuMDMxMjUsLTIuMjk4NjUgLTUuMDMxMjUsLTUuMTI1MDA0IDJlLTYsLTIuODE2MzMgMi4yNjE2OTcsLTUuMDkzNzQ3IDUuMDMxMjUsLTUuMDkzNzQ3IHoiLz4KPC9zdmc+Cg==);
  --jp-icon-r-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjE5NkYzIiBkPSJNNC40IDIuNWMxLjItLjEgMi45LS4zIDQuOS0uMyAyLjUgMCA0LjEuNCA1LjIgMS4zIDEgLjcgMS41IDEuOSAxLjUgMy41IDAgMi0xLjQgMy41LTIuOSA0LjEgMS4yLjQgMS43IDEuNiAyLjIgMyAuNiAxLjkgMSAzLjkgMS4zIDQuNmgtMy44Yy0uMy0uNC0uOC0xLjctMS4yLTMuN3MtMS4yLTIuNi0yLjYtMi42aC0uOXY2LjRINC40VjIuNXptMy43IDYuOWgxLjRjMS45IDAgMi45LS45IDIuOS0yLjNzLTEtMi4zLTIuOC0yLjNjLS43IDAtMS4zIDAtMS42LjJ2NC41aC4xdi0uMXoiLz4KPC9zdmc+Cg==);
  --jp-icon-react: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMTUwIDE1MCA1NDEuOSAyOTUuMyI+CiAgPGcgY2xhc3M9ImpwLWljb24tYnJhbmQyIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzYxREFGQiI+CiAgICA8cGF0aCBkPSJNNjY2LjMgMjk2LjVjMC0zMi41LTQwLjctNjMuMy0xMDMuMS04Mi40IDE0LjQtNjMuNiA4LTExNC4yLTIwLjItMTMwLjQtNi41LTMuOC0xNC4xLTUuNi0yMi40LTUuNnYyMi4zYzQuNiAwIDguMy45IDExLjQgMi42IDEzLjYgNy44IDE5LjUgMzcuNSAxNC45IDc1LjctMS4xIDkuNC0yLjkgMTkuMy01LjEgMjkuNC0xOS42LTQuOC00MS04LjUtNjMuNS0xMC45LTEzLjUtMTguNS0yNy41LTM1LjMtNDEuNi01MCAzMi42LTMwLjMgNjMuMi00Ni45IDg0LTQ2LjlWNzhjLTI3LjUgMC02My41IDE5LjYtOTkuOSA1My42LTM2LjQtMzMuOC03Mi40LTUzLjItOTkuOS01My4ydjIyLjNjMjAuNyAwIDUxLjQgMTYuNSA4NCA0Ni42LTE0IDE0LjctMjggMzEuNC00MS4zIDQ5LjktMjIuNiAyLjQtNDQgNi4xLTYzLjYgMTEtMi4zLTEwLTQtMTkuNy01LjItMjktNC43LTM4LjIgMS4xLTY3LjkgMTQuNi03NS44IDMtMS44IDYuOS0yLjYgMTEuNS0yLjZWNzguNWMtOC40IDAtMTYgMS44LTIyLjYgNS42LTI4LjEgMTYuMi0zNC40IDY2LjctMTkuOSAxMzAuMS02Mi4yIDE5LjItMTAyLjcgNDkuOS0xMDIuNyA4Mi4zIDAgMzIuNSA0MC43IDYzLjMgMTAzLjEgODIuNC0xNC40IDYzLjYtOCAxMTQuMiAyMC4yIDEzMC40IDYuNSAzLjggMTQuMSA1LjYgMjIuNSA1LjYgMjcuNSAwIDYzLjUtMTkuNiA5OS45LTUzLjYgMzYuNCAzMy44IDcyLjQgNTMuMiA5OS45IDUzLjIgOC40IDAgMTYtMS44IDIyLjYtNS42IDI4LjEtMTYuMiAzNC40LTY2LjcgMTkuOS0xMzAuMSA2Mi0xOS4xIDEwMi41LTQ5LjkgMTAyLjUtODIuM3ptLTEzMC4yLTY2LjdjLTMuNyAxMi45LTguMyAyNi4yLTEzLjUgMzkuNS00LjEtOC04LjQtMTYtMTMuMS0yNC00LjYtOC05LjUtMTUuOC0xNC40LTIzLjQgMTQuMiAyLjEgMjcuOSA0LjcgNDEgNy45em0tNDUuOCAxMDYuNWMtNy44IDEzLjUtMTUuOCAyNi4zLTI0LjEgMzguMi0xNC45IDEuMy0zMCAyLTQ1LjIgMi0xNS4xIDAtMzAuMi0uNy00NS0xLjktOC4zLTExLjktMTYuNC0yNC42LTI0LjItMzgtNy42LTEzLjEtMTQuNS0yNi40LTIwLjgtMzkuOCA2LjItMTMuNCAxMy4yLTI2LjggMjAuNy0zOS45IDcuOC0xMy41IDE1LjgtMjYuMyAyNC4xLTM4LjIgMTQuOS0xLjMgMzAtMiA0NS4yLTIgMTUuMSAwIDMwLjIuNyA0NSAxLjkgOC4zIDExLjkgMTYuNCAyNC42IDI0LjIgMzggNy42IDEzLjEgMTQuNSAyNi40IDIwLjggMzkuOC02LjMgMTMuNC0xMy4yIDI2LjgtMjAuNyAzOS45em0zMi4zLTEzYzUuNCAxMy40IDEwIDI2LjggMTMuOCAzOS44LTEzLjEgMy4yLTI2LjkgNS45LTQxLjIgOCA0LjktNy43IDkuOC0xNS42IDE0LjQtMjMuNyA0LjYtOCA4LjktMTYuMSAxMy0yNC4xek00MjEuMiA0MzBjLTkuMy05LjYtMTguNi0yMC4zLTI3LjgtMzIgOSAuNCAxOC4yLjcgMjcuNS43IDkuNCAwIDE4LjctLjIgMjcuOC0uNy05IDExLjctMTguMyAyMi40LTI3LjUgMzJ6bS03NC40LTU4LjljLTE0LjItMi4xLTI3LjktNC43LTQxLTcuOSAzLjctMTIuOSA4LjMtMjYuMiAxMy41LTM5LjUgNC4xIDggOC40IDE2IDEzLjEgMjQgNC43IDggOS41IDE1LjggMTQuNCAyMy40ek00MjAuNyAxNjNjOS4zIDkuNiAxOC42IDIwLjMgMjcuOCAzMi05LS40LTE4LjItLjctMjcuNS0uNy05LjQgMC0xOC43LjItMjcuOC43IDktMTEuNyAxOC4zLTIyLjQgMjcuNS0zMnptLTc0IDU4LjljLTQuOSA3LjctOS44IDE1LjYtMTQuNCAyMy43LTQuNiA4LTguOSAxNi0xMyAyNC01LjQtMTMuNC0xMC0yNi44LTEzLjgtMzkuOCAxMy4xLTMuMSAyNi45LTUuOCA0MS4yLTcuOXptLTkwLjUgMTI1LjJjLTM1LjQtMTUuMS01OC4zLTM0LjktNTguMy01MC42IDAtMTUuNyAyMi45LTM1LjYgNTguMy01MC42IDguNi0zLjcgMTgtNyAyNy43LTEwLjEgNS43IDE5LjYgMTMuMiA0MCAyMi41IDYwLjktOS4yIDIwLjgtMTYuNiA0MS4xLTIyLjIgNjAuNi05LjktMy4xLTE5LjMtNi41LTI4LTEwLjJ6TTMxMCA0OTBjLTEzLjYtNy44LTE5LjUtMzcuNS0xNC45LTc1LjcgMS4xLTkuNCAyLjktMTkuMyA1LjEtMjkuNCAxOS42IDQuOCA0MSA4LjUgNjMuNSAxMC45IDEzLjUgMTguNSAyNy41IDM1LjMgNDEuNiA1MC0zMi42IDMwLjMtNjMuMiA0Ni45LTg0IDQ2LjktNC41LS4xLTguMy0xLTExLjMtMi43em0yMzcuMi03Ni4yYzQuNyAzOC4yLTEuMSA2Ny45LTE0LjYgNzUuOC0zIDEuOC02LjkgMi42LTExLjUgMi42LTIwLjcgMC01MS40LTE2LjUtODQtNDYuNiAxNC0xNC43IDI4LTMxLjQgNDEuMy00OS45IDIyLjYtMi40IDQ0LTYuMSA2My42LTExIDIuMyAxMC4xIDQuMSAxOS44IDUuMiAyOS4xem0zOC41LTY2LjdjLTguNiAzLjctMTggNy0yNy43IDEwLjEtNS43LTE5LjYtMTMuMi00MC0yMi41LTYwLjkgOS4yLTIwLjggMTYuNi00MS4xIDIyLjItNjAuNiA5LjkgMy4xIDE5LjMgNi41IDI4LjEgMTAuMiAzNS40IDE1LjEgNTguMyAzNC45IDU4LjMgNTAuNi0uMSAxNS43LTIzIDM1LjYtNTguNCA1MC42ek0zMjAuOCA3OC40eiIvPgogICAgPGNpcmNsZSBjeD0iNDIwLjkiIGN5PSIyOTYuNSIgcj0iNDUuNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-redo: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIGhlaWdodD0iMjQiIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjE2Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCBkPSJNMCAwaDI0djI0SDB6IiBmaWxsPSJub25lIi8+PHBhdGggZD0iTTE4LjQgMTAuNkMxNi41NSA4Ljk5IDE0LjE1IDggMTEuNSA4Yy00LjY1IDAtOC41OCAzLjAzLTkuOTYgNy4yMkwzLjkgMTZjMS4wNS0zLjE5IDQuMDUtNS41IDcuNi01LjUgMS45NSAwIDMuNzMuNzIgNS4xMiAxLjg4TDEzIDE2aDlWN2wtMy42IDMuNnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-refresh: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTkgMTMuNWMtMi40OSAwLTQuNS0yLjAxLTQuNS00LjVTNi41MSA0LjUgOSA0LjVjMS4yNCAwIDIuMzYuNTIgMy4xNyAxLjMzTDEwIDhoNVYzbC0xLjc2IDEuNzZDMTIuMTUgMy42OCAxMC42NiAzIDkgMyA1LjY5IDMgMy4wMSA1LjY5IDMuMDEgOVM1LjY5IDE1IDkgMTVjMi45NyAwIDUuNDMtMi4xNiA1LjktNWgtMS41MmMtLjQ2IDItMi4yNCAzLjUtNC4zOCAzLjV6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-regex: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi1hY2NlbnQyIiBmaWxsPSIjRkZGIj4KICAgIDxjaXJjbGUgY2xhc3M9InN0MiIgY3g9IjUuNSIgY3k9IjE0LjUiIHI9IjEuNSIvPgogICAgPHJlY3QgeD0iMTIiIHk9IjQiIGNsYXNzPSJzdDIiIHdpZHRoPSIxIiBoZWlnaHQ9IjgiLz4KICAgIDxyZWN0IHg9IjguNSIgeT0iNy41IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjg2NiAtMC41IDAuNSAwLjg2NiAtMi4zMjU1IDcuMzIxOSkiIGNsYXNzPSJzdDIiIHdpZHRoPSI4IiBoZWlnaHQ9IjEiLz4KICAgIDxyZWN0IHg9IjEyIiB5PSI0IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjUgLTAuODY2IDAuODY2IDAuNSAtMC42Nzc5IDE0LjgyNTIpIiBjbGFzcz0ic3QyIiB3aWR0aD0iMSIgaGVpZ2h0PSI4Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-run: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTggNXYxNGwxMS03eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-running: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMjU2IDhDMTE5IDggOCAxMTkgOCAyNTZzMTExIDI0OCAyNDggMjQ4IDI0OC0xMTEgMjQ4LTI0OFMzOTMgOCAyNTYgOHptOTYgMzI4YzAgOC44LTcuMiAxNi0xNiAxNkgxNzZjLTguOCAwLTE2LTcuMi0xNi0xNlYxNzZjMC04LjggNy4yLTE2IDE2LTE2aDE2MGM4LjggMCAxNiA3LjIgMTYgMTZ2MTYweiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-save: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE3IDNINWMtMS4xMSAwLTIgLjktMiAydjE0YzAgMS4xLjg5IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjdsLTQtNHptLTUgMTZjLTEuNjYgMC0zLTEuMzQtMy0zczEuMzQtMyAzLTMgMyAxLjM0IDMgMy0xLjM0IDMtMyAzem0zLTEwSDVWNWgxMHY0eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-search: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjEsMTAuOWgtMC43bC0wLjItMC4yYzAuOC0wLjksMS4zLTIuMiwxLjMtMy41YzAtMy0yLjQtNS40LTUuNC01LjRTMS44LDQuMiwxLjgsNy4xczIuNCw1LjQsNS40LDUuNCBjMS4zLDAsMi41LTAuNSwzLjUtMS4zbDAuMiwwLjJ2MC43bDQuMSw0LjFsMS4yLTEuMkwxMi4xLDEwLjl6IE03LjEsMTAuOWMtMi4xLDAtMy43LTEuNy0zLjctMy43czEuNy0zLjcsMy43LTMuN3MzLjcsMS43LDMuNywzLjcgUzkuMiwxMC45LDcuMSwxMC45eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-settings: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuNDMgMTIuOThjLjA0LS4zMi4wNy0uNjQuMDctLjk4cy0uMDMtLjY2LS4wNy0uOThsMi4xMS0xLjY1Yy4xOS0uMTUuMjQtLjQyLjEyLS42NGwtMi0zLjQ2Yy0uMTItLjIyLS4zOS0uMy0uNjEtLjIybC0yLjQ5IDFjLS41Mi0uNC0xLjA4LS43My0xLjY5LS45OGwtLjM4LTIuNjVBLjQ4OC40ODggMCAwMDE0IDJoLTRjLS4yNSAwLS40Ni4xOC0uNDkuNDJsLS4zOCAyLjY1Yy0uNjEuMjUtMS4xNy41OS0xLjY5Ljk4bC0yLjQ5LTFjLS4yMy0uMDktLjQ5IDAtLjYxLjIybC0yIDMuNDZjLS4xMy4yMi0uMDcuNDkuMTIuNjRsMi4xMSAxLjY1Yy0uMDQuMzItLjA3LjY1LS4wNy45OHMuMDMuNjYuMDcuOThsLTIuMTEgMS42NWMtLjE5LjE1LS4yNC40Mi0uMTIuNjRsMiAzLjQ2Yy4xMi4yMi4zOS4zLjYxLjIybDIuNDktMWMuNTIuNCAxLjA4LjczIDEuNjkuOThsLjM4IDIuNjVjLjAzLjI0LjI0LjQyLjQ5LjQyaDRjLjI1IDAgLjQ2LS4xOC40OS0uNDJsLjM4LTIuNjVjLjYxLS4yNSAxLjE3LS41OSAxLjY5LS45OGwyLjQ5IDFjLjIzLjA5LjQ5IDAgLjYxLS4yMmwyLTMuNDZjLjEyLS4yMi4wNy0uNDktLjEyLS42NGwtMi4xMS0xLjY1ek0xMiAxNS41Yy0xLjkzIDAtMy41LTEuNTctMy41LTMuNXMxLjU3LTMuNSAzLjUtMy41IDMuNSAxLjU3IDMuNSAzLjUtMS41NyAzLjUtMy41IDMuNXoiLz4KPC9zdmc+Cg==);
  --jp-icon-share: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTSAxOCAyIEMgMTYuMzU0OTkgMiAxNSAzLjM1NDk5MDQgMTUgNSBDIDE1IDUuMTkwOTUyOSAxNS4wMjE3OTEgNS4zNzcxMjI0IDE1LjA1NjY0MSA1LjU1ODU5MzggTCA3LjkyMTg3NSA5LjcyMDcwMzEgQyA3LjM5ODUzOTkgOS4yNzc4NTM5IDYuNzMyMDc3MSA5IDYgOSBDIDQuMzU0OTkwNCA5IDMgMTAuMzU0OTkgMyAxMiBDIDMgMTMuNjQ1MDEgNC4zNTQ5OTA0IDE1IDYgMTUgQyA2LjczMjA3NzEgMTUgNy4zOTg1Mzk5IDE0LjcyMjE0NiA3LjkyMTg3NSAxNC4yNzkyOTcgTCAxNS4wNTY2NDEgMTguNDM5NDUzIEMgMTUuMDIxNTU1IDE4LjYyMTUxNCAxNSAxOC44MDgzODYgMTUgMTkgQyAxNSAyMC42NDUwMSAxNi4zNTQ5OSAyMiAxOCAyMiBDIDE5LjY0NTAxIDIyIDIxIDIwLjY0NTAxIDIxIDE5IEMgMjEgMTcuMzU0OTkgMTkuNjQ1MDEgMTYgMTggMTYgQyAxNy4yNjc0OCAxNiAxNi42MDE1OTMgMTYuMjc5MzI4IDE2LjA3ODEyNSAxNi43MjI2NTYgTCA4Ljk0MzM1OTQgMTIuNTU4NTk0IEMgOC45NzgyMDk1IDEyLjM3NzEyMiA5IDEyLjE5MDk1MyA5IDEyIEMgOSAxMS44MDkwNDcgOC45NzgyMDk1IDExLjYyMjg3OCA4Ljk0MzM1OTQgMTEuNDQxNDA2IEwgMTYuMDc4MTI1IDcuMjc5Mjk2OSBDIDE2LjYwMTQ2IDcuNzIyMTQ2MSAxNy4yNjc5MjMgOCAxOCA4IEMgMTkuNjQ1MDEgOCAyMSA2LjY0NTAwOTYgMjEgNSBDIDIxIDMuMzU0OTkwNCAxOS42NDUwMSAyIDE4IDIgeiBNIDE4IDQgQyAxOC41NjQxMjkgNCAxOSA0LjQzNTg3MDYgMTkgNSBDIDE5IDUuNTY0MTI5NCAxOC41NjQxMjkgNiAxOCA2IEMgMTcuNDM1ODcxIDYgMTcgNS41NjQxMjk0IDE3IDUgQyAxNyA0LjQzNTg3MDYgMTcuNDM1ODcxIDQgMTggNCB6IE0gNiAxMSBDIDYuNTY0MTI5NCAxMSA3IDExLjQzNTg3MSA3IDEyIEMgNyAxMi41NjQxMjkgNi41NjQxMjk0IDEzIDYgMTMgQyA1LjQzNTg3MDYgMTMgNSAxMi41NjQxMjkgNSAxMiBDIDUgMTEuNDM1ODcxIDUuNDM1ODcwNiAxMSA2IDExIHogTSAxOCAxOCBDIDE4LjU2NDEyOSAxOCAxOSAxOC40MzU4NzEgMTkgMTkgQyAxOSAxOS41NjQxMjkgMTguNTY0MTI5IDIwIDE4IDIwIEMgMTcuNDM1ODcxIDIwIDE3IDE5LjU2NDEyOSAxNyAxOSBDIDE3IDE4LjQzNTg3MSAxNy40MzU4NzEgMTggMTggMTggeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-spreadsheet: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNENBRjUwIiBkPSJNMi4yIDIuMnYxNy42aDE3LjZWMi4ySDIuMnptMTUuNCA3LjdoLTUuNVY0LjRoNS41djUuNXpNOS45IDQuNHY1LjVINC40VjQuNGg1LjV6bS01LjUgNy43aDUuNXY1LjVINC40di01LjV6bTcuNyA1LjV2LTUuNWg1LjV2NS41aC01LjV6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-stop: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik02IDZoMTJ2MTJINnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tab: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIxIDNIM2MtMS4xIDAtMiAuOS0yIDJ2MTRjMCAxLjEuOSAyIDIgMmgxOGMxLjEgMCAyLS45IDItMlY1YzAtMS4xLS45LTItMi0yem0wIDE2SDNWNWgxMHY0aDh2MTB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-table-rows: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik0yMSw4SDNWNGgxOFY4eiBNMjEsMTBIM3Y0aDE4VjEweiBNMjEsMTZIM3Y0aDE4VjE2eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-tag: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjgiIGhlaWdodD0iMjgiIHZpZXdCb3g9IjAgMCA0MyAyOCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CgkJPHBhdGggZD0iTTI4LjgzMzIgMTIuMzM0TDMyLjk5OTggMTYuNTAwN0wzNy4xNjY1IDEyLjMzNEgyOC44MzMyWiIvPgoJCTxwYXRoIGQ9Ik0xNi4yMDk1IDIxLjYxMDRDMTUuNjg3MyAyMi4xMjk5IDE0Ljg0NDMgMjIuMTI5OSAxNC4zMjQ4IDIxLjYxMDRMNi45ODI5IDE0LjcyNDVDNi41NzI0IDE0LjMzOTQgNi4wODMxMyAxMy42MDk4IDYuMDQ3ODYgMTMuMDQ4MkM1Ljk1MzQ3IDExLjUyODggNi4wMjAwMiA4LjYxOTQ0IDYuMDY2MjEgNy4wNzY5NUM2LjA4MjgxIDYuNTE0NzcgNi41NTU0OCA2LjA0MzQ3IDcuMTE4MDQgNi4wMzA1NUM5LjA4ODYzIDUuOTg0NzMgMTMuMjYzOCA1LjkzNTc5IDEzLjY1MTggNi4zMjQyNUwyMS43MzY5IDEzLjYzOUMyMi4yNTYgMTQuMTU4NSAyMS43ODUxIDE1LjQ3MjQgMjEuMjYyIDE1Ljk5NDZMMTYuMjA5NSAyMS42MTA0Wk05Ljc3NTg1IDguMjY1QzkuMzM1NTEgNy44MjU2NiA4LjYyMzUxIDcuODI1NjYgOC4xODI4IDguMjY1QzcuNzQzNDYgOC43MDU3MSA3Ljc0MzQ2IDkuNDE3MzMgOC4xODI4IDkuODU2NjdDOC42MjM4MiAxMC4yOTY0IDkuMzM1ODIgMTAuMjk2NCA5Ljc3NTg1IDkuODU2NjdDMTAuMjE1NiA5LjQxNzMzIDEwLjIxNTYgOC43MDUzMyA5Ljc3NTg1IDguMjY1WiIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-terminal: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0IiA+CiAgICA8cmVjdCBjbGFzcz0ianAtdGVybWluYWwtaWNvbi1iYWNrZ3JvdW5kLWNvbG9yIGpwLWljb24tc2VsZWN0YWJsZSIgd2lkdGg9IjIwIiBoZWlnaHQ9IjIwIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgyIDIpIiBmaWxsPSIjMzMzMzMzIi8+CiAgICA8cGF0aCBjbGFzcz0ianAtdGVybWluYWwtaWNvbi1jb2xvciBqcC1pY29uLXNlbGVjdGFibGUtaW52ZXJzZSIgZD0iTTUuMDU2NjQgOC43NjE3MkM1LjA1NjY0IDguNTk3NjYgNS4wMzEyNSA4LjQ1MzEyIDQuOTgwNDcgOC4zMjgxMkM0LjkzMzU5IDguMTk5MjIgNC44NTU0NyA4LjA4MjAzIDQuNzQ2MDkgNy45NzY1NkM0LjY0MDYyIDcuODcxMDkgNC41IDcuNzc1MzkgNC4zMjQyMiA3LjY4OTQ1QzQuMTUyMzQgNy41OTk2MSAzLjk0MzM2IDcuNTExNzIgMy42OTcyNyA3LjQyNTc4QzMuMzAyNzMgNy4yODUxNiAyLjk0MzM2IDcuMTM2NzIgMi42MTkxNCA2Ljk4MDQ3QzIuMjk0OTIgNi44MjQyMiAyLjAxNzU4IDYuNjQyNTggMS43ODcxMSA2LjQzNTU1QzEuNTYwNTUgNi4yMjg1MiAxLjM4NDc3IDUuOTg4MjggMS4yNTk3NyA1LjcxNDg0QzEuMTM0NzcgNS40Mzc1IDEuMDcyMjcgNS4xMDkzOCAxLjA3MjI3IDQuNzMwNDdDMS4wNzIyNyA0LjM5ODQ0IDEuMTI4OTEgNC4wOTU3IDEuMjQyMTkgMy44MjIyN0MxLjM1NTQ3IDMuNTQ0OTIgMS41MTU2MiAzLjMwNDY5IDEuNzIyNjYgMy4xMDE1NkMxLjkyOTY5IDIuODk4NDQgMi4xNzk2OSAyLjczNDM3IDIuNDcyNjYgMi42MDkzOEMyLjc2NTYyIDIuNDg0MzggMy4wOTE4IDIuNDA0MyAzLjQ1MTE3IDIuMzY5MTRWMS4xMDkzOEg0LjM4ODY3VjIuMzgwODZDNC43NDAyMyAyLjQyNzczIDUuMDU2NjQgMi41MjM0NCA1LjMzNzg5IDIuNjY3OTdDNS42MTkxNCAyLjgxMjUgNS44NTc0MiAzLjAwMTk1IDYuMDUyNzMgMy4yMzYzM0M2LjI1MTk1IDMuNDY2OCA2LjQwNDMgMy43NDAyMyA2LjUwOTc3IDQuMDU2NjRDNi42MTkxNCA0LjM2OTE0IDYuNjczODMgNC43MjA3IDYuNjczODMgNS4xMTEzM0g1LjA0NDkyQzUuMDQ0OTIgNC42Mzg2NyA0LjkzNzUgNC4yODEyNSA0LjcyMjY2IDQuMDM5MDZDNC41MDc4MSAzLjc5Mjk3IDQuMjE2OCAzLjY2OTkyIDMuODQ5NjEgMy42Njk5MkMzLjY1MDM5IDMuNjY5OTIgMy40NzY1NiAzLjY5NzI3IDMuMzI4MTIgMy43NTE5NUMzLjE4MzU5IDMuODAyNzMgMy4wNjQ0NSAzLjg3Njk1IDIuOTcwNyAzLjk3NDYxQzIuODc2OTUgNC4wNjgzNiAyLjgwNjY0IDQuMTc5NjkgMi43NTk3NyA0LjMwODU5QzIuNzE2OCA0LjQzNzUgMi42OTUzMSA0LjU3ODEyIDIuNjk1MzEgNC43MzA0N0MyLjY5NTMxIDQuODgyODEgMi43MTY4IDUuMDE5NTMgMi43NTk3NyA1LjE0MDYyQzIuODA2NjQgNS4yNTc4MSAyLjg4MjgxIDUuMzY3MTkgMi45ODgyOCA1LjQ2ODc1QzMuMDk3NjYgNS41NzAzMSAzLjI0MDIzIDUuNjY3OTcgMy40MTYwMiA1Ljc2MTcyQzMuNTkxOCA1Ljg1MTU2IDMuODEwNTUgNS45NDMzNiA0LjA3MjI3IDYuMDM3MTFDNC40NjY4IDYuMTg1NTUgNC44MjQyMiA2LjMzOTg0IDUuMTQ0NTMgNi41QzUuNDY0ODQgNi42NTYyNSA1LjczODI4IDYuODM5ODQgNS45NjQ4NCA3LjA1MDc4QzYuMTk1MzEgNy4yNTc4MSA2LjM3MTA5IDcuNSA2LjQ5MjE5IDcuNzc3MzRDNi42MTcxOSA4LjA1MDc4IDYuNjc5NjkgOC4zNzUgNi42Nzk2OSA4Ljc1QzYuNjc5NjkgOS4wOTM3NSA2LjYyMzA1IDkuNDA0MyA2LjUwOTc3IDkuNjgxNjRDNi4zOTY0OCA5Ljk1NTA4IDYuMjM0MzggMTAuMTkxNCA2LjAyMzQ0IDEwLjM5MDZDNS44MTI1IDEwLjU4OTggNS41NTg1OSAxMC43NSA1LjI2MTcyIDEwLjg3MTFDNC45NjQ4NCAxMC45ODgzIDQuNjMyODEgMTEuMDY0NSA0LjI2NTYyIDExLjA5OTZWMTIuMjQ4SDMuMzMzOThWMTEuMDk5NkMzLjAwMTk1IDExLjA2ODQgMi42Nzk2OSAxMC45OTYxIDIuMzY3MTkgMTAuODgyOEMyLjA1NDY5IDEwLjc2NTYgMS43NzczNCAxMC41OTc3IDEuNTM1MTYgMTAuMzc4OUMxLjI5Njg4IDEwLjE2MDIgMS4xMDU0NyA5Ljg4NDc3IDAuOTYwOTM4IDkuNTUyNzNDMC44MTY0MDYgOS4yMTY4IDAuNzQ0MTQxIDguODE0NDUgMC43NDQxNDEgOC4zNDU3SDIuMzc4OTFDMi4zNzg5MSA4LjYyNjk1IDIuNDE5OTIgOC44NjMyOCAyLjUwMTk1IDkuMDU0NjlDMi41ODM5OCA5LjI0MjE5IDIuNjg5NDUgOS4zOTI1OCAyLjgxODM2IDkuNTA1ODZDMi45NTExNyA5LjYxNTIzIDMuMTAxNTYgOS42OTMzNiAzLjI2OTUzIDkuNzQwMjNDMy40Mzc1IDkuNzg3MTEgMy42MDkzOCA5LjgxMDU1IDMuNzg1MTYgOS44MTA1NUM0LjIwMzEyIDkuODEwNTUgNC41MTk1MyA5LjcxMjg5IDQuNzM0MzggOS41MTc1OEM0Ljk0OTIyIDkuMzIyMjcgNS4wNTY2NCA5LjA3MDMxIDUuMDU2NjQgOC43NjE3MlpNMTMuNDE4IDEyLjI3MTVIOC4wNzQyMlYxMUgxMy40MThWMTIuMjcxNVoiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDMuOTUyNjQgNikiIGZpbGw9IndoaXRlIi8+Cjwvc3ZnPgo=);
  --jp-icon-text-editor: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtdGV4dC1lZGl0b3ItaWNvbi1jb2xvciBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiIGQ9Ik0xNSAxNUgzdjJoMTJ2LTJ6bTAtOEgzdjJoMTJWN3pNMyAxM2gxOHYtMkgzdjJ6bTAgOGgxOHYtMkgzdjJ6TTMgM3YyaDE4VjNIM3oiLz4KPC9zdmc+Cg==);
  --jp-icon-toc: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxwYXRoIGQ9Ik03LDVIMjFWN0g3VjVNNywxM1YxMUgyMVYxM0g3TTQsNC41QTEuNSwxLjUgMCAwLDEgNS41LDZBMS41LDEuNSAwIDAsMSA0LDcuNUExLjUsMS41IDAgMCwxIDIuNSw2QTEuNSwxLjUgMCAwLDEgNCw0LjVNNCwxMC41QTEuNSwxLjUgMCAwLDEgNS41LDEyQTEuNSwxLjUgMCAwLDEgNCwxMy41QTEuNSwxLjUgMCAwLDEgMi41LDEyQTEuNSwxLjUgMCAwLDEgNCwxMC41TTcsMTlWMTdIMjFWMTlIN000LDE2LjVBMS41LDEuNSAwIDAsMSA1LjUsMThBMS41LDEuNSAwIDAsMSA0LDE5LjVBMS41LDEuNSAwIDAsMSAyLjUsMThBMS41LDEuNSAwIDAsMSA0LDE2LjVaIiAvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tree-view: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik0yMiAxMVYzaC03djNIOVYzSDJ2OGg3VjhoMnYxMGg0djNoN3YtOGgtN3YzaC0yVjhoMnYzeiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMiAxNy4xODQ0IDIuOTY5NjggMTQuMzAzMiAxLjg2MDk0IDExLjQ0MDlaIi8+CiAgICA8cGF0aCBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiMzMzMzMzMiIHN0cm9rZT0iIzMzMzMzMyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOCA5Ljg2NzE5KSIgZD0iTTIuODYwMTUgNC44NjUzNUwwLjcyNjU0OSAyLjk5OTU5TDAgMy42MzA0NUwyLjg2MDE1IDYuMTMxNTdMOCAwLjYzMDg3Mkw3LjI3ODU3IDBMMi44NjAxNSA0Ljg2NTM1WiIvPgo8L3N2Zz4K);
  --jp-icon-undo: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjUgOGMtMi42NSAwLTUuMDUuOTktNi45IDIuNkwyIDd2OWg5bC0zLjYyLTMuNjJjMS4zOS0xLjE2IDMuMTYtMS44OCA1LjEyLTEuODggMy41NCAwIDYuNTUgMi4zMSA3LjYgNS41bDIuMzctLjc4QzIxLjA4IDExLjAzIDE3LjE1IDggMTIuNSA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-user: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE2IDdhNCA0IDAgMTEtOCAwIDQgNCAwIDAxOCAwek0xMiAxNGE3IDcgMCAwMC03IDdoMTRhNyA3IDAgMDAtNy03eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-users: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMjQiIGhlaWdodD0iMjQiIHZlcnNpb249IjEuMSIgdmlld0JveD0iMCAwIDM2IDI0IiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciPgogPGcgY2xhc3M9ImpwLWljb24zIiB0cmFuc2Zvcm09Im1hdHJpeCgxLjczMjcgMCAwIDEuNzMyNyAtMy42MjgyIC4wOTk1NzcpIiBmaWxsPSIjNjE2MTYxIj4KICA8cGF0aCB0cmFuc2Zvcm09Im1hdHJpeCgxLjUsMCwwLDEuNSwwLC02KSIgZD0ibTEyLjE4NiA3LjUwOThjLTEuMDUzNSAwLTEuOTc1NyAwLjU2NjUtMi40Nzg1IDEuNDEwMiAwLjc1MDYxIDAuMzEyNzcgMS4zOTc0IDAuODI2NDggMS44NzMgMS40NzI3aDMuNDg2M2MwLTEuNTkyLTEuMjg4OS0yLjg4MjgtMi44ODA5LTIuODgyOHoiLz4KICA8cGF0aCBkPSJtMjAuNDY1IDIuMzg5NWEyLjE4ODUgMi4xODg1IDAgMCAxLTIuMTg4NCAyLjE4ODUgMi4xODg1IDIuMTg4NSAwIDAgMS0yLjE4ODUtMi4xODg1IDIuMTg4NSAyLjE4ODUgMCAwIDEgMi4xODg1LTIuMTg4NSAyLjE4ODUgMi4xODg1IDAgMCAxIDIuMTg4NCAyLjE4ODV6Ii8+CiAgPHBhdGggdHJhbnNmb3JtPSJtYXRyaXgoMS41LDAsMCwxLjUsMCwtNikiIGQ9Im0zLjU4OTggOC40MjE5Yy0xLjExMjYgMC0yLjAxMzcgMC45MDExMS0yLjAxMzcgMi4wMTM3aDIuODE0NWMwLjI2Nzk3LTAuMzczMDkgMC41OTA3LTAuNzA0MzUgMC45NTg5OC0wLjk3ODUyLTAuMzQ0MzMtMC42MTY4OC0xLjAwMzEtMS4wMzUyLTEuNzU5OC0xLjAzNTJ6Ii8+CiAgPHBhdGggZD0ibTYuOTE1NCA0LjYyM2ExLjUyOTQgMS41Mjk0IDAgMCAxLTEuNTI5NCAxLjUyOTQgMS41Mjk0IDEuNTI5NCAwIDAgMS0xLjUyOTQtMS41Mjk0IDEuNTI5NCAxLjUyOTQgMCAwIDEgMS41Mjk0LTEuNTI5NCAxLjUyOTQgMS41Mjk0IDAgMCAxIDEuNTI5NCAxLjUyOTR6Ii8+CiAgPHBhdGggZD0ibTYuMTM1IDEzLjUzNWMwLTMuMjM5MiAyLjYyNTktNS44NjUgNS44NjUtNS44NjUgMy4yMzkyIDAgNS44NjUgMi42MjU5IDUuODY1IDUuODY1eiIvPgogIDxjaXJjbGUgY3g9IjEyIiBjeT0iMy43Njg1IiByPSIyLjk2ODUiLz4KIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-vega: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbjEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjEyMTIxIj4KICAgIDxwYXRoIGQ9Ik0xMC42IDUuNGwyLjItMy4ySDIuMnY3LjNsNC02LjZ6Ii8+CiAgICA8cGF0aCBkPSJNMTUuOCAyLjJsLTQuNCA2LjZMNyA2LjNsLTQuOCA4djUuNWgxNy42VjIuMmgtNHptLTcgMTUuNEg1LjV2LTQuNGgzLjN2NC40em00LjQgMEg5LjhWOS44aDMuNHY3Ljh6bTQuNCAwaC0zLjRWNi41aDMuNHYxMS4xeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-word: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KIDxnIGNsYXNzPSJqcC1pY29uMiIgZmlsbD0iIzQxNDE0MSI+CiAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiA8L2c+CiA8ZyBjbGFzcz0ianAtaWNvbi1hY2NlbnQyIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSguNDMgLjA0MDEpIiBmaWxsPSIjZmZmIj4KICA8cGF0aCBkPSJtNC4xNCA4Ljc2cTAuMDY4Mi0xLjg5IDIuNDItMS44OSAxLjE2IDAgMS42OCAwLjQyIDAuNTY3IDAuNDEgMC41NjcgMS4xNnYzLjQ3cTAgMC40NjIgMC41MTQgMC40NjIgMC4xMDMgMCAwLjItMC4wMjMxdjAuNzE0cS0wLjM5OSAwLjEwMy0wLjY1MSAwLjEwMy0wLjQ1MiAwLTAuNjkzLTAuMjItMC4yMzEtMC4yLTAuMjg0LTAuNjYyLTAuOTU2IDAuODcyLTIgMC44NzItMC45MDMgMC0xLjQ3LTAuNDcyLTAuNTI1LTAuNDcyLTAuNTI1LTEuMjYgMC0wLjI2MiAwLjA0NTItMC40NzIgMC4wNTY3LTAuMjIgMC4xMTYtMC4zNzggMC4wNjgyLTAuMTY4IDAuMjMxLTAuMzA0IDAuMTU4LTAuMTQ3IDAuMjYyLTAuMjQyIDAuMTE2LTAuMDkxNCAwLjM2OC0wLjE2OCAwLjI2Mi0wLjA5MTQgMC4zOTktMC4xMjYgMC4xMzYtMC4wNDUyIDAuNDcyLTAuMTAzIDAuMzM2LTAuMDU3OCAwLjUwNC0wLjA3OTggMC4xNTgtMC4wMjMxIDAuNTY3LTAuMDc5OCAwLjU1Ni0wLjA2ODIgMC43NzctMC4yMjEgMC4yMi0wLjE1MiAwLjIyLTAuNDQxdi0wLjI1MnEwLTAuNDMtMC4zNTctMC42NjItMC4zMzYtMC4yMzEtMC45NzYtMC4yMzEtMC42NjIgMC0wLjk5OCAwLjI2Mi0wLjMzNiAwLjI1Mi0wLjM5OSAwLjc5OHptMS44OSAzLjY4cTAuNzg4IDAgMS4yNi0wLjQxIDAuNTA0LTAuNDIgMC41MDQtMC45MDN2LTEuMDVxLTAuMjg0IDAuMTM2LTAuODYxIDAuMjMxLTAuNTY3IDAuMDkxNC0wLjk4NyAwLjE1OC0wLjQyIDAuMDY4Mi0wLjc2NiAwLjMyNi0wLjMzNiAwLjI1Mi0wLjMzNiAwLjcwNHQwLjMwNCAwLjcwNCAwLjg2MSAwLjI1MnoiIHN0cm9rZS13aWR0aD0iMS4wNSIvPgogIDxwYXRoIGQ9Im0xMCA0LjU2aDAuOTQ1djMuMTVxMC42NTEtMC45NzYgMS44OS0wLjk3NiAxLjE2IDAgMS44OSAwLjg0IDAuNjgyIDAuODQgMC42ODIgMi4zMSAwIDEuNDctMC43MDQgMi40Mi0wLjcwNCAwLjg4Mi0xLjg5IDAuODgyLTEuMjYgMC0xLjg5LTEuMDJ2MC43NjZoLTAuODV6bTIuNjIgMy4wNHEtMC43NDYgMC0xLjE2IDAuNjQtMC40NTIgMC42My0wLjQ1MiAxLjY4IDAgMS4wNSAwLjQ1MiAxLjY4dDEuMTYgMC42M3EwLjc3NyAwIDEuMjYtMC42MyAwLjQ5NC0wLjY0IDAuNDk0LTEuNjggMC0xLjA1LTAuNDcyLTEuNjgtMC40NjItMC42NC0xLjI2LTAuNjR6IiBzdHJva2Utd2lkdGg9IjEuMDUiLz4KICA8cGF0aCBkPSJtMi43MyAxNS44IDEzLjYgMC4wMDgxYzAuMDA2OSAwIDAtMi42IDAtMi42IDAtMC4wMDc4LTEuMTUgMC0xLjE1IDAtMC4wMDY5IDAtMC4wMDgzIDEuNS0wLjAwODMgMS41LTJlLTMgLTAuMDAxNC0xMS4zLTAuMDAxNC0xMS4zLTAuMDAxNGwtMC4wMDU5Mi0xLjVjMC0wLjAwNzgtMS4xNyAwLjAwMTMtMS4xNyAwLjAwMTN6IiBzdHJva2Utd2lkdGg9Ii45NzUiLz4KIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-yaml: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1jb250cmFzdDIganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjRDgxQjYwIj4KICAgIDxwYXRoIGQ9Ik03LjIgMTguNnYtNS40TDMgNS42aDMuM2wxLjQgMy4xYy4zLjkuNiAxLjYgMSAyLjUuMy0uOC42LTEuNiAxLTIuNWwxLjQtMy4xaDMuNGwtNC40IDcuNnY1LjVsLTIuOS0uMXoiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxNi41IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxMSIgcj0iMi4xIi8+CiAgPC9nPgo8L3N2Zz4K);
}

/* Icon CSS class declarations */

.jp-AddAboveIcon {
  background-image: var(--jp-icon-add-above);
}

.jp-AddBelowIcon {
  background-image: var(--jp-icon-add-below);
}

.jp-AddIcon {
  background-image: var(--jp-icon-add);
}

.jp-BellIcon {
  background-image: var(--jp-icon-bell);
}

.jp-BugDotIcon {
  background-image: var(--jp-icon-bug-dot);
}

.jp-BugIcon {
  background-image: var(--jp-icon-bug);
}

.jp-BuildIcon {
  background-image: var(--jp-icon-build);
}

.jp-CaretDownEmptyIcon {
  background-image: var(--jp-icon-caret-down-empty);
}

.jp-CaretDownEmptyThinIcon {
  background-image: var(--jp-icon-caret-down-empty-thin);
}

.jp-CaretDownIcon {
  background-image: var(--jp-icon-caret-down);
}

.jp-CaretLeftIcon {
  background-image: var(--jp-icon-caret-left);
}

.jp-CaretRightIcon {
  background-image: var(--jp-icon-caret-right);
}

.jp-CaretUpEmptyThinIcon {
  background-image: var(--jp-icon-caret-up-empty-thin);
}

.jp-CaretUpIcon {
  background-image: var(--jp-icon-caret-up);
}

.jp-CaseSensitiveIcon {
  background-image: var(--jp-icon-case-sensitive);
}

.jp-CheckIcon {
  background-image: var(--jp-icon-check);
}

.jp-CircleEmptyIcon {
  background-image: var(--jp-icon-circle-empty);
}

.jp-CircleIcon {
  background-image: var(--jp-icon-circle);
}

.jp-ClearIcon {
  background-image: var(--jp-icon-clear);
}

.jp-CloseIcon {
  background-image: var(--jp-icon-close);
}

.jp-CodeCheckIcon {
  background-image: var(--jp-icon-code-check);
}

.jp-CodeIcon {
  background-image: var(--jp-icon-code);
}

.jp-CollapseAllIcon {
  background-image: var(--jp-icon-collapse-all);
}

.jp-ConsoleIcon {
  background-image: var(--jp-icon-console);
}

.jp-CopyIcon {
  background-image: var(--jp-icon-copy);
}

.jp-CopyrightIcon {
  background-image: var(--jp-icon-copyright);
}

.jp-CutIcon {
  background-image: var(--jp-icon-cut);
}

.jp-DeleteIcon {
  background-image: var(--jp-icon-delete);
}

.jp-DownloadIcon {
  background-image: var(--jp-icon-download);
}

.jp-DuplicateIcon {
  background-image: var(--jp-icon-duplicate);
}

.jp-EditIcon {
  background-image: var(--jp-icon-edit);
}

.jp-EllipsesIcon {
  background-image: var(--jp-icon-ellipses);
}

.jp-ErrorIcon {
  background-image: var(--jp-icon-error);
}

.jp-ExpandAllIcon {
  background-image: var(--jp-icon-expand-all);
}

.jp-ExtensionIcon {
  background-image: var(--jp-icon-extension);
}

.jp-FastForwardIcon {
  background-image: var(--jp-icon-fast-forward);
}

.jp-FileIcon {
  background-image: var(--jp-icon-file);
}

.jp-FileUploadIcon {
  background-image: var(--jp-icon-file-upload);
}

.jp-FilterDotIcon {
  background-image: var(--jp-icon-filter-dot);
}

.jp-FilterIcon {
  background-image: var(--jp-icon-filter);
}

.jp-FilterListIcon {
  background-image: var(--jp-icon-filter-list);
}

.jp-FolderFavoriteIcon {
  background-image: var(--jp-icon-folder-favorite);
}

.jp-FolderIcon {
  background-image: var(--jp-icon-folder);
}

.jp-HomeIcon {
  background-image: var(--jp-icon-home);
}

.jp-Html5Icon {
  background-image: var(--jp-icon-html5);
}

.jp-ImageIcon {
  background-image: var(--jp-icon-image);
}

.jp-InfoIcon {
  background-image: var(--jp-icon-info);
}

.jp-InspectorIcon {
  background-image: var(--jp-icon-inspector);
}

.jp-JsonIcon {
  background-image: var(--jp-icon-json);
}

.jp-JuliaIcon {
  background-image: var(--jp-icon-julia);
}

.jp-JupyterFaviconIcon {
  background-image: var(--jp-icon-jupyter-favicon);
}

.jp-JupyterIcon {
  background-image: var(--jp-icon-jupyter);
}

.jp-JupyterlabWordmarkIcon {
  background-image: var(--jp-icon-jupyterlab-wordmark);
}

.jp-KernelIcon {
  background-image: var(--jp-icon-kernel);
}

.jp-KeyboardIcon {
  background-image: var(--jp-icon-keyboard);
}

.jp-LaunchIcon {
  background-image: var(--jp-icon-launch);
}

.jp-LauncherIcon {
  background-image: var(--jp-icon-launcher);
}

.jp-LineFormIcon {
  background-image: var(--jp-icon-line-form);
}

.jp-LinkIcon {
  background-image: var(--jp-icon-link);
}

.jp-ListIcon {
  background-image: var(--jp-icon-list);
}

.jp-MarkdownIcon {
  background-image: var(--jp-icon-markdown);
}

.jp-MoveDownIcon {
  background-image: var(--jp-icon-move-down);
}

.jp-MoveUpIcon {
  background-image: var(--jp-icon-move-up);
}

.jp-NewFolderIcon {
  background-image: var(--jp-icon-new-folder);
}

.jp-NotTrustedIcon {
  background-image: var(--jp-icon-not-trusted);
}

.jp-NotebookIcon {
  background-image: var(--jp-icon-notebook);
}

.jp-NumberingIcon {
  background-image: var(--jp-icon-numbering);
}

.jp-OfflineBoltIcon {
  background-image: var(--jp-icon-offline-bolt);
}

.jp-PaletteIcon {
  background-image: var(--jp-icon-palette);
}

.jp-PasteIcon {
  background-image: var(--jp-icon-paste);
}

.jp-PdfIcon {
  background-image: var(--jp-icon-pdf);
}

.jp-PythonIcon {
  background-image: var(--jp-icon-python);
}

.jp-RKernelIcon {
  background-image: var(--jp-icon-r-kernel);
}

.jp-ReactIcon {
  background-image: var(--jp-icon-react);
}

.jp-RedoIcon {
  background-image: var(--jp-icon-redo);
}

.jp-RefreshIcon {
  background-image: var(--jp-icon-refresh);
}

.jp-RegexIcon {
  background-image: var(--jp-icon-regex);
}

.jp-RunIcon {
  background-image: var(--jp-icon-run);
}

.jp-RunningIcon {
  background-image: var(--jp-icon-running);
}

.jp-SaveIcon {
  background-image: var(--jp-icon-save);
}

.jp-SearchIcon {
  background-image: var(--jp-icon-search);
}

.jp-SettingsIcon {
  background-image: var(--jp-icon-settings);
}

.jp-ShareIcon {
  background-image: var(--jp-icon-share);
}

.jp-SpreadsheetIcon {
  background-image: var(--jp-icon-spreadsheet);
}

.jp-StopIcon {
  background-image: var(--jp-icon-stop);
}

.jp-TabIcon {
  background-image: var(--jp-icon-tab);
}

.jp-TableRowsIcon {
  background-image: var(--jp-icon-table-rows);
}

.jp-TagIcon {
  background-image: var(--jp-icon-tag);
}

.jp-TerminalIcon {
  background-image: var(--jp-icon-terminal);
}

.jp-TextEditorIcon {
  background-image: var(--jp-icon-text-editor);
}

.jp-TocIcon {
  background-image: var(--jp-icon-toc);
}

.jp-TreeViewIcon {
  background-image: var(--jp-icon-tree-view);
}

.jp-TrustedIcon {
  background-image: var(--jp-icon-trusted);
}

.jp-UndoIcon {
  background-image: var(--jp-icon-undo);
}

.jp-UserIcon {
  background-image: var(--jp-icon-user);
}

.jp-UsersIcon {
  background-image: var(--jp-icon-users);
}

.jp-VegaIcon {
  background-image: var(--jp-icon-vega);
}

.jp-WordIcon {
  background-image: var(--jp-icon-word);
}

.jp-YamlIcon {
  background-image: var(--jp-icon-yaml);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * (DEPRECATED) Support for consuming icons as CSS background images
 */

.jp-Icon,
.jp-MaterialIcon {
  background-position: center;
  background-repeat: no-repeat;
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-cover {
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
}

/**
 * (DEPRECATED) Support for specific CSS icon sizes
 */

.jp-Icon-16 {
  background-size: 16px;
  min-width: 16px;
  min-height: 16px;
}

.jp-Icon-18 {
  background-size: 18px;
  min-width: 18px;
  min-height: 18px;
}

.jp-Icon-20 {
  background-size: 20px;
  min-width: 20px;
  min-height: 20px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.lm-TabBar .lm-TabBar-addButton {
  align-items: center;
  display: flex;
  padding: 4px;
  padding-bottom: 5px;
  margin-right: 1px;
  background-color: var(--jp-layout-color2);
}

.lm-TabBar .lm-TabBar-addButton:hover {
  background-color: var(--jp-layout-color1);
}

.lm-DockPanel-tabBar .lm-TabBar-tab {
  width: var(--jp-private-horizontal-tab-width);
}

.lm-DockPanel-tabBar .lm-TabBar-content {
  flex: unset;
}

.lm-DockPanel-tabBar[data-orientation='horizontal'] {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for icons as inline SVG HTMLElements
 */

/* recolor the primary elements of an icon */
.jp-icon0[fill] {
  fill: var(--jp-inverse-layout-color0);
}

.jp-icon1[fill] {
  fill: var(--jp-inverse-layout-color1);
}

.jp-icon2[fill] {
  fill: var(--jp-inverse-layout-color2);
}

.jp-icon3[fill] {
  fill: var(--jp-inverse-layout-color3);
}

.jp-icon4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}

.jp-icon1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}

.jp-icon2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}

.jp-icon3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}

.jp-icon4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/* recolor the accent elements of an icon */
.jp-icon-accent0[fill] {
  fill: var(--jp-layout-color0);
}

.jp-icon-accent1[fill] {
  fill: var(--jp-layout-color1);
}

.jp-icon-accent2[fill] {
  fill: var(--jp-layout-color2);
}

.jp-icon-accent3[fill] {
  fill: var(--jp-layout-color3);
}

.jp-icon-accent4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-accent0[stroke] {
  stroke: var(--jp-layout-color0);
}

.jp-icon-accent1[stroke] {
  stroke: var(--jp-layout-color1);
}

.jp-icon-accent2[stroke] {
  stroke: var(--jp-layout-color2);
}

.jp-icon-accent3[stroke] {
  stroke: var(--jp-layout-color3);
}

.jp-icon-accent4[stroke] {
  stroke: var(--jp-layout-color4);
}

/* set the color of an icon to transparent */
.jp-icon-none[fill] {
  fill: none;
}

.jp-icon-none[stroke] {
  stroke: none;
}

/* brand icon colors. Same for light and dark */
.jp-icon-brand0[fill] {
  fill: var(--jp-brand-color0);
}

.jp-icon-brand1[fill] {
  fill: var(--jp-brand-color1);
}

.jp-icon-brand2[fill] {
  fill: var(--jp-brand-color2);
}

.jp-icon-brand3[fill] {
  fill: var(--jp-brand-color3);
}

.jp-icon-brand4[fill] {
  fill: var(--jp-brand-color4);
}

.jp-icon-brand0[stroke] {
  stroke: var(--jp-brand-color0);
}

.jp-icon-brand1[stroke] {
  stroke: var(--jp-brand-color1);
}

.jp-icon-brand2[stroke] {
  stroke: var(--jp-brand-color2);
}

.jp-icon-brand3[stroke] {
  stroke: var(--jp-brand-color3);
}

.jp-icon-brand4[stroke] {
  stroke: var(--jp-brand-color4);
}

/* warn icon colors. Same for light and dark */
.jp-icon-warn0[fill] {
  fill: var(--jp-warn-color0);
}

.jp-icon-warn1[fill] {
  fill: var(--jp-warn-color1);
}

.jp-icon-warn2[fill] {
  fill: var(--jp-warn-color2);
}

.jp-icon-warn3[fill] {
  fill: var(--jp-warn-color3);
}

.jp-icon-warn0[stroke] {
  stroke: var(--jp-warn-color0);
}

.jp-icon-warn1[stroke] {
  stroke: var(--jp-warn-color1);
}

.jp-icon-warn2[stroke] {
  stroke: var(--jp-warn-color2);
}

.jp-icon-warn3[stroke] {
  stroke: var(--jp-warn-color3);
}

/* icon colors that contrast well with each other and most backgrounds */
.jp-icon-contrast0[fill] {
  fill: var(--jp-icon-contrast-color0);
}

.jp-icon-contrast1[fill] {
  fill: var(--jp-icon-contrast-color1);
}

.jp-icon-contrast2[fill] {
  fill: var(--jp-icon-contrast-color2);
}

.jp-icon-contrast3[fill] {
  fill: var(--jp-icon-contrast-color3);
}

.jp-icon-contrast0[stroke] {
  stroke: var(--jp-icon-contrast-color0);
}

.jp-icon-contrast1[stroke] {
  stroke: var(--jp-icon-contrast-color1);
}

.jp-icon-contrast2[stroke] {
  stroke: var(--jp-icon-contrast-color2);
}

.jp-icon-contrast3[stroke] {
  stroke: var(--jp-icon-contrast-color3);
}

.jp-icon-dot[fill] {
  fill: var(--jp-warn-color0);
}

.jp-jupyter-icon-color[fill] {
  fill: var(--jp-jupyter-icon-color, var(--jp-warn-color0));
}

.jp-notebook-icon-color[fill] {
  fill: var(--jp-notebook-icon-color, var(--jp-warn-color0));
}

.jp-json-icon-color[fill] {
  fill: var(--jp-json-icon-color, var(--jp-warn-color1));
}

.jp-console-icon-color[fill] {
  fill: var(--jp-console-icon-color, white);
}

.jp-console-icon-background-color[fill] {
  fill: var(--jp-console-icon-background-color, var(--jp-brand-color1));
}

.jp-terminal-icon-color[fill] {
  fill: var(--jp-terminal-icon-color, var(--jp-layout-color2));
}

.jp-terminal-icon-background-color[fill] {
  fill: var(
    --jp-terminal-icon-background-color,
    var(--jp-inverse-layout-color2)
  );
}

.jp-text-editor-icon-color[fill] {
  fill: var(--jp-text-editor-icon-color, var(--jp-inverse-layout-color3));
}

.jp-inspector-icon-color[fill] {
  fill: var(--jp-inspector-icon-color, var(--jp-inverse-layout-color3));
}

/* CSS for icons in selected filebrowser listing items */
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}

.jp-DirListing-item.jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* stylelint-disable selector-max-class, selector-max-compound-selectors */

/**
* TODO: come up with non css-hack solution for showing the busy icon on top
*  of the close icon
* CSS for complex behavior of close icon of tabs in the main area tabbar
*/
.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}

.lm-DockPanel-tabBar
  .lm-TabBar-tab.lm-mod-closable.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

/* stylelint-enable selector-max-class, selector-max-compound-selectors */

/* CSS for icons in status bar */
#jp-main-statusbar .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}

#jp-main-statusbar .jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* special handling for splash icon CSS. While the theme CSS reloads during
   splash, the splash icon can loose theming. To prevent that, we set a
   default for its color variable */
:root {
  --jp-warn-color0: var(--md-orange-700);
}

/* not sure what to do with this one, used in filebrowser listing */
.jp-DragIcon {
  margin-right: 4px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/**
 * Support for alt colors for icons as inline SVG HTMLElements
 */

/* alt recolor the primary elements of an icon */
.jp-icon-alt .jp-icon0[fill] {
  fill: var(--jp-layout-color0);
}

.jp-icon-alt .jp-icon1[fill] {
  fill: var(--jp-layout-color1);
}

.jp-icon-alt .jp-icon2[fill] {
  fill: var(--jp-layout-color2);
}

.jp-icon-alt .jp-icon3[fill] {
  fill: var(--jp-layout-color3);
}

.jp-icon-alt .jp-icon4[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-alt .jp-icon0[stroke] {
  stroke: var(--jp-layout-color0);
}

.jp-icon-alt .jp-icon1[stroke] {
  stroke: var(--jp-layout-color1);
}

.jp-icon-alt .jp-icon2[stroke] {
  stroke: var(--jp-layout-color2);
}

.jp-icon-alt .jp-icon3[stroke] {
  stroke: var(--jp-layout-color3);
}

.jp-icon-alt .jp-icon4[stroke] {
  stroke: var(--jp-layout-color4);
}

/* alt recolor the accent elements of an icon */
.jp-icon-alt .jp-icon-accent0[fill] {
  fill: var(--jp-inverse-layout-color0);
}

.jp-icon-alt .jp-icon-accent1[fill] {
  fill: var(--jp-inverse-layout-color1);
}

.jp-icon-alt .jp-icon-accent2[fill] {
  fill: var(--jp-inverse-layout-color2);
}

.jp-icon-alt .jp-icon-accent3[fill] {
  fill: var(--jp-inverse-layout-color3);
}

.jp-icon-alt .jp-icon-accent4[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-alt .jp-icon-accent0[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}

.jp-icon-alt .jp-icon-accent1[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}

.jp-icon-alt .jp-icon-accent2[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}

.jp-icon-alt .jp-icon-accent3[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}

.jp-icon-alt .jp-icon-accent4[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-icon-hoverShow:not(:hover) .jp-icon-hoverShow-content {
  display: none !important;
}

/**
 * Support for hover colors for icons as inline SVG HTMLElements
 */

/**
 * regular colors
 */

/* recolor the primary elements of an icon */
.jp-icon-hover :hover .jp-icon0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}

.jp-icon-hover :hover .jp-icon1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}

.jp-icon-hover :hover .jp-icon2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}

.jp-icon-hover :hover .jp-icon3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}

.jp-icon-hover :hover .jp-icon4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}

.jp-icon-hover :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}

.jp-icon-hover :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}

.jp-icon-hover :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}

.jp-icon-hover :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/* recolor the accent elements of an icon */
.jp-icon-hover :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-layout-color0);
}

.jp-icon-hover :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-layout-color1);
}

.jp-icon-hover :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-layout-color2);
}

.jp-icon-hover :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-layout-color3);
}

.jp-icon-hover :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}

.jp-icon-hover :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}

.jp-icon-hover :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}

.jp-icon-hover :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}

.jp-icon-hover :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* set the color of an icon to transparent */
.jp-icon-hover :hover .jp-icon-none-hover[fill] {
  fill: none;
}

.jp-icon-hover :hover .jp-icon-none-hover[stroke] {
  stroke: none;
}

/**
 * inverse colors
 */

/* inverse recolor the primary elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[fill] {
  fill: var(--jp-layout-color0);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[fill] {
  fill: var(--jp-layout-color1);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[fill] {
  fill: var(--jp-layout-color2);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[fill] {
  fill: var(--jp-layout-color3);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[fill] {
  fill: var(--jp-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon0-hover[stroke] {
  stroke: var(--jp-layout-color0);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon1-hover[stroke] {
  stroke: var(--jp-layout-color1);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon2-hover[stroke] {
  stroke: var(--jp-layout-color2);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon3-hover[stroke] {
  stroke: var(--jp-layout-color3);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon4-hover[stroke] {
  stroke: var(--jp-layout-color4);
}

/* inverse recolor the accent elements of an icon */
.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[fill] {
  fill: var(--jp-inverse-layout-color0);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[fill] {
  fill: var(--jp-inverse-layout-color1);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[fill] {
  fill: var(--jp-inverse-layout-color2);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[fill] {
  fill: var(--jp-inverse-layout-color3);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[fill] {
  fill: var(--jp-inverse-layout-color4);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent0-hover[stroke] {
  stroke: var(--jp-inverse-layout-color0);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent1-hover[stroke] {
  stroke: var(--jp-inverse-layout-color1);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent2-hover[stroke] {
  stroke: var(--jp-inverse-layout-color2);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent3-hover[stroke] {
  stroke: var(--jp-inverse-layout-color3);
}

.jp-icon-hover.jp-icon-alt :hover .jp-icon-accent4-hover[stroke] {
  stroke: var(--jp-inverse-layout-color4);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-IFrame {
  width: 100%;
  height: 100%;
}

.jp-IFrame > iframe {
  border: none;
}

/*
When drag events occur, `lm-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-IFrame {
  position: relative;
}

body.lm-mod-override-cursor .jp-IFrame::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-HoverBox {
  position: fixed;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-FormGroup-content fieldset {
  border: none;
  padding: 0;
  min-width: 0;
  width: 100%;
}

/* stylelint-disable selector-max-type */

.jp-FormGroup-content fieldset .jp-inputFieldWrapper input,
.jp-FormGroup-content fieldset .jp-inputFieldWrapper select,
.jp-FormGroup-content fieldset .jp-inputFieldWrapper textarea {
  font-size: var(--jp-content-font-size2);
  border-color: var(--jp-input-border-color);
  border-style: solid;
  border-radius: var(--jp-border-radius);
  border-width: 1px;
  padding: 6px 8px;
  background: none;
  color: var(--jp-ui-font-color0);
  height: inherit;
}

.jp-FormGroup-content fieldset input[type='checkbox'] {
  position: relative;
  top: 2px;
  margin-left: 0;
}

.jp-FormGroup-content button.jp-mod-styled {
  cursor: pointer;
}

.jp-FormGroup-content .checkbox label {
  cursor: pointer;
  font-size: var(--jp-content-font-size1);
}

.jp-FormGroup-content .jp-root > fieldset > legend {
  display: none;
}

.jp-FormGroup-content .jp-root > fieldset > p {
  display: none;
}

/** copy of `input.jp-mod-styled:focus` style */
.jp-FormGroup-content fieldset input:focus,
.jp-FormGroup-content fieldset select:focus {
  -moz-outline-radius: unset;
  outline: var(--jp-border-width) solid var(--md-blue-500);
  outline-offset: -1px;
  box-shadow: inset 0 0 4px var(--md-blue-300);
}

.jp-FormGroup-content fieldset input:hover:not(:focus),
.jp-FormGroup-content fieldset select:hover:not(:focus) {
  background-color: var(--jp-border-color2);
}

/* stylelint-enable selector-max-type */

.jp-FormGroup-content .checkbox .field-description {
  /* Disable default description field for checkbox:
   because other widgets do not have description fields,
   we add descriptions to each widget on the field level.
  */
  display: none;
}

.jp-FormGroup-content #root__description {
  display: none;
}

.jp-FormGroup-content .jp-modifiedIndicator {
  width: 5px;
  background-color: var(--jp-brand-color2);
  margin-top: 0;
  margin-left: calc(var(--jp-private-settingeditor-modifier-indent) * -1);
  flex-shrink: 0;
}

.jp-FormGroup-content .jp-modifiedIndicator.jp-errorIndicator {
  background-color: var(--jp-error-color0);
  margin-right: 0.5em;
}

/* RJSF ARRAY style */

.jp-arrayFieldWrapper legend {
  font-size: var(--jp-content-font-size2);
  color: var(--jp-ui-font-color0);
  flex-basis: 100%;
  padding: 4px 0;
  font-weight: var(--jp-content-heading-font-weight);
  border-bottom: 1px solid var(--jp-border-color2);
}

.jp-arrayFieldWrapper .field-description {
  padding: 4px 0;
  white-space: pre-wrap;
}

.jp-arrayFieldWrapper .array-item {
  width: 100%;
  border: 1px solid var(--jp-border-color2);
  border-radius: 4px;
  margin: 4px;
}

.jp-ArrayOperations {
  display: flex;
  margin-left: 8px;
}

.jp-ArrayOperationsButton {
  margin: 2px;
}

.jp-ArrayOperationsButton .jp-icon3[fill] {
  fill: var(--jp-ui-font-color0);
}

button.jp-ArrayOperationsButton.jp-mod-styled:disabled {
  cursor: not-allowed;
  opacity: 0.5;
}

/* RJSF form validation error */

.jp-FormGroup-content .validationErrors {
  color: var(--jp-error-color0);
}

/* Hide panel level error as duplicated the field level error */
.jp-FormGroup-content .panel.errors {
  display: none;
}

/* RJSF normal content (settings-editor) */

.jp-FormGroup-contentNormal {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
}

.jp-FormGroup-contentNormal .jp-FormGroup-contentItem {
  margin-left: 7px;
  color: var(--jp-ui-font-color0);
}

.jp-FormGroup-contentNormal .jp-FormGroup-description {
  flex-basis: 100%;
  padding: 4px 7px;
}

.jp-FormGroup-contentNormal .jp-FormGroup-default {
  flex-basis: 100%;
  padding: 4px 7px;
}

.jp-FormGroup-contentNormal .jp-FormGroup-fieldLabel {
  font-size: var(--jp-content-font-size1);
  font-weight: normal;
  min-width: 120px;
}

.jp-FormGroup-contentNormal fieldset:not(:first-child) {
  margin-left: 7px;
}

.jp-FormGroup-contentNormal .field-array-of-string .array-item {
  /* Display `jp-ArrayOperations` buttons side-by-side with content except
    for small screens where flex-wrap will place them one below the other.
  */
  display: flex;
  align-items: center;
  flex-wrap: wrap;
}

.jp-FormGroup-contentNormal .jp-objectFieldWrapper .form-group {
  padding: 2px 8px 2px var(--jp-private-settingeditor-modifier-indent);
  margin-top: 2px;
}

/* RJSF compact content (metadata-form) */

.jp-FormGroup-content.jp-FormGroup-contentCompact {
  width: 100%;
}

.jp-FormGroup-contentCompact .form-group {
  display: flex;
  padding: 0.5em 0.2em 0.5em 0;
}

.jp-FormGroup-contentCompact
  .jp-FormGroup-compactTitle
  .jp-FormGroup-description {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color2);
}

.jp-FormGroup-contentCompact .jp-FormGroup-fieldLabel {
  padding-bottom: 0.3em;
}

.jp-FormGroup-contentCompact .jp-inputFieldWrapper .form-control {
  width: 100%;
  box-sizing: border-box;
}

.jp-FormGroup-contentCompact .jp-arrayFieldWrapper .jp-FormGroup-compactTitle {
  padding-bottom: 7px;
}

.jp-FormGroup-contentCompact
  .jp-objectFieldWrapper
  .jp-objectFieldWrapper
  .form-group {
  padding: 2px 8px 2px var(--jp-private-settingeditor-modifier-indent);
  margin-top: 2px;
}

.jp-FormGroup-contentCompact ul.error-detail {
  margin-block-start: 0.5em;
  margin-block-end: 0.5em;
  padding-inline-start: 1em;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

.jp-SidePanel {
  display: flex;
  flex-direction: column;
  min-width: var(--jp-sidebar-min-width);
  overflow-y: auto;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  font-size: var(--jp-ui-font-size1);
}

.jp-SidePanel-header {
  flex: 0 0 auto;
  display: flex;
  border-bottom: var(--jp-border-width) solid var(--jp-border-color2);
  font-size: var(--jp-ui-font-size0);
  font-weight: 600;
  letter-spacing: 1px;
  margin: 0;
  padding: 2px;
  text-transform: uppercase;
}

.jp-SidePanel-toolbar {
  flex: 0 0 auto;
}

.jp-SidePanel-content {
  flex: 1 1 auto;
}

.jp-SidePanel-toolbar,
.jp-AccordionPanel-toolbar {
  height: var(--jp-private-toolbar-height);
}

.jp-SidePanel-toolbar.jp-Toolbar-micro {
  display: none;
}

.lm-AccordionPanel .jp-AccordionPanel-title {
  box-sizing: border-box;
  line-height: 25px;
  margin: 0;
  display: flex;
  align-items: center;
  background: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  box-shadow: var(--jp-toolbar-box-shadow);
  font-size: var(--jp-ui-font-size0);
}

.jp-AccordionPanel-title {
  cursor: pointer;
  user-select: none;
  -moz-user-select: none;
  -webkit-user-select: none;
  text-transform: uppercase;
}

.lm-AccordionPanel[data-orientation='horizontal'] > .jp-AccordionPanel-title {
  /* Title is rotated for horizontal accordion panel using CSS */
  display: block;
  transform-origin: top left;
  transform: rotate(-90deg) translate(-100%);
}

.jp-AccordionPanel-title .lm-AccordionPanel-titleLabel {
  user-select: none;
  text-overflow: ellipsis;
  white-space: nowrap;
  overflow: hidden;
}

.jp-AccordionPanel-title .lm-AccordionPanel-titleCollapser {
  transform: rotate(-90deg);
  margin: auto 0;
  height: 16px;
}

.jp-AccordionPanel-title.lm-mod-expanded .lm-AccordionPanel-titleCollapser {
  transform: rotate(0deg);
}

.lm-AccordionPanel .jp-AccordionPanel-toolbar {
  background: none;
  box-shadow: none;
  border: none;
  margin-left: auto;
}

.lm-AccordionPanel .lm-SplitPanel-handle:hover {
  background: var(--jp-layout-color3);
}

.jp-text-truncated {
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Spinner {
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 10;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-layout-color0);
  outline: none;
}

.jp-SpinnerContent {
  font-size: 10px;
  margin: 50px auto;
  text-indent: -9999em;
  width: 3em;
  height: 3em;
  border-radius: 50%;
  background: var(--jp-brand-color3);
  background: linear-gradient(
    to right,
    #f37626 10%,
    rgba(255, 255, 255, 0) 42%
  );
  position: relative;
  animation: load3 1s infinite linear, fadeIn 1s;
}

.jp-SpinnerContent::before {
  width: 50%;
  height: 50%;
  background: #f37626;
  border-radius: 100% 0 0;
  position: absolute;
  top: 0;
  left: 0;
  content: '';
}

.jp-SpinnerContent::after {
  background: var(--jp-layout-color0);
  width: 75%;
  height: 75%;
  border-radius: 50%;
  content: '';
  margin: auto;
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}

@keyframes fadeIn {
  0% {
    opacity: 0;
  }

  100% {
    opacity: 1;
  }
}

@keyframes load3 {
  0% {
    transform: rotate(0deg);
  }

  100% {
    transform: rotate(360deg);
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

button.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: none;
  box-sizing: border-box;
  text-align: center;
  line-height: 32px;
  height: 32px;
  padding: 0 12px;
  letter-spacing: 0.8px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input.jp-mod-styled {
  background: var(--jp-input-background);
  height: 28px;
  box-sizing: border-box;
  border: var(--jp-border-width) solid var(--jp-border-color1);
  padding-left: 7px;
  padding-right: 7px;
  font-size: var(--jp-ui-font-size2);
  color: var(--jp-ui-font-color0);
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

input[type='checkbox'].jp-mod-styled {
  appearance: checkbox;
  -webkit-appearance: checkbox;
  -moz-appearance: checkbox;
  height: auto;
}

input.jp-mod-styled:focus {
  border: var(--jp-border-width) solid var(--md-blue-500);
  box-shadow: inset 0 0 4px var(--md-blue-300);
}

.jp-select-wrapper {
  display: flex;
  position: relative;
  flex-direction: column;
  padding: 1px;
  background-color: var(--jp-layout-color1);
  box-sizing: border-box;
  margin-bottom: 12px;
}

.jp-select-wrapper:not(.multiple) {
  height: 28px;
}

.jp-select-wrapper.jp-mod-focused select.jp-mod-styled {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-input-active-background);
}

select.jp-mod-styled:hover {
  cursor: pointer;
  color: var(--jp-ui-font-color0);
  background-color: var(--jp-input-hover-background);
  box-shadow: inset 0 0 1px rgba(0, 0, 0, 0.5);
}

select.jp-mod-styled {
  flex: 1 1 auto;
  width: 100%;
  font-size: var(--jp-ui-font-size2);
  background: var(--jp-input-background);
  color: var(--jp-ui-font-color0);
  padding: 0 25px 0 8px;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
}

select.jp-mod-styled:not([multiple]) {
  height: 32px;
}

select.jp-mod-styled[multiple] {
  max-height: 200px;
  overflow-y: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-switch {
  display: flex;
  align-items: center;
  padding-left: 4px;
  padding-right: 4px;
  font-size: var(--jp-ui-font-size1);
  background-color: transparent;
  color: var(--jp-ui-font-color1);
  border: none;
  height: 20px;
}

.jp-switch:hover {
  background-color: var(--jp-layout-color2);
}

.jp-switch-label {
  margin-right: 5px;
  font-family: var(--jp-ui-font-family);
}

.jp-switch-track {
  cursor: pointer;
  background-color: var(--jp-switch-color, var(--jp-border-color1));
  -webkit-transition: 0.4s;
  transition: 0.4s;
  border-radius: 34px;
  height: 16px;
  width: 35px;
  position: relative;
}

.jp-switch-track::before {
  content: '';
  position: absolute;
  height: 10px;
  width: 10px;
  margin: 3px;
  left: 0;
  background-color: var(--jp-ui-inverse-font-color1);
  -webkit-transition: 0.4s;
  transition: 0.4s;
  border-radius: 50%;
}

.jp-switch[aria-checked='true'] .jp-switch-track {
  background-color: var(--jp-switch-true-position-color, var(--jp-warn-color0));
}

.jp-switch[aria-checked='true'] .jp-switch-track::before {
  /* track width (35) - margins (3 + 3) - thumb width (10) */
  left: 19px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

:root {
  --jp-private-toolbar-height: calc(
    28px + var(--jp-border-width)
  ); /* leave 28px for content */
}

.jp-Toolbar {
  color: var(--jp-ui-font-color1);
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  box-shadow: var(--jp-toolbar-box-shadow);
  background: var(--jp-toolbar-background);
  min-height: var(--jp-toolbar-micro-height);
  padding: 2px;
  z-index: 8;
  overflow-x: hidden;
}

/* Toolbar items */

.jp-Toolbar > .jp-Toolbar-item.jp-Toolbar-spacer {
  flex-grow: 1;
  flex-shrink: 1;
}

.jp-Toolbar-item.jp-Toolbar-kernelStatus {
  display: inline-block;
  width: 32px;
  background-repeat: no-repeat;
  background-position: center;
  background-size: 16px;
}

.jp-Toolbar > .jp-Toolbar-item {
  flex: 0 0 auto;
  display: flex;
  padding-left: 1px;
  padding-right: 1px;
  font-size: var(--jp-ui-font-size1);
  line-height: var(--jp-private-toolbar-height);
  height: 100%;
}

/* Toolbar buttons */

/* This is the div we use to wrap the react component into a Widget */
div.jp-ToolbarButton {
  color: transparent;
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0;
  margin: 0;
}

button.jp-ToolbarButtonComponent {
  background: var(--jp-layout-color1);
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0 6px;
  margin: 0;
  height: 24px;
  border-radius: var(--jp-border-radius);
  display: flex;
  align-items: center;
  text-align: center;
  font-size: 14px;
  min-width: unset;
  min-height: unset;
}

button.jp-ToolbarButtonComponent:disabled {
  opacity: 0.4;
}

button.jp-ToolbarButtonComponent > span {
  padding: 0;
  flex: 0 0 auto;
}

button.jp-ToolbarButtonComponent .jp-ToolbarButtonComponent-label {
  font-size: var(--jp-ui-font-size1);
  line-height: 100%;
  padding-left: 2px;
  color: var(--jp-ui-font-color1);
  font-family: var(--jp-ui-font-family);
}

#jp-main-dock-panel[data-mode='single-document']
  .jp-MainAreaWidget
  > .jp-Toolbar.jp-Toolbar-micro {
  padding: 0;
  min-height: 0;
}

#jp-main-dock-panel[data-mode='single-document']
  .jp-MainAreaWidget
  > .jp-Toolbar {
  border: none;
  box-shadow: none;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

.jp-WindowedPanel-outer {
  position: relative;
  overflow-y: auto;
}

.jp-WindowedPanel-inner {
  position: relative;
}

.jp-WindowedPanel-window {
  position: absolute;
  left: 0;
  right: 0;
  overflow: visible;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* Sibling imports */

body {
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
}

/* Disable native link decoration styles everywhere outside of dialog boxes */
a {
  text-decoration: unset;
  color: unset;
}

a:hover {
  text-decoration: unset;
  color: unset;
}

/* Accessibility for links inside dialog box text */
.jp-Dialog-content a {
  text-decoration: revert;
  color: var(--jp-content-link-color);
}

.jp-Dialog-content a:hover {
  text-decoration: revert;
}

/* Styles for ui-components */
.jp-Button {
  color: var(--jp-ui-font-color2);
  border-radius: var(--jp-border-radius);
  padding: 0 12px;
  font-size: var(--jp-ui-font-size1);

  /* Copy from blueprint 3 */
  display: inline-flex;
  flex-direction: row;
  border: none;
  cursor: pointer;
  align-items: center;
  justify-content: center;
  text-align: left;
  vertical-align: middle;
  min-height: 30px;
  min-width: 30px;
}

.jp-Button:disabled {
  cursor: not-allowed;
}

.jp-Button:empty {
  padding: 0 !important;
}

.jp-Button.jp-mod-small {
  min-height: 24px;
  min-width: 24px;
  font-size: 12px;
  padding: 0 7px;
}

/* Use our own theme for hover styles */
.jp-Button.jp-mod-minimal:hover {
  background-color: var(--jp-layout-color2);
}

.jp-Button.jp-mod-minimal {
  background: none;
}

.jp-InputGroup {
  display: block;
  position: relative;
}

.jp-InputGroup input {
  box-sizing: border-box;
  border: none;
  border-radius: 0;
  background-color: transparent;
  color: var(--jp-ui-font-color0);
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
  padding-bottom: 0;
  padding-top: 0;
  padding-left: 10px;
  padding-right: 28px;
  position: relative;
  width: 100%;
  -webkit-appearance: none;
  -moz-appearance: none;
  appearance: none;
  font-size: 14px;
  font-weight: 400;
  height: 30px;
  line-height: 30px;
  outline: none;
  vertical-align: middle;
}

.jp-InputGroup input:focus {
  box-shadow: inset 0 0 0 var(--jp-border-width)
      var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-InputGroup input:disabled {
  cursor: not-allowed;
  resize: block;
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color2);
}

.jp-InputGroup input:disabled ~ span {
  cursor: not-allowed;
  color: var(--jp-ui-font-color2);
}

.jp-InputGroup input::placeholder,
input::placeholder {
  color: var(--jp-ui-font-color2);
}

.jp-InputGroupAction {
  position: absolute;
  bottom: 1px;
  right: 0;
  padding: 6px;
}

.jp-HTMLSelect.jp-DefaultStyle select {
  background-color: initial;
  border: none;
  border-radius: 0;
  box-shadow: none;
  color: var(--jp-ui-font-color0);
  display: block;
  font-size: var(--jp-ui-font-size1);
  font-family: var(--jp-ui-font-family);
  height: 24px;
  line-height: 14px;
  padding: 0 25px 0 10px;
  text-align: left;
  -moz-appearance: none;
  -webkit-appearance: none;
}

.jp-HTMLSelect.jp-DefaultStyle select:disabled {
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color2);
  cursor: not-allowed;
  resize: block;
}

.jp-HTMLSelect.jp-DefaultStyle select:disabled ~ span {
  cursor: not-allowed;
}

/* Use our own theme for hover and option styles */
/* stylelint-disable-next-line selector-max-type */
.jp-HTMLSelect.jp-DefaultStyle select:hover,
.jp-HTMLSelect.jp-DefaultStyle select > option {
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color0);
}

select {
  box-sizing: border-box;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Styles
|----------------------------------------------------------------------------*/

.jp-StatusBar-Widget {
  display: flex;
  align-items: center;
  background: var(--jp-layout-color2);
  min-height: var(--jp-statusbar-height);
  justify-content: space-between;
  padding: 0 10px;
}

.jp-StatusBar-Left {
  display: flex;
  align-items: center;
  flex-direction: row;
}

.jp-StatusBar-Middle {
  display: flex;
  align-items: center;
}

.jp-StatusBar-Right {
  display: flex;
  align-items: center;
  flex-direction: row-reverse;
}

.jp-StatusBar-Item {
  max-height: var(--jp-statusbar-height);
  margin: 0 2px;
  height: var(--jp-statusbar-height);
  white-space: nowrap;
  text-overflow: ellipsis;
  color: var(--jp-ui-font-color1);
  padding: 0 6px;
}

.jp-mod-highlighted:hover {
  background-color: var(--jp-layout-color3);
}

.jp-mod-clicked {
  background-color: var(--jp-brand-color1);
}

.jp-mod-clicked:hover {
  background-color: var(--jp-brand-color0);
}

.jp-mod-clicked .jp-StatusBar-TextItem {
  color: var(--jp-ui-inverse-font-color1);
}

.jp-StatusBar-HoverItem {
  box-shadow: '0px 4px 4px rgba(0, 0, 0, 0.25)';
}

.jp-StatusBar-TextItem {
  font-size: var(--jp-ui-font-size1);
  font-family: var(--jp-ui-font-family);
  line-height: 24px;
  color: var(--jp-ui-font-color1);
}

.jp-StatusBar-GroupItem {
  display: flex;
  align-items: center;
  flex-direction: row;
}

.jp-Statusbar-ProgressCircle svg {
  display: block;
  margin: 0 auto;
  width: 16px;
  height: 24px;
  align-self: normal;
}

.jp-Statusbar-ProgressCircle path {
  fill: var(--jp-inverse-layout-color3);
}

.jp-Statusbar-ProgressBar-progress-bar {
  height: 10px;
  width: 100px;
  border: solid 0.25px var(--jp-brand-color2);
  border-radius: 3px;
  overflow: hidden;
  align-self: center;
}

.jp-Statusbar-ProgressBar-progress-bar > div {
  background-color: var(--jp-brand-color2);
  background-image: linear-gradient(
    -45deg,
    rgba(255, 255, 255, 0.2) 25%,
    transparent 25%,
    transparent 50%,
    rgba(255, 255, 255, 0.2) 50%,
    rgba(255, 255, 255, 0.2) 75%,
    transparent 75%,
    transparent
  );
  background-size: 40px 40px;
  float: left;
  width: 0%;
  height: 100%;
  font-size: 12px;
  line-height: 14px;
  color: #fff;
  text-align: center;
  animation: jp-Statusbar-ExecutionTime-progress-bar 2s linear infinite;
}

.jp-Statusbar-ProgressBar-progress-bar p {
  color: var(--jp-ui-font-color1);
  font-family: var(--jp-ui-font-family);
  font-size: var(--jp-ui-font-size1);
  line-height: 10px;
  width: 100px;
}

@keyframes jp-Statusbar-ExecutionTime-progress-bar {
  0% {
    background-position: 0 0;
  }

  100% {
    background-position: 40px 40px;
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-commandpalette-search-height: 28px;
}

/*-----------------------------------------------------------------------------
| Overall styles
|----------------------------------------------------------------------------*/

.lm-CommandPalette {
  padding-bottom: 0;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);

  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Modal variant
|----------------------------------------------------------------------------*/

.jp-ModalCommandPalette {
  position: absolute;
  z-index: 10000;
  top: 38px;
  left: 30%;
  margin: 0;
  padding: 4px;
  width: 40%;
  box-shadow: var(--jp-elevation-z4);
  border-radius: 4px;
  background: var(--jp-layout-color0);
}

.jp-ModalCommandPalette .lm-CommandPalette {
  max-height: 40vh;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-close-icon::after {
  display: none;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-CommandPalette-header {
  display: none;
}

.jp-ModalCommandPalette .lm-CommandPalette .lm-CommandPalette-item {
  margin-left: 4px;
  margin-right: 4px;
}

.jp-ModalCommandPalette
  .lm-CommandPalette
  .lm-CommandPalette-item.lm-mod-disabled {
  display: none;
}

/*-----------------------------------------------------------------------------
| Search
|----------------------------------------------------------------------------*/

.lm-CommandPalette-search {
  padding: 4px;
  background-color: var(--jp-layout-color1);
  z-index: 2;
}

.lm-CommandPalette-wrapper {
  overflow: overlay;
  padding: 0 9px;
  background-color: var(--jp-input-active-background);
  height: 30px;
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.lm-CommandPalette.lm-mod-focused .lm-CommandPalette-wrapper {
  box-shadow: inset 0 0 0 1px var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-SearchIconGroup {
  color: white;
  background-color: var(--jp-brand-color1);
  position: absolute;
  top: 4px;
  right: 4px;
  padding: 5px 5px 1px;
}

.jp-SearchIconGroup svg {
  height: 20px;
  width: 20px;
}

.jp-SearchIconGroup .jp-icon3[fill] {
  fill: var(--jp-layout-color0);
}

.lm-CommandPalette-input {
  background: transparent;
  width: calc(100% - 18px);
  float: left;
  border: none;
  outline: none;
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  line-height: var(--jp-private-commandpalette-search-height);
}

.lm-CommandPalette-input::-webkit-input-placeholder,
.lm-CommandPalette-input::-moz-placeholder,
.lm-CommandPalette-input:-ms-input-placeholder {
  color: var(--jp-ui-font-color2);
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Results
|----------------------------------------------------------------------------*/

.lm-CommandPalette-header:first-child {
  margin-top: 0;
}

.lm-CommandPalette-header {
  border-bottom: solid var(--jp-border-width) var(--jp-border-color2);
  color: var(--jp-ui-font-color1);
  cursor: pointer;
  display: flex;
  font-size: var(--jp-ui-font-size0);
  font-weight: 600;
  letter-spacing: 1px;
  margin-top: 8px;
  padding: 8px 0 8px 12px;
  text-transform: uppercase;
}

.lm-CommandPalette-header.lm-mod-active {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-header > mark {
  background-color: transparent;
  font-weight: bold;
  color: var(--jp-ui-font-color1);
}

.lm-CommandPalette-item {
  padding: 4px 12px 4px 4px;
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  font-weight: 400;
  display: flex;
}

.lm-CommandPalette-item.lm-mod-disabled {
  color: var(--jp-ui-font-color2);
}

.lm-CommandPalette-item.lm-mod-active {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.lm-CommandPalette-item.lm-mod-active .lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-inverse-font-color0);
}

.lm-CommandPalette-item.lm-mod-active .jp-icon-selectable[fill] {
  fill: var(--jp-layout-color0);
}

.lm-CommandPalette-item.lm-mod-active:hover:not(.lm-mod-disabled) {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.lm-CommandPalette-item:hover:not(.lm-mod-active):not(.lm-mod-disabled) {
  background: var(--jp-layout-color2);
}

.lm-CommandPalette-itemContent {
  overflow: hidden;
}

.lm-CommandPalette-itemLabel > mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

.lm-CommandPalette-item.lm-mod-disabled mark {
  color: var(--jp-ui-font-color2);
}

.lm-CommandPalette-item .lm-CommandPalette-itemIcon {
  margin: 0 4px 0 0;
  position: relative;
  width: 16px;
  top: 2px;
  flex: 0 0 auto;
}

.lm-CommandPalette-item.lm-mod-disabled .lm-CommandPalette-itemIcon {
  opacity: 0.6;
}

.lm-CommandPalette-item .lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}

.lm-CommandPalette-itemCaption {
  display: none;
}

.lm-CommandPalette-content {
  background-color: var(--jp-layout-color1);
}

.lm-CommandPalette-content:empty::after {
  content: 'No results';
  margin: auto;
  margin-top: 20px;
  width: 100px;
  display: block;
  font-size: var(--jp-ui-font-size2);
  font-family: var(--jp-ui-font-family);
  font-weight: lighter;
}

.lm-CommandPalette-emptyMessage {
  text-align: center;
  margin-top: 24px;
  line-height: 1.32;
  padding: 0 8px;
  color: var(--jp-content-font-color3);
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Dialog {
  position: absolute;
  z-index: 10000;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  top: 0;
  left: 0;
  margin: 0;
  padding: 0;
  width: 100%;
  height: 100%;
  background: var(--jp-dialog-background);
}

.jp-Dialog-content {
  display: flex;
  flex-direction: column;
  margin-left: auto;
  margin-right: auto;
  background: var(--jp-layout-color1);
  padding: 24px 24px 12px;
  min-width: 300px;
  min-height: 150px;
  max-width: 1000px;
  max-height: 500px;
  box-sizing: border-box;
  box-shadow: var(--jp-elevation-z20);
  word-wrap: break-word;
  border-radius: var(--jp-border-radius);

  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color1);
  resize: both;
}

.jp-Dialog-content.jp-Dialog-content-small {
  max-width: 500px;
}

.jp-Dialog-button {
  overflow: visible;
}

button.jp-Dialog-button:focus {
  outline: 1px solid var(--jp-brand-color1);
  outline-offset: 4px;
  -moz-outline-radius: 0;
}

button.jp-Dialog-button:focus::-moz-focus-inner {
  border: 0;
}

button.jp-Dialog-button.jp-mod-styled.jp-mod-accept:focus,
button.jp-Dialog-button.jp-mod-styled.jp-mod-warn:focus,
button.jp-Dialog-button.jp-mod-styled.jp-mod-reject:focus {
  outline-offset: 4px;
  -moz-outline-radius: 0;
}

button.jp-Dialog-button.jp-mod-styled.jp-mod-accept:focus {
  outline: 1px solid var(--jp-accept-color-normal, var(--jp-brand-color1));
}

button.jp-Dialog-button.jp-mod-styled.jp-mod-warn:focus {
  outline: 1px solid var(--jp-warn-color-normal, var(--jp-error-color1));
}

button.jp-Dialog-button.jp-mod-styled.jp-mod-reject:focus {
  outline: 1px solid var(--jp-reject-color-normal, var(--md-grey-600));
}

button.jp-Dialog-close-button {
  padding: 0;
  height: 100%;
  min-width: unset;
  min-height: unset;
}

.jp-Dialog-header {
  display: flex;
  justify-content: space-between;
  flex: 0 0 auto;
  padding-bottom: 12px;
  font-size: var(--jp-ui-font-size3);
  font-weight: 400;
  color: var(--jp-ui-font-color1);
}

.jp-Dialog-body {
  display: flex;
  flex-direction: column;
  flex: 1 1 auto;
  font-size: var(--jp-ui-font-size1);
  background: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  overflow: auto;
}

.jp-Dialog-footer {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  align-items: center;
  flex: 0 0 auto;
  margin-left: -12px;
  margin-right: -12px;
  padding: 12px;
}

.jp-Dialog-checkbox {
  padding-right: 5px;
}

.jp-Dialog-checkbox > input:focus-visible {
  outline: 1px solid var(--jp-input-active-border-color);
  outline-offset: 1px;
}

.jp-Dialog-spacer {
  flex: 1 1 auto;
}

.jp-Dialog-title {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

.jp-Dialog-body > .jp-select-wrapper {
  width: 100%;
}

.jp-Dialog-body > button {
  padding: 0 16px;
}

.jp-Dialog-body > label {
  line-height: 1.4;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-button.jp-mod-styled:not(:last-child) {
  margin-right: 12px;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

.jp-Input-Boolean-Dialog {
  flex-direction: row-reverse;
  align-items: end;
  width: 100%;
}

.jp-Input-Boolean-Dialog > label {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MainAreaWidget > :focus {
  outline: none;
}

.jp-MainAreaWidget .jp-MainAreaWidget-error {
  padding: 6px;
}

.jp-MainAreaWidget .jp-MainAreaWidget-error > pre {
  width: auto;
  padding: 10px;
  background: var(--jp-error-color3);
  border: var(--jp-border-width) solid var(--jp-error-color1);
  border-radius: var(--jp-border-radius);
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  white-space: pre-wrap;
  word-wrap: break-word;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/**
 * google-material-color v1.2.6
 * https://github.com/danlevan/google-material-color
 */
:root {
  --md-red-50: #ffebee;
  --md-red-100: #ffcdd2;
  --md-red-200: #ef9a9a;
  --md-red-300: #e57373;
  --md-red-400: #ef5350;
  --md-red-500: #f44336;
  --md-red-600: #e53935;
  --md-red-700: #d32f2f;
  --md-red-800: #c62828;
  --md-red-900: #b71c1c;
  --md-red-A100: #ff8a80;
  --md-red-A200: #ff5252;
  --md-red-A400: #ff1744;
  --md-red-A700: #d50000;
  --md-pink-50: #fce4ec;
  --md-pink-100: #f8bbd0;
  --md-pink-200: #f48fb1;
  --md-pink-300: #f06292;
  --md-pink-400: #ec407a;
  --md-pink-500: #e91e63;
  --md-pink-600: #d81b60;
  --md-pink-700: #c2185b;
  --md-pink-800: #ad1457;
  --md-pink-900: #880e4f;
  --md-pink-A100: #ff80ab;
  --md-pink-A200: #ff4081;
  --md-pink-A400: #f50057;
  --md-pink-A700: #c51162;
  --md-purple-50: #f3e5f5;
  --md-purple-100: #e1bee7;
  --md-purple-200: #ce93d8;
  --md-purple-300: #ba68c8;
  --md-purple-400: #ab47bc;
  --md-purple-500: #9c27b0;
  --md-purple-600: #8e24aa;
  --md-purple-700: #7b1fa2;
  --md-purple-800: #6a1b9a;
  --md-purple-900: #4a148c;
  --md-purple-A100: #ea80fc;
  --md-purple-A200: #e040fb;
  --md-purple-A400: #d500f9;
  --md-purple-A700: #a0f;
  --md-deep-purple-50: #ede7f6;
  --md-deep-purple-100: #d1c4e9;
  --md-deep-purple-200: #b39ddb;
  --md-deep-purple-300: #9575cd;
  --md-deep-purple-400: #7e57c2;
  --md-deep-purple-500: #673ab7;
  --md-deep-purple-600: #5e35b1;
  --md-deep-purple-700: #512da8;
  --md-deep-purple-800: #4527a0;
  --md-deep-purple-900: #311b92;
  --md-deep-purple-A100: #b388ff;
  --md-deep-purple-A200: #7c4dff;
  --md-deep-purple-A400: #651fff;
  --md-deep-purple-A700: #6200ea;
  --md-indigo-50: #e8eaf6;
  --md-indigo-100: #c5cae9;
  --md-indigo-200: #9fa8da;
  --md-indigo-300: #7986cb;
  --md-indigo-400: #5c6bc0;
  --md-indigo-500: #3f51b5;
  --md-indigo-600: #3949ab;
  --md-indigo-700: #303f9f;
  --md-indigo-800: #283593;
  --md-indigo-900: #1a237e;
  --md-indigo-A100: #8c9eff;
  --md-indigo-A200: #536dfe;
  --md-indigo-A400: #3d5afe;
  --md-indigo-A700: #304ffe;
  --md-blue-50: #e3f2fd;
  --md-blue-100: #bbdefb;
  --md-blue-200: #90caf9;
  --md-blue-300: #64b5f6;
  --md-blue-400: #42a5f5;
  --md-blue-500: #2196f3;
  --md-blue-600: #1e88e5;
  --md-blue-700: #1976d2;
  --md-blue-800: #1565c0;
  --md-blue-900: #0d47a1;
  --md-blue-A100: #82b1ff;
  --md-blue-A200: #448aff;
  --md-blue-A400: #2979ff;
  --md-blue-A700: #2962ff;
  --md-light-blue-50: #e1f5fe;
  --md-light-blue-100: #b3e5fc;
  --md-light-blue-200: #81d4fa;
  --md-light-blue-300: #4fc3f7;
  --md-light-blue-400: #29b6f6;
  --md-light-blue-500: #03a9f4;
  --md-light-blue-600: #039be5;
  --md-light-blue-700: #0288d1;
  --md-light-blue-800: #0277bd;
  --md-light-blue-900: #01579b;
  --md-light-blue-A100: #80d8ff;
  --md-light-blue-A200: #40c4ff;
  --md-light-blue-A400: #00b0ff;
  --md-light-blue-A700: #0091ea;
  --md-cyan-50: #e0f7fa;
  --md-cyan-100: #b2ebf2;
  --md-cyan-200: #80deea;
  --md-cyan-300: #4dd0e1;
  --md-cyan-400: #26c6da;
  --md-cyan-500: #00bcd4;
  --md-cyan-600: #00acc1;
  --md-cyan-700: #0097a7;
  --md-cyan-800: #00838f;
  --md-cyan-900: #006064;
  --md-cyan-A100: #84ffff;
  --md-cyan-A200: #18ffff;
  --md-cyan-A400: #00e5ff;
  --md-cyan-A700: #00b8d4;
  --md-teal-50: #e0f2f1;
  --md-teal-100: #b2dfdb;
  --md-teal-200: #80cbc4;
  --md-teal-300: #4db6ac;
  --md-teal-400: #26a69a;
  --md-teal-500: #009688;
  --md-teal-600: #00897b;
  --md-teal-700: #00796b;
  --md-teal-800: #00695c;
  --md-teal-900: #004d40;
  --md-teal-A100: #a7ffeb;
  --md-teal-A200: #64ffda;
  --md-teal-A400: #1de9b6;
  --md-teal-A700: #00bfa5;
  --md-green-50: #e8f5e9;
  --md-green-100: #c8e6c9;
  --md-green-200: #a5d6a7;
  --md-green-300: #81c784;
  --md-green-400: #66bb6a;
  --md-green-500: #4caf50;
  --md-green-600: #43a047;
  --md-green-700: #388e3c;
  --md-green-800: #2e7d32;
  --md-green-900: #1b5e20;
  --md-green-A100: #b9f6ca;
  --md-green-A200: #69f0ae;
  --md-green-A400: #00e676;
  --md-green-A700: #00c853;
  --md-light-green-50: #f1f8e9;
  --md-light-green-100: #dcedc8;
  --md-light-green-200: #c5e1a5;
  --md-light-green-300: #aed581;
  --md-light-green-400: #9ccc65;
  --md-light-green-500: #8bc34a;
  --md-light-green-600: #7cb342;
  --md-light-green-700: #689f38;
  --md-light-green-800: #558b2f;
  --md-light-green-900: #33691e;
  --md-light-green-A100: #ccff90;
  --md-light-green-A200: #b2ff59;
  --md-light-green-A400: #76ff03;
  --md-light-green-A700: #64dd17;
  --md-lime-50: #f9fbe7;
  --md-lime-100: #f0f4c3;
  --md-lime-200: #e6ee9c;
  --md-lime-300: #dce775;
  --md-lime-400: #d4e157;
  --md-lime-500: #cddc39;
  --md-lime-600: #c0ca33;
  --md-lime-700: #afb42b;
  --md-lime-800: #9e9d24;
  --md-lime-900: #827717;
  --md-lime-A100: #f4ff81;
  --md-lime-A200: #eeff41;
  --md-lime-A400: #c6ff00;
  --md-lime-A700: #aeea00;
  --md-yellow-50: #fffde7;
  --md-yellow-100: #fff9c4;
  --md-yellow-200: #fff59d;
  --md-yellow-300: #fff176;
  --md-yellow-400: #ffee58;
  --md-yellow-500: #ffeb3b;
  --md-yellow-600: #fdd835;
  --md-yellow-700: #fbc02d;
  --md-yellow-800: #f9a825;
  --md-yellow-900: #f57f17;
  --md-yellow-A100: #ffff8d;
  --md-yellow-A200: #ff0;
  --md-yellow-A400: #ffea00;
  --md-yellow-A700: #ffd600;
  --md-amber-50: #fff8e1;
  --md-amber-100: #ffecb3;
  --md-amber-200: #ffe082;
  --md-amber-300: #ffd54f;
  --md-amber-400: #ffca28;
  --md-amber-500: #ffc107;
  --md-amber-600: #ffb300;
  --md-amber-700: #ffa000;
  --md-amber-800: #ff8f00;
  --md-amber-900: #ff6f00;
  --md-amber-A100: #ffe57f;
  --md-amber-A200: #ffd740;
  --md-amber-A400: #ffc400;
  --md-amber-A700: #ffab00;
  --md-orange-50: #fff3e0;
  --md-orange-100: #ffe0b2;
  --md-orange-200: #ffcc80;
  --md-orange-300: #ffb74d;
  --md-orange-400: #ffa726;
  --md-orange-500: #ff9800;
  --md-orange-600: #fb8c00;
  --md-orange-700: #f57c00;
  --md-orange-800: #ef6c00;
  --md-orange-900: #e65100;
  --md-orange-A100: #ffd180;
  --md-orange-A200: #ffab40;
  --md-orange-A400: #ff9100;
  --md-orange-A700: #ff6d00;
  --md-deep-orange-50: #fbe9e7;
  --md-deep-orange-100: #ffccbc;
  --md-deep-orange-200: #ffab91;
  --md-deep-orange-300: #ff8a65;
  --md-deep-orange-400: #ff7043;
  --md-deep-orange-500: #ff5722;
  --md-deep-orange-600: #f4511e;
  --md-deep-orange-700: #e64a19;
  --md-deep-orange-800: #d84315;
  --md-deep-orange-900: #bf360c;
  --md-deep-orange-A100: #ff9e80;
  --md-deep-orange-A200: #ff6e40;
  --md-deep-orange-A400: #ff3d00;
  --md-deep-orange-A700: #dd2c00;
  --md-brown-50: #efebe9;
  --md-brown-100: #d7ccc8;
  --md-brown-200: #bcaaa4;
  --md-brown-300: #a1887f;
  --md-brown-400: #8d6e63;
  --md-brown-500: #795548;
  --md-brown-600: #6d4c41;
  --md-brown-700: #5d4037;
  --md-brown-800: #4e342e;
  --md-brown-900: #3e2723;
  --md-grey-50: #fafafa;
  --md-grey-100: #f5f5f5;
  --md-grey-200: #eee;
  --md-grey-300: #e0e0e0;
  --md-grey-400: #bdbdbd;
  --md-grey-500: #9e9e9e;
  --md-grey-600: #757575;
  --md-grey-700: #616161;
  --md-grey-800: #424242;
  --md-grey-900: #212121;
  --md-blue-grey-50: #eceff1;
  --md-blue-grey-100: #cfd8dc;
  --md-blue-grey-200: #b0bec5;
  --md-blue-grey-300: #90a4ae;
  --md-blue-grey-400: #78909c;
  --md-blue-grey-500: #607d8b;
  --md-blue-grey-600: #546e7a;
  --md-blue-grey-700: #455a64;
  --md-blue-grey-800: #37474f;
  --md-blue-grey-900: #263238;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2017, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| RenderedText
|----------------------------------------------------------------------------*/

:root {
  /* This is the padding value to fill the gaps between lines containing spans with background color. */
  --jp-private-code-span-padding: calc(
    (var(--jp-code-line-height) - 1) * var(--jp-code-font-size) / 2
  );
}

.jp-RenderedText {
  text-align: left;
  padding-left: var(--jp-code-padding);
  line-height: var(--jp-code-line-height);
  font-family: var(--jp-code-font-family);
}

.jp-RenderedText pre,
.jp-RenderedJavaScript pre,
.jp-RenderedHTMLCommon pre {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-code-font-size);
  border: none;
  margin: 0;
  padding: 0;
}

.jp-RenderedText pre a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

.jp-RenderedText pre a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}

.jp-RenderedText pre a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* console foregrounds and backgrounds */
.jp-RenderedText pre .ansi-black-fg {
  color: #3e424d;
}

.jp-RenderedText pre .ansi-red-fg {
  color: #e75c58;
}

.jp-RenderedText pre .ansi-green-fg {
  color: #00a250;
}

.jp-RenderedText pre .ansi-yellow-fg {
  color: #ddb62b;
}

.jp-RenderedText pre .ansi-blue-fg {
  color: #208ffb;
}

.jp-RenderedText pre .ansi-magenta-fg {
  color: #d160c4;
}

.jp-RenderedText pre .ansi-cyan-fg {
  color: #60c6c8;
}

.jp-RenderedText pre .ansi-white-fg {
  color: #c5c1b4;
}

.jp-RenderedText pre .ansi-black-bg {
  background-color: #3e424d;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-red-bg {
  background-color: #e75c58;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-green-bg {
  background-color: #00a250;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-yellow-bg {
  background-color: #ddb62b;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-blue-bg {
  background-color: #208ffb;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-magenta-bg {
  background-color: #d160c4;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-cyan-bg {
  background-color: #60c6c8;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-white-bg {
  background-color: #c5c1b4;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-black-intense-fg {
  color: #282c36;
}

.jp-RenderedText pre .ansi-red-intense-fg {
  color: #b22b31;
}

.jp-RenderedText pre .ansi-green-intense-fg {
  color: #007427;
}

.jp-RenderedText pre .ansi-yellow-intense-fg {
  color: #b27d12;
}

.jp-RenderedText pre .ansi-blue-intense-fg {
  color: #0065ca;
}

.jp-RenderedText pre .ansi-magenta-intense-fg {
  color: #a03196;
}

.jp-RenderedText pre .ansi-cyan-intense-fg {
  color: #258f8f;
}

.jp-RenderedText pre .ansi-white-intense-fg {
  color: #a1a6b2;
}

.jp-RenderedText pre .ansi-black-intense-bg {
  background-color: #282c36;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-red-intense-bg {
  background-color: #b22b31;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-green-intense-bg {
  background-color: #007427;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-yellow-intense-bg {
  background-color: #b27d12;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-blue-intense-bg {
  background-color: #0065ca;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-magenta-intense-bg {
  background-color: #a03196;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-cyan-intense-bg {
  background-color: #258f8f;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-white-intense-bg {
  background-color: #a1a6b2;
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-default-inverse-fg {
  color: var(--jp-ui-inverse-font-color0);
}

.jp-RenderedText pre .ansi-default-inverse-bg {
  background-color: var(--jp-inverse-layout-color0);
  padding: var(--jp-private-code-span-padding) 0;
}

.jp-RenderedText pre .ansi-bold {
  font-weight: bold;
}

.jp-RenderedText pre .ansi-underline {
  text-decoration: underline;
}

.jp-RenderedText[data-mime-type='application/vnd.jupyter.stderr'] {
  background: var(--jp-rendermime-error-background);
  padding-top: var(--jp-code-padding);
}

/*-----------------------------------------------------------------------------
| RenderedLatex
|----------------------------------------------------------------------------*/

.jp-RenderedLatex {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);
}

/* Left-justify outputs.*/
.jp-OutputArea-output.jp-RenderedLatex {
  padding: var(--jp-code-padding);
  text-align: left;
}

/*-----------------------------------------------------------------------------
| RenderedHTML
|----------------------------------------------------------------------------*/

.jp-RenderedHTMLCommon {
  color: var(--jp-content-font-color1);
  font-family: var(--jp-content-font-family);
  font-size: var(--jp-content-font-size1);
  line-height: var(--jp-content-line-height);

  /* Give a bit more R padding on Markdown text to keep line lengths reasonable */
  padding-right: 20px;
}

.jp-RenderedHTMLCommon em {
  font-style: italic;
}

.jp-RenderedHTMLCommon strong {
  font-weight: bold;
}

.jp-RenderedHTMLCommon u {
  text-decoration: underline;
}

.jp-RenderedHTMLCommon a:link {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:hover {
  text-decoration: underline;
  color: var(--jp-content-link-color);
}

.jp-RenderedHTMLCommon a:visited {
  text-decoration: none;
  color: var(--jp-content-link-color);
}

/* Headings */

.jp-RenderedHTMLCommon h1,
.jp-RenderedHTMLCommon h2,
.jp-RenderedHTMLCommon h3,
.jp-RenderedHTMLCommon h4,
.jp-RenderedHTMLCommon h5,
.jp-RenderedHTMLCommon h6 {
  line-height: var(--jp-content-heading-line-height);
  font-weight: var(--jp-content-heading-font-weight);
  font-style: normal;
  margin: var(--jp-content-heading-margin-top) 0
    var(--jp-content-heading-margin-bottom) 0;
}

.jp-RenderedHTMLCommon h1:first-child,
.jp-RenderedHTMLCommon h2:first-child,
.jp-RenderedHTMLCommon h3:first-child,
.jp-RenderedHTMLCommon h4:first-child,
.jp-RenderedHTMLCommon h5:first-child,
.jp-RenderedHTMLCommon h6:first-child {
  margin-top: calc(0.5 * var(--jp-content-heading-margin-top));
}

.jp-RenderedHTMLCommon h1:last-child,
.jp-RenderedHTMLCommon h2:last-child,
.jp-RenderedHTMLCommon h3:last-child,
.jp-RenderedHTMLCommon h4:last-child,
.jp-RenderedHTMLCommon h5:last-child,
.jp-RenderedHTMLCommon h6:last-child {
  margin-bottom: calc(0.5 * var(--jp-content-heading-margin-bottom));
}

.jp-RenderedHTMLCommon h1 {
  font-size: var(--jp-content-font-size5);
}

.jp-RenderedHTMLCommon h2 {
  font-size: var(--jp-content-font-size4);
}

.jp-RenderedHTMLCommon h3 {
  font-size: var(--jp-content-font-size3);
}

.jp-RenderedHTMLCommon h4 {
  font-size: var(--jp-content-font-size2);
}

.jp-RenderedHTMLCommon h5 {
  font-size: var(--jp-content-font-size1);
}

.jp-RenderedHTMLCommon h6 {
  font-size: var(--jp-content-font-size0);
}

/* Lists */

/* stylelint-disable selector-max-type, selector-max-compound-selectors */

.jp-RenderedHTMLCommon ul:not(.list-inline),
.jp-RenderedHTMLCommon ol:not(.list-inline) {
  padding-left: 2em;
}

.jp-RenderedHTMLCommon ul {
  list-style: disc;
}

.jp-RenderedHTMLCommon ul ul {
  list-style: square;
}

.jp-RenderedHTMLCommon ul ul ul {
  list-style: circle;
}

.jp-RenderedHTMLCommon ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol ol {
  list-style: upper-alpha;
}

.jp-RenderedHTMLCommon ol ol ol {
  list-style: lower-alpha;
}

.jp-RenderedHTMLCommon ol ol ol ol {
  list-style: lower-roman;
}

.jp-RenderedHTMLCommon ol ol ol ol ol {
  list-style: decimal;
}

.jp-RenderedHTMLCommon ol,
.jp-RenderedHTMLCommon ul {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon ul ul,
.jp-RenderedHTMLCommon ul ol,
.jp-RenderedHTMLCommon ol ul,
.jp-RenderedHTMLCommon ol ol {
  margin-bottom: 0;
}

/* stylelint-enable selector-max-type, selector-max-compound-selectors */

.jp-RenderedHTMLCommon hr {
  color: var(--jp-border-color2);
  background-color: var(--jp-border-color1);
  margin-top: 1em;
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon > pre {
  margin: 1.5em 2em;
}

.jp-RenderedHTMLCommon pre,
.jp-RenderedHTMLCommon code {
  border: 0;
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  line-height: var(--jp-code-line-height);
  padding: 0;
  white-space: pre-wrap;
}

.jp-RenderedHTMLCommon :not(pre) > code {
  background-color: var(--jp-layout-color2);
  padding: 1px 5px;
}

/* Tables */

.jp-RenderedHTMLCommon table {
  border-collapse: collapse;
  border-spacing: 0;
  border: none;
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  table-layout: fixed;
  margin-left: auto;
  margin-bottom: 1em;
  margin-right: auto;
}

.jp-RenderedHTMLCommon thead {
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  vertical-align: bottom;
}

.jp-RenderedHTMLCommon td,
.jp-RenderedHTMLCommon th,
.jp-RenderedHTMLCommon tr {
  vertical-align: middle;
  padding: 0.5em;
  line-height: normal;
  white-space: normal;
  max-width: none;
  border: none;
}

.jp-RenderedMarkdown.jp-RenderedHTMLCommon td,
.jp-RenderedMarkdown.jp-RenderedHTMLCommon th {
  max-width: none;
}

:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon td,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon th,
:not(.jp-RenderedMarkdown).jp-RenderedHTMLCommon tr {
  text-align: right;
}

.jp-RenderedHTMLCommon th {
  font-weight: bold;
}

.jp-RenderedHTMLCommon tbody tr:nth-child(odd) {
  background: var(--jp-layout-color0);
}

.jp-RenderedHTMLCommon tbody tr:nth-child(even) {
  background: var(--jp-rendermime-table-row-background);
}

.jp-RenderedHTMLCommon tbody tr:hover {
  background: var(--jp-rendermime-table-row-hover-background);
}

.jp-RenderedHTMLCommon p {
  text-align: left;
  margin: 0;
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon img {
  -moz-force-broken-image-icon: 1;
}

/* Restrict to direct children as other images could be nested in other content. */
.jp-RenderedHTMLCommon > img {
  display: block;
  margin-left: 0;
  margin-right: 0;
  margin-bottom: 1em;
}

/* Change color behind transparent images if they need it... */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-light-background {
  background-color: var(--jp-inverse-layout-color1);
}

[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-dark-background {
  background-color: var(--jp-inverse-layout-color1);
}

.jp-RenderedHTMLCommon img,
.jp-RenderedImage img,
.jp-RenderedHTMLCommon svg,
.jp-RenderedSVG svg {
  max-width: 100%;
  height: auto;
}

.jp-RenderedHTMLCommon img.jp-mod-unconfined,
.jp-RenderedImage img.jp-mod-unconfined,
.jp-RenderedHTMLCommon svg.jp-mod-unconfined,
.jp-RenderedSVG svg.jp-mod-unconfined {
  max-width: none;
}

.jp-RenderedHTMLCommon .alert {
  padding: var(--jp-notebook-padding);
  border: var(--jp-border-width) solid transparent;
  border-radius: var(--jp-border-radius);
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon .alert-info {
  color: var(--jp-info-color0);
  background-color: var(--jp-info-color3);
  border-color: var(--jp-info-color2);
}

.jp-RenderedHTMLCommon .alert-info hr {
  border-color: var(--jp-info-color3);
}

.jp-RenderedHTMLCommon .alert-info > p:last-child,
.jp-RenderedHTMLCommon .alert-info > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-warning {
  color: var(--jp-warn-color0);
  background-color: var(--jp-warn-color3);
  border-color: var(--jp-warn-color2);
}

.jp-RenderedHTMLCommon .alert-warning hr {
  border-color: var(--jp-warn-color3);
}

.jp-RenderedHTMLCommon .alert-warning > p:last-child,
.jp-RenderedHTMLCommon .alert-warning > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-success {
  color: var(--jp-success-color0);
  background-color: var(--jp-success-color3);
  border-color: var(--jp-success-color2);
}

.jp-RenderedHTMLCommon .alert-success hr {
  border-color: var(--jp-success-color3);
}

.jp-RenderedHTMLCommon .alert-success > p:last-child,
.jp-RenderedHTMLCommon .alert-success > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon .alert-danger {
  color: var(--jp-error-color0);
  background-color: var(--jp-error-color3);
  border-color: var(--jp-error-color2);
}

.jp-RenderedHTMLCommon .alert-danger hr {
  border-color: var(--jp-error-color3);
}

.jp-RenderedHTMLCommon .alert-danger > p:last-child,
.jp-RenderedHTMLCommon .alert-danger > ul:last-child {
  margin-bottom: 0;
}

.jp-RenderedHTMLCommon blockquote {
  margin: 1em 2em;
  padding: 0 1em;
  border-left: 5px solid var(--jp-border-color2);
}

a.jp-InternalAnchorLink {
  visibility: hidden;
  margin-left: 8px;
  color: var(--md-blue-800);
}

h1:hover .jp-InternalAnchorLink,
h2:hover .jp-InternalAnchorLink,
h3:hover .jp-InternalAnchorLink,
h4:hover .jp-InternalAnchorLink,
h5:hover .jp-InternalAnchorLink,
h6:hover .jp-InternalAnchorLink {
  visibility: visible;
}

.jp-RenderedHTMLCommon kbd {
  background-color: var(--jp-rendermime-table-row-background);
  border: 1px solid var(--jp-border-color0);
  border-bottom-color: var(--jp-border-color2);
  border-radius: 3px;
  box-shadow: inset 0 -1px 0 rgba(0, 0, 0, 0.25);
  display: inline-block;
  font-size: var(--jp-ui-font-size0);
  line-height: 1em;
  padding: 0.2em 0.5em;
}

/* Most direct children of .jp-RenderedHTMLCommon have a margin-bottom of 1.0.
 * At the bottom of cells this is a bit too much as there is also spacing
 * between cells. Going all the way to 0 gets too tight between markdown and
 * code cells.
 */
.jp-RenderedHTMLCommon > *:last-child {
  margin-bottom: 0.5em;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

.lm-cursor-backdrop {
  position: fixed;
  width: 200px;
  height: 200px;
  margin-top: -100px;
  margin-left: -100px;
  will-change: transform;
  z-index: 100;
}

.lm-mod-drag-image {
  will-change: transform;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

.jp-lineFormSearch {
  padding: 4px 12px;
  background-color: var(--jp-layout-color2);
  box-shadow: var(--jp-toolbar-box-shadow);
  z-index: 2;
  font-size: var(--jp-ui-font-size1);
}

.jp-lineFormCaption {
  font-size: var(--jp-ui-font-size0);
  line-height: var(--jp-ui-font-size1);
  margin-top: 4px;
  color: var(--jp-ui-font-color0);
}

.jp-baseLineForm {
  border: none;
  border-radius: 0;
  position: absolute;
  background-size: 16px;
  background-repeat: no-repeat;
  background-position: center;
  outline: none;
}

.jp-lineFormButtonContainer {
  top: 4px;
  right: 8px;
  height: 24px;
  padding: 0 12px;
  width: 12px;
}

.jp-lineFormButtonIcon {
  top: 0;
  right: 0;
  background-color: var(--jp-brand-color1);
  height: 100%;
  width: 100%;
  box-sizing: border-box;
  padding: 4px 6px;
}

.jp-lineFormButton {
  top: 0;
  right: 0;
  background-color: transparent;
  height: 100%;
  width: 100%;
  box-sizing: border-box;
}

.jp-lineFormWrapper {
  overflow: hidden;
  padding: 0 8px;
  border: 1px solid var(--jp-border-color0);
  background-color: var(--jp-input-active-background);
  height: 22px;
}

.jp-lineFormWrapperFocusWithin {
  border: var(--jp-border-width) solid var(--md-blue-500);
  box-shadow: inset 0 0 4px var(--md-blue-300);
}

.jp-lineFormInput {
  background: transparent;
  width: 200px;
  height: 100%;
  border: none;
  outline: none;
  color: var(--jp-ui-font-color0);
  line-height: 28px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-JSONEditor {
  display: flex;
  flex-direction: column;
  width: 100%;
}

.jp-JSONEditor-host {
  flex: 1 1 auto;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0;
  background: var(--jp-layout-color0);
  min-height: 50px;
  padding: 1px;
}

.jp-JSONEditor.jp-mod-error .jp-JSONEditor-host {
  border-color: red;
  outline-color: red;
}

.jp-JSONEditor-header {
  display: flex;
  flex: 1 0 auto;
  padding: 0 0 0 12px;
}

.jp-JSONEditor-header label {
  flex: 0 0 auto;
}

.jp-JSONEditor-commitButton {
  height: 16px;
  width: 16px;
  background-size: 18px;
  background-repeat: no-repeat;
  background-position: center;
}

.jp-JSONEditor-host.jp-mod-focused {
  background-color: var(--jp-input-active-background);
  border: 1px solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

.jp-Editor.jp-mod-dropTarget {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/
.jp-DocumentSearch-input {
  border: none;
  outline: none;
  color: var(--jp-ui-font-color0);
  font-size: var(--jp-ui-font-size1);
  background-color: var(--jp-layout-color0);
  font-family: var(--jp-ui-font-family);
  padding: 2px 1px;
  resize: none;
}

.jp-DocumentSearch-overlay {
  position: absolute;
  background-color: var(--jp-toolbar-background);
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  border-left: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  top: 0;
  right: 0;
  z-index: 7;
  min-width: 405px;
  padding: 2px;
  font-size: var(--jp-ui-font-size1);

  --jp-private-document-search-button-height: 20px;
}

.jp-DocumentSearch-overlay button {
  background-color: var(--jp-toolbar-background);
  outline: 0;
}

.jp-DocumentSearch-overlay button:hover {
  background-color: var(--jp-layout-color2);
}

.jp-DocumentSearch-overlay button:active {
  background-color: var(--jp-layout-color3);
}

.jp-DocumentSearch-overlay-row {
  display: flex;
  align-items: center;
  margin-bottom: 2px;
}

.jp-DocumentSearch-button-content {
  display: inline-block;
  cursor: pointer;
  box-sizing: border-box;
  width: 100%;
  height: 100%;
}

.jp-DocumentSearch-button-content svg {
  width: 100%;
  height: 100%;
}

.jp-DocumentSearch-input-wrapper {
  border: var(--jp-border-width) solid var(--jp-border-color0);
  display: flex;
  background-color: var(--jp-layout-color0);
  margin: 2px;
}

.jp-DocumentSearch-input-wrapper:focus-within {
  border-color: var(--jp-cell-editor-active-border-color);
}

.jp-DocumentSearch-toggle-wrapper,
.jp-DocumentSearch-button-wrapper {
  all: initial;
  overflow: hidden;
  display: inline-block;
  border: none;
  box-sizing: border-box;
}

.jp-DocumentSearch-toggle-wrapper {
  width: 14px;
  height: 14px;
}

.jp-DocumentSearch-button-wrapper {
  width: var(--jp-private-document-search-button-height);
  height: var(--jp-private-document-search-button-height);
}

.jp-DocumentSearch-toggle-wrapper:focus,
.jp-DocumentSearch-button-wrapper:focus {
  outline: var(--jp-border-width) solid
    var(--jp-cell-editor-active-border-color);
  outline-offset: -1px;
}

.jp-DocumentSearch-toggle-wrapper,
.jp-DocumentSearch-button-wrapper,
.jp-DocumentSearch-button-content:focus {
  outline: none;
}

.jp-DocumentSearch-toggle-placeholder {
  width: 5px;
}

.jp-DocumentSearch-input-button::before {
  display: block;
  padding-top: 100%;
}

.jp-DocumentSearch-input-button-off {
  opacity: var(--jp-search-toggle-off-opacity);
}

.jp-DocumentSearch-input-button-off:hover {
  opacity: var(--jp-search-toggle-hover-opacity);
}

.jp-DocumentSearch-input-button-on {
  opacity: var(--jp-search-toggle-on-opacity);
}

.jp-DocumentSearch-index-counter {
  padding-left: 10px;
  padding-right: 10px;
  user-select: none;
  min-width: 35px;
  display: inline-block;
}

.jp-DocumentSearch-up-down-wrapper {
  display: inline-block;
  padding-right: 2px;
  margin-left: auto;
  white-space: nowrap;
}

.jp-DocumentSearch-spacer {
  margin-left: auto;
}

.jp-DocumentSearch-up-down-wrapper button {
  outline: 0;
  border: none;
  width: var(--jp-private-document-search-button-height);
  height: var(--jp-private-document-search-button-height);
  vertical-align: middle;
  margin: 1px 5px 2px;
}

.jp-DocumentSearch-up-down-button:hover {
  background-color: var(--jp-layout-color2);
}

.jp-DocumentSearch-up-down-button:active {
  background-color: var(--jp-layout-color3);
}

.jp-DocumentSearch-filter-button {
  border-radius: var(--jp-border-radius);
}

.jp-DocumentSearch-filter-button:hover {
  background-color: var(--jp-layout-color2);
}

.jp-DocumentSearch-filter-button-enabled {
  background-color: var(--jp-layout-color2);
}

.jp-DocumentSearch-filter-button-enabled:hover {
  background-color: var(--jp-layout-color3);
}

.jp-DocumentSearch-search-options {
  padding: 0 8px;
  margin-left: 3px;
  width: 100%;
  display: grid;
  justify-content: start;
  grid-template-columns: 1fr 1fr;
  align-items: center;
  justify-items: stretch;
}

.jp-DocumentSearch-search-filter-disabled {
  color: var(--jp-ui-font-color2);
}

.jp-DocumentSearch-search-filter {
  display: flex;
  align-items: center;
  user-select: none;
}

.jp-DocumentSearch-regex-error {
  color: var(--jp-error-color0);
}

.jp-DocumentSearch-replace-button-wrapper {
  overflow: hidden;
  display: inline-block;
  box-sizing: border-box;
  border: var(--jp-border-width) solid var(--jp-border-color0);
  margin: auto 2px;
  padding: 1px 4px;
  height: calc(var(--jp-private-document-search-button-height) + 2px);
}

.jp-DocumentSearch-replace-button-wrapper:focus {
  border: var(--jp-border-width) solid var(--jp-cell-editor-active-border-color);
}

.jp-DocumentSearch-replace-button {
  display: inline-block;
  text-align: center;
  cursor: pointer;
  box-sizing: border-box;
  color: var(--jp-ui-font-color1);

  /* height - 2 * (padding of wrapper) */
  line-height: calc(var(--jp-private-document-search-button-height) - 2px);
  width: 100%;
  height: 100%;
}

.jp-DocumentSearch-replace-button:focus {
  outline: none;
}

.jp-DocumentSearch-replace-wrapper-class {
  margin-left: 14px;
  display: flex;
}

.jp-DocumentSearch-replace-toggle {
  border: none;
  background-color: var(--jp-toolbar-background);
  border-radius: var(--jp-border-radius);
}

.jp-DocumentSearch-replace-toggle:hover {
  background-color: var(--jp-layout-color2);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.cm-editor {
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  border: 0;
  border-radius: 0;
  height: auto;

  /* Changed to auto to autogrow */
}

.cm-editor pre {
  padding: 0 var(--jp-code-padding);
}

.jp-CodeMirrorEditor[data-type='inline'] .cm-dialog {
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

.jp-CodeMirrorEditor {
  cursor: text;
}

/* When zoomed out 67% and 33% on a screen of 1440 width x 900 height */
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .jp-CodeMirrorEditor[data-type='inline'] .cm-cursor {
    border-left: var(--jp-code-cursor-width1) solid
      var(--jp-editor-cursor-color);
  }
}

/* When zoomed out less than 33% */
@media screen and (min-width: 4320px) {
  .jp-CodeMirrorEditor[data-type='inline'] .cm-cursor {
    border-left: var(--jp-code-cursor-width2) solid
      var(--jp-editor-cursor-color);
  }
}

.cm-editor.jp-mod-readOnly .cm-cursor {
  display: none;
}

.jp-CollaboratorCursor {
  border-left: 5px solid transparent;
  border-right: 5px solid transparent;
  border-top: none;
  border-bottom: 3px solid;
  background-clip: content-box;
  margin-left: -5px;
  margin-right: -5px;
}

.cm-searching,
.cm-searching span {
  /* `.cm-searching span`: we need to override syntax highlighting */
  background-color: var(--jp-search-unselected-match-background-color);
  color: var(--jp-search-unselected-match-color);
}

.cm-searching::selection,
.cm-searching span::selection {
  background-color: var(--jp-search-unselected-match-background-color);
  color: var(--jp-search-unselected-match-color);
}

.jp-current-match > .cm-searching,
.jp-current-match > .cm-searching span,
.cm-searching > .jp-current-match,
.cm-searching > .jp-current-match span {
  background-color: var(--jp-search-selected-match-background-color);
  color: var(--jp-search-selected-match-color);
}

.jp-current-match > .cm-searching::selection,
.cm-searching > .jp-current-match::selection,
.jp-current-match > .cm-searching span::selection {
  background-color: var(--jp-search-selected-match-background-color);
  color: var(--jp-search-selected-match-color);
}

.cm-trailingspace {
  background-image: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAgAAAAFCAYAAAB4ka1VAAAAsElEQVQIHQGlAFr/AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA7+r3zKmT0/+pk9P/7+r3zAAAAAAAAAAABAAAAAAAAAAA6OPzM+/q9wAAAAAA6OPzMwAAAAAAAAAAAgAAAAAAAAAAGR8NiRQaCgAZIA0AGR8NiQAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAQyoYJ/SY80UAAAAASUVORK5CYII=);
  background-position: center left;
  background-repeat: repeat-x;
}

.jp-CollaboratorCursor-hover {
  position: absolute;
  z-index: 1;
  transform: translateX(-50%);
  color: white;
  border-radius: 3px;
  padding-left: 4px;
  padding-right: 4px;
  padding-top: 1px;
  padding-bottom: 1px;
  text-align: center;
  font-size: var(--jp-ui-font-size1);
  white-space: nowrap;
}

.jp-CodeMirror-ruler {
  border-left: 1px dashed var(--jp-border-color2);
}

/* Styles for shared cursors (remote cursor locations and selected ranges) */
.jp-CodeMirrorEditor .cm-ySelectionCaret {
  position: relative;
  border-left: 1px solid black;
  margin-left: -1px;
  margin-right: -1px;
  box-sizing: border-box;
}

.jp-CodeMirrorEditor .cm-ySelectionCaret > .cm-ySelectionInfo {
  white-space: nowrap;
  position: absolute;
  top: -1.15em;
  padding-bottom: 0.05em;
  left: -1px;
  font-size: 0.95em;
  font-family: var(--jp-ui-font-family);
  font-weight: bold;
  line-height: normal;
  user-select: none;
  color: white;
  padding-left: 2px;
  padding-right: 2px;
  z-index: 101;
  transition: opacity 0.3s ease-in-out;
}

.jp-CodeMirrorEditor .cm-ySelectionInfo {
  transition-delay: 0.7s;
  opacity: 0;
}

.jp-CodeMirrorEditor .cm-ySelectionCaret:hover > .cm-ySelectionInfo {
  opacity: 1;
  transition-delay: 0s;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-MimeDocument {
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-filebrowser-button-height: 28px;
  --jp-private-filebrowser-button-width: 48px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-FileBrowser .jp-SidePanel-content {
  display: flex;
  flex-direction: column;
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  flex-wrap: wrap;
  row-gap: 12px;
  border-bottom: none;
  height: auto;
  margin: 8px 12px 0;
  box-shadow: none;
  padding: 0;
  justify-content: flex-start;
}

.jp-FileBrowser-Panel {
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
}

.jp-BreadCrumbs {
  flex: 0 0 auto;
  margin: 8px 12px;
}

.jp-BreadCrumbs-item {
  margin: 0 2px;
  padding: 0 2px;
  border-radius: var(--jp-border-radius);
  cursor: pointer;
}

.jp-BreadCrumbs-item:hover {
  background-color: var(--jp-layout-color2);
}

.jp-BreadCrumbs-item:first-child {
  margin-left: 0;
}

.jp-BreadCrumbs-item.jp-mod-dropTarget {
  background-color: var(--jp-brand-color2);
  opacity: 0.7;
}

/*-----------------------------------------------------------------------------
| Buttons
|----------------------------------------------------------------------------*/

.jp-FileBrowser-toolbar > .jp-Toolbar-item {
  flex: 0 0 auto;
  padding-left: 0;
  padding-right: 2px;
  align-items: center;
  height: unset;
}

.jp-FileBrowser-toolbar > .jp-Toolbar-item .jp-ToolbarButtonComponent {
  width: 40px;
}

/*-----------------------------------------------------------------------------
| Other styles
|----------------------------------------------------------------------------*/

.jp-FileDialog.jp-mod-conflict input {
  color: var(--jp-error-color1);
}

.jp-FileDialog .jp-new-name-title {
  margin-top: 12px;
}

.jp-LastModified-hidden {
  display: none;
}

.jp-FileSize-hidden {
  display: none;
}

.jp-FileBrowser .lm-AccordionPanel > h3:first-child {
  display: none;
}

/*-----------------------------------------------------------------------------
| DirListing
|----------------------------------------------------------------------------*/

.jp-DirListing {
  flex: 1 1 auto;
  display: flex;
  flex-direction: column;
  outline: 0;
}

.jp-DirListing-header {
  flex: 0 0 auto;
  display: flex;
  flex-direction: row;
  align-items: center;
  overflow: hidden;
  border-top: var(--jp-border-width) solid var(--jp-border-color2);
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  box-shadow: var(--jp-toolbar-box-shadow);
  z-index: 2;
}

.jp-DirListing-headerItem {
  padding: 4px 12px 2px;
  font-weight: 500;
}

.jp-DirListing-headerItem:hover {
  background: var(--jp-layout-color2);
}

.jp-DirListing-headerItem.jp-id-name {
  flex: 1 0 84px;
}

.jp-DirListing-headerItem.jp-id-modified {
  flex: 0 0 112px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
}

.jp-DirListing-headerItem.jp-id-filesize {
  flex: 0 0 75px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
}

.jp-id-narrow {
  display: none;
  flex: 0 0 5px;
  padding: 4px;
  border-left: var(--jp-border-width) solid var(--jp-border-color2);
  text-align: right;
  color: var(--jp-border-color2);
}

.jp-DirListing-narrow .jp-id-narrow {
  display: block;
}

.jp-DirListing-narrow .jp-id-modified,
.jp-DirListing-narrow .jp-DirListing-itemModified {
  display: none;
}

.jp-DirListing-headerItem.jp-mod-selected {
  font-weight: 600;
}

/* increase specificity to override bundled default */
.jp-DirListing-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

.jp-DirListing-content mark {
  color: var(--jp-ui-font-color0);
  background-color: transparent;
  font-weight: bold;
}

.jp-DirListing-content .jp-DirListing-item.jp-mod-selected mark {
  color: var(--jp-ui-inverse-font-color0);
}

/* Style the directory listing content when a user drops a file to upload */
.jp-DirListing.jp-mod-native-drop .jp-DirListing-content {
  outline: 5px dashed rgba(128, 128, 128, 0.5);
  outline-offset: -10px;
  cursor: copy;
}

.jp-DirListing-item {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 4px 12px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-DirListing-checkboxWrapper {
  /* Increases hit area of checkbox. */
  padding: 4px;
}

.jp-DirListing-header
  .jp-DirListing-checkboxWrapper
  + .jp-DirListing-headerItem {
  padding-left: 4px;
}

.jp-DirListing-content .jp-DirListing-checkboxWrapper {
  position: relative;
  left: -4px;
  margin: -4px 0 -4px -8px;
}

.jp-DirListing-checkboxWrapper.jp-mod-visible {
  visibility: visible;
}

/* For devices that support hovering, hide checkboxes until hovered, selected...
*/
@media (hover: hover) {
  .jp-DirListing-checkboxWrapper {
    visibility: hidden;
  }

  .jp-DirListing-item:hover .jp-DirListing-checkboxWrapper,
  .jp-DirListing-item.jp-mod-selected .jp-DirListing-checkboxWrapper {
    visibility: visible;
  }
}

.jp-DirListing-item[data-is-dot] {
  opacity: 75%;
}

.jp-DirListing-item.jp-mod-selected {
  color: var(--jp-ui-inverse-font-color1);
  background: var(--jp-brand-color1);
}

.jp-DirListing-item.jp-mod-dropTarget {
  background: var(--jp-brand-color3);
}

.jp-DirListing-item:hover:not(.jp-mod-selected) {
  background: var(--jp-layout-color2);
}

.jp-DirListing-itemIcon {
  flex: 0 0 20px;
  margin-right: 4px;
}

.jp-DirListing-itemText {
  flex: 1 0 64px;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  user-select: none;
}

.jp-DirListing-itemText:focus {
  outline-width: 2px;
  outline-color: var(--jp-inverse-layout-color1);
  outline-style: solid;
  outline-offset: 1px;
}

.jp-DirListing-item.jp-mod-selected .jp-DirListing-itemText:focus {
  outline-color: var(--jp-layout-color1);
}

.jp-DirListing-itemModified {
  flex: 0 0 125px;
  text-align: right;
}

.jp-DirListing-itemFileSize {
  flex: 0 0 90px;
  text-align: right;
}

.jp-DirListing-editor {
  flex: 1 0 64px;
  outline: none;
  border: none;
  color: var(--jp-ui-font-color1);
  background-color: var(--jp-layout-color1);
}

.jp-DirListing-item.jp-mod-running .jp-DirListing-itemIcon::before {
  color: var(--jp-success-color1);
  content: '\25CF';
  font-size: 8px;
  position: absolute;
  left: -8px;
}

.jp-DirListing-item.jp-mod-running.jp-mod-selected
  .jp-DirListing-itemIcon::before {
  color: var(--jp-ui-inverse-font-color1);
}

.jp-DirListing-item.lm-mod-drag-image,
.jp-DirListing-item.jp-mod-selected.lm-mod-drag-image {
  font-size: var(--jp-ui-font-size1);
  padding-left: 4px;
  margin-left: 4px;
  width: 160px;
  background-color: var(--jp-ui-inverse-font-color2);
  box-shadow: var(--jp-elevation-z2);
  border-radius: 0;
  color: var(--jp-ui-font-color1);
  transform: translateX(-40%) translateY(-58%);
}

.jp-Document {
  min-width: 120px;
  min-height: 120px;
  outline: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Main OutputArea
| OutputArea has a list of Outputs
|----------------------------------------------------------------------------*/

.jp-OutputArea {
  overflow-y: auto;
}

.jp-OutputArea-child {
  display: table;
  table-layout: fixed;
  width: 100%;
  overflow: hidden;
}

.jp-OutputPrompt {
  width: var(--jp-cell-prompt-width);
  color: var(--jp-cell-outprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
  opacity: var(--jp-cell-prompt-opacity);

  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;

  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-OutputArea-prompt {
  display: table-cell;
  vertical-align: top;
}

.jp-OutputArea-output {
  display: table-cell;
  width: 100%;
  height: auto;
  overflow: auto;
  user-select: text;
  -moz-user-select: text;
  -webkit-user-select: text;
  -ms-user-select: text;
}

.jp-OutputArea .jp-RenderedText {
  padding-left: 1ch;
}

/**
 * Prompt overlay.
 */

.jp-OutputArea-promptOverlay {
  position: absolute;
  top: 0;
  width: var(--jp-cell-prompt-width);
  height: 100%;
  opacity: 0.5;
}

.jp-OutputArea-promptOverlay:hover {
  background: var(--jp-layout-color2);
  box-shadow: inset 0 0 1px var(--jp-inverse-layout-color0);
  cursor: zoom-out;
}

.jp-mod-outputsScrolled .jp-OutputArea-promptOverlay:hover {
  cursor: zoom-in;
}

/**
 * Isolated output.
 */
.jp-OutputArea-output.jp-mod-isolated {
  width: 100%;
  display: block;
}

/*
When drag events occur, `lm-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated {
  position: relative;
}

body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: transparent;
}

/* pre */

.jp-OutputArea-output pre {
  border: none;
  margin: 0;
  padding: 0;
  overflow-x: auto;
  overflow-y: auto;
  word-break: break-all;
  word-wrap: break-word;
  white-space: pre-wrap;
}

/* tables */

.jp-OutputArea-output.jp-RenderedHTMLCommon table {
  margin-left: 0;
  margin-right: 0;
}

/* description lists */

.jp-OutputArea-output dl,
.jp-OutputArea-output dt,
.jp-OutputArea-output dd {
  display: block;
}

.jp-OutputArea-output dl {
  width: 100%;
  overflow: hidden;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dt {
  font-weight: bold;
  float: left;
  width: 20%;
  padding: 0;
  margin: 0;
}

.jp-OutputArea-output dd {
  float: left;
  width: 80%;
  padding: 0;
  margin: 0;
}

.jp-TrimmedOutputs pre {
  background: var(--jp-layout-color3);
  font-size: calc(var(--jp-code-font-size) * 1.4);
  text-align: center;
  text-transform: uppercase;
}

/* Hide the gutter in case of
 *  - nested output areas (e.g. in the case of output widgets)
 *  - mirrored output areas
 */
.jp-OutputArea .jp-OutputArea .jp-OutputArea-prompt {
  display: none;
}

/* Hide empty lines in the output area, for instance due to cleared widgets */
.jp-OutputArea-prompt:empty {
  padding: 0;
  border: 0;
}

/*-----------------------------------------------------------------------------
| executeResult is added to any Output-result for the display of the object
| returned by a cell
|----------------------------------------------------------------------------*/

.jp-OutputArea-output.jp-OutputArea-executeResult {
  margin-left: 0;
  width: 100%;
}

/* Text output with the Out[] prompt needs a top padding to match the
 * alignment of the Out[] prompt itself.
 */
.jp-OutputArea-executeResult .jp-RenderedText.jp-OutputArea-output {
  padding-top: var(--jp-code-padding);
  border-top: var(--jp-border-width) solid transparent;
}

/*-----------------------------------------------------------------------------
| The Stdin output
|----------------------------------------------------------------------------*/

.jp-Stdin-prompt {
  color: var(--jp-content-font-color0);
  padding-right: var(--jp-code-padding);
  vertical-align: baseline;
  flex: 0 0 auto;
}

.jp-Stdin-input {
  font-family: var(--jp-code-font-family);
  font-size: inherit;
  color: inherit;
  background-color: inherit;
  width: 42%;
  min-width: 200px;

  /* make sure input baseline aligns with prompt */
  vertical-align: baseline;

  /* padding + margin = 0.5em between prompt and cursor */
  padding: 0 0.25em;
  margin: 0 0.25em;
  flex: 0 0 70%;
}

.jp-Stdin-input::placeholder {
  opacity: 0;
}

.jp-Stdin-input:focus {
  box-shadow: none;
}

.jp-Stdin-input:focus::placeholder {
  opacity: 1;
}

/*-----------------------------------------------------------------------------
| Output Area View
|----------------------------------------------------------------------------*/

.jp-LinkedOutputView .jp-OutputArea {
  height: 100%;
  display: block;
}

.jp-LinkedOutputView .jp-OutputArea-output:only-child {
  height: 100%;
}

/*-----------------------------------------------------------------------------
| Printing
|----------------------------------------------------------------------------*/

@media print {
  .jp-OutputArea-child {
    break-inside: avoid-page;
  }
}

/*-----------------------------------------------------------------------------
| Mobile
|----------------------------------------------------------------------------*/
@media only screen and (max-width: 760px) {
  .jp-OutputPrompt {
    display: table-row;
    text-align: left;
  }

  .jp-OutputArea-child .jp-OutputArea-output {
    display: table-row;
    margin-left: var(--jp-notebook-padding);
  }
}

/* Trimmed outputs warning */
.jp-TrimmedOutputs > a {
  margin: 10px;
  text-decoration: none;
  cursor: pointer;
}

.jp-TrimmedOutputs > a:hover {
  text-decoration: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Table of Contents
|----------------------------------------------------------------------------*/

:root {
  --jp-private-toc-active-width: 4px;
}

.jp-TableOfContents {
  display: flex;
  flex-direction: column;
  background: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  font-size: var(--jp-ui-font-size1);
  height: 100%;
}

.jp-TableOfContents-placeholder {
  text-align: center;
}

.jp-TableOfContents-placeholderContent {
  color: var(--jp-content-font-color2);
  padding: 8px;
}

.jp-TableOfContents-placeholderContent > h3 {
  margin-bottom: var(--jp-content-heading-margin-bottom);
}

.jp-TableOfContents .jp-SidePanel-content {
  overflow-y: auto;
}

.jp-TableOfContents-tree {
  margin: 4px;
}

.jp-TableOfContents ol {
  list-style-type: none;
}

/* stylelint-disable-next-line selector-max-type */
.jp-TableOfContents li > ol {
  /* Align left border with triangle icon center */
  padding-left: 11px;
}

.jp-TableOfContents-content {
  /* left margin for the active heading indicator */
  margin: 0 0 0 var(--jp-private-toc-active-width);
  padding: 0;
  background-color: var(--jp-layout-color1);
}

.jp-tocItem {
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-tocItem-heading {
  display: flex;
  cursor: pointer;
}

.jp-tocItem-heading:hover {
  background-color: var(--jp-layout-color2);
}

.jp-tocItem-content {
  display: block;
  padding: 4px 0;
  white-space: nowrap;
  text-overflow: ellipsis;
  overflow-x: hidden;
}

.jp-tocItem-collapser {
  height: 20px;
  margin: 2px 2px 0;
  padding: 0;
  background: none;
  border: none;
  cursor: pointer;
}

.jp-tocItem-collapser:hover {
  background-color: var(--jp-layout-color3);
}

/* Active heading indicator */

.jp-tocItem-heading::before {
  content: ' ';
  background: transparent;
  width: var(--jp-private-toc-active-width);
  height: 24px;
  position: absolute;
  left: 0;
  border-radius: var(--jp-border-radius);
}

.jp-tocItem-heading.jp-tocItem-active::before {
  background-color: var(--jp-brand-color1);
}

.jp-tocItem-heading:hover.jp-tocItem-active::before {
  background: var(--jp-brand-color0);
  opacity: 1;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapser {
  flex: 0 0 var(--jp-cell-collapser-width);
  padding: 0;
  margin: 0;
  border: none;
  outline: none;
  background: transparent;
  border-radius: var(--jp-border-radius);
  opacity: 1;
}

.jp-Collapser-child {
  display: block;
  width: 100%;
  box-sizing: border-box;

  /* height: 100% doesn't work because the height of its parent is computed from content */
  position: absolute;
  top: 0;
  bottom: 0;
}

/*-----------------------------------------------------------------------------
| Printing
|----------------------------------------------------------------------------*/

/*
Hiding collapsers in print mode.

Note: input and output wrappers have "display: block" propery in print mode.
*/

@media print {
  .jp-Collapser {
    display: none;
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Header/Footer
|----------------------------------------------------------------------------*/

/* Hidden by zero height by default */
.jp-CellHeader,
.jp-CellFooter {
  height: 0;
  width: 100%;
  padding: 0;
  margin: 0;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Input
|----------------------------------------------------------------------------*/

/* All input areas */
.jp-InputArea {
  display: table;
  table-layout: fixed;
  width: 100%;
  overflow: hidden;
}

.jp-InputArea-editor {
  display: table-cell;
  overflow: hidden;
  vertical-align: top;

  /* This is the non-active, default styling */
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  border-radius: 0;
  background: var(--jp-cell-editor-background);
}

.jp-InputPrompt {
  display: table-cell;
  vertical-align: top;
  width: var(--jp-cell-prompt-width);
  color: var(--jp-cell-inprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  opacity: var(--jp-cell-prompt-opacity);
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;

  /* Right align prompt text, don't wrap to handle large prompt numbers */
  text-align: right;
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;

  /* Disable text selection */
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

/*-----------------------------------------------------------------------------
| Mobile
|----------------------------------------------------------------------------*/
@media only screen and (max-width: 760px) {
  .jp-InputArea-editor {
    display: table-row;
    margin-left: var(--jp-notebook-padding);
  }

  .jp-InputPrompt {
    display: table-row;
    text-align: left;
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Placeholder {
  display: table;
  table-layout: fixed;
  width: 100%;
}

.jp-Placeholder-prompt {
  display: table-cell;
  box-sizing: border-box;
}

.jp-Placeholder-content {
  display: table-cell;
  padding: 4px 6px;
  border: 1px solid transparent;
  border-radius: 0;
  background: none;
  box-sizing: border-box;
  cursor: pointer;
}

.jp-Placeholder-contentContainer {
  display: flex;
}

.jp-Placeholder-content:hover,
.jp-InputPlaceholder > .jp-Placeholder-content:hover {
  border-color: var(--jp-layout-color3);
}

.jp-Placeholder-content .jp-MoreHorizIcon {
  width: 32px;
  height: 16px;
  border: 1px solid transparent;
  border-radius: var(--jp-border-radius);
}

.jp-Placeholder-content .jp-MoreHorizIcon:hover {
  border: 1px solid var(--jp-border-color1);
  box-shadow: 0 0 2px 0 rgba(0, 0, 0, 0.25);
  background-color: var(--jp-layout-color0);
}

.jp-PlaceholderText {
  white-space: nowrap;
  overflow-x: hidden;
  color: var(--jp-inverse-layout-color3);
  font-family: var(--jp-code-font-family);
}

.jp-InputPlaceholder > .jp-Placeholder-content {
  border-color: var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-cell-scrolling-output-offset: 5px;
}

/*-----------------------------------------------------------------------------
| Cell
|----------------------------------------------------------------------------*/

.jp-Cell {
  padding: var(--jp-cell-padding);
  margin: 0;
  border: none;
  outline: none;
  background: transparent;
}

/*-----------------------------------------------------------------------------
| Common input/output
|----------------------------------------------------------------------------*/

.jp-Cell-inputWrapper,
.jp-Cell-outputWrapper {
  display: flex;
  flex-direction: row;
  padding: 0;
  margin: 0;

  /* Added to reveal the box-shadow on the input and output collapsers. */
  overflow: visible;
}

/* Only input/output areas inside cells */
.jp-Cell-inputArea,
.jp-Cell-outputArea {
  flex: 1 1 auto;
}

/*-----------------------------------------------------------------------------
| Collapser
|----------------------------------------------------------------------------*/

/* Make the output collapser disappear when there is not output, but do so
 * in a manner that leaves it in the layout and preserves its width.
 */
.jp-Cell.jp-mod-noOutputs .jp-Cell-outputCollapser {
  border: none !important;
  background: transparent !important;
}

.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputCollapser {
  min-height: var(--jp-cell-collapser-min-height);
}

/*-----------------------------------------------------------------------------
| Output
|----------------------------------------------------------------------------*/

/* Put a space between input and output when there IS output */
.jp-Cell:not(.jp-mod-noOutputs) .jp-Cell-outputWrapper {
  margin-top: 5px;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-Cell-outputArea {
  overflow-y: auto;
  max-height: 24em;
  margin-left: var(--jp-private-cell-scrolling-output-offset);
  resize: vertical;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-Cell-outputArea[style*='height'] {
  max-height: unset;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-Cell-outputArea::after {
  content: ' ';
  box-shadow: inset 0 0 6px 2px rgb(0 0 0 / 30%);
  width: 100%;
  height: 100%;
  position: sticky;
  bottom: 0;
  top: 0;
  margin-top: -50%;
  float: left;
  display: block;
  pointer-events: none;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-child {
  padding-top: 6px;
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-prompt {
  width: calc(
    var(--jp-cell-prompt-width) - var(--jp-private-cell-scrolling-output-offset)
  );
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-promptOverlay {
  left: calc(-1 * var(--jp-private-cell-scrolling-output-offset));
}

/*-----------------------------------------------------------------------------
| CodeCell
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| MarkdownCell
|----------------------------------------------------------------------------*/

.jp-MarkdownOutput {
  display: table-cell;
  width: 100%;
  margin-top: 0;
  margin-bottom: 0;
  padding-left: var(--jp-code-padding);
}

.jp-MarkdownOutput.jp-RenderedHTMLCommon {
  overflow: auto;
}

/* collapseHeadingButton (show always if hiddenCellsButton is _not_ shown) */
.jp-collapseHeadingButton {
  display: flex;
  min-height: var(--jp-cell-collapser-min-height);
  font-size: var(--jp-code-font-size);
  position: absolute;
  background-color: transparent;
  background-size: 25px;
  background-repeat: no-repeat;
  background-position-x: center;
  background-position-y: top;
  background-image: var(--jp-icon-caret-down);
  right: 0;
  top: 0;
  bottom: 0;
}

.jp-collapseHeadingButton.jp-mod-collapsed {
  background-image: var(--jp-icon-caret-right);
}

/*
 set the container font size to match that of content
 so that the nested collapse buttons have the right size
*/
.jp-MarkdownCell .jp-InputPrompt {
  font-size: var(--jp-content-font-size1);
}

/*
  Align collapseHeadingButton with cell top header
  The font sizes are identical to the ones in packages/rendermime/style/base.css
*/
.jp-mod-rendered .jp-collapseHeadingButton[data-heading-level='1'] {
  font-size: var(--jp-content-font-size5);
  background-position-y: calc(0.3 * var(--jp-content-font-size5));
}

.jp-mod-rendered .jp-collapseHeadingButton[data-heading-level='2'] {
  font-size: var(--jp-content-font-size4);
  background-position-y: calc(0.3 * var(--jp-content-font-size4));
}

.jp-mod-rendered .jp-collapseHeadingButton[data-heading-level='3'] {
  font-size: var(--jp-content-font-size3);
  background-position-y: calc(0.3 * var(--jp-content-font-size3));
}

.jp-mod-rendered .jp-collapseHeadingButton[data-heading-level='4'] {
  font-size: var(--jp-content-font-size2);
  background-position-y: calc(0.3 * var(--jp-content-font-size2));
}

.jp-mod-rendered .jp-collapseHeadingButton[data-heading-level='5'] {
  font-size: var(--jp-content-font-size1);
  background-position-y: top;
}

.jp-mod-rendered .jp-collapseHeadingButton[data-heading-level='6'] {
  font-size: var(--jp-content-font-size0);
  background-position-y: top;
}

/* collapseHeadingButton (show only on (hover,active) if hiddenCellsButton is shown) */
.jp-Notebook.jp-mod-showHiddenCellsButton .jp-collapseHeadingButton {
  display: none;
}

.jp-Notebook.jp-mod-showHiddenCellsButton
  :is(.jp-MarkdownCell:hover, .jp-mod-active)
  .jp-collapseHeadingButton {
  display: flex;
}

/* showHiddenCellsButton (only show if jp-mod-showHiddenCellsButton is set, which
is a consequence of the showHiddenCellsButton option in Notebook Settings)*/
.jp-Notebook.jp-mod-showHiddenCellsButton .jp-showHiddenCellsButton {
  margin-left: calc(var(--jp-cell-prompt-width) + 2 * var(--jp-code-padding));
  margin-top: var(--jp-code-padding);
  border: 1px solid var(--jp-border-color2);
  background-color: var(--jp-border-color3) !important;
  color: var(--jp-content-font-color0) !important;
  display: flex;
}

.jp-Notebook.jp-mod-showHiddenCellsButton .jp-showHiddenCellsButton:hover {
  background-color: var(--jp-border-color2) !important;
}

.jp-showHiddenCellsButton {
  display: none;
}

/*-----------------------------------------------------------------------------
| Printing
|----------------------------------------------------------------------------*/

/*
Using block instead of flex to allow the use of the break-inside CSS property for
cell outputs.
*/

@media print {
  .jp-Cell-inputWrapper,
  .jp-Cell-outputWrapper {
    display: block;
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

:root {
  --jp-notebook-toolbar-padding: 2px 5px 2px 2px;
}

/*-----------------------------------------------------------------------------

/*-----------------------------------------------------------------------------
| Styles
|----------------------------------------------------------------------------*/

.jp-NotebookPanel-toolbar {
  padding: var(--jp-notebook-toolbar-padding);

  /* disable paint containment from lumino 2.0 default strict CSS containment */
  contain: style size !important;
}

.jp-Toolbar-item.jp-Notebook-toolbarCellType .jp-select-wrapper.jp-mod-focused {
  border: none;
  box-shadow: none;
}

.jp-Notebook-toolbarCellTypeDropdown select {
  height: 24px;
  font-size: var(--jp-ui-font-size1);
  line-height: 14px;
  border-radius: 0;
  display: block;
}

.jp-Notebook-toolbarCellTypeDropdown span {
  top: 5px !important;
}

.jp-Toolbar-responsive-popup {
  position: absolute;
  height: fit-content;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: flex-end;
  border-bottom: var(--jp-border-width) solid var(--jp-toolbar-border-color);
  box-shadow: var(--jp-toolbar-box-shadow);
  background: var(--jp-toolbar-background);
  min-height: var(--jp-toolbar-micro-height);
  padding: var(--jp-notebook-toolbar-padding);
  z-index: 1;
  right: 0;
  top: 0;
}

.jp-Toolbar > .jp-Toolbar-responsive-opener {
  margin-left: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Variables
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------

/*-----------------------------------------------------------------------------
| Styles
|----------------------------------------------------------------------------*/

.jp-Notebook-ExecutionIndicator {
  position: relative;
  display: inline-block;
  height: 100%;
  z-index: 9997;
}

.jp-Notebook-ExecutionIndicator-tooltip {
  visibility: hidden;
  height: auto;
  width: max-content;
  width: -moz-max-content;
  background-color: var(--jp-layout-color2);
  color: var(--jp-ui-font-color1);
  text-align: justify;
  border-radius: 6px;
  padding: 0 5px;
  position: fixed;
  display: table;
}

.jp-Notebook-ExecutionIndicator-tooltip.up {
  transform: translateX(-50%) translateY(-100%) translateY(-32px);
}

.jp-Notebook-ExecutionIndicator-tooltip.down {
  transform: translateX(calc(-100% + 16px)) translateY(5px);
}

.jp-Notebook-ExecutionIndicator-tooltip.hidden {
  display: none;
}

.jp-Notebook-ExecutionIndicator:hover .jp-Notebook-ExecutionIndicator-tooltip {
  visibility: visible;
}

.jp-Notebook-ExecutionIndicator span {
  font-size: var(--jp-ui-font-size1);
  font-family: var(--jp-ui-font-family);
  color: var(--jp-ui-font-color1);
  line-height: 24px;
  display: block;
}

.jp-Notebook-ExecutionIndicator-progress-bar {
  display: flex;
  justify-content: center;
  height: 100%;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

/*
 * Execution indicator
 */
.jp-tocItem-content::after {
  content: '';

  /* Must be identical to form a circle */
  width: 12px;
  height: 12px;
  background: none;
  border: none;
  position: absolute;
  right: 0;
}

.jp-tocItem-content[data-running='0']::after {
  border-radius: 50%;
  border: var(--jp-border-width) solid var(--jp-inverse-layout-color3);
  background: none;
}

.jp-tocItem-content[data-running='1']::after {
  border-radius: 50%;
  border: var(--jp-border-width) solid var(--jp-inverse-layout-color3);
  background-color: var(--jp-inverse-layout-color3);
}

.jp-tocItem-content[data-running='0'],
.jp-tocItem-content[data-running='1'] {
  margin-right: 12px;
}

/*
 * Copyright (c) Jupyter Development Team.
 * Distributed under the terms of the Modified BSD License.
 */

.jp-Notebook-footer {
  height: 27px;
  margin-left: calc(
    var(--jp-cell-prompt-width) + var(--jp-cell-collapser-width) +
      var(--jp-cell-padding)
  );
  width: calc(
    100% -
      (
        var(--jp-cell-prompt-width) + var(--jp-cell-collapser-width) +
          var(--jp-cell-padding) + var(--jp-cell-padding)
      )
  );
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  color: var(--jp-ui-font-color3);
  margin-top: 6px;
  background: none;
  cursor: pointer;
}

.jp-Notebook-footer:focus {
  border-color: var(--jp-cell-editor-active-border-color);
}

/* For devices that support hovering, hide footer until hover */
@media (hover: hover) {
  .jp-Notebook-footer {
    opacity: 0;
  }

  .jp-Notebook-footer:focus,
  .jp-Notebook-footer:hover {
    opacity: 1;
  }
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Imports
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-side-by-side-output-size: 1fr;
  --jp-side-by-side-resized-cell: var(--jp-side-by-side-output-size);
  --jp-private-notebook-dragImage-width: 304px;
  --jp-private-notebook-dragImage-height: 36px;
  --jp-private-notebook-selected-color: var(--md-blue-400);
  --jp-private-notebook-active-color: var(--md-green-400);
}

/*-----------------------------------------------------------------------------
| Notebook
|----------------------------------------------------------------------------*/

/* stylelint-disable selector-max-class */

.jp-NotebookPanel {
  display: block;
  height: 100%;
}

.jp-NotebookPanel.jp-Document {
  min-width: 240px;
  min-height: 120px;
}

.jp-Notebook {
  padding: var(--jp-notebook-padding);
  outline: none;
  overflow: auto;
  background: var(--jp-layout-color0);
}

.jp-Notebook.jp-mod-scrollPastEnd::after {
  display: block;
  content: '';
  min-height: var(--jp-notebook-scroll-padding);
}

.jp-MainAreaWidget-ContainStrict .jp-Notebook * {
  contain: strict;
}

.jp-Notebook .jp-Cell {
  overflow: visible;
}

.jp-Notebook .jp-Cell .jp-InputPrompt {
  cursor: move;
}

/*-----------------------------------------------------------------------------
| Notebook state related styling
|
| The notebook and cells each have states, here are the possibilities:
|
| - Notebook
|   - Command
|   - Edit
| - Cell
|   - None
|   - Active (only one can be active)
|   - Selected (the cells actions are applied to)
|   - Multiselected (when multiple selected, the cursor)
|   - No outputs
|----------------------------------------------------------------------------*/

/* Command or edit modes */

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-InputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

.jp-Notebook .jp-Cell:not(.jp-mod-active) .jp-OutputPrompt {
  opacity: var(--jp-cell-prompt-not-active-opacity);
  color: var(--jp-cell-prompt-not-active-font-color);
}

/* cell is active */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser {
  background: var(--jp-brand-color1);
}

/* cell is dirty */
.jp-Notebook .jp-Cell.jp-mod-dirty .jp-InputPrompt {
  color: var(--jp-warn-color1);
}

.jp-Notebook .jp-Cell.jp-mod-dirty .jp-InputPrompt::before {
  color: var(--jp-warn-color1);
  content: '•';
}

.jp-Notebook .jp-Cell.jp-mod-active.jp-mod-dirty .jp-Collapser {
  background: var(--jp-warn-color1);
}

/* collapser is hovered */
.jp-Notebook .jp-Cell .jp-Collapser:hover {
  box-shadow: var(--jp-elevation-z2);
  background: var(--jp-brand-color1);
  opacity: var(--jp-cell-collapser-not-active-hover-opacity);
}

/* cell is active and collapser is hovered */
.jp-Notebook .jp-Cell.jp-mod-active .jp-Collapser:hover {
  background: var(--jp-brand-color0);
  opacity: 1;
}

/* Command mode */

.jp-Notebook.jp-mod-commandMode .jp-Cell.jp-mod-selected {
  background: var(--jp-notebook-multiselected-color);
}

.jp-Notebook.jp-mod-commandMode
  .jp-Cell.jp-mod-active.jp-mod-selected:not(.jp-mod-multiSelected) {
  background: transparent;
}

/* Edit mode */

.jp-Notebook.jp-mod-editMode .jp-Cell.jp-mod-active .jp-InputArea-editor {
  border: var(--jp-border-width) solid var(--jp-cell-editor-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-cell-editor-active-background);
}

/*-----------------------------------------------------------------------------
| Notebook drag and drop
|----------------------------------------------------------------------------*/

.jp-Notebook-cell.jp-mod-dropSource {
  opacity: 0.5;
}

.jp-Notebook-cell.jp-mod-dropTarget,
.jp-Notebook.jp-mod-commandMode
  .jp-Notebook-cell.jp-mod-active.jp-mod-selected.jp-mod-dropTarget {
  border-top-color: var(--jp-private-notebook-selected-color);
  border-top-style: solid;
  border-top-width: 2px;
}

.jp-dragImage {
  display: block;
  flex-direction: row;
  width: var(--jp-private-notebook-dragImage-width);
  height: var(--jp-private-notebook-dragImage-height);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background);
  overflow: visible;
}

.jp-dragImage-singlePrompt {
  box-shadow: 2px 2px 4px 0 rgba(0, 0, 0, 0.12);
}

.jp-dragImage .jp-dragImage-content {
  flex: 1 1 auto;
  z-index: 2;
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  line-height: var(--jp-code-line-height);
  padding: var(--jp-code-padding);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background-color);
  color: var(--jp-content-font-color3);
  text-align: left;
  margin: 4px 4px 4px 0;
}

.jp-dragImage .jp-dragImage-prompt {
  flex: 0 0 auto;
  min-width: 36px;
  color: var(--jp-cell-inprompt-font-color);
  padding: var(--jp-code-padding);
  padding-left: 12px;
  font-family: var(--jp-cell-prompt-font-family);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  line-height: 1.9;
  font-size: var(--jp-code-font-size);
  border: var(--jp-border-width) solid transparent;
}

.jp-dragImage-multipleBack {
  z-index: -1;
  position: absolute;
  height: 32px;
  width: 300px;
  top: 8px;
  left: 8px;
  background: var(--jp-layout-color2);
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  box-shadow: 2px 2px 4px 0 rgba(0, 0, 0, 0.12);
}

/*-----------------------------------------------------------------------------
| Cell toolbar
|----------------------------------------------------------------------------*/

.jp-NotebookTools {
  display: block;
  min-width: var(--jp-sidebar-min-width);
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);

  /* This is needed so that all font sizing of children done in ems is
    * relative to this base size */
  font-size: var(--jp-ui-font-size1);
  overflow: auto;
}

.jp-ActiveCellTool {
  padding: 12px 0;
  display: flex;
}

.jp-ActiveCellTool-Content {
  flex: 1 1 auto;
}

.jp-ActiveCellTool .jp-ActiveCellTool-CellContent {
  background: var(--jp-cell-editor-background);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  border-radius: 0;
  min-height: 29px;
}

.jp-ActiveCellTool .jp-InputPrompt {
  min-width: calc(var(--jp-cell-prompt-width) * 0.75);
}

.jp-ActiveCellTool-CellContent > pre {
  padding: 5px 4px;
  margin: 0;
  white-space: normal;
}

.jp-MetadataEditorTool {
  flex-direction: column;
  padding: 12px 0;
}

.jp-RankedPanel > :not(:first-child) {
  margin-top: 12px;
}

.jp-KeySelector select.jp-mod-styled {
  font-size: var(--jp-ui-font-size1);
  color: var(--jp-ui-font-color0);
  border: var(--jp-border-width) solid var(--jp-border-color1);
}

.jp-KeySelector label,
.jp-MetadataEditorTool label,
.jp-NumberSetter label {
  line-height: 1.4;
}

.jp-NotebookTools .jp-select-wrapper {
  margin-top: 4px;
  margin-bottom: 0;
}

.jp-NumberSetter input {
  width: 100%;
  margin-top: 4px;
}

.jp-NotebookTools .jp-Collapse {
  margin-top: 16px;
}

/*-----------------------------------------------------------------------------
| Presentation Mode (.jp-mod-presentationMode)
|----------------------------------------------------------------------------*/

.jp-mod-presentationMode .jp-Notebook {
  --jp-content-font-size1: var(--jp-content-presentation-font-size1);
  --jp-code-font-size: var(--jp-code-presentation-font-size);
}

.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-InputPrompt,
.jp-mod-presentationMode .jp-Notebook .jp-Cell .jp-OutputPrompt {
  flex: 0 0 110px;
}

/*-----------------------------------------------------------------------------
| Side-by-side Mode (.jp-mod-sideBySide)
|----------------------------------------------------------------------------*/
.jp-mod-sideBySide.jp-Notebook .jp-Notebook-cell {
  margin-top: 3em;
  margin-bottom: 3em;
  margin-left: 5%;
  margin-right: 5%;
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell {
  display: grid;
  grid-template-columns: minmax(0, 1fr) min-content minmax(
      0,
      var(--jp-side-by-side-output-size)
    );
  grid-template-rows: auto minmax(0, 1fr) auto;
  grid-template-areas:
    'header header header'
    'input handle output'
    'footer footer footer';
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell.jp-mod-resizedCell {
  grid-template-columns: minmax(0, 1fr) min-content minmax(
      0,
      var(--jp-side-by-side-resized-cell)
    );
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell .jp-CellHeader {
  grid-area: header;
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell .jp-Cell-inputWrapper {
  grid-area: input;
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell .jp-Cell-outputWrapper {
  /* overwrite the default margin (no vertical separation needed in side by side move */
  margin-top: 0;
  grid-area: output;
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell .jp-CellFooter {
  grid-area: footer;
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell .jp-CellResizeHandle {
  grid-area: handle;
  user-select: none;
  display: block;
  height: 100%;
  cursor: ew-resize;
  padding: 0 var(--jp-cell-padding);
}

.jp-mod-sideBySide.jp-Notebook .jp-CodeCell .jp-CellResizeHandle::after {
  content: '';
  display: block;
  background: var(--jp-border-color2);
  height: 100%;
  width: 5px;
}

.jp-mod-sideBySide.jp-Notebook
  .jp-CodeCell.jp-mod-resizedCell
  .jp-CellResizeHandle::after {
  background: var(--jp-border-color0);
}

.jp-CellResizeHandle {
  display: none;
}

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Cell-Placeholder {
  padding-left: 55px;
}

.jp-Cell-Placeholder-wrapper {
  background: #fff;
  border: 1px solid;
  border-color: #e5e6e9 #dfe0e4 #d0d1d5;
  border-radius: 4px;
  -webkit-border-radius: 4px;
  margin: 10px 15px;
}

.jp-Cell-Placeholder-wrapper-inner {
  padding: 15px;
  position: relative;
}

.jp-Cell-Placeholder-wrapper-body {
  background-repeat: repeat;
  background-size: 50% auto;
}

.jp-Cell-Placeholder-wrapper-body div {
  background: #f6f7f8;
  background-image: -webkit-linear-gradient(
    left,
    #f6f7f8 0%,
    #edeef1 20%,
    #f6f7f8 40%,
    #f6f7f8 100%
  );
  background-repeat: no-repeat;
  background-size: 800px 104px;
  height: 104px;
  position: absolute;
  right: 15px;
  left: 15px;
  top: 15px;
}

div.jp-Cell-Placeholder-h1 {
  top: 20px;
  height: 20px;
  left: 15px;
  width: 150px;
}

div.jp-Cell-Placeholder-h2 {
  left: 15px;
  top: 50px;
  height: 10px;
  width: 100px;
}

div.jp-Cell-Placeholder-content-1,
div.jp-Cell-Placeholder-content-2,
div.jp-Cell-Placeholder-content-3 {
  left: 15px;
  right: 15px;
  height: 10px;
}

div.jp-Cell-Placeholder-content-1 {
  top: 100px;
}

div.jp-Cell-Placeholder-content-2 {
  top: 120px;
}

div.jp-Cell-Placeholder-content-3 {
  top: 140px;
}

</style>
<style type="text/css">
/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*
The following CSS variables define the main, public API for styling JupyterLab.
These variables should be used by all plugins wherever possible. In other
words, plugins should not define custom colors, sizes, etc unless absolutely
necessary. This enables users to change the visual theme of JupyterLab
by changing these variables.

Many variables appear in an ordered sequence (0,1,2,3). These sequences
are designed to work well together, so for example, `--jp-border-color1` should
be used with `--jp-layout-color1`. The numbers have the following meanings:

* 0: super-primary, reserved for special emphasis
* 1: primary, most important under normal situations
* 2: secondary, next most important under normal situations
* 3: tertiary, next most important under normal situations

Throughout JupyterLab, we are mostly following principles from Google's
Material Design when selecting colors. We are not, however, following
all of MD as it is not optimized for dense, information rich UIs.
*/

:root {
  /* Elevation
   *
   * We style box-shadows using Material Design's idea of elevation. These particular numbers are taken from here:
   *
   * https://github.com/material-components/material-components-web
   * https://material-components-web.appspot.com/elevation.html
   */

  --jp-shadow-base-lightness: 0;
  --jp-shadow-umbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.2
  );
  --jp-shadow-penumbra-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.14
  );
  --jp-shadow-ambient-color: rgba(
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    var(--jp-shadow-base-lightness),
    0.12
  );
  --jp-elevation-z0: none;
  --jp-elevation-z1: 0 2px 1px -1px var(--jp-shadow-umbra-color),
    0 1px 1px 0 var(--jp-shadow-penumbra-color),
    0 1px 3px 0 var(--jp-shadow-ambient-color);
  --jp-elevation-z2: 0 3px 1px -2px var(--jp-shadow-umbra-color),
    0 2px 2px 0 var(--jp-shadow-penumbra-color),
    0 1px 5px 0 var(--jp-shadow-ambient-color);
  --jp-elevation-z4: 0 2px 4px -1px var(--jp-shadow-umbra-color),
    0 4px 5px 0 var(--jp-shadow-penumbra-color),
    0 1px 10px 0 var(--jp-shadow-ambient-color);
  --jp-elevation-z6: 0 3px 5px -1px var(--jp-shadow-umbra-color),
    0 6px 10px 0 var(--jp-shadow-penumbra-color),
    0 1px 18px 0 var(--jp-shadow-ambient-color);
  --jp-elevation-z8: 0 5px 5px -3px var(--jp-shadow-umbra-color),
    0 8px 10px 1px var(--jp-shadow-penumbra-color),
    0 3px 14px 2px var(--jp-shadow-ambient-color);
  --jp-elevation-z12: 0 7px 8px -4px var(--jp-shadow-umbra-color),
    0 12px 17px 2px var(--jp-shadow-penumbra-color),
    0 5px 22px 4px var(--jp-shadow-ambient-color);
  --jp-elevation-z16: 0 8px 10px -5px var(--jp-shadow-umbra-color),
    0 16px 24px 2px var(--jp-shadow-penumbra-color),
    0 6px 30px 5px var(--jp-shadow-ambient-color);
  --jp-elevation-z20: 0 10px 13px -6px var(--jp-shadow-umbra-color),
    0 20px 31px 3px var(--jp-shadow-penumbra-color),
    0 8px 38px 7px var(--jp-shadow-ambient-color);
  --jp-elevation-z24: 0 11px 15px -7px var(--jp-shadow-umbra-color),
    0 24px 38px 3px var(--jp-shadow-penumbra-color),
    0 9px 46px 8px var(--jp-shadow-ambient-color);

  /* Borders
   *
   * The following variables, specify the visual styling of borders in JupyterLab.
   */

  --jp-border-width: 1px;
  --jp-border-color0: var(--md-grey-400);
  --jp-border-color1: var(--md-grey-400);
  --jp-border-color2: var(--md-grey-300);
  --jp-border-color3: var(--md-grey-200);
  --jp-inverse-border-color: var(--md-grey-600);
  --jp-border-radius: 2px;

  /* UI Fonts
   *
   * The UI font CSS variables are used for the typography all of the JupyterLab
   * user interface elements that are not directly user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-ui-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-ui-font-scale-factor: 1.2;
  --jp-ui-font-size0: 0.83333em;
  --jp-ui-font-size1: 13px; /* Base font size */
  --jp-ui-font-size2: 1.2em;
  --jp-ui-font-size3: 1.44em;
  --jp-ui-font-family: system-ui, -apple-system, blinkmacsystemfont, 'Segoe UI',
    helvetica, arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji',
    'Segoe UI Symbol';

  /*
   * Use these font colors against the corresponding main layout colors.
   * In a light theme, these go from dark to light.
   */

  /* Defaults use Material Design specification */
  --jp-ui-font-color0: rgba(0, 0, 0, 1);
  --jp-ui-font-color1: rgba(0, 0, 0, 0.87);
  --jp-ui-font-color2: rgba(0, 0, 0, 0.54);
  --jp-ui-font-color3: rgba(0, 0, 0, 0.38);

  /*
   * Use these against the brand/accent/warn/error colors.
   * These will typically go from light to darker, in both a dark and light theme.
   */

  --jp-ui-inverse-font-color0: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color1: rgba(255, 255, 255, 1);
  --jp-ui-inverse-font-color2: rgba(255, 255, 255, 0.7);
  --jp-ui-inverse-font-color3: rgba(255, 255, 255, 0.5);

  /* Content Fonts
   *
   * Content font variables are used for typography of user generated content.
   *
   * The font sizing here is done assuming that the body font size of --jp-content-font-size1
   * is applied to a parent element. When children elements, such as headings, are sized
   * in em all things will be computed relative to that body size.
   */

  --jp-content-line-height: 1.6;
  --jp-content-font-scale-factor: 1.2;
  --jp-content-font-size0: 0.83333em;
  --jp-content-font-size1: 14px; /* Base font size */
  --jp-content-font-size2: 1.2em;
  --jp-content-font-size3: 1.44em;
  --jp-content-font-size4: 1.728em;
  --jp-content-font-size5: 2.0736em;

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-content-presentation-font-size1: 17px;
  --jp-content-heading-line-height: 1;
  --jp-content-heading-margin-top: 1.2em;
  --jp-content-heading-margin-bottom: 0.8em;
  --jp-content-heading-font-weight: 500;

  /* Defaults use Material Design specification */
  --jp-content-font-color0: rgba(0, 0, 0, 1);
  --jp-content-font-color1: rgba(0, 0, 0, 0.87);
  --jp-content-font-color2: rgba(0, 0, 0, 0.54);
  --jp-content-font-color3: rgba(0, 0, 0, 0.38);
  --jp-content-link-color: var(--md-blue-900);
  --jp-content-font-family: system-ui, -apple-system, blinkmacsystemfont,
    'Segoe UI', helvetica, arial, sans-serif, 'Apple Color Emoji',
    'Segoe UI Emoji', 'Segoe UI Symbol';

  /*
   * Code Fonts
   *
   * Code font variables are used for typography of code and other monospaces content.
   */

  --jp-code-font-size: 13px;
  --jp-code-line-height: 1.3077; /* 17px for 13px base */
  --jp-code-padding: 5px; /* 5px for 13px base, codemirror highlighting needs integer px value */
  --jp-code-font-family-default: menlo, consolas, 'DejaVu Sans Mono', monospace;
  --jp-code-font-family: var(--jp-code-font-family-default);

  /* This gives a magnification of about 125% in presentation mode over normal. */
  --jp-code-presentation-font-size: 16px;

  /* may need to tweak cursor width if you change font size */
  --jp-code-cursor-width0: 1.4px;
  --jp-code-cursor-width1: 2px;
  --jp-code-cursor-width2: 4px;

  /* Layout
   *
   * The following are the main layout colors use in JupyterLab. In a light
   * theme these would go from light to dark.
   */

  --jp-layout-color0: white;
  --jp-layout-color1: white;
  --jp-layout-color2: var(--md-grey-200);
  --jp-layout-color3: var(--md-grey-400);
  --jp-layout-color4: var(--md-grey-600);

  /* Inverse Layout
   *
   * The following are the inverse layout colors use in JupyterLab. In a light
   * theme these would go from dark to light.
   */

  --jp-inverse-layout-color0: #111;
  --jp-inverse-layout-color1: var(--md-grey-900);
  --jp-inverse-layout-color2: var(--md-grey-800);
  --jp-inverse-layout-color3: var(--md-grey-700);
  --jp-inverse-layout-color4: var(--md-grey-600);

  /* Brand/accent */

  --jp-brand-color0: var(--md-blue-900);
  --jp-brand-color1: var(--md-blue-700);
  --jp-brand-color2: var(--md-blue-300);
  --jp-brand-color3: var(--md-blue-100);
  --jp-brand-color4: var(--md-blue-50);
  --jp-accent-color0: var(--md-green-900);
  --jp-accent-color1: var(--md-green-700);
  --jp-accent-color2: var(--md-green-300);
  --jp-accent-color3: var(--md-green-100);

  /* State colors (warn, error, success, info) */

  --jp-warn-color0: var(--md-orange-900);
  --jp-warn-color1: var(--md-orange-700);
  --jp-warn-color2: var(--md-orange-300);
  --jp-warn-color3: var(--md-orange-100);
  --jp-error-color0: var(--md-red-900);
  --jp-error-color1: var(--md-red-700);
  --jp-error-color2: var(--md-red-300);
  --jp-error-color3: var(--md-red-100);
  --jp-success-color0: var(--md-green-900);
  --jp-success-color1: var(--md-green-700);
  --jp-success-color2: var(--md-green-300);
  --jp-success-color3: var(--md-green-100);
  --jp-info-color0: var(--md-cyan-900);
  --jp-info-color1: var(--md-cyan-700);
  --jp-info-color2: var(--md-cyan-300);
  --jp-info-color3: var(--md-cyan-100);

  /* Cell specific styles */

  --jp-cell-padding: 5px;
  --jp-cell-collapser-width: 8px;
  --jp-cell-collapser-min-height: 20px;
  --jp-cell-collapser-not-active-hover-opacity: 0.6;
  --jp-cell-editor-background: var(--md-grey-100);
  --jp-cell-editor-border-color: var(--md-grey-300);
  --jp-cell-editor-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-cell-editor-active-background: var(--jp-layout-color0);
  --jp-cell-editor-active-border-color: var(--jp-brand-color1);
  --jp-cell-prompt-width: 64px;
  --jp-cell-prompt-font-family: var(--jp-code-font-family-default);
  --jp-cell-prompt-letter-spacing: 0;
  --jp-cell-prompt-opacity: 1;
  --jp-cell-prompt-not-active-opacity: 0.5;
  --jp-cell-prompt-not-active-font-color: var(--md-grey-700);

  /* A custom blend of MD grey and blue 600
   * See https://meyerweb.com/eric/tools/color-blend/#546E7A:1E88E5:5:hex */
  --jp-cell-inprompt-font-color: #307fc1;

  /* A custom blend of MD grey and orange 600
   * https://meyerweb.com/eric/tools/color-blend/#546E7A:F4511E:5:hex */
  --jp-cell-outprompt-font-color: #bf5b3d;

  /* Notebook specific styles */

  --jp-notebook-padding: 10px;
  --jp-notebook-select-background: var(--jp-layout-color1);
  --jp-notebook-multiselected-color: var(--md-blue-50);

  /* The scroll padding is calculated to fill enough space at the bottom of the
  notebook to show one single-line cell (with appropriate padding) at the top
  when the notebook is scrolled all the way to the bottom. We also subtract one
  pixel so that no scrollbar appears if we have just one single-line cell in the
  notebook. This padding is to enable a 'scroll past end' feature in a notebook.
  */
  --jp-notebook-scroll-padding: calc(
    100% - var(--jp-code-font-size) * var(--jp-code-line-height) -
      var(--jp-code-padding) - var(--jp-cell-padding) - 1px
  );

  /* Rendermime styles */

  --jp-rendermime-error-background: #fdd;
  --jp-rendermime-table-row-background: var(--md-grey-100);
  --jp-rendermime-table-row-hover-background: var(--md-light-blue-50);

  /* Dialog specific styles */

  --jp-dialog-background: rgba(0, 0, 0, 0.25);

  /* Console specific styles */

  --jp-console-padding: 10px;

  /* Toolbar specific styles */

  --jp-toolbar-border-color: var(--jp-border-color1);
  --jp-toolbar-micro-height: 8px;
  --jp-toolbar-background: var(--jp-layout-color1);
  --jp-toolbar-box-shadow: 0 0 2px 0 rgba(0, 0, 0, 0.24);
  --jp-toolbar-header-margin: 4px 4px 0 4px;
  --jp-toolbar-active-background: var(--md-grey-300);

  /* Statusbar specific styles */

  --jp-statusbar-height: 24px;

  /* Input field styles */

  --jp-input-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-input-active-background: var(--jp-layout-color1);
  --jp-input-hover-background: var(--jp-layout-color1);
  --jp-input-background: var(--md-grey-100);
  --jp-input-border-color: var(--jp-inverse-border-color);
  --jp-input-active-border-color: var(--jp-brand-color1);
  --jp-input-active-box-shadow-color: rgba(19, 124, 189, 0.3);

  /* General editor styles */

  --jp-editor-selected-background: #d9d9d9;
  --jp-editor-selected-focused-background: #d7d4f0;
  --jp-editor-cursor-color: var(--jp-ui-font-color0);

  /* Code mirror specific styles */

  --jp-mirror-editor-keyword-color: #008000;
  --jp-mirror-editor-atom-color: #88f;
  --jp-mirror-editor-number-color: #080;
  --jp-mirror-editor-def-color: #00f;
  --jp-mirror-editor-variable-color: var(--md-grey-900);
  --jp-mirror-editor-variable-2-color: rgb(0, 54, 109);
  --jp-mirror-editor-variable-3-color: #085;
  --jp-mirror-editor-punctuation-color: #05a;
  --jp-mirror-editor-property-color: #05a;
  --jp-mirror-editor-operator-color: #a2f;
  --jp-mirror-editor-comment-color: #408080;
  --jp-mirror-editor-string-color: #ba2121;
  --jp-mirror-editor-string-2-color: #708;
  --jp-mirror-editor-meta-color: #a2f;
  --jp-mirror-editor-qualifier-color: #555;
  --jp-mirror-editor-builtin-color: #008000;
  --jp-mirror-editor-bracket-color: #997;
  --jp-mirror-editor-tag-color: #170;
  --jp-mirror-editor-attribute-color: #00c;
  --jp-mirror-editor-header-color: blue;
  --jp-mirror-editor-quote-color: #090;
  --jp-mirror-editor-link-color: #00c;
  --jp-mirror-editor-error-color: #f00;
  --jp-mirror-editor-hr-color: #999;

  /*
    RTC user specific colors.
    These colors are used for the cursor, username in the editor,
    and the icon of the user.
  */

  --jp-collaborator-color1: #ffad8e;
  --jp-collaborator-color2: #dac83d;
  --jp-collaborator-color3: #72dd76;
  --jp-collaborator-color4: #00e4d0;
  --jp-collaborator-color5: #45d4ff;
  --jp-collaborator-color6: #e2b1ff;
  --jp-collaborator-color7: #ff9de6;

  /* Vega extension styles */

  --jp-vega-background: white;

  /* Sidebar-related styles */

  --jp-sidebar-min-width: 250px;

  /* Search-related styles */

  --jp-search-toggle-off-opacity: 0.5;
  --jp-search-toggle-hover-opacity: 0.8;
  --jp-search-toggle-on-opacity: 1;
  --jp-search-selected-match-background-color: rgb(245, 200, 0);
  --jp-search-selected-match-color: black;
  --jp-search-unselected-match-background-color: var(
    --jp-inverse-layout-color0
  );
  --jp-search-unselected-match-color: var(--jp-ui-inverse-font-color0);

  /* Icon colors that work well with light or dark backgrounds */
  --jp-icon-contrast-color0: var(--md-purple-600);
  --jp-icon-contrast-color1: var(--md-green-600);
  --jp-icon-contrast-color2: var(--md-pink-600);
  --jp-icon-contrast-color3: var(--md-blue-600);

  /* Button colors */
  --jp-accept-color-normal: var(--md-blue-700);
  --jp-accept-color-hover: var(--md-blue-800);
  --jp-accept-color-active: var(--md-blue-900);
  --jp-warn-color-normal: var(--md-red-700);
  --jp-warn-color-hover: var(--md-red-800);
  --jp-warn-color-active: var(--md-red-900);
  --jp-reject-color-normal: var(--md-grey-600);
  --jp-reject-color-hover: var(--md-grey-700);
  --jp-reject-color-active: var(--md-grey-800);

  /* File or activity icons and switch semantic variables */
  --jp-jupyter-icon-color: #f37626;
  --jp-notebook-icon-color: #f37626;
  --jp-json-icon-color: var(--md-orange-700);
  --jp-console-icon-background-color: var(--md-blue-700);
  --jp-console-icon-color: white;
  --jp-terminal-icon-background-color: var(--md-grey-800);
  --jp-terminal-icon-color: var(--md-grey-200);
  --jp-text-editor-icon-color: var(--md-grey-700);
  --jp-inspector-icon-color: var(--md-grey-700);
  --jp-switch-color: var(--md-grey-400);
  --jp-switch-true-position-color: var(--md-orange-900);
}
</style>
<style type="text/css">
/* Force rendering true colors when outputing to pdf */
* {
  -webkit-print-color-adjust: exact;
}

/* Misc */
a.anchor-link {
  display: none;
}

/* Input area styling */
.jp-InputArea {
  overflow: hidden;
}

.jp-InputArea-editor {
  overflow: hidden;
}

.cm-editor.cm-s-jupyter .highlight pre {
/* weird, but --jp-code-padding defined to be 5px but 4px horizontal padding is hardcoded for pre.cm-line */
  padding: var(--jp-code-padding) 4px;
  margin: 0;

  font-family: inherit;
  font-size: inherit;
  line-height: inherit;
  color: inherit;

}

.jp-OutputArea-output pre {
  line-height: inherit;
  font-family: inherit;
}

.jp-RenderedText pre {
  color: var(--jp-content-font-color1);
  font-size: var(--jp-code-font-size);
}

/* Hiding the collapser by default */
.jp-Collapser {
  display: none;
}

@page {
    margin: 0.5in; /* Margin for each printed piece of paper */
}

@media print {
  .jp-Cell-inputWrapper,
  .jp-Cell-outputWrapper {
    display: block;
  }
}
</style>
<!-- Load mathjax -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/latest.js?config=TeX-AMS_CHTML-full,Safe"> </script>
<!-- MathJax configuration -->
<script type="text/x-mathjax-config">
    init_mathjax = function() {
        if (window.MathJax) {
        // MathJax loaded
            MathJax.Hub.Config({
                TeX: {
                    equationNumbers: {
                    autoNumber: "AMS",
                    useLabelIds: true
                    }
                },
                tex2jax: {
                    inlineMath: [ ['$','$'], ["\\(","\\)"] ],
                    displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
                    processEscapes: true,
                    processEnvironments: true
                },
                displayAlign: 'center',
                CommonHTML: {
                    linebreaks: {
                    automatic: true
                    }
                }
            });

            MathJax.Hub.Queue(["Typeset", MathJax.Hub]);
        }
    }
    init_mathjax();
    </script>
<!-- End of mathjax configuration --><script type="module">
  document.addEventListener("DOMContentLoaded", async () => {
    const diagrams = document.querySelectorAll(".jp-Mermaid > pre.mermaid");
    // do not load mermaidjs if not needed
    if (!diagrams.length) {
      return;
    }
    const mermaid = (await import("https://cdnjs.cloudflare.com/ajax/libs/mermaid/10.6.0/mermaid.esm.min.mjs")).default;
    const parser = new DOMParser();

    mermaid.initialize({
      maxTextSize: 100000,
      startOnLoad: false,
      fontFamily: window
        .getComputedStyle(document.body)
        .getPropertyValue("--jp-ui-font-family"),
      theme: document.querySelector("body[data-jp-theme-light='true']")
        ? "default"
        : "dark",
    });

    let _nextMermaidId = 0;

    function makeMermaidImage(svg) {
      const img = document.createElement("img");
      const doc = parser.parseFromString(svg, "image/svg+xml");
      const svgEl = doc.querySelector("svg");
      const { maxWidth } = svgEl?.style || {};
      const firstTitle = doc.querySelector("title");
      const firstDesc = doc.querySelector("desc");

      img.setAttribute("src", `data:image/svg+xml,${encodeURIComponent(svg)}`);
      if (maxWidth) {
        img.width = parseInt(maxWidth);
      }
      if (firstTitle) {
        img.setAttribute("alt", firstTitle.textContent);
      }
      if (firstDesc) {
        const caption = document.createElement("figcaption");
        caption.className = "sr-only";
        caption.textContent = firstDesc.textContent;
        return [img, caption];
      }
      return [img];
    }

    async function makeMermaidError(text) {
      let errorMessage = "";
      try {
        await mermaid.parse(text);
      } catch (err) {
        errorMessage = `${err}`;
      }

      const result = document.createElement("details");
      result.className = 'jp-RenderedMermaid-Details';
      const summary = document.createElement("summary");
      summary.className = 'jp-RenderedMermaid-Summary';
      const pre = document.createElement("pre");
      const code = document.createElement("code");
      code.innerText = text;
      pre.appendChild(code);
      summary.appendChild(pre);
      result.appendChild(summary);

      const warning = document.createElement("pre");
      warning.innerText = errorMessage;
      result.appendChild(warning);
      return [result];
    }

    async function renderOneMarmaid(src) {
      const id = `jp-mermaid-${_nextMermaidId++}`;
      const parent = src.parentNode;
      let raw = src.textContent.trim();
      const el = document.createElement("div");
      el.style.visibility = "hidden";
      document.body.appendChild(el);
      let results = null;
      let output = null;
      try {
        const { svg } = await mermaid.render(id, raw, el);
        results = makeMermaidImage(svg);
        output = document.createElement("figure");
        results.map(output.appendChild, output);
      } catch (err) {
        parent.classList.add("jp-mod-warning");
        results = await makeMermaidError(raw);
        output = results[0];
      } finally {
        el.remove();
      }
      parent.classList.add("jp-RenderedMermaid");
      parent.appendChild(output);
    }

    void Promise.all([...diagrams].map(renderOneMarmaid));
  });
</script>
<style>
  .jp-Mermaid:not(.jp-RenderedMermaid) {
    display: none;
  }

  .jp-RenderedMermaid {
    overflow: auto;
    display: flex;
  }

  .jp-RenderedMermaid.jp-mod-warning {
    width: auto;
    padding: 0.5em;
    margin-top: 0.5em;
    border: var(--jp-border-width) solid var(--jp-warn-color2);
    border-radius: var(--jp-border-radius);
    color: var(--jp-ui-font-color1);
    font-size: var(--jp-ui-font-size1);
    white-space: pre-wrap;
    word-wrap: break-word;
  }

  .jp-RenderedMermaid figure {
    margin: 0;
    overflow: auto;
    max-width: 100%;
  }

  .jp-RenderedMermaid img {
    max-width: 100%;
  }

  .jp-RenderedMermaid-Details > pre {
    margin-top: 1em;
  }

  .jp-RenderedMermaid-Summary {
    color: var(--jp-warn-color2);
  }

  .jp-RenderedMermaid:not(.jp-mod-warning) pre {
    display: none;
  }

  .jp-RenderedMermaid-Summary > pre {
    display: inline-block;
    white-space: normal;
  }
</style>
<!-- End of mermaid configuration --></head>
<body class="jp-Notebook" data-jp-theme-light="true" data-jp-theme-name="JupyterLab Light">
<main>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=5e402230">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Exploring-Red-Wine-Quality-Through-Data-Science">Exploring Red Wine Quality Through Data Science<a class="anchor-link" href="#Exploring-Red-Wine-Quality-Through-Data-Science">¶</a></h2><img alt="No description has been provided for this image" src="https://media.giphy.com/media/jRuv9xc10lVyE/giphy.gif"/>
<p>You can read more about the Data Science Methodology from this <a href="https://tdwi.org/~/media/64511A895D86457E964174EDC5C4C7B1.PDF">IBM whitepaper</a> by John Rollins</p>
<p><a href="https://archive.ics.uci.edu/ml/datasets/wine+quality">Link</a> for the dataset for context</p>
<img alt="No description has been provided for this image" src="https://media-exp1.licdn.com/dms/image/C4D12AQGOPVf5iqhhwQ/article-inline_image-shrink_1000_1488/0/1597756152693?e=1652918400&amp;v=beta&amp;t=iKZ2jX3khsx11lD9JyZWDz-j-Gt2hZsKPXz5rZ0iE1M"/>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=96fa59d2">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h3 id="Business-Understanding">Business Understanding<a class="anchor-link" href="#Business-Understanding">¶</a></h3><p>The red wine industry shows a recent exponential growth as social drinking is on the rise. Nowadays, industry players are using product quality certifications to promote their products. This is a time-consuming process and requires the assessment given by human experts, which makes this process very expensive. Also, the price of red wine depends on a rather abstract concept of wine appreciation by wine tasters, opinion among whom may have a high degree of variability. Another vital factor in red wine certification and quality assessment is physicochemical tests, which are laboratory-based and consider factors like acidity, pH level, sugar, and other chemical properties. The red wine market would be of interest if the human quality of tasting can be related to wine’s chemical properties so that certification and quality assessment and assurance processes are more controlled.</p>
<p>The goal is to implement Regression Models and Classification Models on the Red Wine Quality Dataset to determine which features are the best quality red wine indicators and generate insights into each of these factors to our model’s red wine quality.</p>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=ead99b54">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h3 id="Analytic-Approach">Analytic Approach<a class="anchor-link" href="#Analytic-Approach">¶</a></h3><p>Based on the above business understanding one should decide the analytical approach to follow. The approaches can be of 4 types: Descriptive approach (current status and information provided), Diagnostic approach(a.k.a statistical analysis, what is happening and why it is happening), Predictive approach(it forecasts on the trends or future events probability) and Prescriptive approach( how the problem should be solved actually).</p>
<p><strong>Q1. What is the analytical approach that you would take for this project? Why do you think its the right approach?</strong></p>
<p><em>I would take Descriptive approach as we yet do not know what information are useful and have high impact on our wine quality. We are just presented with the raw data and descriptive approach would enable us to have an understanding of the potential relationships between variables and also helps us to present the data in a more meaningful way. After our analysis is finished, we would do the modellings.</em></p>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=12766c3d">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h3 id="Data-Requirements">Data Requirements<a class="anchor-link" href="#Data-Requirements">¶</a></h3><p><strong>Q2. What kind of data do we require for predicting the red wine quality and for determining the features that are the best quality red wine indicators?</strong></p>
<p><em>We need a data which has many features like the physiochemical attributes (acidity, pH level, sugar, etc) so that we would have enough features to play around with to determine the features that are the best quality red wine indicators.</em></p>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=5d59c819">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h3 id="Data-Collection">Data Collection<a class="anchor-link" href="#Data-Collection">¶</a></h3><p><strong>Q3. From where do we get our data?</strong></p>
<p><em>We get our data from Wine Quality Dataset which is gathered by:</em></p>
<ul>
<li><p><em>Paulo Cortez, University of Minho, Guimarães, Portugal, <a href="http://www3.dsi.uminho.pt/pcortez">http://www3.dsi.uminho.pt/pcortez</a></em></p>
</li>
<li><p><em>A. Cerdeira, F. Almeida, T. Matos and J. Reis, Viticulture Commission of the Vinho Verde Region(CVRVV), Porto, Portugal
@2009</em></p>
</li>
</ul>
<p><em>and is accessible on UCI ML repository via this link <a href="https://archive.ics.uci.edu/ml/datasets/wine+quality">https://archive.ics.uci.edu/ml/datasets/wine+quality</a></em></p>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=c8419dbc">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h3 id="Data-Understanding">Data Understanding<a class="anchor-link" href="#Data-Understanding">¶</a></h3><p>Link for the dataset <a href="https://archive.ics.uci.edu/ml/datasets/wine+quality">https://archive.ics.uci.edu/ml/datasets/wine+quality</a> for context</p>
<p><strong>Q4. From where are red wine samples obtained?</strong></p>
<p><em>The red wine samples were obtained from the north of Portugal to model red wine quality based on physicochemical tests. The dataset is related to the red variant of Portuguese "Vinho Verde" wine.</em></p>
<p><strong>Q5. How can knowing the impact of each variable on the red wine quality help businesses(producers, distributors, etc) ?</strong></p>
<p><em>Knowing the impact of each variable would help businesses(producers, distributors, etc) better assess their production, distribution, and pricing strategy.</em></p>
<li>Check the shape of data, and the datatypes of the features</li>
<li>Understand the data by carrying out any steps that you think are necessary</li>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=f1733b3d-e6b6-4989-b39e-448a2b78db5d">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [1]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>
<span class="kn">import</span> <span class="nn">joblib</span>
<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="kn">import</span> <span class="nn">warnings</span>
<span class="kn">from</span> <span class="nn">sklearn.preprocessing</span> <span class="kn">import</span> <span class="n">normalize</span><span class="p">,</span> <span class="n">StandardScaler</span>
<span class="n">warnings</span><span class="o">.</span><span class="n">filterwarnings</span><span class="p">(</span><span class="s2">"ignore"</span><span class="p">,</span> <span class="n">category</span><span class="o">=</span><span class="ne">UserWarning</span><span class="p">)</span>
<span class="n">warnings</span><span class="o">.</span><span class="n">filterwarnings</span><span class="p">(</span><span class="s2">"ignore"</span><span class="p">,</span> <span class="n">category</span><span class="o">=</span><span class="ne">FutureWarning</span><span class="p">)</span>
<span class="n">warnings</span><span class="o">.</span><span class="n">filterwarnings</span><span class="p">(</span><span class="s1">'ignore'</span><span class="p">,</span> <span class="n">category</span><span class="o">=</span><span class="ne">DeprecationWarning</span><span class="p">)</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">train_test_split</span>
<span class="kn">from</span> <span class="nn">sklearn</span> <span class="kn">import</span> <span class="n">svm</span>
<span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">accuracy_score</span><span class="p">,</span> <span class="n">precision_score</span><span class="p">,</span> <span class="n">recall_score</span><span class="p">,</span> <span class="n">classification_report</span>
<span class="kn">from</span> <span class="nn">sklearn.model_selection</span> <span class="kn">import</span> <span class="n">GridSearchCV</span>

<span class="n">wine</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s2">"winequality-red.csv"</span><span class="p">)</span>
<span class="n">wine</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
<div class="jp-OutputPrompt jp-OutputArea-prompt">Out[1]:</div>
<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html" tabindex="0">
<div>
<style scoped="">
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
<thead>
<tr style="text-align: right;">
<th></th>
<th>fixed acidity</th>
<th>volatile acidity</th>
<th>citric acid</th>
<th>residual sugar</th>
<th>chlorides</th>
<th>free sulfur dioxide</th>
<th>total sulfur dioxide</th>
<th>density</th>
<th>pH</th>
<th>sulphates</th>
<th>alcohol</th>
<th>quality</th>
</tr>
</thead>
<tbody>
<tr>
<th>0</th>
<td>7.4</td>
<td>0.70</td>
<td>0.00</td>
<td>1.9</td>
<td>0.076</td>
<td>11.0</td>
<td>34.0</td>
<td>0.9978</td>
<td>3.51</td>
<td>0.56</td>
<td>9.4</td>
<td>5</td>
</tr>
<tr>
<th>1</th>
<td>7.8</td>
<td>0.88</td>
<td>0.00</td>
<td>2.6</td>
<td>0.098</td>
<td>25.0</td>
<td>67.0</td>
<td>0.9968</td>
<td>3.20</td>
<td>0.68</td>
<td>9.8</td>
<td>5</td>
</tr>
<tr>
<th>2</th>
<td>7.8</td>
<td>0.76</td>
<td>0.04</td>
<td>2.3</td>
<td>0.092</td>
<td>15.0</td>
<td>54.0</td>
<td>0.9970</td>
<td>3.26</td>
<td>0.65</td>
<td>9.8</td>
<td>5</td>
</tr>
<tr>
<th>3</th>
<td>11.2</td>
<td>0.28</td>
<td>0.56</td>
<td>1.9</td>
<td>0.075</td>
<td>17.0</td>
<td>60.0</td>
<td>0.9980</td>
<td>3.16</td>
<td>0.58</td>
<td>9.8</td>
<td>6</td>
</tr>
<tr>
<th>4</th>
<td>7.4</td>
<td>0.70</td>
<td>0.00</td>
<td>1.9</td>
<td>0.076</td>
<td>11.0</td>
<td>34.0</td>
<td>0.9978</td>
<td>3.51</td>
<td>0.56</td>
<td>9.4</td>
<td>5</td>
</tr>
</tbody>
</table>
</div>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=58db6169-3bdb-47f9-a4ae-686cd999b871">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [2]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># The shape of data</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">'Number of samples: '</span><span class="p">,</span> <span class="n">wine</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">])</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">'Number of features: '</span><span class="p">,</span> <span class="n">wine</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">1</span><span class="p">])</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>Number of samples:  1599
Number of features:  12
</pre>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=ef377561-61aa-4e4d-8e05-ca997a173f3b">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [3]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># The datatypes of the features</span>
<span class="n">wine</span><span class="o">.</span><span class="n">info</span><span class="p">()</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>&lt;class 'pandas.core.frame.DataFrame'&gt;
RangeIndex: 1599 entries, 0 to 1598
Data columns (total 12 columns):
 #   Column                Non-Null Count  Dtype  
---  ------                --------------  -----  
 0   fixed acidity         1599 non-null   float64
 1   volatile acidity      1599 non-null   float64
 2   citric acid           1599 non-null   float64
 3   residual sugar        1599 non-null   float64
 4   chlorides             1599 non-null   float64
 5   free sulfur dioxide   1599 non-null   float64
 6   total sulfur dioxide  1599 non-null   float64
 7   density               1599 non-null   float64
 8   pH                    1599 non-null   float64
 9   sulphates             1599 non-null   float64
 10  alcohol               1599 non-null   float64
 11  quality               1599 non-null   int64  
dtypes: float64(11), int64(1)
memory usage: 150.0 KB
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=e65c0197-c956-4ccd-8674-239f866c5ca8">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>From the below table, we can see that the data in our dataset is not distributed well and we have a lot more medium quality wines than the very high or low quality wines.</p>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=a5068c28-ac3f-4274-856c-77252023a573">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [4]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># understanding the data</span>
<span class="nb">print</span><span class="p">(</span><span class="nb">list</span><span class="p">(</span><span class="n">wine</span><span class="o">.</span><span class="n">columns</span><span class="p">))</span>
<span class="n">wine</span><span class="p">[</span><span class="s1">'quality'</span><span class="p">]</span><span class="o">.</span><span class="n">value_counts</span><span class="p">()</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>['fixed acidity', 'volatile acidity', 'citric acid', 'residual sugar', 'chlorides', 'free sulfur dioxide', 'total sulfur dioxide', 'density', 'pH', 'sulphates', 'alcohol', 'quality']
</pre>
</div>
</div>
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
<div class="jp-OutputPrompt jp-OutputArea-prompt">Out[4]:</div>
<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain" tabindex="0">
<pre>5    681
6    638
7    199
4     53
8     18
3     10
Name: quality, dtype: int64</pre>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=05f931e4-9c91-42cc-8fa4-b7b11818f31c">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>As we can see in the graphs below, generally, when there is low volatile acidity, chlorides, density, and pH, the quality of the wine is higher and with the increase in citric acid, sulphates, and alcohol the quality becomes higher. The residual sugar does not have much of a impact; as we can see in the graph of <code>residual sugar Vs. quality</code>, across different wine qualities, the residual sugar remains the same. The rest of the features have a mixture of behaviours regarding their impact on the quality.</p>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=b0fcc7ec-e623-455f-a19b-e38e28e31993">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [5]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="k">for</span> <span class="n">i</span><span class="p">,</span> <span class="n">col</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="nb">list</span><span class="p">(</span><span class="n">wine</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">'quality'</span><span class="p">,</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span><span class="o">.</span><span class="n">columns</span><span class="p">)):</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">i</span><span class="p">)</span>
    <span class="n">sns</span><span class="o">.</span><span class="n">catplot</span><span class="p">(</span><span class="n">x</span><span class="o">=</span><span class="s1">'quality'</span><span class="p">,</span> <span class="n">y</span><span class="o">=</span><span class="n">col</span><span class="p">,</span> <span class="n">data</span><span class="o">=</span><span class="n">wine</span><span class="p">,</span> <span class="n">kind</span><span class="o">=</span><span class="s1">'point'</span><span class="p">,</span> <span class="n">aspect</span><span class="o">=</span><span class="mi">2</span><span class="p">,</span> <span class="p">)</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>&lt;Figure size 432x288 with 0 Axes&gt;</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAsgAAAFgCAYAAACmDI9oAAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjQuMywgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy/MnkTPAAAACXBIWXMAAAsTAAALEwEAmpwYAABAPUlEQVR4nO3deXiV5Z3/8fc3G0kgkEA2IOwkYQkCgqgICYsLWJeq7bjUpZa6TK1Lrdpt5jftTGfGrS6dutStrbZVa1utbQVFIeyLgKABkrBDgGwQSCB7cv/+OMf4AAGicnI4yed1XbmS3M/znPN9rhPIJ/e5F3POISIiIiIiPmHBLkBERERE5HSigCwiIiIi4qGALCIiIiLioYAsIiIiIuKhgCwiIiIi4hER7ALaw4wZM9ycOXOCXYaIiIiInF6stcZO0YNcXl4e7BJEREREJER0ioAsIiIiItJWCsgiIiIiIh4KyCIiIiIiHgrIIiIiIiIeCsgiIiIiIh4KyCIiIiIiHgrIIiIiIiIeCsgiIiIiIh4KyCIiIiIiHgrIIiIiIiIeCsgiIiIiIh4RwS5AvpgbXlxBUUUNaQkxvDLr7GCXIyIiItJhKCCHqKKKGraVHw52GSIiIiIdjoZYiIiIiIh4KCCLiIiIiHgoIIuIiIiIeCggi4iIiIh4KCCLiIiIiHgoIIuIiIiIeCggi4iIiIh4KCCLiIiIiHgoIIuIiIiIeCggi4iIiIh4KCCLiIiIiHgoIIuIiIiIeCggi4iIiIh4KCCLiIiIiHgoIIuIiIiIeCggi4iIiIh4KCCLiIiIiHgoIIuIiIiIeCggi4iIiIh4KCCLiIiIiHgoIIuIiIiIeCggi4iIiIh4KCCLiIiIiHgoIIuIiIiIeCggi4iIiIh4KCCLiIiIiHgoIIuIiIiIeCggi4iIiIh4KCCLiIiIiHgoIIuIiIiIeCggi4iIiIh4KCCLiIiIiHgoIIuIiIiIeCggi4iIiIh4KCCLiIiIiHgoIIuIiIiIeAQ0IJvZDDMrMLPNZvbDVo4nmNmbZvaxma00syzPsbvNLM/M1pvZPZ72MWa23MzWmtkqM5sQyHsQERERkc4lYAHZzMKBp4CZwAjgWjMbcdRpPwbWOufOAG4EnvRfmwXcAkwARgOXmFm6/5qHgZ8558YA/8//vYiIiIjIKRHIHuQJwGbn3FbnXD3wGnD5UeeMAD4AcM7lAwPNLAUYDix3zlU75xqBBcAV/msc0N3/dQ9gTwDvQUREREQ6mUAG5L7ALs/3Rf42r3XAlQD+oRIDgDQgD8g2s15mFgtcDPTzX3MP8IiZ7QIeBX7U2pOb2a3+IRirysrKTs0diYiIiEiHF8iAbK20uaO+fxBIMLO1wJ3AR0Cjc24j8BAwF5iDL0g3+q/5V+B7zrl+wPeAF1t7cufcc8658c658UlJSV/2XkRERESkkwhkQC7is15f8PUMHzEcwjlX6Zy72T+e+EYgCdjmP/aic+5M51w2sB/Y5L/sJuCv/q/fwDeUQ0RERETklAhkQP4QSDezQWYWBVwDvO09wczi/ccAvg0sdM5V+o8l+z/3xzcM41X/eXuAHP/X0/gsOIuIiIiIfGkRgXpg51yjmX0XeBcIB15yzq03s9v9x5/FNxnvZTNrAjYAszwP8Rcz6wU0AHc45yr87bcAT5pZBFAL3BqoexARERGRzidgARnAOfcO8M5Rbc96vl4GpB99nf/Y5OO0LwbGncIyRURERERaaCc9EREREREPBWQREREREQ8FZBERERERDwVkEREREREPBWQREREREQ8FZBERERERDwVkEREREREPBWQREREREQ8FZBERERERDwVkEREREREPBWQREREREQ8FZBERERERDwVkEREREREPBWQREREREQ8FZBERERERDwVkEREREREPBWQREREREQ8FZBERERERDwVkEREREREPBWQREREREQ8FZBERERERDwVkEREREREPBWQREREREQ8F5BDT3OzILShl36E6AKrrG2ludkGuSkRERKTjUEAOIfsP13PlM0v55m8+pLK2EYCSyjqueGZpS2AWERERkS9HATmE3PP6WtbuOnBM+7pdB7jn9bXtXo+IiIhIR6SAHCI2lVSxsLDsuMcXbSqnoLiqHSsSERER6ZgUkEPEuqKDJz+nld5lEREREfl8FJBDRExk+EnPyS+uxDlN2BMRERH5MhSQQ8TkjMSThuSXlmzn8qeWsGRzeTtVJSIiItLxKCCHiO7RkdxzfvpJz/u46CDfeGEF17+wgo+LDgS+MBEREZEORgE5hNyaPZiffzWL3j2iW9rCw4z/+moWb31nIpOGJra0L95czmW/WsIdf1jDlrJDwShXREREJCRZZxizOn78eLdq1apgl3HKNDY1k/NILrsP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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=05546ed7">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h3 id="Data-Preparation">Data Preparation<a class="anchor-link" href="#Data-Preparation">¶</a></h3><h4 id="Explore-the-dataset-further">Explore the dataset further<a class="anchor-link" href="#Explore-the-dataset-further">¶</a></h4><p><em>TODO</em></p>
<li>Check for missing values and handle if any</li>
<li>Check for outliers if any and handle them</li>
<li>Implement Correlation heatmap</li>
<li>Check the distribution of data using histograms</li>
<li>Prepare the data for modeling by carrying out any steps that you think are necessary</li> (masalan feature scaling mitoonim anjam bedim ba standard scalar chon ke az plot e outlier ha mishe fahmid ke scale ashoon aslaaan yeki nist)


</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=6c45224a-0dd2-478f-b955-0dbfc99c6ae7">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>There are no missing values in our dataset.</p>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=2d039198-fb5b-4e10-b1ae-14b789ef75d0">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [6]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Check for missing values and handle if any</span>
<span class="kn">import</span> <span class="nn">missingno</span> <span class="k">as</span> <span class="nn">msno</span>

<span class="n">msno</span><span class="o">.</span><span class="n">matrix</span><span class="p">(</span><span class="n">wine</span><span class="p">,</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span><span class="mi">3</span><span class="p">))</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
<div class="jp-OutputPrompt jp-OutputArea-prompt">Out[6]:</div>
<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain" tabindex="0">
<pre>&lt;AxesSubplot:&gt;</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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KCGBKIQQQgghSkggCiGEEEKIEhKIQgghhBCihASiEEIIIYQoIYEohBBCCCFKSCAKIYQQQogSEohCCCGEEKKEBKIQQgghhCghgSiEEEIIIUpIIAohhBBCiBISiEIIIYQQooQEohBCCCGEKCGBKIQQQgghSkggCiGEEEKIEhKIQgghhBCihASiEEIIIYQoIYEohBBCCCFKSCAKIYQQQogSEohCCCGEEKKEBKIQQgghhCghgSiEEEIIIUpIIAohhBBCiBISiEIIIYQQooQEohBCCCGEKCGBKIQQQgghSkggCiGEEEKIEhKIQgghhBCihASiEEIIIYQoIYEohBBCCCFKSCAKIYQQQogSEohCCCGEEKKEBKIQQgghhCghgSiEEEIIIUpIIAohhBBCiBISiEIIIYQQooQEohBCCCGEKCGBKIQQQgghSkggCiGEEEKIEhKIQgghhBCihASiEEIIIYQoIYEohBBCCCFKSCAKIYQQQogSEohCCCGEEKKEBKIQQgghhCghgSiEEEIIIUpIIAohhBBCiBISiEIIIYQQooQEohBCCCGEKCGBKIQQQgghSkggCiGEEEKIEhKIQgghhBCihASiEEIIIYQoIYEohBBCCCFKSCAKIYQQQogSEohCCCGEEKKEBKIQQgghhCghgSiEEEIIIUpIIAohhBBCiBISiEIIIYQQooQEohBCCCGEKCGBKIQQQgghSkggCiGEEEKIEhKIQgghhBCihASiEEIIIYQoIYEohBBCCCFKSCAKIYQQQogSEohCCCGEEKKEBKIQQgghhCghgSiEEEIIIUpIIAohhBBCiBISiEIIIYQQooQEohBCCCGEKCGBKIQQQgghSkggCiGEEEKIEhKIQgghhBCihASiEEIIIYQoIYEohBBCCCFKSCAKIYQQQogSEohCCCGEEKKEBKIQQgghhCghgSiEEEIIIUpIIAohhBBCiBISiEIIIYQQooQEohBCCCGEKCGBKIQQQgghSkggCiGEEEKIEhKIQgghhBCihASiEEIIIYQoIYEohBBCCCFKSCAKIYQQQogSEohCCCGEEKKEBKIQQgghhCghgSiEEEIIIUpIIAohhBBCiBISiEIIIYQQooQEohBCCCGEKCGBKIQQQgghSkggCiGEEEKIEhKIQgghhBCihASiEEIIIYQoIYEohBBCCCFKSCAKIYQQQogSEohCCCGE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
"/>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=42e05c29-2d96-4bbb-ab82-fbf8bbb5ee56">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>There are obviously some outliers in our dataset which need to be handled. Also, from this graph we can see that the features are not on the same scale so we have class imbalance which we will need to handle using feature scaling.</p>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=25f0321a-cb35-43bb-9e3f-701ce3a9fdd4">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [7]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Check for outliers if any and handle them</span>
<span class="n">fig</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span> <span class="o">=</span> <span class="p">(</span><span class="mi">15</span><span class="p">,</span><span class="mi">8</span><span class="p">))</span>
<span class="n">wine</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">'quality'</span><span class="p">],</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span><span class="o">.</span><span class="n">boxplot</span><span class="p">(</span><span class="n">grid</span><span class="o">=</span><span class="kc">False</span><span class="p">)</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
<div class="jp-OutputPrompt jp-OutputArea-prompt">Out[7]:</div>
<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain" tabindex="0">
<pre>&lt;AxesSubplot:&gt;</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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3wBgmfi5n/u5fPvb387evXvz7W9/Oz/3cz836pIAlr2DhrbW2ieTDLsL7aVJLmutPdBa+3qS65M85zDqAwB65LLLLssZZ5yRsbGxnHHGGbnssstGXRLAsnc4NyL5+aq6pjt98sSu3xOSfGvKMDd2/QCAJW7VqlW56667ct9992Xv3r257777ctddd2XVKvc1A1hMh7qUvSTJU5I8K8nNSd7W9a8Zhp3xh+Cq6jVVtb2qtt92222HWAYAcKSccMIJaa3llltuSZLccsstaa3lhBNOGG1hAMvcIYW21totrbU9rbW9Sd6T75wCeWOSJ04Z9NQkN80yjXe31iZaaxMnn3zyoZQBABxBs91wxI1IABbXIYW2qnrclIc/kWTfnSU/nOQVVXVUVZ2R5KlJPnd4JQIAffK6170uu3btyute97pRlwKwIgxzy//JJJ9O8j1VdWNVbUjyH6vq2qq6Jsm6JG9IktbajiQfSPLlJH+e5PWttT2LVj0AcEQde+yxOe+88/LIRz4y5513Xo499thRlwSw7FVrM15ydkRNTEy07du3j7oMAGAOVZWTTz45U69F3/e4D9sTAEtZVV3dWpuY6Tm3ewIAhjb95mFuJgaw+IQ2AACAHhPaAAAAekxoAwCG9uQnPzlnnnlmVq1alTPPPDNPfvKTR10SwLK3etQFAABLx9e+9rX93Tt27BhhJQArhyNtAAAAPSa0AQAA9JjQBgAMbWxsbM7HACw8oQ0AGNqePXvytre9Lffcc0/e9ra3Zc+ePaMuCWDZq9baqGvIxMRE2759+6jLAADmUFVJkhNPPDG33377/v9J0oftCYClrKqubq1NzPScI20AwNCe/exnZ9euXUmSXbt25dnPfvZoCwJYAYQ2AGAop556anbu3JnVqwe/GLR69ers3Lkzp5566ogrA1jehDYAYChPf/rTc99992X37t1Jkt27d+e+++7L05/+9BFXBrC8CW0AwFCuvPLKVFUe+9jHHvD/yiuvHHVpAMua0AYADGXv3r157nOfm127dqW1ll27duW5z31u9u7dO+rSAJa11aMuAABYOj7zmc/s737ggQcOeAzA4nCkDQCYl+c973m56aab8rznPW/UpQCsCI60AQDz8tnPfjaPf/zjMzY2NupSAFYER9oAgKEdf/zx2bNnT5Jkz549Of7440dcEcDyJ7QBAEO78847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
"/>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=d501f196-74ed-41e4-8ef9-86d4b4a94e27">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>As the number of outliers detected in total are more than 25% of our dataset, then not dropping them would be more reasonable. We will try to cap and floor the outliers by the 10th and 90th percentile.</p>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=d70d4db6-428a-407c-9322-b66ff64054ae">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [8]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># handling the outliers present</span>

<span class="n">df</span> <span class="o">=</span> <span class="n">wine</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>

<span class="n">Q1</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">quantile</span><span class="p">(</span><span class="mf">0.25</span><span class="p">)</span>
<span class="n">Q3</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">quantile</span><span class="p">(</span><span class="mf">0.75</span><span class="p">)</span>
<span class="n">IQR</span> <span class="o">=</span> <span class="n">Q3</span> <span class="o">-</span> <span class="n">Q1</span>

<span class="c1"># This part of the code is taken from StackOverflow</span>
<span class="n">df</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="o">~</span><span class="p">((</span><span class="n">df</span> <span class="o">&lt;</span> <span class="p">(</span><span class="n">Q1</span> <span class="o">-</span> <span class="mf">1.5</span> <span class="o">*</span> <span class="n">IQR</span><span class="p">))</span> <span class="o">|</span><span class="p">(</span><span class="n">df</span> <span class="o">&gt;</span> <span class="p">(</span><span class="n">Q3</span> <span class="o">+</span> <span class="mf">1.5</span> <span class="o">*</span> <span class="n">IQR</span><span class="p">)))</span><span class="o">.</span><span class="n">any</span><span class="p">(</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)]</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">"Number of outliers detected </span><span class="si">%d</span><span class="s2">"</span> <span class="o">%</span> <span class="p">(</span><span class="nb">len</span><span class="p">(</span><span class="n">wine</span><span class="p">)</span> <span class="o">-</span> <span class="nb">len</span><span class="p">(</span><span class="n">df</span><span class="p">)))</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">"Proportion of outliers to the whole dataset is </span><span class="si">%f</span><span class="s2">"</span> <span class="o">%</span> <span class="p">((</span><span class="nb">len</span><span class="p">(</span><span class="n">wine</span><span class="p">)</span> <span class="o">-</span> <span class="nb">len</span><span class="p">(</span><span class="n">df</span><span class="p">))</span><span class="o">/</span><span class="nb">len</span><span class="p">(</span><span class="n">wine</span><span class="p">)))</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>Number of outliers detected 420
Proportion of outliers to the whole dataset is 0.262664
</pre>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=59aaa6cc-5499-4ef6-9f1d-dc9277f77931">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [9]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># handling the outliers present</span>

<span class="n">df</span> <span class="o">=</span> <span class="n">wine</span><span class="o">.</span><span class="n">copy</span><span class="p">()</span>

<span class="n">tenth_percentile</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">quantile</span><span class="p">(</span><span class="mf">0.1</span><span class="p">)</span>
<span class="n">ninetieth_percentile</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">quantile</span><span class="p">(</span><span class="mf">0.9</span><span class="p">)</span>

<span class="n">df</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">'quality'</span><span class="p">],</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span><span class="o">.</span><span class="n">clip</span><span class="p">(</span><span class="n">tenth_percentile</span><span class="p">,</span> <span class="n">ninetieth_percentile</span><span class="p">,</span> <span class="n">axis</span> <span class="o">=</span> <span class="mi">1</span><span class="p">)</span>

<span class="c1"># savng the dataframe for future use</span>
<span class="n">df</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">assign</span><span class="p">(</span><span class="n">quality</span> <span class="o">=</span> <span class="n">wine</span><span class="p">[</span><span class="s1">'quality'</span><span class="p">])</span>
<span class="n">wineMod</span> <span class="o">=</span> <span class="n">df</span>

<span class="n">wineMod</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
<div class="jp-OutputPrompt jp-OutputArea-prompt">Out[9]:</div>
<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html" tabindex="0">
<div>
<style scoped="">
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
<thead>
<tr style="text-align: right;">
<th></th>
<th>fixed acidity</th>
<th>volatile acidity</th>
<th>citric acid</th>
<th>residual sugar</th>
<th>chlorides</th>
<th>free sulfur dioxide</th>
<th>total sulfur dioxide</th>
<th>density</th>
<th>pH</th>
<th>sulphates</th>
<th>alcohol</th>
<th>quality</th>
</tr>
</thead>
<tbody>
<tr>
<th>0</th>
<td>7.4</td>
<td>0.700</td>
<td>0.010</td>
<td>1.9</td>
<td>0.076</td>
<td>11.0</td>
<td>34.0</td>
<td>0.9978</td>
<td>3.51</td>
<td>0.56</td>
<td>9.4</td>
<td>5</td>
</tr>
<tr>
<th>1</th>
<td>7.8</td>
<td>0.745</td>
<td>0.010</td>
<td>2.6</td>
<td>0.098</td>
<td>25.0</td>
<td>67.0</td>
<td>0.9968</td>
<td>3.20</td>
<td>0.68</td>
<td>9.8</td>
<td>5</td>
</tr>
<tr>
<th>2</th>
<td>7.8</td>
<td>0.745</td>
<td>0.040</td>
<td>2.3</td>
<td>0.092</td>
<td>15.0</td>
<td>54.0</td>
<td>0.9970</td>
<td>3.26</td>
<td>0.65</td>
<td>9.8</td>
<td>5</td>
</tr>
<tr>
<th>3</th>
<td>10.7</td>
<td>0.310</td>
<td>0.522</td>
<td>1.9</td>
<td>0.075</td>
<td>17.0</td>
<td>60.0</td>
<td>0.9980</td>
<td>3.16</td>
<td>0.58</td>
<td>9.8</td>
<td>6</td>
</tr>
<tr>
<th>4</th>
<td>7.4</td>
<td>0.700</td>
<td>0.010</td>
<td>1.9</td>
<td>0.076</td>
<td>11.0</td>
<td>34.0</td>
<td>0.9978</td>
<td>3.51</td>
<td>0.56</td>
<td>9.4</td>
<td>5</td>
</tr>
</tbody>
</table>
</div>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=7610b8fe-c4ba-4dee-ae02-49ba552556ba">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>The correlation heatmap shows that there is no feature that is highly correlated (correlation &gt; 0.5) with the <code>quality</code> of the wines.</p>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=5c9c9ac0-ddc1-4bd7-a1ae-935aed91d338">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [10]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Implement Correlation heatmap</span>

<span class="n">corrMatt</span> <span class="o">=</span> <span class="n">wineMod</span><span class="o">.</span><span class="n">corr</span><span class="p">()</span>
<span class="n">mask</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">(</span><span class="n">corrMatt</span><span class="p">)</span>
<span class="n">mask</span><span class="p">[</span><span class="n">np</span><span class="o">.</span><span class="n">tril_indices_from</span><span class="p">(</span><span class="n">mask</span><span class="p">)]</span> <span class="o">=</span> <span class="kc">False</span>
<span class="n">fig</span><span class="p">,</span><span class="n">ax</span><span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">()</span>
<span class="n">fig</span><span class="o">.</span><span class="n">set_size_inches</span><span class="p">(</span><span class="mi">20</span><span class="p">,</span><span class="mi">10</span><span class="p">)</span>
<span class="n">sns</span><span class="o">.</span><span class="n">heatmap</span><span class="p">(</span><span class="n">corrMatt</span><span class="p">,</span> <span class="n">mask</span><span class="o">=</span><span class="n">mask</span><span class="p">,</span><span class="n">vmax</span><span class="o">=</span><span class="mf">.8</span><span class="p">,</span> <span class="n">square</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span><span class="n">annot</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child jp-OutputArea-executeResult">
<div class="jp-OutputPrompt jp-OutputArea-prompt">Out[10]:</div>
<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain" tabindex="0">
<pre>&lt;AxesSubplot:&gt;</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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B0abWS7Qewf7KjCzU4FnzSwS/3yCAcDmEmHvAF+a2RRgOv6ORGXzOB941cxygKqVACopNCSEW88bzuUPv4TP52N4n160b5nMh9/9AcApA3vTrnkSh3beh5NvfgIz44S+B9GhZTIAAw/qyGm3PUWIx8O+bZpzUv+DayLNCn03/mcGDjqSf2b8QG5uLlddfkvxtg8+folrr7qdtWvX8dQTLzLmlSe4/Mrz2LIlh2uvuh2Am265ivj4xjz+xL0AFBUV0f/IE2ot/7JG3v0Ik6fNJCtrE/2Hn8UVF57NicdUrZMnIiIiUhOsojHaUn/lTR27x/3Bmh15Y12nsEvSltZIP61GhSW2q+sURETkv6n8RL//iJwXrq7Va6uoy5+tl+fyvzh8SEREREREquA/N3xIRERERKTS9PQhQJUCEREREZGgp0qBiIiIiASvevxEoNqkSoGIiIiISJBTpUBEREREgpcqBYAqBSIiIiIiQU+dAhERERGRIKfhQyIiIiISvPRDvoAqBSIiIiIiQU+VAhEREREJXppoDKhSICIiIiIS9FQpEBEREZHg5dOcAlClQEREREQk6KlSICIiIiLBy2lOAahSICIiIiIS9FQpEBEREZHgpTkFgCoFIiIiIiJBT5WCPczGG56o6xSq7MuGnes6hV2SOuTiuk6hylLGvVTXKVRZWGK7uk5BRESCmNPvFACqFIiIiIiIBD1VCkREREQkeGlOAaBKgYiIiIhI0FOlQERERESCl36nAFClQEREREQk6KlTICIiIiIS5DR8SERERESClyYaA6oUiIiIiIjUG2Y2xMzmm9kiM7tlB3E9zcxrZidVx3FVKRARERGR4FWPfrzMzEKA54CBwCpgspmNdc7NrSDuUWB8dR1blQIRERERkfqhF7DIObfEOVcAvA8cV0Hc1cAnwLrqOrA6BSIiIiISvHyuVl9mdomZTSnxuqRENs2BlSWWVwXWFTOz5sDxwOjqPA0aPiQiIiIiUkucc2OAMdvZbBU1KbP8FHCzc85rVlH4rlGnQERERESCV/368bJVQMsSyy2ANWViegDvBzoEicAwMytyzn2+OwdWp0BEREREpH6YDHQws7bAauA04IySAc65tlvfm9nrwFe72yEAdQpEREREJJjVo98pcM4VmdlV+J8qFAK86pybY2aXBbZX6zyCktQpEBERERGpJ5xz3wDf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eWXjn4twWWDY0nz8Q4hqj9dL9tNPE/f44+DxkPftt3iXLSPy2GMByB07lkbnnosnJobo668vbpN56aW1kJuPJbe9zAHv3QEhHta99yO581eRfM4gANa+OYEN308lrn83uv05Cl9uPouuex6A8KZxdHjmKizEAx4jY+zvbPjuHwDaPXQhnvAwDvjA/7jPzf8sZPHNY2rsM2Q+/ixNn30UQjxsGfsthUuW0+jEo/3H/uQrPAlxJL/5Ap6GUeAc0aefSOopF+C25GARETTo1Z3MB5+smfx20ci7H2HytJlkZW2i//CzuOLCsznxmMF1nZaIiEj1qMeTf2uTlRu3LbvNzCIAr3OuyMx6Ay8457pUx753Z/hQXVk0r+qTbeuDli32vCE8KeNequsUqiwssV1dpyAiIju3owey7NE233BsrV5bNXpibL08l/WmUvAf0wr4MPDbCwXAxXWcj4iIiIhUwKlSAKhTUCOccwuBrnWdh4iIiIhIZahTICIiIiLBS5UCoH49fUhEREREROqAKgUiIiIiErx8+p0CUKVARERERCToqVIgIiIiIsFLcwoAVQpERERERIKeKgUiIiIiErxUKQBUKRARERERCXqqFIiIiIhI0HJOlQJQpUBEREREJOipUyAiIiIiEuQ0fEhEREREgpcmGgOqFIiIiIiIBD1VCkREREQkeKlSAKhSICIiIiIS9FQpEBEREZGg5VQpANQp2ONYyJ73xU1psqmuU9gleVvC6jqFKss86YK6TqHK4j9+ta5T2CVhie3qOgUREZFqo06BiIiIiAQvVQoAzSkQEREREQl6qhSIiIiISPDy1XUC9YMqBSIiIiIiQU6VAhEREREJWnr6kJ8qBSIiIiIiQU6VAhEREREJXqoUAKoUiIiIiIgEPVUKRERERCR46elDgCoFIiIiIiJBT50CEREREZEgp+FDIiIiIhK09EhSP1UKRERERESCnCoFIiIiIhK8NNEYUKVARERERCToqVIgIiIiIkFLcwr8VCkQEREREQlyQVkpMLPXga+ccx+XWd8msP7AKuyrGfCMc+6kCrb9DIxwzk3ZrYR3U3jPXjS68mrweMj75mty3n+31PaI/gNoeNoZALjcXLKfeoKiJYvxNGlCzC2344mLB+cj9+svyf30k1rJOfLQHiTcfDkW4mHTp+PY+MoHpbaHtW1Jk/tvJGK/9mQ+8zob3/i49A48Hpq/P4qidemkXXVXreQMEHVYd5redjl4PGz8eBwbXv6wTN4tSH7oRiL234uMp95gw2v+8xmanEjyIyMJSYwD59j44TdkvfVFreW9VXivXkRfdRWEhJD79dfkvFv6u9JgwACiTj8dCHxXnnySosWLaz3PnbnjoSeY9NvfxMc15vO3R9d1OiIiUp9pTgEQpJ2C6mJmoc65NUC5DkG94fEQfc11bLjpRnzr1xP3/Ivk//Eb3uXLi0O8qalsuP4a3ObNhPc6iOgbRrDhqsvB62Xz6OcoWrgQi4wkbvRLFPwzpVTbmso58farSL3kForWptP8/WfJ+ekPCpes2JbzxmwyHn6eqH6HVLiL2LOOp3DpCqxhVM3mWpLHQ9M7r2T1hbdRmJZO6w+fYctPf1KweFvevo3ZrHvwBRr1712qqfP6WP/YS+TPXYRFRdL6k2fJ+X1aqba1kX/0tdeSNWIE3vXriR89mvzfKviuXHtt4LvSi5gbbyTziitqL8dKGj5sIGeceCy33f9/dZ2KiIjIHiEohg+Z2TlmNtPMZpjZW4HVR5jZ72a2xMwqusvfwMxeM7NZZjbNzPoG1p9nZh+Z2ZfABDNrY2azA9sizez9wLE+ACJL7G+Qmf1hZlMD7RsF1j9iZnMDbar9CiZ03/0oWr0aX2oqFBWR/9OPRBxyWKmYorlzcJs3A1A4dw6eJk0A8GVmUrRwIeC/K+xdvhxPYpPqTrGciI77ULhiDUWr1kJREVu+nUjDvqUv/n2ZWeTPWQBF3nLtQ5ISiTq8F5s+GVfjuZbUoNM+FK5IpXDVWigsYtM3E2nYr/TFvzdzI/mzy+ftXZ9J/txFALicXAoWryQ0KaHWcgcI23dfvKtX4w18V/J+/JGIQw8tFVM4p+R3ZW7xd6W+6dGlI7Ex0XWdhoiI7AGcr3Zf9dV/vlJgZgcAtwOHOufSzSweeAJIAQ4D9gXGAmXGn3AlgHOuo5nti78DsHdgW2+gk3MuMzDkaKvLgRznXCcz6wRMDeSQCNwBDHDObTGzm4EbzGwUcDywr3POmVnj6v78IYmJ+NavK172rV9P6H77bTe+wdCjKPj7r3LrPUnJhLbvQNG/c6s7xXJCmyZStHZ98XJR2noiOu1b6fYJN11OxpMv44mK3HlwNQptmlAm73QiO+1T9f00SyJiv73ImzG/OtPbKU+TJvjWb8vft349Yfvvv934yKOOouDvv2sjNREREalhwVAp6Ad87JxLB3DOZQbWf+6c8znn5gJJFbQ7DHgr0GYesBzY2in4rsR+SjoCeDvQZiYwM7D+YGB/4Dczmw6cC7QGNgF5wMtmdgKQU9EHMLNLzGyKmU15c3VqpT94oHX5VduZZB/WpSuRQ49i80svlt5Dg0hi77mPzc8/i8upMMXqVUHKuMo9GSDqiIPwZmZRMHdh9eZUGVY+cVfJvIt3EdWAZs/cwfpHXsS3pRbO9c5sJ/+wLl2IHDaM7BdfrHC7iIjIHsNXy6966j9fKcB/iVnRlU1+mZiK2m3Plh1sq+hYhr8jcXq5DWa9gP7AacBV+DsxpXfo3BhgDMC6/kdW6SrTm74eT5OmxcueJk3wZaSXiwtp146YG0eSdetNuE2bSmwIIeae+8j74Xvyf/2lKofeZUVp6YQmbxuWEprUBO+6ivpg5UV0PYCGfQ8m6vCeWEQ4noZRNHn4Ztbf+mhNpVusfN6JFFUyb3+DEJo9fSebvvyJzd/9VgMZ7phv/fpSw4E8TZrgTS//XQlt146YkSPJuvnm0t8VERER2WMFQ6XgB+AUM0sACAwfqoxJwJmBNnsDrYCdjeco2eZAoFNg/Z/AoWbWPrAtysz2DswriHXOfQNcB3SpZG6VVjRvHqHNW+BJTobQUCL69iP/99IXnJ6mTYm95342Pvwg3lWrSm2LHnEz3hXLyf249FN0alL+7PmEtW5OaHN/zg2HHsmWn/+oVNsNT7/KigFnsnLIOawb+RC5f0+vlQ4BQN6s+YS1bkZo8yQICyVm2JFs+enPSrdPfuB6CpasIOuNT2swy+0rnD+fkBbbvisN+vUj//ffS8V4mjYl9v772fTQQ+W+KyIiInsizSnw+89XCpxzc8zsQWCimXmBaZVs+jww2sxmAUXAec65fKtgiEgJLwCvmdlMYDrwdyCH9WZ2HvCemUUEYu8AsoEvzKwB/mrC9VX6cJXh85L97FM0fvT/MI+H3G+/wbt8GQ2OPhaAvK/G0vDsc/HExBJ9beDwXi8brriUsAM7EjloMEVLFhP34ssAbHnlpQrnHFQrr4/0h0aRPPohLMRD9mfjKVy8nOiTjwIg+6OvCUmIo/kHo/A0jML5HLFnH8/K4y7G1eWQG6+P9Q88T4uXHwSPh02fTqBg0XJiTx0GwMYPviEkMY5WHz2Dp1EU+ByNzxnO8qMvJXyftsQcN4D8+Utp9elzAGQ89TpbJk2uxfy9ZD/9NHGPP+5/fO233+JdtozIY/3fldyxY2l07rl4YmKIvn7bdyXz0ktrL8dKGnn3I0yeNpOsrE30H34WV1x4NiceM7iu0xIREam3rKpjnqVuVXX4UH2weV3EzoPqoaKiPa+QFpuUV9cpVFn8x6/WdQq7JCyxXV2nICJSm3Z4V3RPlj64dq+tEsdPrJfncs+76hERERERkWqlToGIiIiISJD7z88pEBERERHZnvo8+bc2qVIgIiIiIhLkVCkQERERkaClSoGfKgUiIiIiIkFOlQIRERERCVqqFPipUiAiIiIiEuTUKRARERGR4OWsdl87YWZDzGy+mS0ys1sq2H6mmc0MvH43s87VcRrUKRARERERqQfMLAR4DhgK7A+cbmb7lwlbChzpnOsE3A+MqY5ja06BiIiIiAStejanoBewyDm3BMDM3geOA+ZuDXDO/V4i/k+gRXUcWJUCEREREZFaYmaXmNmUEq9LSmxuDqwssbwqsG57LgS+rY68VCkQERERkaDlfDsf51+tx3NuDNsf8lNRMq7CQLO++DsFh1VHXuoUiIiIiIjUD6uAliWWWwBrygaZWSfgZWCocy6jOg6sToGIiIiIBK16NqdgMtDBzNoCq4HTgDNKBphZK+BT4Gzn3ILqOrA6BSIiIiIi9YBzrsjMrgLGAyHAq865OWZ2WWD7aOAuIAF43swAipxzPXb32OoUiIiIiEjQcpX47YDa5Jz7BvimzLrRJd5fBFxU3cfV04dERERERIKcKgV7mDcXttx5UD3TNb+wrlPYJZmePe+fR4ec7LpOocqmHXBbXaewS/rPeaiuU6iysMR2dZ2CiIjUU3veVY+IiIiISDWpZxON64yGD4mIiIiIBDlVCkREREQkaNX2j5fVV6oUiIiIiIgEOVUKRERERCRoOVfXGdQPqhSIiIiIiAQ5VQpEREREJGhpToGfKgUiIiIiIkFOlQIRERERCVqqFPipUiAiIiIiEuRUKRARERGRoKWnD/mpUiAiIiIiEuRUKRARERGRoKU5BX6qFIiIiIiIBDlVCkREREQkaDmnSgGoUiAiIiIiEvTUKRARERERCXJVGj5kZtcAlwNTnXNn1kxKlcrjHmCzc+7/zGxf4H3AASc55xZXw/6XAT2cc+lm9rtz7pBd2MdlQI5z7s0y69sAXznnDtzdPKui371n07ZvF4py8/n2xjGsm72sXEzXcwfS7cIhxLVJ4rnOl5G7YXPxtpYH70ffu8/CExZCbmY2H5zyYLXkFd+3M3s/cB4W4mHNOz+y/NkvysXs/eB5JPTvijc3n3+veYHsWUsr1bbV5UfT4Z6zmbTfRRRmZmNhIez7+CXEdGmH8zkW3PE6Wb/PrZbP0eX+c0jp35mi3AImX/ciWbOWlYuJatmEg0dfRXjjRmTNWsZfVz+PK/TSpPd+HPr6DWxZsR6AVd9M5t8nPwOg/UWDaXdmXzBj6Ts/sfClcdWSb/SR3Wh+90VYSAgZ709g3QuflItpfs/FxPTtgS83nxUjniJ39hIi2jWnzaiRxTHhrZJZ+8S7rH91LJH7t6XFg1fgiQjDeb2sumM0OTMWVku+W+334Lkk9u+KLzefWde8wKYKznNkqyZ0fvFawho3ZNOsZcy8chSu0EvD9s3o+PRlxHRsy4KHP2DZC18B0KBZAh1HXUFEk8Y4n49Vb//I8pe+rda8K+OOh55g0m9/Ex/XmM/fHl3rxxcRCVbOV9cZ1A9VrRRcAQwr2yEws7qcmzAc+MI517WyHYKq5LsrHYJAu9FlOwR1pW3fzsS1SeaVI25kwi2vMPDB8yqMWz1lAR+d8TAbV64vtT4iJooBD57HZxc+wesDbuHLy5+tnsQ8xj6PXMD0Mx7mz8NvIOn4Q2m4d/NSIQn9uxDZNpk/Dr6WeSNeYp/HLqxU24hmCcQf2YncEp+l+Vn9Afirz0imnfIAHe45G2z3xxEm9+tMo3bJfHvIjfwz8hW6PXJ+hXGd7jiNhWO+ZdyhN1KwcQttT+9TvG39X/P5buBtfDfwtuIOQcw+LWh3Zl9+GHYX3/W/lZQBXWnUNmm388XjocX9l7Lk3HuZN+BK4o49gogOLUuFRPftTkTbZvx75KWsvPU5WjxwOQD5S1Yzf9h1/tfRN+DLzSdr/B8ApNx6Hmuffo/5w64j9Yl3aXbrebufawmJ/bsQ1TaFXw6+jtkjXmL/xy6qMG7vO85g2Ytf80vv6ynM2kyLM/oBUJi1mbm3v87SQGdgK1fkZf7db/Hr4Tfy57A7aXX+oHLfw9owfNhARj/xQK0fV0REBKrQKTCz0UA7YKyZXW9m95jZGDObALxpZk3M7BMzmxx4HRpo19DMXg2sm2Zmx1Ww7xQzm2Rm081stpkdHli/uUTMSWb2epl2w4DrgIvM7Ccza2Nms0tsHxGoKmBmP5vZQ2Y2Ebi2zH4SzGxCIL8XASuxbXPgv2Zmjwfym2VmpwbWP2NmdwXeDw58Dk/g/IwIrO9uZjPM7A/gyhL7Dgnsc7KZzTSzSyv796iK9oO6M+eTXwFInbaYiJiGNGzauFzcujnL2bQqvdz6/Y47hAXfTiZ7TQYAORmbqiWvmG7tyV2aRt7ydbhCL2mf/07ikJ6lYpoM6cnajyYBsOmfhYTGNCS8aeOdtt37vnNYdN87pX6RpOHeLdjwyywACtM3UbRpCzFd2u3252g2pDvLP/oFgMypiwiPiaJBBee36WEHsOqrvwFY9uEkmg/tscP9xnRoRsY/i/DmFuC8Ptb/+S/Nh/bcYZvKiOrSgfxlqRSsTMMVFrHhy1+IHXhQqZjYgQeR+clPAORMm09ITENCm8aViok+tBP5K9ZSuDrQ8XKOkEZRAIREN6RwXeZu51pS0pAerAl8Fzb+s4iwmCgiKjjPCYcdQNqXfwGw5sNJJAXOc0H6JjZNX4Ir9JaKz1+XVVxx8G7JY/PC1TRIjq/W3CujR5eOxMZE1/pxRUSCnc9Zrb7qq0p3CpxzlwFrgL7OuScDq7sDxznnzgCeBp50zvUETgReDsTcDvwYWN8XeNzMGpbZ/RnAeOdcF6AzML2SOX0DjA4ct28lmjR2zh3pnPtfmfV3A78657oCY4FWFbQ9Adia34DA50gBbgFONbO+wDPA+c6VK0S9BlzjnOtdZv2FwMbAuekJXGxmbSvxOaqkUXIc2akZxcvZazNplBy3gxalxbVLpkFsQ0794HbO+vp+9j/xsGrJq0FyPHlrtuWVvyaDiDJ5RaTEkbe6RExqBhEp8Ttsmzi4O/lrM9k8d3mpfWXPXU7ikJ5YiIcGrZoQ3akdEc0SdvtzRCbHk1Mil5zUTCJTSn+O8PhGFG7cgvP6vxq5qZlElvisCd3bM/D7hzjsnZuICdyl3jh/FU0O3pfwuEaERIaT0q8Lkc12/2I1LDmBwtRtnb/C1HTCkhPKx6zZVmUpXJtBWFLpmMbHHkHW2EnFy6vve5lmt53P/n+8QrPbz2fNo9VbKItIiSe3xHchLzWTiJTS5yMsPprCTTnF5zlvTfmYHYls2YSYA9uQNXVR9SQtIiKyh9jdYT9jnXO5gfcDgP1t23CMGDOLBgYBx269aw40wH/R/W+J/UwGXjWzMOBz59z03cxrez7Yzvoj8F/045z72sw2VBBzGPCec84LpAUqDj2dc2PN7GJgEnB92SFMZhaLvzMyMbDqLWBo4P0goJOZnRRYjgU6AEvL7OMS4BKAE+N6cXCjDpX+wABGBb3SKvymtyfEQ1LHtnx0+sOENgjjjM/vIXXqIjYsXVulPMonVpne8nZy305bT2Q4ba47nmkVzHlIffcnGnZoTs8JD5O3aj0bJy8ovnjcHRWl4sqe3wqD/P/ZMGsZX/e8Fm9OPsn9OnPIazcw7tAbyV64hnnPfckRH9xC0ZZ8suauqJZ8t3tOdxJSMsbCQokd0IvUEhf+iWcNZfX9L7Px2z9ofNShtHrsahafeVc15LsDVcx7R0KiIujyyvXMu/MNvJtzd95ARET+E/RIUr/d7RRsKfHeA/Qu0UkA/MNugBOdc/O3txPn3CQzOwI4CnjLzB4PjMcv+f/mDSqRTxGlqx9l22xh+3Z25bCjb0xHIANotp1229u3AVc758bv6MDOuTHAGID/a3VWpa5wupwzgE6n+4sna2cuITpl213e6OR4NqdlVWY3AGSv3UDuhpkU5uZTmJvPqr/m0WT/VrvdKchLzaBBiTv1Ec0SyF9buj+Wn5pJg+YJbNwak+KPsfDQCttGtkkislVTDvrxseL1vb57hMlDbqNg/UYW3rXtIrb7V/eRuyR1l3Lf67yB/gnAQOaMJUQ1S2DrPeyolHjy1maVii/IyCYstiEW4sF5fUSmxJOb5v+sRSUuQNf+OAPPIyGExzeiIHMzy96byLL3/P3JA289hdw1uz8kp3BtOmEpicXLYSmJFKaV3m9hagZhzZqwte8elpxQajhQdJ/u5MxeTFH6ts8Zf2I/Vt/zEgBZX/9Gy0ev3u1cW50/iBZn+ecEbJy+mMjmCWw9YoOU+HLfl8KMbMJioorPc4Nm5WMqYqEhdH31BlI/+ZW0bybvdt4iIiJ7mup8JOkE4KqtC2bWJfB2PHB1oHOAmXUt29DMWgPrnHMvAa8A3QKb0sxsPzPzAMdXIoc0oGlgjkAEcHQlc58EnBnIZShQ0diaSfiHCYWYWRP81YW/A7nfCHQFhppZqcHZzrksYKOZbR1zU3KS9njg8kCFBDPbu4KhVbtk+pvf8+bQ23lz6O0sGv8PBwSG/KR03Yv87By2rMuq9L4WTfiH5r32wUI8hDYIJ6XrXmQuXLPbOWZPW0xUu2QatGqChYWQNPwQ0sdPKRWzfvwUkk8+AoCY7h0oys6hYF3Wdttu+XclvxxwCb/3vJrfe15N/poM/h54CwXrN+KJDMcTFQFA/BEdcUU+tixYvUu5L379u+KJwau/nULrkw/377dbewqzc8mr4Pyu+20uLY7uBUCbU45gzbh/AIhoElscE9elHeYxCjL902kiEmIAiGyeQPNhPVnx+e+7lG9JOTMWEtG2GeEtk7CwUOKOOZxN3/1VKmbT938Tf6K/0xPVdR+82TkUrdt2cR137OGlhg4BFK7LpNHB/odqNTq0E/nLdv87suK1Cfze/xZ+738L676dQrPAdyG2e3sKs3PIr+A8Z/42l6Rj/P8Mm51yBGnjppSLKevAJy9l88LVLHvxm93OWURE9izOZ7X6qq+q86lB1wDPmdnMwH4nAZcB9wNPATMDHYNllL9Y7wOMNLNCYDNwTmD9LcBXwEpgNtBoRwk45wrN7D7gL/xDcOZVMvd7gffMbCowEVhRQcxnQG9gBv47/zfh74R8B4xwzq0xswuB182s7GzQ8/EPj8rB3xHY6mWgDTA1cG7W43+aUrVa8uN02vbtzEW//I/C3ALGjRhTvO2E10cw/uaX2ZKWRdfzB9HrsqNp2CSWcyc8zJIfZzDh5pfJXLSGZT/P5LwJD+N8Pma+/zPpC1btdl7O62P+ra/S9f3bIMRD6ns/s2X+KpqfMwCA1W9+T8b300js35Xefz2NL7eAude+sMO2OxKeGEuX928DnyN/bSZzrxq1258BYO0P00np34WhfzyBN7eAyde/WLztsLdHMuXGl8hLy2LWA+9x8OirOfDmk9kwezlL3/sZgBZH92Kvcwfgirx48wr587JtefV+5Voi4qLxFRYx7dbXKdyYs/sJe32suutF2r15DxbiIfPD78lbuJKEM4cAkPHOODb9OIXovt3Zb9KLgUeSPlPc3BqEE314F1be9nyp3a68eRTN77kYCwnBl1/Aylue2/1cS1j//TQS+3fhiL+expubz6xrtz22s/s7NzP7hjHkp21g/gPv0vnFa+hwy6lkz1rGqnf9E6bDm8RyyISHCI2OxPkcbS4Zyi+HjyB6/1Y0P+UIsucu55AfHgFgwUPvk/7D9GrNf2dG3v0Ik6fNJCtrE/2Hn8UVF57NiccMrtUcREQkeFm5sc9Sr1V2+FB90jW/sK5T2CWZnrp80u6u6RCeXdcpVNnavKi6TmGX9J/zUF2nUGVhibv/tC0RCVr19xb3bvq3w7Bavbbab+E39fJc6heNRURERESC3J53K1REREREpJrU53H+tUmVAhERERGRIKdKgYiIiIgErfr8K8O1SZUCEREREZEgp0qBiIiIiAQt/aKxnyoFIiIiIiJBTp0CEREREZEgp+FDIiIiIhK09Du+fqoUiIiIiIgEOVUKRERERCRo6ZGkfqoUiIiIiIgEOVUKRERERCRo6ZGkfqoUiIiIiIgEOVUKRERERCRo6elDfqoUiIiIiIgEOVUKRERERCRo6elDfqoUiIiIiIgEOVUK9jBxvrrOoOpSGm2u6xR2ScjmqLpOocpiG+fWdQpVFplfWNcp7BJf2tK6TqHK9sQzHZbYrq5TEJH/OD19yE+VAhERERGRIKdKgYiIiIgELc0p8FOlQEREREQkyKlSICIiIiJBSz9T4KdKgYiIiIhIkFOlQERERESCluYU+KlSICIiIiIS5NQpEBEREREJcho+JCIiIiJBSz9e5qdKgYiIiIhIkFOlQERERESClq+uE6gnVCkQEREREQlyqhSIiIiISNByaE4BqFIgIiIiIhL0VCkQERERkaDlc3WdQf2gSoGIiIiISJBTpUBEREREgpZPcwoAVQpEREREROoNMxtiZvPNbJGZ3VLBdjOzZwLbZ5pZt+o47g4rBWbWGDjDOff8TuLaAIc4596tRNxXzrkDq5Zmuf3cA2x2zv2fme0LvA844CTn3OLd2Xdg/8uAHs65dDP73Tl3yC7s4zIgxzn3Zpn1baiGc1BVB993Ni37daEoN59J148hY/aycjH7nTeQAy8aQkybJN7ueBn5GzYDELtXCkc8cQkJB7ZhymMfMfvFb2ozdQAaHtGd5DsvwUI8bPhgAhkvflRqe3i7FjR79DoaHNCe9U+8ScbLn9ZabvF9u9D+gfOxEA+p7/zAimc/LxfT/sHzSejfDW9uPvOueY7Ns5YCsM9Tl5MwsDuF6RuZfOSNxfH7j7meqL2aARAaE0XRphym9B9ZI/lHHtKD+JuvwDwesj/7lo2vflBqe1ibliTeN4KI/dqT+exrbHrz4+JtLb55C5eTi/P6wOtlzRlX1kiOZUUd1p2k2y8Dj4eNH48j86Uy34e2LUh++AYi9m9P+lNvsOHVTwAITU4k5dERhCTGgc+R9eG3ZL31Ra3kDPDr1Dk8+upH+HyOEwYcwoUnDC61/bXPv+ObSZMBKPJ6Wbp6LRNfe4zY6IbcNeotJk6ZRXxsNJ89fWet5bwjdzz0BJN++5v4uMZ8/vbouk5HRGSX1KenD5lZCPAcMBBYBUw2s7HOubklwoYCHQKvg4AXAv/dLTsbPtQYuALYYacAaAOcAeywU1BDhgNfOOfurmwDMwt1zhVVJnZXOgSBdvXm/yFb9OtMTNtkPjrsRpp024tDHj6PL4+5p1zcuskL+Pb7aQz76PZS6/OztvDHXW/RenD3Wsq4DI+HlHsuZ/m5d1C4Np12nz1J9g9/UrBoZXGId2M2a+97kehBvWs9tw6PXMiMU+4nf00m3cc/TPr4KeQsWFUcEt+/K5FtU/jr4KuJ6d6BvR+7mKlDbwNg7fs/s/qVcew36qpSu517yZPF7/e65xyKNuXUWP4Jt13N2ktvpigtnWbvjiLn5z8oXLKiOMS7KZuMR5+jYd9DK9xF6kUj8GVtqpn8KuLxkHTXlay64DYK09Jp/dHTbP7xLwoWl8h5YzbrHhhNowGlvw/O62Xdoy+RP3cx1jCSNp88Q87v00q1rSler4+HXvqAMXdfQ1JCY06/6VH69OzEXi1TimPOHz6Q84cPBODnyTN568sfiY1uCMCxfQ/mtKFHcvszb9R4rpU1fNhAzjjxWG67///qOhURkf+KXsAi59wSADN7HzgOKNkpOA540znngD/NrLGZpTjnUnfnwDsbPvQIsJeZTTezxwPlisfNbLaZzTKzU0vEHR6Iu97M2pjZL2Y2NfDa4YW1maWY2aRA+9lmdnhg/eYSMSeZ2etl2g0DrgMuMrOfAsedXWL7iEBVATP72cweMrOJwLVl9pNgZhPMbJqZvQjbuoxbc9jeZw+Ub+4KvB8c+BweM7vHzEYE1nc3sxlm9gdwZYl9hwT2OTlQ/rl0J3+PXdJ6UHcWffwrAOunLiY8piGRTRuXi8uYs5zNq9LLrc/L2ET6jCX4irw1kd5ORXbem4LlayhcuRYKi9j41SSiBxxcKsabsZG8WQuhsFJ9vWoT0609uUvXkrd8Ha6wiHWf/0bikB6lYhKH9CTto4kAbPpnIaExDQkPnP+Nf/5LUdbmsrstpcmxvVn32a81kn/EgftQuHINRavXQlERW8b9TFSf0v9cfZlZFMxZgCuq3XO7PQ067U3hijUUrvJ/H7K/mUij/mW+D5kbyZtdPmfv+g3kz/UXE92WXPIXryQ0KaFW8p69aBmtUprQIjmRsLBQhhzWnZ/+nrHd+G9/ncLQw7d9l3oc0KG4g1Bf9OjSkdiY6LpOQ0Rkt/hq+bUTzYGVJZZXBdZVNabKdtYpuAVY7Jzr4pwbCZwAdAE6AwOAx80sJRD3SyDuSWAdMNA51w04FXhmJ8c5AxjvnNu67+mVSd459w0wGnjSOde3Ek0aO+eOdM79r8z6u4FfnXNdgbFAqwra7uizn2pmffF/zvOdc2X/5q8B1zjnyt7GvhDY6JzrCfQELjaztpX4HFUSlRzHljUZxcs5qZk0TI6r7sPUmNCkBApTt3VWitamE1ZLF3I7E5EcT36Jc5u/JpOI5NK5RaTEk7+6RExqBhEp8ZXaf+zB+1G4fiO5S9dWT8JlhDRNxLt2ffGyd106oUmJVdiDI3n0IzR77zmiTxxW/QlWIDQpkcLUbTkXrU3fpQv70OZNabDfXuTNmF+d6W1XWkYWSQnb/t0lJcSxLnNjhbG5+QX8Nm0uAw/uWiu5iYhI7TGzS8xsSonXJSU3V9Ck7ENTKxNTZVV9+tBhwHvOOS+QFrjr3hMoO3YgDBhlZl0AL7D3TvY7GXjVzMKAz51z06uYV2V9sJ31R+C/6Mc597WZbaggpsLP7pwba2YXA5OA68vOaTCzWPydkYmBVW/hHwsGMAjoZGYnBZZj8Y8PW1pmH5cAlwCc3bgXRzbsUOkPHGhfbp2/4rSHqCD/eqOC1Fwl/u1W9vQ3Pf4w0mqoSgBUeG6r8t1IPfd6vOsz8MQ3Jnn0IxQuXUne1FnVmWHlVPHrbFENaP7MHax7+EV8W2poaFZl8tjO+omTZ9Jl33b1rjIgIvJfVNtzCpxzY4Ax29m8CmhZYrkFsGYXYqqsqk8fquxZux5Iw39XvQcQvqNg59wk/Bfmq4G3zOycrZtKhDWoxHGLKP2ZyrbZsqM0drLvHX32jkAG0Gw77ba3bwOuDlRYujjn2jrnJpRLzLkxzrkezrkele0Q7HfuAIaPf5Dh4x8kJ20DDZttu5MalRJPTlpWpfZTHxStTScsZdvd69DkRArTMnbQovbkp2YSUeLcRjSLp2BtZpmYDCKal4hJSSgXUxEL8dDkqF6s/+L36ku4DG/aekKSmxQvhzRNxLuu8ufWu94f68vMIufH3wg/cJ9qz7GsorR0wlK25RyanEhRFXImNITmz9zBpi9/YvN3NXduy0pKaExaxrb7DWkZG2gSH1th7Lhf/2HoYT1rKzUREak/JgMdzKytmYUDp+EfxVLSWOCcwND2g/GPOtmt+QSw805BNlBywOgk/ENlQsysCf4L+b8riIsFUgPDaM4GQnZ0EDNrDaxzzr0EvAJsfbRSmpntZ2Ye4PhKfJ40oGlgjkAEcHQl2mz9XGcGchkKVDS2psLPHsj9RqArMNTMSs3+ds5lARvN7LDAqjNLbB4PXB6okGBme5tZtdwa/PeN7/l88O18Pvh2lo/7h/Yn+Q/fpNteFGbnkLsuqzoOUytyZy4gvE1zwlokQVgosUcfweYf/qrrtADInraIyHYpNGjVFAsLpenwQ0kfP6VUTPr4KSSdfCQAMd07UJSdQ0Elzn/cEZ3IWbiG/NSddyB2Vf6c+YS1ak5o82QIDaXhkD7kTPyjUm0tsgEWFVn8PrJ3dwoXLauxXLfKm7WAsNbNCGvu/z5EDzuSzT/+Wen2yQ9cR/7ilWx4/bMazLK8A9q3ZnnqOlalpVNYWMS4X/+hT89O5eKyt+QyZe5C+vYqv01ERP7bAg/CuQr/NeK/wIfOuTlmdlngyZYA3wBLgEXAS/gfCrTbdjh8yDmXYWa/BSbvfgvcBPQGZuC/+32Tc26tmWUARWY2A3gd/9OKPjGzk4Gf2PEdeoA+wEgzKwQ2A1srBbcAX+GfTDEbaLSTfAvN7D7gL/xDcObt5Lhb3Qu8Z2ZTgYlARY8i+Ywynx1/J+Q7YIRzbo2ZXQi8bmZlb/Gdj394VA7+P/JWL+N/ctNU84/xWY//aUrVauWP02nRrzMn//o/ivIK+OWGbRWrQW+O4NeRL5OTlsX+Fwyi0+VHE9kkluO/e5hVP83g15EvE9kkluO+uZ+wRpE4n48DLxrCJ31vpnBzbnWnWjGvj7X3vkCr1+/HPB6yPv6O/IUriDvdPwprw3vfEpIYR7vPn8LTKAqcj/jzjmPxkMvw1XCOzutj4a2v0On92/2PJH3vJ3Lmr6LZOf4nyKx58zsyv59KQv+uHPTXs3hzC5h/7XPF7fcbfS2NDzmAsPhoek8bzdLHP2Ttuz8C0HT4oTU2wbiY10fGw6NIfuFh8HjI/nw8hYuXE32yvz+d/dFXhCTE0ey95/A0jML5HLFnncCq4y8ipHEMTZ+8BwALDWHzNz+R+/uUHRys+nJed/8LtHjlAfCEsPGTCRQsWkHsqf45DRs/+IaQxDhaf/yM//vg8xF3znCWHXUpEfu0JXb4APLnLyXqs1EApD/5BlsCjwGtSaEhIdx20alcft8ovD4fw/v3pn2rZnw4fhIApww+AoAf/5rOIZ33I6pBRKn2Nz3xKlNmLyArezMDLrqNK047ihMGVPxEqNoy8u5HmDxtJllZm+g//CyuuPBsTjxm8M4biojUI5WY/FurAnNmvymzbnSJ944SD66pLrZHjS0XXmlx1h73B+sdUdEUjfpv3eaouk6hylonZ9V1ClVWkL9n/rB6m09G1HUKVeZJqvbnGNS4sMR2dZ2CiPjV4wl+u2dc0mm1em01JO39enku98z/NxYRERERqQb1rVJQV6o60VhERERERP5jVCkQERERkaBV248kra9UKRARERERCXKqFIiIiIhI0PKpUACoUiAiIiIiEvRUKRARERGRoOXTnAJAlQIRERERkaCnSoGIiIiIBK097ldha4gqBSIiIiIiQU6VAhEREREJWvpFYz9VCkREREREgpwqBSIiIiIStHympw+BKgUiIiIiIkFPnQIRERERkSCn4UMiIiIiErT0SFI/VQpERERERIKcKgV7mDPe7lfXKVTZ5NO+resUdkn30/PqOoUq8yQm1XUKVeayc+o6hV0yrv8rdZ1Cle3beENdp1Bl7X59rq5TqLKwxHZ1nYKIVIEeSeqnSoGIiIiISJBTpUBEREREgpZPTyQFVCkQEREREQl6qhSIiIiISNDyoVIBqFIgIiIiIhL0VCkQERERkaCl3ynwU6VARERERCTIqVIgIiIiIkFLTx/yU6VARERERCTIqVIgIiIiIkFLv2jsp0qBiIiIiEiQU6VARERERIKWnj7kp0qBiIiIiEiQU6dARERERCTIafiQiIiIiAQtPZLUT5UCEREREZEgp0qBiIiIiAQtPZLUT5UCEREREZEgp0pBBczsHmCzc+7/qml/3wBnBBbPcM49Xx37razfZi/hsQ9/wOfzcfxhnblgyMHlYibPX8HjH/5AkddLXKMoXhlxBvmFRVzwf+9SWFREkdfHgG77cMWxh9dYnnF9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
"/>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=567f8687-73ee-429a-8adc-27110eaaf2d7">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>In the below graphs, we can see the distribution of data which would help us have a basic understanding of effects of different features on the quality of the wine.</p>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=1a463687-90e2-411f-831d-1ac4d26a7808">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [11]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Check the distribution of data using histograms</span>

<span class="n">sns</span><span class="o">.</span><span class="n">set_palette</span><span class="p">(</span><span class="s2">"dark"</span><span class="p">)</span>
<span class="n">features</span> <span class="o">=</span> <span class="nb">list</span><span class="p">(</span><span class="n">wineMod</span><span class="o">.</span><span class="n">drop</span><span class="p">([</span><span class="s1">'quality'</span><span class="p">],</span> <span class="n">axis</span> <span class="o">=</span> <span class="mi">1</span><span class="p">)</span><span class="o">.</span><span class="n">columns</span><span class="o">.</span><span class="n">values</span><span class="p">)</span>
<span class="k">for</span> <span class="n">i</span> <span class="ow">in</span> <span class="n">features</span><span class="p">:</span>
    <span class="n">quality3</span> <span class="o">=</span> <span class="nb">list</span><span class="p">(</span><span class="n">wineMod</span><span class="p">[</span><span class="n">wineMod</span><span class="p">[</span><span class="s1">'quality'</span><span class="p">]</span> <span class="o">==</span> <span class="mi">3</span><span class="p">][</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">dropna</span><span class="p">())</span>
    <span class="n">quality4</span> <span class="o">=</span> <span class="nb">list</span><span class="p">(</span><span class="n">wineMod</span><span class="p">[</span><span class="n">wineMod</span><span class="p">[</span><span class="s1">'quality'</span><span class="p">]</span> <span class="o">==</span> <span class="mi">4</span><span class="p">][</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">dropna</span><span class="p">())</span>
    <span class="n">quality5</span> <span class="o">=</span> <span class="nb">list</span><span class="p">(</span><span class="n">wineMod</span><span class="p">[</span><span class="n">wineMod</span><span class="p">[</span><span class="s1">'quality'</span><span class="p">]</span> <span class="o">==</span> <span class="mi">5</span><span class="p">][</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">dropna</span><span class="p">())</span>
    <span class="n">quality6</span> <span class="o">=</span> <span class="nb">list</span><span class="p">(</span><span class="n">wineMod</span><span class="p">[</span><span class="n">wineMod</span><span class="p">[</span><span class="s1">'quality'</span><span class="p">]</span> <span class="o">==</span> <span class="mi">6</span><span class="p">][</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">dropna</span><span class="p">())</span>
    <span class="n">quality7</span> <span class="o">=</span> <span class="nb">list</span><span class="p">(</span><span class="n">wineMod</span><span class="p">[</span><span class="n">wineMod</span><span class="p">[</span><span class="s1">'quality'</span><span class="p">]</span> <span class="o">==</span> <span class="mi">7</span><span class="p">][</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">dropna</span><span class="p">())</span>
    <span class="n">quality8</span> <span class="o">=</span> <span class="nb">list</span><span class="p">(</span><span class="n">wineMod</span><span class="p">[</span><span class="n">wineMod</span><span class="p">[</span><span class="s1">'quality'</span><span class="p">]</span> <span class="o">==</span> <span class="mi">8</span><span class="p">][</span><span class="n">i</span><span class="p">]</span><span class="o">.</span><span class="n">dropna</span><span class="p">())</span>
    <span class="n">xmin</span> <span class="o">=</span> <span class="nb">min</span><span class="p">(</span><span class="nb">min</span><span class="p">(</span><span class="n">quality3</span><span class="p">),</span> <span class="nb">min</span><span class="p">(</span><span class="n">quality4</span><span class="p">),</span> <span class="nb">min</span><span class="p">(</span><span class="n">quality5</span><span class="p">),</span> <span class="nb">min</span><span class="p">(</span><span class="n">quality6</span><span class="p">),</span> <span class="nb">min</span><span class="p">(</span><span class="n">quality7</span><span class="p">),</span> <span class="nb">min</span><span class="p">(</span><span class="n">quality8</span><span class="p">))</span>
    <span class="n">xmax</span> <span class="o">=</span> <span class="nb">max</span><span class="p">(</span><span class="nb">max</span><span class="p">(</span><span class="n">quality3</span><span class="p">),</span> <span class="nb">max</span><span class="p">(</span><span class="n">quality4</span><span class="p">),</span> <span class="nb">max</span><span class="p">(</span><span class="n">quality5</span><span class="p">),</span> <span class="nb">max</span><span class="p">(</span><span class="n">quality6</span><span class="p">),</span> <span class="nb">max</span><span class="p">(</span><span class="n">quality7</span><span class="p">),</span> <span class="nb">max</span><span class="p">(</span><span class="n">quality8</span><span class="p">))</span>
    <span class="n">width</span> <span class="o">=</span> <span class="p">(</span><span class="n">xmax</span> <span class="o">-</span> <span class="n">xmin</span><span class="p">)</span> <span class="o">/</span> <span class="mi">40</span>
    <span class="n">sns</span><span class="o">.</span><span class="n">distplot</span><span class="p">(</span><span class="n">quality3</span><span class="p">,</span> <span class="n">kde</span><span class="o">=</span><span class="kc">False</span><span class="p">,</span> <span class="n">bins</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="n">xmin</span><span class="p">,</span> <span class="n">xmax</span><span class="p">,</span> <span class="n">width</span><span class="p">))</span>
    <span class="n">sns</span><span class="o">.</span><span class="n">distplot</span><span class="p">(</span><span class="n">quality4</span><span class="p">,</span> <span class="n">kde</span><span class="o">=</span><span class="kc">False</span><span class="p">,</span> <span class="n">bins</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="n">xmin</span><span class="p">,</span> <span class="n">xmax</span><span class="p">,</span> <span class="n">width</span><span class="p">))</span>
    <span class="n">sns</span><span class="o">.</span><span class="n">distplot</span><span class="p">(</span><span class="n">quality5</span><span class="p">,</span> <span class="n">kde</span><span class="o">=</span><span class="kc">False</span><span class="p">,</span> <span class="n">bins</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="n">xmin</span><span class="p">,</span> <span class="n">xmax</span><span class="p">,</span> <span class="n">width</span><span class="p">))</span>
    <span class="n">sns</span><span class="o">.</span><span class="n">distplot</span><span class="p">(</span><span class="n">quality6</span><span class="p">,</span> <span class="n">kde</span><span class="o">=</span><span class="kc">False</span><span class="p">,</span> <span class="n">bins</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="n">xmin</span><span class="p">,</span> <span class="n">xmax</span><span class="p">,</span> <span class="n">width</span><span class="p">))</span>
    <span class="n">sns</span><span class="o">.</span><span class="n">distplot</span><span class="p">(</span><span class="n">quality7</span><span class="p">,</span> <span class="n">kde</span><span class="o">=</span><span class="kc">False</span><span class="p">,</span> <span class="n">bins</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="n">xmin</span><span class="p">,</span> <span class="n">xmax</span><span class="p">,</span> <span class="n">width</span><span class="p">))</span>
    <span class="n">sns</span><span class="o">.</span><span class="n">distplot</span><span class="p">(</span><span class="n">quality8</span><span class="p">,</span> <span class="n">kde</span><span class="o">=</span><span class="kc">False</span><span class="p">,</span> <span class="n">bins</span><span class="o">=</span><span class="n">np</span><span class="o">.</span><span class="n">arange</span><span class="p">(</span><span class="n">xmin</span><span class="p">,</span> <span class="n">xmax</span><span class="p">,</span> <span class="n">width</span><span class="p">))</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">([</span><span class="s1">'quality = 3'</span><span class="p">,</span> <span class="s1">'quality = 4'</span><span class="p">,</span> <span class="s1">'quality = 5'</span><span class="p">,</span> <span class="s1">'quality = 6'</span><span class="p">,</span> <span class="s1">'quality = 7'</span><span class="p">,</span> <span class="s1">'quality = 8'</span><span class="p">])</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">'Overlaid histogram for </span><span class="si">{}</span><span class="s1">'</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">i</span><span class="p">))</span>
    <span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAXAAAAEICAYAAABGaK+TAAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjQuMywgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy/MnkTPAAAACXBIWXMAAAsTAAALEwEAmpwYAAAgKUlEQVR4nO3deZwU9bnv8c8TFgcERdnCPqAe1KhHh7nBDUJEvZiggoKKQyQeCWYx0Ry5xhhzXW6MRM0x4rknisuE4MKJJB4Ql4joRI5bAoIJhiCKqAOELbLIOjM854+qgWboqe6Z7p7umvm+X6959XRX1a+eru5++qlfVf3a3B0REYmfz+U7ABERaRwlcBGRmFICFxGJKSVwEZGYUgIXEYkpJXARkZhSAm+mzMzN7Og05utrZp+ZWat6pt9qZo/VM22YmVVGtP2Amf04/ajjycxGm9kn4XY8JQvtdTezV81sm5n93MxuMrOHsxFrnfVUmNnELLcZGauZrTKzs9OZV1Jrne8AWgoz+zpwPXAUsBV4Gvihu2/OY1i4+8dAhxy1/c105jOzVcBEd38pF3E0gXuAa9x9dpbamwRsBA7zmF2o4e4/bcy8ZlYMfAi0cffqHITWLKkCbwJmdj3wM+D/AIcDpwL9gHlm1jbL69KXcoIm2h79gHcbs2A9ez79gL/GLXlL01MCzzEzOwy4Dfiuu7/g7lXuvgq4hOCDOt7MeprZTjM7MmG5U8xso5m1Ce//i5ktM7NPzez3ZtYvYV43s++Y2QpgRZIYvmpmi81sa7irf2vCtOJw+dbh/f5m9odw930e0CWN53i9ma03s7VmdmXC478ys5+E/3cxs7lmttnM/mFmC8zsc2Y2A+gLPBN2QdwQzn+Bmb0bzl9hZscltFsSPp9tZvaUmf1nwnqGmVmlmf3AzP4OlJvZEeG6N4Tbb66Z9U5or8LMfmJmr4cxPGNmnc3s8XCb/SmsEOs+70PM7DOgFfCOmX0QPn5c2Obm8DlcUGeb/NLMnjOz7cCX67T5K2ACcEMYy9mJ3VhmdqmZrQzfV5jZeWb2dzPrGt6Pep+cY2Z/M7MtZvbvgEW8pl80szfC57DWzP49sdgwsy+Y2bzwtVxnZjeFjx/Q5WZmXzOzj8xsk5n9qM46Eud9NbzdHD7vL4Vtn5gwfzcLPidd64u7xXF3/eXwDxgBVAOtk0ybDjwZ/v8y8I2EaXcDD4T/jwLeB44j6Pa6GXg9YV4H5gFHAu0SHjs6/H8YcCLBF/ZJwDpgVDitOJy3dXj/DeDfgEOAocA24LF6ntuw8LndDrQBvgLsAI4Ip/8K+En4/53AA+F8bYAhgIXTVgFnJ7T7T8B24Jxw3hvC5982/PsIuDacdhGwJ2E9tTH9LHwO7YDOwMVAe6Aj8BTwXwnrqwjbP4pgD+mvwHvA2eH2/jVQHvEaJ27rNmFbN4WxnhVuw4EJ22QLcEb4ehQlaW/fdgvv35r4GgCPh/N0BtYAI1O9Twi+iLcCY8IYvx9up4n1PKdBBHuKrcP3yDLgunBaR2AtQZdgUXh/cN1YgeOBzwjeR4cQvK+qa1/rOvMWk/A+DB/7D+BnCfevBZ7J92e6kP5UgedeF2CjJ+/XW8v+CvcJYByAmRlwWfgYwNXAne6+LGznp8DJidVVOP0f7r6z7krcvcLd/+Lue939z8CTwJfqzmdmfYH/BfzY3Xe7+6vAMymeXxVwuwd7Fs8RfGAH1jNfD6BfOO8CDz+VSVwKPOvu89y9iqCPuR1wOvuTytSwnd8Bf6yz/F7glvA57HT3Te7+W3ff4e7bgDuSPP9yd//A3bcAzwMfuPtL4fZ+Ckj34OSpBMcUprj7Hnd/GZhL+NqGZrv7a+HrsSvNdhN9h+CLoYIgoc0NH496n3yFoFtmVrhNfwH8vb4VuPsid3/T3as92GN8kP3bbCTwd3f/ubvvcvdt7v5WkmbGAHPd/VV33w38mOC1Sdd04HIzq81TXwNmNGD5Zk8JPPc2Al0seV9sj3A6wCzgNDPrSVCxOLAgnNYPuC/cnd0M/INg97dXQluf1BeAmQ02s1fCLoQtwDdJ3jXSE/jU3bcnPPZRiue3qc6X0w6SHxS9m6A6fDHsArgxos2eiet1970Ez69XOG11neRf97lvSEyMZtbezB4Md+W3Euyud7ID+5/XJfy/M8n9dA/09gQ+CWOu9RFpvlbp8ODA91PACcDPEyZFvU96Jq433H5R75l/Crua/h5us5+y/z3TB/ggjVDrrnM7sCmN5Wrnf4tgT+xLZnYscDQwJ93lWwIl8Nx7A9hNsKu/j5kdCpwHzId9H8oXCfrGLyfoWqlNUp8AV7t7p4S/du7+ekKTUQe8niB44/dx98MJujKS9X+uBY4IY6vVN72nGS2s0q539wHA+cC/mtnw2sl1Zl9DkIyAfXskfYDVYYy9wsdq9am7ujr3ryfYKxjs7ocRfEFCRB9wBtYAfRKqRgi24eqI+BrEzE4G/oVgT2pqwqSo98laErZTwjatzy+BvwHHhNvsJvZvr08IuptSqbvO9gTdPsnUt02mA+MJqu9ZjdxjabaUwHMs3CW/DbjfzEaYWZvwgNhTQCUH7hI+AVxB0F/7RMLjDwA/NLMvAJjZ4WY2tgFhdAT+4e67zOyLBF8QyWL9CFgI3GZmbc3sTIJkmzEzG2lmR4eJYytQE/5BUO0OSJj9N8BXzWy4BQdxryf4Enyd4AuxBrjGzFqb2YXAF1OsviNBFb3ZggPFt2TjOdWjtmq8IXythxFsw5nZaNzMioDHCBLqlQRfZt8OJ0e9T54FvmBmF4V7g98DPh+xqo4Er9NnYfX7rYRpc4HPm9l1FhzI7Whmg5O0MQsYaWZnhgdAb6f+nLOBoHtlQJ3HZwCjCZL4ryPibZGUwJuAu99F8IG7h+BD8RZBFTM87BusNQc4Bljn7u8kLP80wUG5meHu7FKC6j1d3wZuN7NtwP8lSJD1uRwYTLD7fQvZ+9AcA7xE0Ef+BvAf7l4RTrsTuDnc9Z/s7ssJPrD3E3QxnQ+cH/Yp7yHYm7kK2BzON5cgwdfnFwR96BuBN4EXsvScDhLGdwHB67OR4EDcFe7+tyyt4k6g0t1/Gb53xgM/MbNjot4n7r4RGAtMIejGOAZ4LWI9kwneC9uAh4D/THiO2wgOMJ9P0I++gjpn04TzvUvQX/8EQTX+KUHRchB330FwbOK18H1wavh4JfA2B3YpSqj2LACR2DKztwjO2CnPdyySfWb2KLDG3W/OdyyFRhd9SOyY2ZeA5QQVbhnBqZE5q6olf8LuxotI/yygFkVdKBJHA4F3CM6nvh4Y4+5r8xuSZJuZ/T+CbqC73f3DfMdTiNSFIiISU6rARURiqkn7wLt06eLFxcVNuUoRkdhbtGjRRnc/aAyYJk3gxcXFLFy4sClXKSISe2aW9IpodaGIiMSUEriISEwpgYuIxJQu5BGRSFVVVVRWVrJrl8aRyrWioiJ69+5NmzZt0ppfCVxEIlVWVtKxY0eKi4s5cBBIySZ3Z9OmTVRWVtK/f/+0llEXiohE2rVrF507d1byzjEzo3Pnzg3a01ECF5GUlLybRkO3sxK4iEhMqQ9cRBpk2uPZvRhvUllpVtuLsmrVKkaOHMnSpUtZuHAhv/71r5k6dSoVFRW0bduW008/PSfr3bVrF0OHDmX37t1UV1czZswYbrvttozbjU0C//Mj0yKnn3TVpCaKRESag9LSUkpLgy+PiooKOnTokLMEfsghh/Dyyy/ToUMHqqqqOPPMMznvvPM49dRTM2pXXSgiUvDuuOMOBg4cyNlnn824ceO45557ABg2bNi+4Tk2btxI7VhLq1atYsiQIZSUlFBSUsLrr79+UJsVFRWMHDmSVatW8cADD3Dvvfdy8skns2DBAvr3709VVRUAW7dupbi4eN/9xjAzOnQIfhe7qqqKqqqqrBxXiE0FLiIt06JFi5g5cyaLFy+murqakpISBg0aFLlMt27dmDdvHkVFRaxYsYJx48bVOw5TcXEx3/zmN+nQoQOTJ08Ggi+GZ599llGjRjFz5kwuvvjig87Nfvzxx7n77rsPau/oo49m1qxZBz1eU1PDoEGDeP/99/nOd77D4MHJfka0YZTARaSgLViwgNGjR9O+fXsALrjggpTLVFVVcc0117BkyRJatWrFe++916B1Tpw4kbvuuotRo0ZRXl7OQw89dNA8ZWVllJWVpd1mq1atWLJkCZs3b2b06NEsXbqUE044oUFx1aUELiIFr77uhtatW7N3716AA86fvvfee+nevTvvvPMOe/fupaioqEHrO+OMM1i1ahV/+MMfqKmpSZpoG1qB1+rUqRPDhg3jhRdeyDiBqw9cRAra0KFDefrpp9m5cyfbtm3jmWee2TetuLiYRYsWARyQNLds2UKPHj343Oc+x4wZM6ipqYlcR8eOHdm2bdsBj11xxRWMGzeOK6+8MukyZWVlLFmy5KC/ZMl7w4YNbN68GYCdO3fy0ksvceyxx6b1/KOoAheRBmnK0/4ASkpKuPTSSzn55JPp168fQ4YM2Tdt8uTJXHLJJcyYMYOzzjpr3+Pf/va3ufjii3nqqaf48pe/zKGHHhq5jvPPP58xY8Ywe/Zs7r//foYMGUJZWRk333wz48aNy/g5rF27lgkTJlBTU8PevXu55JJLGDlyZMbtNulvYpaWlnpjf9BBpxGK5MeyZcs47rjj8h3GPrfeeusBBxxzZdasWcyePZsZM2bkdD11JdveZrbI3Q/65lQFLiJSx3e/+12ef/55nnvuuXyHEkkJXERi5dZbb835Ou6///6cryMbdBBTRCSmlMBFRGJKCVxEJKbSSuBm9n0ze9fMlprZk2ZWZGZHmtk8M1sR3h6R62BFRGS/lAcxzawX8D3geHffaWa/AS4Djgfmu/sUM7sRuBH4QU6jFZG8W/VMeVbbKz4/+YUyuZCv4WRr1dTUUFpaSq9evZg7d27G7aXbhdIaaGdmrYH2wBrgQmB6OH06MCrjaEREmkhpaSlTp04FgpEJk41YmG333XdfVs+pT5nA3X01cA/wMbAW2OLuLwLd3X1tOM9aoFuy5c1skpktNLOFGzZsyFrgItJyxH04WQh+HPrZZ59l4sSJGbWTKJ0ulCMIqu3+wGbgKTMbn+4K3H0aMA2CKzEbF6aItFTNZTjZ6667jrvuuuugMVcykc6FPGcDH7r7BgAz+x1wOrDOzHq4+1oz6wGsz1pUIiKh5jCc7Ny5c+nWrRuDBg2ioqKiQbFESSeBfwycambtgZ3AcGAhsB2YAEwJb2dnLSoRkQRxH072tddeY86cOTz33HPs2rWLrVu3Mn78eB577LEGxVVXOn3gbwGzgLeBv4TLTCNI3OeY2QrgnPC+iEhWNYfhZO+8804qKytZtWoVM2fO5Kyzzso4eUOaY6G4+y3ALXUe3k1QjYtIC9KUp/1B8xhONlc0nKyIRNJwshpOVkQkNjScrIhIDmg42f00mJWISEzFpgJ/Y+VbkdNPQn3gItKyqAIXEYkpJXARkZiKTReKiBSG6W88ntX2JpyW3uXo2ZDP4WSLi4vp2LEjrVq1onXr1vWOzdIQSuAi0iKVlpZSWhqcWl1RUUGHDh1yPh74K6+8QpcuXbLWnrpQRKTgNYfhZHNBFbiIFLTmMpysmXHuuediZlx99dVMmpT5mXNK4CJS0JrDcLIQjEjYs2dP1q9fzznnnMOxxx7L0KFDGxRXXUrgIlLw4j6cLEDPnj2BYO9g9OjR/PGPf8w4gasPXEQKWnMYTnb79u372t++fTsvvvhi0i+FhlIFLiIN0pSn/UHzGE523bp1jB49GoDq6mouv/xyRowYkXG7sRlO9sEfXRU5/eo7HmlUuyISTcPJajhZEZHY0HCyIiI5oOFk99NBTBGRmFICFxGJKSVwEZGYUgIXEYkpHcQUkQb58yPTstreSVc13a9p5XM42c2bNzNx4kSWLl2KmfHoo49y2mmnZdSmEriItEhNPZzstddey4gRI5g1axZ79uxhx44dGbepLhQRKXhxH05269atvPrqq1x1VXBBYtu2benUqVOj26ulClxEClpzGE525cqVdO3alSuvvJJ33nmHQYMGcd9996W8xD8VVeAiUtASh5M97LDD0h5O9hvf+AYnnngiY8eO5a9//WuD1jlx4kTKy8sBKC8vTzqgVUMGs6qurubtt9/mW9/6FosXL+bQQw9lypQpDYopGVXgIlLw4j6cbO/evenduzeDBw8GYMyYMVlJ4KrARaSgNYfhZD//+c/Tp08fli9fDsD8+fM5/vjj09sAEVSBi0iDNOVpf9A8hpOFYHyVsrIy9uzZw4ABA/Z10WRCw8mKSCQNJ6vhZEVEYkPDyYqI5ICGk91PBzFFRGJKCVxEJKaUwEVEYkoJXEQkpnQQU0QaZP4Tb2S1veGXZzakakPkazjZ5cuXc+mll+67v3LlSm6//Xauu+66jNpVAheRFqkph5MdOHAgS5YsAaCmpoZevXoxevTojNtNqwvFzDqZ2Swz+5uZLTOz08zsSDObZ2YrwtsjMo5GRCSJuA8nm2j+/PkcddRR9OvXL+O20q3A7wNecPcxZtYWaA/cBMx39ylmdiNwI/CDjCMSEUnQHIaTTTRz5sysXZ6fMoGb2WHAUODrAO6+B9hjZhcCw8LZpgMVKIGLSJYlDicLpD2c7DXXXMOSJUto1aoV7733XoPWOXHiRO666y5GjRpFeXk5Dz300EHzlJWVUVZW1qB29+zZw5w5c7jzzjsbtFx90qnABwAbgHIz+2dgEXAt0N3d1wK4+1oz65ZsYTObBEwC6Nu3b1aCFpGWJe7DydZ6/vnnKSkpoXv37g2Kpz7p9IG3BkqAX7r7KcB2gu6StLj7NHcvdffSrl27NjJMEWmpmsNwsrWefPLJrHWfQHoVeCVQ6e5vhfdnESTwdWbWI6y+ewDrsxaViBSspjztD5rPcLI7duxg3rx5PPjgg1lpD9IcTtbMFgAT3X25md0K1G6NTQkHMY909xui2tFwsiLxo+Fk4z+c7HeBx8MzUFYCVxJ0v/zGzK4CPgbGZhS1iEiBaFbDybr7EuCg7A8Mz2o0IiIpaDjZ/TQWiohITCmBi4jElBK4iEhMKYGLiMSURiMUkQaZP6s8q+0NH5P8QplcyNdwshBcHfrwww9jZpx44omUl5c3+ArRulSBi0iLVFpaytSpU4FgZMJkIxZmy+rVq5k6dSoLFy5k6dKl1NTUMHPmzIzbVQIXkYLXHIaTra6uZufOnVRXV7Njxw569uyZUXugLhQRKXDNYTjZXr16MXnyZPr27Uu7du0499xzOffccxuyGZJSAheRgtYchpP99NNPmT17Nh9++CGdOnVi7NixPPbYY4wfP75BcdWlBC4iBS/uw8m+9NJL9O/fn9oRWS+66CJef/31jBO4+sBFpKA1h+Fk+/bty5tvvsmOHTtwd+bPn5+VAcJUgYtIgzTlaX/QPIaTHTx4MGPGjKGkpITWrVtzyimnMGnSpIzbTWs42WzRcLIi8aPhZOM/nKyISIvRrIaTFREpFBpOdj8dxBSRlJqyq7Ula+h2VgIXkUhFRUVs2rRJSTzH3J1NmzY16JRHdaGISKTevXtTWVnJhg0b8h1Ks1dUVETv3r3Tnl8JXEQitWnThv79++c7DElCXSgiIjGlBC4iElNK4CIiMaUELiISU0rgIiIxpQQuIhJTSuAiIjGlBC4iElNK4CIiMaUELiISU0rgIiIxpQQuIhJTSuAiIjGlBC4iElNK4CIiMaUELiISU0rgIiIxpQQuIhJTSuAiIjGVdgI3s1ZmttjM5ob3jzSzeWa2Irw9IndhiohIXQ2pwK8FliXcvxGY7+7HAPPD+yIi0kTSSuBm1hv4KvBwwsMXAtPD/6cDo7IamYiIREq3Av8FcAOwN+Gx7u6+FiC87Zbd0EREJErKBG5mI4H17r6oMSsws0lmttDMFm7YsKExTYiISBLpVOBnABeY2SpgJnCWmT0GrDOzHgDh7fpkC7v7NHcvdffSrl27ZilsERFJmcDd/Yfu3tvdi4HLgJfdfTwwB5gQzjYBmJ2zKEVE5CCZnAc+BTjHzFYA54T3RUSkibRuyMzuXgFUhP9vAoZnPyQREUmHrsQUEYkpJXARkZhSAhcRiSklcBGRmFICFxGJKSVwEZGYUgIXEYkpJXARkZhSAhcRiSklcBGRmFICFxGJKSVwEZGYUgIXEYkpJXARkZhSAhcRiSklcBGRmGrQDzpIctPfeDyj5SecVpalSESkJVEFLiISU6rAJVKqvQvtPYjkjypwEZGYUgIXEYkpJXARkZhSAhcRiSkdxGzhMj0FUkTyRxW4iEhMKYGLiMSUEriISEwpgYuIxJQSuIhITCmBi4jElE4jbOZ0mmByGuNFmgNV4CIiMaUELiISU+pCaQK75r4cPUMGu+vqIhFpuVSBi4jElCrwNDz4o6sipxeNPCun62+pVfafH5kWOf2kqyY1USQihUkVuIhITMWmAl+zok2+Q8iZllphi0hmVIGLiMRUygRuZn3M7BUzW2Zm75rZteHjR5rZPDNbEd4ekftwRUSkVjpdKNXA9e7+tpl1BBaZ2Tzg68B8d59iZjcCNwI/yF2ouZXqgFmUlKcJ5lCqdef6AGsUHYQUya2UFbi7r3X3t8P/twHLgF7AhcD0cLbpwKgcxSgiIkk06CCmmRUDpwBvAd3dfS0ESd7MutWzzCRgEkDfvn0zCjYTmVTYIiKFKO2DmGbWAfgtcJ27b013OXef5u6l7l7atWvXxsQoIiJJpJXAzawNQfJ+3N1/Fz68zsx6hNN7AOtzE6KIiCSTsgvFzAx4BFjm7v+WMGkOMAGYEt7OzkmEWfLGyrcip582YHATRRIvuRzHRUQyk04f+BnA14C/mNmS8LGbCBL3b8zsKuBjYGxOIhQRkaRSJnB3/2/A6pk8PLvhSNxEHRxOtddzEjqNUA6kH9poGF2JKSISU7EZC0Uap5Av9ElVbZ3SRHE0RqaVYtTyqjIlXarARURiSglcRCSm1IXSwmU6jkuqA5UikjuqwEVEYkoVuMRWqp+6u/qOR5ooEpH8UAUuIhJTqsBD+ezLzed44oVM/esi0VSBi4jElBK4iEhMqQtFmq2oqx0LeZRF/RSdpEsVuIhITMWmAt/96YbI6frJNGlKqSr46ZFTc0sj+rUcqsBFRGJKCVxEJKZi04WSis4ZlkLyyUvRXX59ztYPfEvmVIGLiMRUs6nARbIp1YHAVKr+8rfoGVSBN0o+T7EsxNM7VYGLiMSUKvAmsGZFm8jpPY+paqJIWpZMxpgp5PFpMt07iDP9UPaBVIGLiMSUEriISEypC0UkDyK7aAYMzl3bkNE4L3G+yrM5Xq2tClxEJKZUgYsUmN/+/u3I6QOOH5JR+6kq0cXHH5pR+y3V/CfeiJw+/PLTsr5OVeAiIjGlBC4iElPqQpGCler8+VSizq/XufmNk+kB0jifw75k0ebI6b3ObJo4EqkCFxGJKVXgBSCf1WCm645aPtWyqa92zKwCz0RzrtBTjty5svFtp6qwcz1KY9QB2lQHhy/+3yUZrTsfVIGLiMRUi6nA41xRRcV+WLvoUe869D4q2+FInmU6TksuPwupYqtKse5PUrSfqj5P1U+dS6v/e0H0DDqNUEREaimBi4jEVGy6UD7bWRk5fc2KzA5+fFb5Qb3Ttu48NnLZfHa/bFjTOXJ6h96ZtZ/pqXy5tPvT6ANi0Cln6y7k7ZJLue6KTPVDGGtSHNg+qktGq4/0wcboo7tHdRmQu5XXQxW4iEhMxaYCz1TKaq1d49v+8I+bI6fvsi2R04v88MjphxzR+L2LXFeKWza/X//EFUdHLpu6gs5M1OuSyTaF1LFn2n6UXL+mLXXvItXples37omcnsvqvz6qwEVEYiqjCtzMRgD3Aa2Ah919SlaiaoSNn6zOaPmoeilVtbXts+hvZmu1LXr5mujyf+PmP9U7rUun4uhlU2yXLn16RU6PrLCB6h31P7fdntsKO9V279ihbb3TNq1ZHLls556nNCqmdEVVuali69Au+sBGquo/1Wt6eKfoPadcSvVZS7U3+9nuvfW3vWNT5LJrPv5H5HSI3u6frY7errnQ6ArczFoB/x84DzgeGGdmx2crMBERiZZJF8oXgffdfaW77wFmAhdmJywREUnF3L1xC5qNAUa4+8Tw/teAwe5+TZ35JsG+n4oeCCxvfLgFpwuwMd9BxIS2VXq0ndLT0rZTP3c/qG8skz5wS/LYQd8G7j4NaH4/RgeY2UJ3L813HHGgbZUebaf0aDsFMulCqQT6JNzvDazJLBwREUlXJgn8T8AxZtbfzNoClwFzshOWiIik0uguFHevNrNrgN8TnEb4qLu/m7XI4qFZdg3liLZVerSd0qPtRAYHMUVEJL90JaaISEwpgYuIxJQSeCOY2UAzW5Lwt9XMrst3XIXIzL5vZu+a2VIze9LMivIdUyEys2vDbfSu3ksHMrNHzWy9mS1NeOxIM5tnZivC2yPyGWO+KIE3grsvd/eT3f1kYBCwA3g6v1EVHjPrBXwPKHX3EwgOdl+W36gKj5mdAHyD4OrmfwZGmtkx+Y2qoPwKGFHnsRuB+e5+DDA/vN/iKIFnbjjwgbt/lO9AClRroJ2ZtQbao2sFkjkOeNPdd7h7NfAHYHSeYyoY7v4qUHekqQuB6eH/04FRTRlToVACz9xlwJP5DqIQuftq4B7gY2AtsMXdX8xvVAVpKTDUzDqbWXvgKxx4kZwcrLu7rwUIb7vlOZ68UALPQHgB0wXAU/mOpRCF/ZIXAv2BnsChZjY+v1EVHndfBvwMmAe8ALwDVOc1KIkFJfDMnAe87e7r8h1IgTob+NDdN7h7FfA74PQ8x1SQ3P0Rdy9x96EE3QUr8h1TgVtnZj0Awtv1eY4nL5TAMzMOdZ9E+Rg41czam5kRHC9YlueYCpKZdQtv+wIXofdVKnOACeH/E4DZeYwlb3QlZiOFfZWfAAPcPfpnQlowM7sNuJSgS2AxMNHdd+c3qsJjZguAzkAV8K/uPj/PIRUMM3sSGEYwhOw64Bbgv4DfAH0JCoWx7p7qJ3WaHSVwEZGYUheKiEhMKYGLiMSUEriISEwpgYuIxJQSuIhITCmBi4jElBK4iEhM/Q/ViQgYrAUgcAAAAABJRU5ErkJggg==
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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ncv999/PrbfeyuzZs+ncuTNf/OIXi7LdTZs2MXz4cD799FPq6+sZM2YMV199dd7tJiK5//WeO5tcdviESa0YiZklQVVVFVVV0R+W2bNn061bt6Il91133ZVnn32Wbt26UVdXx5e+9CW+8pWvcNRRR+XVrqdlzKysXXvttQwZMoQTTjiBcePGcdNNNwEwYsSIbWVNVq1axdb6VUuXLuXYY4+lsrKSyspK5syZs1Obs2fPZuTIkSxdupTbb7+dm2++mSOOOILnn3+ewYMHU1dXB8DatWupqKjY9rwlJNGtW/Rd6nV1ddTV1RXkPEYiRu5m1j7NmzePKVOmMH/+fOrr66msrGTo0KEZ39OnTx9mzpxJly5dWLx4MePGjWuytlVFRQUXXHAB3bp1Y/Lk6FsJR4wYweOPP86oUaOYMmUKp59++k7Xnz/00EPceOONO7V34IEHMnXq1J1eb2hoYOjQobz99ttceOGFDBs2LNdd0CQndzMrW88//zyjR49m9913B+DUU0/N+p66ujouuugiFixYQIcOHXjrrbeatc2JEydyww03MGrUKGpqarjrrrt2Wqe6uprq6uqc2+zQoQMLFixgzZo1jB49moULF/LZz362WXE15uRuZmWtqSmMjh07smXLFoAd7qC9+eab2WeffXj11VfZsmULXbp0adb2jjnmGJYuXcof//hHGhoa0ibh5o7ct+rRowcjRozgqaeeyju5e87dzMrW8OHD+e1vf8vGjRtZt24djz322LZlFRUVzJs3D2CHhPrxxx/Tt29fdtllFx544AEaGjLfRN+9e3fWrVu3w2vnnHMO48aN49xzz037nurqahYsWLDTT7rEvnLlStasWQPAxo0beeaZZzj44INz6n8mHrmbWcG05qWLAJWVlZx55pkcccQRDBo0iGOPPXbbssmTJ3PGGWfwwAMPcNxxx217/bvf/S6nn346jz76KF/+8pfp2rVrxm2ccsopjBkzhmnTpnHbbbdx7LHHUl1dzQ9/+EPGjWvqBv7cLV++nPHjx9PQ0MCWLVs444wzGDlyZN7tlsR3qFZVVYV8vqzDl0KatY033niDQw45pK3D2Oaqq67a4eRnsUydOpVp06bxwAMPFHU7qdLta0nzQghp/6J65G5m1gwXX3wxTz75JE888URbh5KRk7uZJcZVV11V9G3cdtttRd9GIfiEqplZ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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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qKGhgQEDBlBTU8POBRytXCKCtWvX0tDQwOjRo4t+XkeHZe4BpqR/TwHm5kz/uJKvHxtNUiyq5RcpmFlGbNmyhX333deJvYIkse+++7b77KiYWyHvJPn6q0FKvt/wSpIqb3dJmkryVVbnAETEs5LuIvmaskbgcxGRr/yomWWEE3vldaSN20zuETGplVkn55sYEdeQfOWVmZlVSZf4hKqZZcOM28v7YcTpk+vKur5C6uvrGTduHMuXL2fJkiX89Kc/5cYbb2ThwoX07duX4447riLb3bJlCyeeeCJvv/02jY2NTJw4kauvvrrk9WYiuc9afHur86YcO7kTIzGzLKirq6OuLnljWbhwIf37969Yct9tt9145JFH6N+/P9u2beODH/wgH/7whznmmGNKWq8Lh5lZt3bNNddw0EEHccoppzBp0iS+/e1vAzB27NgdZU1ef/11mutX1dfXc8IJJ1BbW0ttbS2LFi3aZZ0LFy5k3Lhx1NfXc/PNN/Od73yHI488kkcffZTRo0ezbds2ANavX09NTc2Oxx0hif79k+9f37ZtG9u2bSvLdYxM9NzNrGdaunQps2fP5qmnnqKxsZHa2lqOPvrogs8ZMmQI8+fPp1+/frzwwgtMmjSp1dpWNTU1XHzxxfTv35/LL78cSN407rvvPsaPH8/s2bM5++yzd7n//Pbbb+db3/rWLut773vfy5w5c3aZ3tTUxNFHH82LL77I5z73OcaMGVNsE7TKyd3Muq1HH32UCRMmsMceewBw5plntvmcbdu2cckll7Bs2TJ69erF888/365tTps2jeuvv57x48czc+ZMfvjDH+6yzOTJk5k8ufgh4V69erFs2TLWrVvHhAkTWL58Oe9///vbFVdLTu5m1q21NoTRu3dvtm/fDrDTPeLf+c532G+//Xj66afZvn07/fr1a9f2jj/+eOrr6/n1r39NU1NT3iTc3p57s4EDBzJ27FgefPDBkpO7x9zNrNs68cQT+eUvf8nmzZvZsGED99577455NTU1LF26FGCnhPrmm28ydOhQ3vWud3HrrbfS1FT4ozgDBgxgw4YNO0375Cc/yaRJk7jwwgvzPmfy5MksW7Zsl598iX3NmjWsW7cOgM2bN/Pwww9z8MEHF/X6C3HP3czKpjNvXQSora3lvPPO48gjj2TUqFGccMIJO+ZdfvnlnHvuudx6662c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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAXAAAAEICAYAAABGaK+TAAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjQuMywgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy/MnkTPAAAACXBIWXMAAAsTAAALEwEAmpwYAAAlCUlEQVR4nO3de5hU5ZXv8e8SUORiEGkI0DaNkUE9XhD6iFeGiHowQYUIGoSE8UAwiWZ0jk5iJjf1jKNjcsZBZyYJ0TAEjUSZOCBeRmzT0URiBgQSDCoRO9pKuLQgyLW7WeeP/TYWTXVduqq6anf/Ps/TT9W+r72ravVb7957lbk7IiISP0cUOwAREWkbJXARkZhSAhcRiSklcBGRmFICFxGJKSVwEZGYUgIvEWbmZnZiBvNVmNmHZtallem3mdlDrUwba2Z1Kdb9AzP7VuZRx5OZTTKzd8JxPLPY8aST6jXNYZ2HvBfMbLiZrTKznWb21/ncVsI2as3sovD878zsgRzX1+bPQkehBN4KM/srM/u9me02sz+b2ffNrE+x43L3t929l7s3FWDdX3T3/5tuvsQPYkx9D7ghHMdVua7MzGrMbFah5m8nXwVq3L23u99X6I25+z+4e07HoJCfhbhQAk/CzG4G/hH4W+BjwNnAEGCZmR2Z5211zef64q6djscQ4NW2LNhaa68DyOWY6D1cJErgLZjZMcDtwFfc/Rl3b3D3WuAqojf5dDMbZGZ7zKxvwnJnmtlWM+sWhv+3ma0zs21m9l9mNiRhXjez681sPbA+SQyfDl9nd4Sv+rclTKsMy3cNw0PN7Jfhq+8yoF8G+3izmW02s41mdm3C+H83s78Pz/uZ2VIz225m75vZi2Z2hJktACqAJ8LX16+G+S83s1fD/DVmdnLCekcmfD1/zMx+lrCdsWZWZ2ZfM7M/A/PM7Niw7S3h+C01s/KE9dWY2d+b2UshhifM7Dgzezgcs/82s8ok+32UmX0IdAHWmNmbYfzJYZ3bwz5c3uKYfN/MnjKzXcAnW6zzTuAC4F9CLP8Sxp8b4vggPJ6bZv454bXeYWYrzeyCdK9jqtcpTDukWy7x9W2xjufDfjXH9BfW4luCRd9If5UwnPI9HOb5nJn9yczqzewbLaYd0r3R2vsnvC9+k/B+/1KYr3u2nwUzOzu8Z7ab2RozG5vJMS5p7q6/hD9gPNAIdE0ybT7wSHj+PPCFhGnfBX4Qnk8E/gicDHQFvgm8lDCvA8uAvsDRCeNODM/HAqcR/YM9HdgETAzTKsO8XcPwcuCfgKOAMcBO4KFW9m1s2Lc7gG7Ap4DdwLFh+r8Dfx+e3wX8IMzXjSjpWJhWC1yUsN6/AHYBF4d5vxr2/8jw9yfgxjDtM8D+hO00x/SPYR+OBo4DrgR6AL2Bx4D/TNheTVj/J4i+If0BeAO4KBzvnwDzUrzGice6W1jX34VYLwzHcHjCMfkAOC+8Ht2TrK8GmJUw3BfYBnwuxDM1DB+XbP4wbnrY767AzcCfm7cF3JbiNU31Oh3czySv71igLsU+tBz+K+BXqd7DLeI6BfiQ6D15FNF7tLH5fZO4T6R+/xwBvBDmHxaO45nZfhaAwUA90Xv+iLCteqCs2Dknlz+1wA/XD9jq7o1Jpm3ko//qPyX6YGJmBnw2jAO4DrjL3deF9fwDMMISWuFh+vvuvqflRty9xt1/7+4H3P13wCPAX7acz8wqgP8JfMvd97n7C8ATafavAbjDo28WTxF9yIa3Mt9AYEiY90UPn4QkrgaedPdl7t5A1Md8NHAuUfdTV+C+sJ6fA79tsfwB4DthH/a4e727/4e773b3ncCdSfZ/nru/6e4fAE8Db7r7c+F4PwZkenLybKAXcLe773f354GlhNc2WOzuvw6vx94M1vlpYL27L3D3Rnd/BHgNuKy1Bdz9obDfje7+/4iSULLXpaVsXqd8a/U9DEwGlrr7C+6+D/gW0eucTKvvH3c/AHwe+GtgCXCPJzlvkcFnYTrwlLs/FV7HZcAKooQeW0rgh9sK9LPk/XoDw3SARcA5ZjaI6L+9Ay+GaUOAOeGr2nbgfcCIWgHN3mktADMbbWa/CF0IHwBfJHnXyCBgm7vvShj3pzT7V9/in9NuogTW0neJWkHPmtkGM7s1xToHJW43fOjeIdrfQcC7LZJKy33fkpgYzayHmf0wfP3eQdQC62OH9j9vSni+J8lwsn1qLfZ3QszN/kSGr1WKdbZ8HVqu8xAWdWutC10u24m+WaTtDiO71ynfUh2XQYnTw3u0PsW8rb1/8KgL8xdELe5/TbGOVJ+FIcCU5s9kOMbnE32mY0sJ/HDLgX1EX/UPMrOewKVANYC7bweeJeobv4aoa6U5Sb0DXOfufRL+jnb3lxJWmaqV9FOi1sbx7v4xoq/IlmS+jcCxIbZmFZntZmruvtPdb3b3E4hajv/HzMY1T24x+3tEHxDg4DeS44F3Q4yDw7hmx7fcXIvhm4lan6Pd/Riif5CQ/Bjk6j3g+OZ+46CCKPbW4msp5fFIss5D5g/93V8jei8d6+59iLpt0u5vmtdpN1E3VLOPp1tfgl0ZLJvquGwk4XU2sx5EXUTJpHr/YGafAs4h+ux9N8X2Un0W3gEWtPhM9nT3u1PsQ8lTAm8hfCW/HbjfzMabWTeLTog9BtQBCxJm/ynR17sr+aj7BKKE+3Uz+x8AZvYxM5uSRRi9gffdfa+ZnUX0DyJZrH8i+hp4u5kdaWbnk+JrejbMbIKZnRg+TDuApvAHUWv3hITZHwU+bWbjLDqJezPRP8GXiP4hNgE3mFlXM7sCOCvN5nsTtaK3W3Si+Dv52KdWvEyUrL4aXuuxRMdwYRbraHk8ngL+wsyuCft8NVGf8NJW5u9N1D+8BehqZt8Gjslkw2lep9XANWbWxczGk6QbLoXVwGfCt6ETgZlZLAvRN9QJZna+RVdu3UHr+abV94+Z9QMeBGYBM4DLQkI/RAafhYfCsv8rHI/uFp1AL2+5rjhRAk/C3e8hOqn1PaIPxctE/8HHhf68ZkuITqxscvc1Ccs/TnRSbmHoAlhL1HrP1JeBO8xsJ/Btojd4a64BRhN103yH6ARePgwDniPqI18O/Ju714RpdwHfDF9Fb3H314n6GO8n6mK6DLgs9CnvJ/o2MxPYHuZbSvQBbc0/E/WBbgV+AzyTp306TIjvcqLXZyvwb8Dn3f21LFYzB5hs0RUz97l7PTCBKBHVE52Um+DuW5PND/wXUT/+G0Rf+/eSebdNqtfpRqLXYjswDfjPLPbpXqKTzZuITt4/nMWyuPurwPVEDZuNRCcfk95Elur9A8wlOgfxVDiuM4EHzCxZa77Vz4K7vwNcQfS53kJ0fP+WmOfA5rPVIu3GzF4mumJnXrFjEYmzWP/3kXgws780s4+H7oQZRJdGFqxVLdJZ6A4qaQ/DibqBegFvApPdfWNxQxKJP3WhiIjEVEZdKGb2NxbdvrrWzB4JZ3D7mtkyM1sfHo8tdLAiIvKRtC1wMxsM/Ao4xd33mNmjRJdJnUJ0qdvd4eaBY939a6nW1a9fP6+srMxP5CIincTKlSu3untZy/GZ9oF3BY42swaii/vfA75OVE8BosuMaohuRmhVZWUlK1asyHCTIiICYGZJ77BO24Xi7u8SXQ/9NtH1nB+4+7PAgOYTUeGxf/7CFRGRdNIm8NC3fQUwlKjeQE8zm57pBsxstpmtMLMVW7ZsaXukIiJyiExOYl4EvOXuW0KlsJ8TVZnbZGYDAcLj5mQLu/tcd69y96qyssO6cEREpI0y6QN/Gzg7FKPZA4wjqjmwi6g2wd3hcXGhghSR4mloaKCuro69ezOppCu56N69O+Xl5XTr1i2j+dMmcHd/2cwWAa8QFdxZRVSfoBfwqJnNJEry2RRrEpGYqKuro3fv3lRWVnJoUUnJJ3envr6euro6hg4dmtEyGV2F4u7f4fCKcPuIWuMi0oHt3btXybsdmBnHHXcc2ZwrVC0UEUlLybt9ZHuclcBFRGJKxaxEJCtzH87vzXizp1XldX2p1NbWMmHCBNauXcuKFSv4yU9+wn333UdNTQ1HHnkk5557bkG2u3fvXsaMGcO+fftobGxk8uTJ3H777TmvNzYJ/HcPzk05/fSZs9spEhHpCKqqqqiqiv551NTU0KtXr4Il8KOOOornn3+eXr160dDQwPnnn8+ll17K2WefndN61YUiIiXvzjvvZPjw4Vx00UVMnTqV733vewCMHTv2YHmOrVu30lxrqba2lgsuuICRI0cycuRIXnrppcPWWVNTw4QJE6itreUHP/gB9957LyNGjODFF19k6NChNDQ0ALBjxw4qKysPDreFmdGrV/Q72w0NDTQ0NOTlvEJsWuAi0jmtXLmShQsXsmrVKhobGxk5ciSjRo1KuUz//v1ZtmwZ3bt3Z/369UydOrXVOkyVlZV88YtfpFevXtxyyy1A9I/hySefZOLEiSxcuJArr7zysGuzH374Yb773cN/Y/nEE09k0aJFh41vampi1KhR/PGPf+T6669n9OjRmR6CVimBi0hJe/HFF5k0aRI9evQA4PLLL0+7TENDAzfccAOrV6+mS5cuvPHGG1ltc9asWdxzzz1MnDiRefPm8aMf/eiweaZNm8a0adMyXmeXLl1YvXo127dvZ9KkSaxdu5ZTTz01q7haUgIXkZLXWndD165dOXDgAMAhd4ree++9DBgwgDVr1nDgwAG6d++e1fbOO+88amtr+eUvf0lTU1PSRJttC7xZnz59GDt2LM8880zOCVx94CJS0saMGcPjjz/Onj172LlzJ0888cTBaZWVlaxcuRLgkKT5wQcfMHDgQI444ggWLFhAU1NTym307t2bnTt3HjLu85//PFOnTuXaa69Nusy0adNYvXr1YX/JkveWLVvYvn07AHv27OG5557jpJNOymj/U1ELXESy0p6X/QGMHDmSq6++mhEjRjBkyBAuuOCCg9NuueUWrrrqKhYsWMCFF154cPyXv/xlrrzySh577DE++clP0rNnz5TbuOyyy5g8eTKLFy/m/vvv54ILLmDatGl885vfZOrUqTnvw8aNG5kxYwZNTU0cOHCAq666igkTJuS83nb9Tcyqqipv6w866DJCkeJYt24dJ598crHDOOi222475IRjoSxatIjFixezYMGCgm6npWTH28xWuvth/znVAhcRaeErX/kKTz/9NE899VSxQ0lJCVxEYuW2224r+Dbuv//+gm8jH3QSU0QkppTARURiSglcRCSmlMBFRGJKJzFFJCu1T8zL6/oqL0t+o0whFKucbLOmpiaqqqoYPHgwS5cuzXl9aRO4mQ0HfpYw6gTg28BPwvhKoBa4yt235RyRiEg7aM9yss3mzJnDySefzI4dO/KyvrRdKO7+uruPcPcRwChgN/A4cCtQ7e7DgOowLCKSd3EvJwvRj0M/+eSTzJo1K6f1JMq2C2Uc8Ka7/8nMrgDGhvHzgRrga3mLTESEjlNO9qabbuKee+45rOZKLrJN4J8FHgnPB7j7RgB332hm/fMWlYhI0BHKyS5dupT+/fszatQoampqsoollYwTuJkdCVwOfD2bDZjZbGA2QEVFRVbBiYhA/MvJ/vrXv2bJkiU89dRT7N27lx07djB9+nQeeuihrOJqKZvLCC8FXnH3TWF4k5kNBAiPm5Mt5O5z3b3K3avKyspyClZEOp+OUE72rrvuoq6ujtraWhYuXMiFF16Yc/KG7LpQpvJR9wnAEmAGcHd4XJxzNCJS8trzsj/oGOVkCyWjcrJm1gN4BzjB3T8I444DHgUqgLeBKe7+fqr1qJysSPyonGzMy8m6+27guBbj6omuShER6VBUTlZEpABUTvYjqoUiIhJTSuAiIjEVmy6U5RteTjn9dHQSU0Q6F7XARURiKjYtcBEpDfOXP5zX9c04J7Pb0fOhmOVkKysr6d27N126dKFr166t1mbJhhK4iHRKxSgn+4tf/IJ+/frlbX3qQhGRktcRyskWglrg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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=d36bef8d-9844-408b-8d07-601d2536494c">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>As we have mentioned earlier, the features are not on the same scale and we have class imbalance in our dataset. To fix this issue, we implement feature scaling by standard scalar.</p>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs" id="cell-id=b4efc7ef-5c0e-4f22-8486-27e44e5761be">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [12]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Prepare the data for modeling by carrying out any steps that you think are necessary</span>
<span class="n">features</span> <span class="o">=</span> <span class="n">wineMod</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="s1">'quality'</span><span class="p">,</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">labels</span> <span class="o">=</span> <span class="n">wineMod</span><span class="p">[</span><span class="s1">'quality'</span><span class="p">]</span>

<span class="c1"># Creating Test and Train data</span>
<span class="n">X_train</span><span class="p">,</span> <span class="n">X_test</span><span class="p">,</span> <span class="n">y_train</span><span class="p">,</span> <span class="n">y_test</span> <span class="o">=</span> <span class="n">train_test_split</span><span class="p">(</span><span class="n">features</span><span class="p">,</span> <span class="n">labels</span><span class="p">,</span> <span class="n">test_size</span><span class="o">=</span><span class="mf">0.2</span><span class="p">,</span> <span class="n">random_state</span><span class="o">=</span><span class="mi">42</span><span class="p">)</span>

<span class="c1"># implementing feature scaling</span>
<span class="n">scaler</span> <span class="o">=</span> <span class="n">StandardScaler</span><span class="p">()</span>
<span class="n">X_train</span> <span class="o">=</span> <span class="n">scaler</span><span class="o">.</span><span class="n">fit_transform</span><span class="p">(</span><span class="n">X_train</span><span class="p">)</span>
<span class="n">X_test</span> <span class="o">=</span> <span class="n">scaler</span><span class="o">.</span><span class="n">transform</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>
</pre></div>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=e59d8dd8">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h3 id="Modeling">Modeling<a class="anchor-link" href="#Modeling">¶</a></h3><li>Implement Multivariable Linear Regression using any 2 Regression algorithms of your choice</li>
<li>Implement a Neural Network using Tensorflow and Keras to classify wine quality</li>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs" id="cell-id=2c9ad45a-4396-4380-9361-9d172490975e">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [13]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Implement Multivariable Linear Regression using any 2 Regression algorithms of your choice</span>

<span class="c1"># First Multivariable Linear Regression (Random Forest)</span>
<span class="kn">from</span> <span class="nn">sklearn.ensemble</span> <span class="kn">import</span> <span class="n">RandomForestRegressor</span>
<span class="n">rfModel</span> <span class="o">=</span> <span class="n">RandomForestRegressor</span><span class="p">(</span><span class="n">n_estimators</span><span class="o">=</span><span class="mi">500</span><span class="p">)</span>
<span class="n">rfModel</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span><span class="n">y_train</span><span class="p">)</span>
<span class="n">rfPreds</span> <span class="o">=</span> <span class="n">rfModel</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>


<span class="c1"># Second Multivariable Linear Regression Model (Gradient Boosting)</span>
<span class="c1"># We used GridSearchCV to find the best hyperparameters but as the output was large, we just used the hyperparameters we got from our GridSearch</span>
<span class="kn">from</span> <span class="nn">sklearn.ensemble</span> <span class="kn">import</span> <span class="n">GradientBoostingRegressor</span>

<span class="c1"># parametersGb = {</span>
<span class="c1">#     "n_estimators":[5,50,250,500],</span>
<span class="c1">#     "max_depth":[1,3,5,7,9],</span>
<span class="c1">#     "learning_rate":[0.01,0.1,1,10,100]</span>
<span class="c1"># }</span>
<span class="c1"># gbGrid = GridSearchCV(GradientBoostingRegressor(), parametersGb, cv = 5)</span>
<span class="c1"># gbModel = gbGrid.fit(X_train, y_train)</span>

<span class="n">gbModel</span> <span class="o">=</span> <span class="n">GradientBoostingRegressor</span><span class="p">(</span><span class="n">learning_rate</span><span class="o">=</span><span class="mf">0.1</span><span class="p">,</span> <span class="n">max_depth</span><span class="o">=</span><span class="mi">3</span><span class="p">,</span> <span class="n">n_estimators</span><span class="o">=</span><span class="mi">250</span><span class="p">)</span>
<span class="n">gbModel</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span><span class="n">y_train</span><span class="p">)</span>
<span class="n">gbPreds</span> <span class="o">=</span> <span class="n">gbModel</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>
</pre></div>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs" id="cell-id=a5c3aa3f-28f3-47ee-bc5e-d2377a0210f3">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [14]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Implement a Neural Network using Tensorflow and Keras to classify wine quality</span>
<span class="kn">import</span> <span class="nn">tensorflow</span> <span class="k">as</span> <span class="nn">tf</span>
<span class="n">tf</span><span class="o">.</span><span class="n">version</span><span class="o">.</span><span class="n">VERSION</span>
<span class="kn">from</span> <span class="nn">tensorflow</span> <span class="kn">import</span> <span class="n">keras</span>
<span class="kn">from</span> <span class="nn">keras.models</span> <span class="kn">import</span> <span class="n">Sequential</span>
<span class="kn">from</span> <span class="nn">keras.layers</span> <span class="kn">import</span> <span class="n">Dense</span><span class="p">,</span> <span class="n">Flatten</span>

<span class="kn">from</span> <span class="nn">tensorflow.keras.utils</span> <span class="kn">import</span> <span class="n">to_categorical</span>
<span class="kn">from</span> <span class="nn">tensorflow.keras.optimizers</span> <span class="kn">import</span> <span class="n">SGD</span>

<span class="n">n_classes</span> <span class="o">=</span> <span class="mi">10</span>
<span class="n">y_train_nn</span> <span class="o">=</span> <span class="n">to_categorical</span><span class="p">(</span><span class="n">y_train</span><span class="p">,</span> <span class="n">n_classes</span><span class="p">)</span>
<span class="n">y_test_nn</span> <span class="o">=</span> <span class="n">to_categorical</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">n_classes</span><span class="p">)</span>

<span class="n">nnModel</span> <span class="o">=</span> <span class="n">Sequential</span><span class="p">()</span>
<span class="n">nnModel</span><span class="o">.</span><span class="n">add</span><span class="p">(</span><span class="n">Dense</span><span class="p">(</span><span class="mi">5</span><span class="p">,</span> <span class="n">activation</span><span class="o">=</span><span class="s1">'relu'</span><span class="p">,</span> <span class="n">input_shape</span><span class="o">=</span><span class="p">(</span><span class="mi">11</span><span class="p">,)))</span>
<span class="n">nnModel</span><span class="o">.</span><span class="n">add</span><span class="p">(</span><span class="n">Dense</span><span class="p">(</span><span class="mi">10</span><span class="p">,</span> <span class="n">activation</span><span class="o">=</span><span class="s1">'softmax'</span><span class="p">))</span>
</pre></div>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=4e46e916-1aed-468e-9f72-292805809d69">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [15]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="n">nnModel</span><span class="o">.</span><span class="n">summary</span><span class="p">()</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>Model: "sequential"
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 dense (Dense)               (None, 5)                 60        
                                                                 
 dense_1 (Dense)             (None, 10)                60        
                                                                 
=================================================================
Total params: 120
Trainable params: 120
Non-trainable params: 0
_________________________________________________________________
</pre>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=a0cff43b-f442-443e-96ea-66fa624a13ce">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [16]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Neural Network Model Configuration</span>
<span class="n">nnModel</span><span class="o">.</span><span class="n">compile</span><span class="p">(</span><span class="n">loss</span><span class="o">=</span><span class="s1">'categorical_crossentropy'</span><span class="p">,</span> <span class="n">optimizer</span><span class="o">=</span><span class="s1">'adam'</span><span class="p">,</span> <span class="n">metrics</span><span class="o">=</span><span class="p">[</span><span class="s1">'accuracy'</span><span class="p">])</span>

<span class="c1"># Neural Network Model Training</span>
<span class="n">history</span> <span class="o">=</span> <span class="n">nnModel</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">X_train</span><span class="p">,</span> <span class="n">y_train_nn</span><span class="p">,</span> <span class="n">batch_size</span><span class="o">=</span><span class="mi">128</span><span class="p">,</span> <span class="n">epochs</span><span class="o">=</span><span class="mi">200</span><span class="p">,</span> <span class="n">verbose</span><span class="o">=</span><span class="mi">1</span><span class="p">,</span> <span class="n">validation_data</span><span class="o">=</span><span class="p">(</span><span class="n">X_test</span><span class="p">,</span> <span class="n">y_test_nn</span><span class="p">))</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>Epoch 1/200
10/10 [==============================] - 1s 31ms/step - loss: 2.7089 - accuracy: 0.0868 - val_loss: 2.6831 - val_accuracy: 0.0938
Epoch 2/200
10/10 [==============================] - 0s 7ms/step - loss: 2.6298 - accuracy: 0.1032 - val_loss: 2.6036 - val_accuracy: 0.1125
Epoch 3/200
10/10 [==============================] - 0s 6ms/step - loss: 2.5549 - accuracy: 0.1235 - val_loss: 2.5281 - val_accuracy: 0.1562
Epoch 4/200
10/10 [==============================] - 0s 5ms/step - loss: 2.4843 - accuracy: 0.1540 - val_loss: 2.4571 - val_accuracy: 0.1750
Epoch 5/200
10/10 [==============================] - 0s 6ms/step - loss: 2.4177 - accuracy: 0.1775 - val_loss: 2.3905 - val_accuracy: 0.1937
Epoch 6/200
10/10 [==============================] - 0s 5ms/step - loss: 2.3565 - accuracy: 0.2064 - val_loss: 2.3276 - val_accuracy: 0.2094
Epoch 7/200
10/10 [==============================] - 0s 5ms/step - loss: 2.2982 - accuracy: 0.2103 - val_loss: 2.2691 - val_accuracy: 0.2125
Epoch 8/200
10/10 [==============================] - 0s 5ms/step - loss: 2.2441 - accuracy: 0.2252 - val_loss: 2.2146 - val_accuracy: 0.2219
Epoch 9/200
10/10 [==============================] - 0s 6ms/step - loss: 2.1933 - accuracy: 0.2392 - val_loss: 2.1642 - val_accuracy: 0.2313
Epoch 10/200
10/10 [==============================] - 0s 5ms/step - loss: 2.1463 - accuracy: 0.2518 - val_loss: 2.1169 - val_accuracy: 0.2562
Epoch 11/200
10/10 [==============================] - 0s 5ms/step - loss: 2.1020 - accuracy: 0.2619 - val_loss: 2.0731 - val_accuracy: 0.2781
Epoch 12/200
10/10 [==============================] - 0s 5ms/step - loss: 2.0617 - accuracy: 0.2682 - val_loss: 2.0312 - val_accuracy: 0.2812
Epoch 13/200
10/10 [==============================] - 0s 6ms/step - loss: 2.0218 - accuracy: 0.2760 - val_loss: 1.9930 - val_accuracy: 0.2812
Epoch 14/200
10/10 [==============================] - 0s 5ms/step - loss: 1.9855 - accuracy: 0.2932 - val_loss: 1.9562 - val_accuracy: 0.3000
Epoch 15/200
10/10 [==============================] - 0s 5ms/step - loss: 1.9502 - accuracy: 0.3159 - val_loss: 1.9221 - val_accuracy: 0.3063
Epoch 16/200
10/10 [==============================] - 0s 6ms/step - loss: 1.9170 - accuracy: 0.3339 - val_loss: 1.8896 - val_accuracy: 0.3281
Epoch 17/200
10/10 [==============================] - 0s 5ms/step - loss: 1.8856 - accuracy: 0.3487 - val_loss: 1.8586 - val_accuracy: 0.3469
Epoch 18/200
10/10 [==============================] - 0s 6ms/step - loss: 1.8556 - accuracy: 0.3698 - val_loss: 1.8293 - val_accuracy: 0.3656
Epoch 19/200
10/10 [==============================] - 0s 5ms/step - loss: 1.8267 - accuracy: 0.3831 - val_loss: 1.8012 - val_accuracy: 0.3781
Epoch 20/200
10/10 [==============================] - 0s 5ms/step - loss: 1.7988 - accuracy: 0.3980 - val_loss: 1.7745 - val_accuracy: 0.3875
Epoch 21/200
10/10 [==============================] - 0s 5ms/step - loss: 1.7727 - accuracy: 0.4081 - val_loss: 1.7483 - val_accuracy: 0.4031
Epoch 22/200
10/10 [==============================] - 0s 5ms/step - loss: 1.7468 - accuracy: 0.4128 - val_loss: 1.7237 - val_accuracy: 0.4156
Epoch 23/200
10/10 [==============================] - 0s 6ms/step - loss: 1.7223 - accuracy: 0.4206 - val_loss: 1.6999 - val_accuracy: 0.4281
Epoch 24/200
10/10 [==============================] - 0s 5ms/step - loss: 1.6986 - accuracy: 0.4269 - val_loss: 1.6767 - val_accuracy: 0.4344
Epoch 25/200
10/10 [==============================] - 0s 5ms/step - loss: 1.6760 - accuracy: 0.4324 - val_loss: 1.6539 - val_accuracy: 0.4406
Epoch 26/200
10/10 [==============================] - 0s 6ms/step - loss: 1.6541 - accuracy: 0.4355 - val_loss: 1.6318 - val_accuracy: 0.4469
Epoch 27/200
10/10 [==============================] - 0s 6ms/step - loss: 1.6329 - accuracy: 0.4418 - val_loss: 1.6104 - val_accuracy: 0.4625
Epoch 28/200
10/10 [==============================] - 0s 5ms/step - loss: 1.6125 - accuracy: 0.4433 - val_loss: 1.5899 - val_accuracy: 0.4625
Epoch 29/200
10/10 [==============================] - 0s 5ms/step - loss: 1.5924 - accuracy: 0.4441 - val_loss: 1.5705 - val_accuracy: 0.4500
Epoch 30/200
10/10 [==============================] - 0s 5ms/step - loss: 1.5737 - accuracy: 0.4480 - val_loss: 1.5516 - val_accuracy: 0.4531
Epoch 31/200
10/10 [==============================] - 0s 6ms/step - loss: 1.5551 - accuracy: 0.4527 - val_loss: 1.5333 - val_accuracy: 0.4594
Epoch 32/200
10/10 [==============================] - 0s 5ms/step - loss: 1.5375 - accuracy: 0.4597 - val_loss: 1.5156 - val_accuracy: 0.4750
Epoch 33/200
10/10 [==============================] - 0s 6ms/step - loss: 1.5201 - accuracy: 0.4629 - val_loss: 1.4989 - val_accuracy: 0.4750
Epoch 34/200
10/10 [==============================] - 0s 6ms/step - loss: 1.5038 - accuracy: 0.4652 - val_loss: 1.4826 - val_accuracy: 0.4781
Epoch 35/200
10/10 [==============================] - 0s 5ms/step - loss: 1.4872 - accuracy: 0.4707 - val_loss: 1.4668 - val_accuracy: 0.4750
Epoch 36/200
10/10 [==============================] - 0s 5ms/step - loss: 1.4714 - accuracy: 0.4722 - val_loss: 1.4511 - val_accuracy: 0.4781
Epoch 37/200
10/10 [==============================] - 0s 5ms/step - loss: 1.4558 - accuracy: 0.4801 - val_loss: 1.4351 - val_accuracy: 0.4938
Epoch 38/200
10/10 [==============================] - 0s 5ms/step - loss: 1.4400 - accuracy: 0.4855 - val_loss: 1.4198 - val_accuracy: 0.4938
Epoch 39/200
10/10 [==============================] - 0s 5ms/step - loss: 1.4243 - accuracy: 0.4902 - val_loss: 1.4049 - val_accuracy: 0.5031
Epoch 40/200
10/10 [==============================] - 0s 5ms/step - loss: 1.4094 - accuracy: 0.4934 - val_loss: 1.3901 - val_accuracy: 0.5031
Epoch 41/200
10/10 [==============================] - 0s 5ms/step - loss: 1.3939 - accuracy: 0.4980 - val_loss: 1.3760 - val_accuracy: 0.5094
Epoch 42/200
10/10 [==============================] - 0s 5ms/step - loss: 1.3795 - accuracy: 0.4988 - val_loss: 1.3620 - val_accuracy: 0.5125
Epoch 43/200
10/10 [==============================] - 0s 5ms/step - loss: 1.3648 - accuracy: 0.5082 - val_loss: 1.3487 - val_accuracy: 0.5281
Epoch 44/200
10/10 [==============================] - 0s 5ms/step - loss: 1.3510 - accuracy: 0.5106 - val_loss: 1.3358 - val_accuracy: 0.5250
Epoch 45/200
10/10 [==============================] - 0s 5ms/step - loss: 1.3374 - accuracy: 0.5168 - val_loss: 1.3231 - val_accuracy: 0.5281
Epoch 46/200
10/10 [==============================] - 0s 5ms/step - loss: 1.3244 - accuracy: 0.5223 - val_loss: 1.3108 - val_accuracy: 0.5250
Epoch 47/200
10/10 [==============================] - 0s 6ms/step - loss: 1.3120 - accuracy: 0.5223 - val_loss: 1.2989 - val_accuracy: 0.5281
Epoch 48/200
10/10 [==============================] - 0s 5ms/step - loss: 1.2999 - accuracy: 0.5262 - val_loss: 1.2877 - val_accuracy: 0.5250
Epoch 49/200
10/10 [==============================] - 0s 5ms/step - loss: 1.2889 - accuracy: 0.5285 - val_loss: 1.2767 - val_accuracy: 0.5250
Epoch 50/200
10/10 [==============================] - 0s 5ms/step - loss: 1.2776 - accuracy: 0.5285 - val_loss: 1.2659 - val_accuracy: 0.5312
Epoch 51/200
10/10 [==============================] - 0s 5ms/step - loss: 1.2664 - accuracy: 0.5309 - val_loss: 1.2560 - val_accuracy: 0.5375
Epoch 52/200
10/10 [==============================] - 0s 5ms/step - loss: 1.2564 - accuracy: 0.5364 - val_loss: 1.2460 - val_accuracy: 0.5375
Epoch 53/200
10/10 [==============================] - 0s 5ms/step - loss: 1.2459 - accuracy: 0.5395 - val_loss: 1.2367 - val_accuracy: 0.5469
Epoch 54/200
10/10 [==============================] - 0s 5ms/step - loss: 1.2362 - accuracy: 0.5395 - val_loss: 1.2278 - val_accuracy: 0.5406
Epoch 55/200
10/10 [==============================] - 0s 5ms/step - loss: 1.2270 - accuracy: 0.5410 - val_loss: 1.2191 - val_accuracy: 0.5406
Epoch 56/200
10/10 [==============================] - 0s 6ms/step - loss: 1.2176 - accuracy: 0.5442 - val_loss: 1.2108 - val_accuracy: 0.5406
Epoch 57/200
10/10 [==============================] - 0s 6ms/step - loss: 1.2089 - accuracy: 0.5465 - val_loss: 1.2028 - val_accuracy: 0.5406
Epoch 58/200
10/10 [==============================] - 0s 5ms/step - loss: 1.2001 - accuracy: 0.5450 - val_loss: 1.1953 - val_accuracy: 0.5375
Epoch 59/200
10/10 [==============================] - 0s 6ms/step - loss: 1.1919 - accuracy: 0.5442 - val_loss: 1.1878 - val_accuracy: 0.5375
Epoch 60/200
10/10 [==============================] - 0s 6ms/step - loss: 1.1840 - accuracy: 0.5481 - val_loss: 1.1808 - val_accuracy: 0.5375
Epoch 61/200
10/10 [==============================] - 0s 5ms/step - loss: 1.1763 - accuracy: 0.5504 - val_loss: 1.1738 - val_accuracy: 0.5406
Epoch 62/200
10/10 [==============================] - 0s 5ms/step - loss: 1.1689 - accuracy: 0.5559 - val_loss: 1.1669 - val_accuracy: 0.5500
Epoch 63/200
10/10 [==============================] - 0s 5ms/step - loss: 1.1618 - accuracy: 0.5582 - val_loss: 1.1602 - val_accuracy: 0.5531
Epoch 64/200
10/10 [==============================] - 0s 6ms/step - loss: 1.1548 - accuracy: 0.5629 - val_loss: 1.1540 - val_accuracy: 0.5531
Epoch 65/200
10/10 [==============================] - 0s 5ms/step - loss: 1.1479 - accuracy: 0.5653 - val_loss: 1.1480 - val_accuracy: 0.5531
Epoch 66/200
10/10 [==============================] - 0s 5ms/step - loss: 1.1412 - accuracy: 0.5684 - val_loss: 1.1425 - val_accuracy: 0.5594
Epoch 67/200
10/10 [==============================] - 0s 5ms/step - loss: 1.1350 - accuracy: 0.5715 - val_loss: 1.1372 - val_accuracy: 0.5625
Epoch 68/200
10/10 [==============================] - 0s 5ms/step - loss: 1.1289 - accuracy: 0.5739 - val_loss: 1.1321 - val_accuracy: 0.5625
Epoch 69/200
10/10 [==============================] - 0s 5ms/step - loss: 1.1230 - accuracy: 0.5754 - val_loss: 1.1271 - val_accuracy: 0.5656
Epoch 70/200
10/10 [==============================] - 0s 5ms/step - loss: 1.1174 - accuracy: 0.5794 - val_loss: 1.1224 - val_accuracy: 0.5656
Epoch 71/200
10/10 [==============================] - 0s 5ms/step - loss: 1.1119 - accuracy: 0.5809 - val_loss: 1.1183 - val_accuracy: 0.5719
Epoch 72/200
10/10 [==============================] - 0s 6ms/step - loss: 1.1067 - accuracy: 0.5825 - val_loss: 1.1144 - val_accuracy: 0.5688
Epoch 73/200
10/10 [==============================] - 0s 5ms/step - loss: 1.1018 - accuracy: 0.5817 - val_loss: 1.1106 - val_accuracy: 0.5719
Epoch 74/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0972 - accuracy: 0.5817 - val_loss: 1.1069 - val_accuracy: 0.5750
Epoch 75/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0929 - accuracy: 0.5825 - val_loss: 1.1035 - val_accuracy: 0.5656
Epoch 76/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0884 - accuracy: 0.5825 - val_loss: 1.1001 - val_accuracy: 0.5625
Epoch 77/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0843 - accuracy: 0.5833 - val_loss: 1.0969 - val_accuracy: 0.5594
Epoch 78/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0805 - accuracy: 0.5825 - val_loss: 1.0939 - val_accuracy: 0.5594
Epoch 79/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0766 - accuracy: 0.5817 - val_loss: 1.0909 - val_accuracy: 0.5562
Epoch 80/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0730 - accuracy: 0.5872 - val_loss: 1.0880 - val_accuracy: 0.5562
Epoch 81/200
10/10 [==============================] - 0s 7ms/step - loss: 1.0693 - accuracy: 0.5864 - val_loss: 1.0850 - val_accuracy: 0.5625
Epoch 82/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0660 - accuracy: 0.5817 - val_loss: 1.0820 - val_accuracy: 0.5625
Epoch 83/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0626 - accuracy: 0.5833 - val_loss: 1.0790 - val_accuracy: 0.5656
Epoch 84/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0594 - accuracy: 0.5848 - val_loss: 1.0760 - val_accuracy: 0.5719
Epoch 85/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0562 - accuracy: 0.5903 - val_loss: 1.0728 - val_accuracy: 0.5750
Epoch 86/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0530 - accuracy: 0.5911 - val_loss: 1.0701 - val_accuracy: 0.5781
Epoch 87/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0504 - accuracy: 0.5934 - val_loss: 1.0672 - val_accuracy: 0.5781
Epoch 88/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0473 - accuracy: 0.5950 - val_loss: 1.0645 - val_accuracy: 0.5781
Epoch 89/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0446 - accuracy: 0.5973 - val_loss: 1.0617 - val_accuracy: 0.5750
Epoch 90/200
10/10 [==============================] - 0s 5ms/step - loss: 1.0420 - accuracy: 0.6005 - val_loss: 1.0590 - val_accuracy: 0.5750
Epoch 91/200
10/10 [==============================] - 0s 5ms/step - loss: 1.0393 - accuracy: 0.6013 - val_loss: 1.0565 - val_accuracy: 0.5813
Epoch 92/200
10/10 [==============================] - 0s 5ms/step - loss: 1.0367 - accuracy: 0.6028 - val_loss: 1.0541 - val_accuracy: 0.5781
Epoch 93/200
10/10 [==============================] - 0s 5ms/step - loss: 1.0344 - accuracy: 0.6020 - val_loss: 1.0518 - val_accuracy: 0.5750
Epoch 94/200
10/10 [==============================] - 0s 5ms/step - loss: 1.0319 - accuracy: 0.6013 - val_loss: 1.0495 - val_accuracy: 0.5750
Epoch 95/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0295 - accuracy: 0.6013 - val_loss: 1.0474 - val_accuracy: 0.5719
Epoch 96/200
10/10 [==============================] - 0s 5ms/step - loss: 1.0274 - accuracy: 0.6028 - val_loss: 1.0453 - val_accuracy: 0.5719
Epoch 97/200
10/10 [==============================] - 0s 5ms/step - loss: 1.0254 - accuracy: 0.6036 - val_loss: 1.0430 - val_accuracy: 0.5719
Epoch 98/200
10/10 [==============================] - 0s 5ms/step - loss: 1.0232 - accuracy: 0.6036 - val_loss: 1.0411 - val_accuracy: 0.5719
Epoch 99/200
10/10 [==============================] - 0s 5ms/step - loss: 1.0212 - accuracy: 0.6020 - val_loss: 1.0392 - val_accuracy: 0.5656
Epoch 100/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0194 - accuracy: 0.6036 - val_loss: 1.0371 - val_accuracy: 0.5625
Epoch 101/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0174 - accuracy: 0.6052 - val_loss: 1.0352 - val_accuracy: 0.5625
Epoch 102/200
10/10 [==============================] - 0s 5ms/step - loss: 1.0156 - accuracy: 0.6052 - val_loss: 1.0334 - val_accuracy: 0.5594
Epoch 103/200
10/10 [==============================] - 0s 5ms/step - loss: 1.0137 - accuracy: 0.6067 - val_loss: 1.0316 - val_accuracy: 0.5625
Epoch 104/200
10/10 [==============================] - 0s 5ms/step - loss: 1.0119 - accuracy: 0.6067 - val_loss: 1.0299 - val_accuracy: 0.5656
Epoch 105/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0102 - accuracy: 0.6083 - val_loss: 1.0280 - val_accuracy: 0.5656
Epoch 106/200
10/10 [==============================] - 0s 5ms/step - loss: 1.0085 - accuracy: 0.6075 - val_loss: 1.0261 - val_accuracy: 0.5656
Epoch 107/200
10/10 [==============================] - 0s 6ms/step - loss: 1.0067 - accuracy: 0.6067 - val_loss: 1.0244 - val_accuracy: 0.5688
Epoch 108/200
10/10 [==============================] - 0s 5ms/step - loss: 1.0049 - accuracy: 0.6059 - val_loss: 1.0228 - val_accuracy: 0.5750
Epoch 109/200
10/10 [==============================] - 0s 5ms/step - loss: 1.0032 - accuracy: 0.6052 - val_loss: 1.0212 - val_accuracy: 0.5781
Epoch 110/200
10/10 [==============================] - 0s 5ms/step - loss: 1.0017 - accuracy: 0.6059 - val_loss: 1.0194 - val_accuracy: 0.5750
Epoch 111/200
10/10 [==============================] - 0s 5ms/step - loss: 1.0001 - accuracy: 0.6075 - val_loss: 1.0178 - val_accuracy: 0.5750
Epoch 112/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9986 - accuracy: 0.6083 - val_loss: 1.0165 - val_accuracy: 0.5750
Epoch 113/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9970 - accuracy: 0.6106 - val_loss: 1.0150 - val_accuracy: 0.5781
Epoch 114/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9955 - accuracy: 0.6106 - val_loss: 1.0135 - val_accuracy: 0.5813
Epoch 115/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9940 - accuracy: 0.6099 - val_loss: 1.0119 - val_accuracy: 0.5813
Epoch 116/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9925 - accuracy: 0.6099 - val_loss: 1.0104 - val_accuracy: 0.5781
Epoch 117/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9911 - accuracy: 0.6075 - val_loss: 1.0088 - val_accuracy: 0.5781
Epoch 118/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9897 - accuracy: 0.6083 - val_loss: 1.0072 - val_accuracy: 0.5781
Epoch 119/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9883 - accuracy: 0.6067 - val_loss: 1.0058 - val_accuracy: 0.5719
Epoch 120/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9869 - accuracy: 0.6067 - val_loss: 1.0043 - val_accuracy: 0.5719
Epoch 121/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9854 - accuracy: 0.6067 - val_loss: 1.0030 - val_accuracy: 0.5719
Epoch 122/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9841 - accuracy: 0.6075 - val_loss: 1.0018 - val_accuracy: 0.5719
Epoch 123/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9827 - accuracy: 0.6052 - val_loss: 1.0005 - val_accuracy: 0.5719
Epoch 124/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9815 - accuracy: 0.6044 - val_loss: 0.9992 - val_accuracy: 0.5688
Epoch 125/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9802 - accuracy: 0.6028 - val_loss: 0.9978 - val_accuracy: 0.5656
Epoch 126/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9791 - accuracy: 0.6028 - val_loss: 0.9964 - val_accuracy: 0.5625
Epoch 127/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9778 - accuracy: 0.6020 - val_loss: 0.9953 - val_accuracy: 0.5656
Epoch 128/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9767 - accuracy: 0.6013 - val_loss: 0.9940 - val_accuracy: 0.5656
Epoch 129/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9756 - accuracy: 0.5997 - val_loss: 0.9927 - val_accuracy: 0.5688
Epoch 130/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9743 - accuracy: 0.5997 - val_loss: 0.9914 - val_accuracy: 0.5688
Epoch 131/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9734 - accuracy: 0.5997 - val_loss: 0.9901 - val_accuracy: 0.5688
Epoch 132/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9723 - accuracy: 0.5981 - val_loss: 0.9889 - val_accuracy: 0.5688
Epoch 133/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9712 - accuracy: 0.5973 - val_loss: 0.9876 - val_accuracy: 0.5719
Epoch 134/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9702 - accuracy: 0.5973 - val_loss: 0.9865 - val_accuracy: 0.5688
Epoch 135/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9691 - accuracy: 0.5973 - val_loss: 0.9854 - val_accuracy: 0.5719
Epoch 136/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9682 - accuracy: 0.5981 - val_loss: 0.9843 - val_accuracy: 0.5719
Epoch 137/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9672 - accuracy: 0.5973 - val_loss: 0.9833 - val_accuracy: 0.5688
Epoch 138/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9662 - accuracy: 0.5973 - val_loss: 0.9821 - val_accuracy: 0.5719
Epoch 139/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9654 - accuracy: 0.5966 - val_loss: 0.9809 - val_accuracy: 0.5813
Epoch 140/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9644 - accuracy: 0.6005 - val_loss: 0.9799 - val_accuracy: 0.5813
Epoch 141/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9635 - accuracy: 0.5989 - val_loss: 0.9790 - val_accuracy: 0.5781
Epoch 142/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9627 - accuracy: 0.5958 - val_loss: 0.9777 - val_accuracy: 0.5750
Epoch 143/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9618 - accuracy: 0.5942 - val_loss: 0.9764 - val_accuracy: 0.5719
Epoch 144/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9610 - accuracy: 0.5934 - val_loss: 0.9754 - val_accuracy: 0.5781
Epoch 145/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9601 - accuracy: 0.5950 - val_loss: 0.9745 - val_accuracy: 0.5813
Epoch 146/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9594 - accuracy: 0.5942 - val_loss: 0.9734 - val_accuracy: 0.5813
Epoch 147/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9586 - accuracy: 0.5934 - val_loss: 0.9724 - val_accuracy: 0.5781
Epoch 148/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9578 - accuracy: 0.5934 - val_loss: 0.9715 - val_accuracy: 0.5781
Epoch 149/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9572 - accuracy: 0.5934 - val_loss: 0.9705 - val_accuracy: 0.5781
Epoch 150/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9564 - accuracy: 0.5950 - val_loss: 0.9696 - val_accuracy: 0.5781
Epoch 151/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9557 - accuracy: 0.5942 - val_loss: 0.9689 - val_accuracy: 0.5781
Epoch 152/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9549 - accuracy: 0.5942 - val_loss: 0.9679 - val_accuracy: 0.5750
Epoch 153/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9542 - accuracy: 0.5958 - val_loss: 0.9671 - val_accuracy: 0.5750
Epoch 154/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9535 - accuracy: 0.5950 - val_loss: 0.9662 - val_accuracy: 0.5719
Epoch 155/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9529 - accuracy: 0.5934 - val_loss: 0.9654 - val_accuracy: 0.5750
Epoch 156/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9522 - accuracy: 0.5927 - val_loss: 0.9645 - val_accuracy: 0.5719
Epoch 157/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9516 - accuracy: 0.5942 - val_loss: 0.9638 - val_accuracy: 0.5750
Epoch 158/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9509 - accuracy: 0.5919 - val_loss: 0.9630 - val_accuracy: 0.5750
Epoch 159/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9502 - accuracy: 0.5895 - val_loss: 0.9621 - val_accuracy: 0.5750
Epoch 160/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9496 - accuracy: 0.5903 - val_loss: 0.9612 - val_accuracy: 0.5719
Epoch 161/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9489 - accuracy: 0.5903 - val_loss: 0.9604 - val_accuracy: 0.5719
Epoch 162/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9483 - accuracy: 0.5934 - val_loss: 0.9596 - val_accuracy: 0.5750
Epoch 163/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9478 - accuracy: 0.5950 - val_loss: 0.9588 - val_accuracy: 0.5781
Epoch 164/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9471 - accuracy: 0.5958 - val_loss: 0.9580 - val_accuracy: 0.5781
Epoch 165/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9464 - accuracy: 0.5966 - val_loss: 0.9571 - val_accuracy: 0.5781
Epoch 166/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9459 - accuracy: 0.5958 - val_loss: 0.9564 - val_accuracy: 0.5781
Epoch 167/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9454 - accuracy: 0.5958 - val_loss: 0.9556 - val_accuracy: 0.5781
Epoch 168/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9450 - accuracy: 0.5942 - val_loss: 0.9549 - val_accuracy: 0.5781
Epoch 169/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9444 - accuracy: 0.5942 - val_loss: 0.9542 - val_accuracy: 0.5813
Epoch 170/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9439 - accuracy: 0.5966 - val_loss: 0.9535 - val_accuracy: 0.5844
Epoch 171/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9434 - accuracy: 0.5950 - val_loss: 0.9530 - val_accuracy: 0.5844
Epoch 172/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9428 - accuracy: 0.5942 - val_loss: 0.9522 - val_accuracy: 0.5844
Epoch 173/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9424 - accuracy: 0.5942 - val_loss: 0.9514 - val_accuracy: 0.5844
Epoch 174/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9417 - accuracy: 0.5927 - val_loss: 0.9507 - val_accuracy: 0.5844
Epoch 175/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9413 - accuracy: 0.5927 - val_loss: 0.9498 - val_accuracy: 0.5938
Epoch 176/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9409 - accuracy: 0.5942 - val_loss: 0.9491 - val_accuracy: 0.5875
Epoch 177/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9403 - accuracy: 0.5927 - val_loss: 0.9486 - val_accuracy: 0.5938
Epoch 178/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9399 - accuracy: 0.5934 - val_loss: 0.9480 - val_accuracy: 0.5969
Epoch 179/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9394 - accuracy: 0.5934 - val_loss: 0.9473 - val_accuracy: 0.5938
Epoch 180/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9390 - accuracy: 0.5942 - val_loss: 0.9469 - val_accuracy: 0.5969
Epoch 181/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9386 - accuracy: 0.5942 - val_loss: 0.9463 - val_accuracy: 0.5906
Epoch 182/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9381 - accuracy: 0.5966 - val_loss: 0.9457 - val_accuracy: 0.5969
Epoch 183/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9377 - accuracy: 0.5966 - val_loss: 0.9451 - val_accuracy: 0.5938
Epoch 184/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9374 - accuracy: 0.5958 - val_loss: 0.9448 - val_accuracy: 0.5906
Epoch 185/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9368 - accuracy: 0.6005 - val_loss: 0.9442 - val_accuracy: 0.5938
Epoch 186/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9364 - accuracy: 0.5981 - val_loss: 0.9434 - val_accuracy: 0.6000
Epoch 187/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9358 - accuracy: 0.5973 - val_loss: 0.9429 - val_accuracy: 0.5969
Epoch 188/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9354 - accuracy: 0.5981 - val_loss: 0.9422 - val_accuracy: 0.5938
Epoch 189/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9350 - accuracy: 0.5981 - val_loss: 0.9415 - val_accuracy: 0.5969
Epoch 190/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9346 - accuracy: 0.5981 - val_loss: 0.9412 - val_accuracy: 0.5969
Epoch 191/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9342 - accuracy: 0.5989 - val_loss: 0.9407 - val_accuracy: 0.5969
Epoch 192/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9336 - accuracy: 0.6013 - val_loss: 0.9399 - val_accuracy: 0.5969
Epoch 193/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9332 - accuracy: 0.6020 - val_loss: 0.9395 - val_accuracy: 0.5969
Epoch 194/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9329 - accuracy: 0.6005 - val_loss: 0.9390 - val_accuracy: 0.5969
Epoch 195/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9325 - accuracy: 0.6020 - val_loss: 0.9383 - val_accuracy: 0.5969
Epoch 196/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9321 - accuracy: 0.6020 - val_loss: 0.9378 - val_accuracy: 0.5938
Epoch 197/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9318 - accuracy: 0.6013 - val_loss: 0.9371 - val_accuracy: 0.5938
Epoch 198/200
10/10 [==============================] - 0s 6ms/step - loss: 0.9311 - accuracy: 0.6036 - val_loss: 0.9367 - val_accuracy: 0.5938
Epoch 199/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9309 - accuracy: 0.6044 - val_loss: 0.9359 - val_accuracy: 0.5938
Epoch 200/200
10/10 [==============================] - 0s 5ms/step - loss: 0.9304 - accuracy: 0.6052 - val_loss: 0.9355 - val_accuracy: 0.5938
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=3b68a874">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h3 id="Model-Evaluation">Model Evaluation<a class="anchor-link" href="#Model-Evaluation">¶</a></h3><p>Evaluating the model accuracy is an essential part of the process in creating machine learning models to describe how well the model is performing in its predictions. Evaluation metrics change according to the problem type. Here, we'll briefly learn how to check the accuracy of the regression model.</p>
<p>The linear model (regression) can be a typical example of this type of problem, and the main characteristic of the regression problem is that the targets of a dataset contain the real numbers only. The errors represent how much the model is making mistakes in its prediction. The basic concept of accuracy evaluation is to compare the original target with the predicted one according to certain metrics.</p>
<p><strong>Regression model evaluation metrics</strong></p>
<p>The MAE, RMSE, and R-Squared metrics are mainly used to evaluate the prediction error rates and model performance in regression analysis.</p>
<p><strong>MAE (Mean absolute error)</strong> represents the difference between the original and predicted values extracted by averaged the absolute difference over the data set.</p>
<p><strong>RMSE (Root Mean Squared Error)</strong> is the error rate by the square root of MSE.</p>
<p><strong>R-squared (Coefficient of determination)</strong> represents the coefficient of how well the values fit compared to the original values. The value from 0 to 1 interpreted as percentages. The higher the value is, the better the model is.</p>
<p>The above metrics can be expressed as following:
<img alt="No description has been provided for this image" src="https://4.bp.blogspot.com/-wG7IbjTfE6k/XGUvqm7TCVI/AAAAAAAAAZU/vpH1kuKTIooKTcVlnm1EVRCXLVZM9cPNgCLcBGAs/s1600/formula-MAE-MSE-RMSE-RSquared.JPG"/></p>
<p>Please find more information on how to implement them from this link: <a href="https://scikit-learn.org/stable/modules/classes.html#regression-metrics">https://scikit-learn.org/stable/modules/classes.html#regression-metrics</a></p>
<p>Find more about feature importances from here: <a href="https://machinelearningmastery.com/calculate-feature-importance-with-python/">https://machinelearningmastery.com/calculate-feature-importance-with-python/</a></p>
<p><strong>Classification model evaluation metrics</strong></p>
<img alt="No description has been provided for this image" src="https://www.researchgate.net/publication/336402347/figure/fig3/AS:812472659349505@1570719985505/Calculation-of-Precision-Recall-and-Accuracy-in-the-confusion-matrix.ppm"/>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=0cc9ec55">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p><strong>For Regression models</strong></p>
<li>Use three metrics: R-squared, RMSE, and MAE, to evaluate model prediction performance</li>
<li>Compare these 3 metrics for the two models and analyze the performance</li>
<li>Calculate the feature importance scores for the top features that help predicting wine quality and visualize them</li>
<p><strong>For Classification model</strong></p>
<li> Plot training loss and validation loss </li>
<li> Plot training accuracy and validation accuracy </li>
<li> Evaluate the classsification model using Precision, Recall and Accuracy metrics </li>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=c424b669-c883-444b-bc31-12ac8be07326">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Evaluation-of-Regression-models">Evaluation of Regression models<a class="anchor-link" href="#Evaluation-of-Regression-models">¶</a></h4>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=0f1a9053-7414-49be-a23f-d6b385779e9a">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>The Random Forest model has better scores in all of the R^2, RMSE, and MAE than the Gradient Boosting model as it is shown below. Random Forest model has R^2 of 0.53 whereas the Gradient Boosting model's R^2 is 0.49 (the higher, the better). Random forest has RMSE and MAE of 0.56, and 0.42, respectively, whereas the Gradient Boosting model has RMSE and MAE of 0.58, and 0.45 (the lower, the better).</p>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=4a28fe35-8cfd-4df6-b595-79b7421e3f1a">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [17]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="kn">from</span> <span class="nn">sklearn.metrics</span> <span class="kn">import</span> <span class="n">mean_absolute_error</span><span class="p">,</span> <span class="n">r2_score</span><span class="p">,</span> <span class="n">mean_squared_error</span>
<span class="kn">from</span> <span class="nn">math</span> <span class="kn">import</span> <span class="n">sqrt</span>

<span class="k">def</span> <span class="nf">r2</span><span class="p">(</span><span class="n">y_</span><span class="p">,</span> <span class="n">y</span><span class="p">):</span>
    <span class="k">return</span> <span class="n">r2_score</span><span class="p">(</span><span class="n">y_</span><span class="p">,</span> <span class="n">y</span><span class="p">)</span>
<span class="k">def</span> <span class="nf">rmse</span><span class="p">(</span><span class="n">y_</span><span class="p">,</span> <span class="n">y</span><span class="p">):</span>
    <span class="k">return</span> <span class="n">sqrt</span><span class="p">(</span><span class="n">mean_squared_error</span><span class="p">(</span><span class="n">y_</span><span class="p">,</span> <span class="n">y</span><span class="p">))</span>
<span class="k">def</span> <span class="nf">mae</span><span class="p">(</span><span class="n">y_</span><span class="p">,</span> <span class="n">y</span><span class="p">):</span>
    <span class="k">return</span> <span class="n">mean_absolute_error</span><span class="p">(</span><span class="n">y_</span><span class="p">,</span> <span class="n">y</span><span class="p">)</span>

<span class="nb">print</span><span class="p">(</span><span class="s1">'Random Forest scores: R^2: </span><span class="si">{}</span><span class="s1">, RMSE: </span><span class="si">{}</span><span class="s1">, MAE: </span><span class="si">{}</span><span class="s1">'</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">r2</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">rfPreds</span><span class="p">),</span> <span class="n">rmse</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">rfPreds</span><span class="p">),</span> <span class="n">mae</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">rfPreds</span><span class="p">)))</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">'Gradient Boosting scores: R^2: </span><span class="si">{}</span><span class="s1">, RMSE: </span><span class="si">{}</span><span class="s1">, MAE: </span><span class="si">{}</span><span class="s1">'</span><span class="o">.</span><span class="n">format</span><span class="p">(</span><span class="n">r2</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">gbPreds</span><span class="p">),</span> <span class="n">rmse</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">gbPreds</span><span class="p">),</span> <span class="n">mae</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">gbPreds</span><span class="p">)))</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>Random Forest scores: R^2: 0.5237219061850895, RMSE: 0.5578983106265872, MAE: 0.42939999999999995
Gradient Boosting scores: R^2: 0.48972586316712086, RMSE: 0.5774661360701656, MAE: 0.4515129888215445
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=dd8b8a25-adc2-456a-88ff-4ccc7dc278ff">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>As we can see from the below graphs, both of our regression models, had almost the same determination for features' importance. The highest feature importance is related to the <code>alcohol</code> feature which was predictable as the <code>alcohol</code> had the highest correlation with the wine's <code>quality</code>.</p>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=02153c72-f30d-4e64-8ebc-4939ea12d58f">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [18]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Calculating feature importance</span>
<span class="kn">from</span> <span class="nn">matplotlib</span> <span class="kn">import</span> <span class="n">pyplot</span>

<span class="n">rfImportance</span> <span class="o">=</span> <span class="n">rfModel</span><span class="o">.</span><span class="n">feature_importances_</span>
<span class="n">gbImportance</span> <span class="o">=</span> <span class="n">gbModel</span><span class="o">.</span><span class="n">feature_importances_</span>

<span class="n">featuresNames</span> <span class="o">=</span> <span class="nb">list</span><span class="p">(</span><span class="n">wineMod</span><span class="o">.</span><span class="n">columns</span><span class="p">)</span>
<span class="c1"># summarize feature importance</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">"Random Forest Regression Feature Importance: "</span><span class="p">)</span>
<span class="k">for</span> <span class="n">i</span><span class="p">,</span><span class="n">v</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">rfImportance</span><span class="p">):</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">'Feature: </span><span class="si">%20s</span><span class="s1">, Score: </span><span class="si">%.5f</span><span class="s1">'</span> <span class="o">%</span> <span class="p">(</span><span class="n">featuresNames</span><span class="p">[</span><span class="n">i</span><span class="p">],</span><span class="n">v</span><span class="p">))</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">"</span><span class="se">\n\n</span><span class="s2">Gradient Boosting Regression Feature Importance: "</span><span class="p">)</span>
<span class="k">for</span> <span class="n">i</span><span class="p">,</span><span class="n">v</span> <span class="ow">in</span> <span class="nb">enumerate</span><span class="p">(</span><span class="n">gbImportance</span><span class="p">):</span>
    <span class="nb">print</span><span class="p">(</span><span class="s1">'Feature: </span><span class="si">%20s</span><span class="s1">, Score: </span><span class="si">%.5f</span><span class="s1">'</span> <span class="o">%</span> <span class="p">(</span><span class="n">featuresNames</span><span class="p">[</span><span class="n">i</span><span class="p">],</span><span class="n">v</span><span class="p">))</span>

<span class="c1"># plot feature importance</span>
<span class="nb">print</span><span class="p">(</span><span class="s2">"</span><span class="se">\n\n</span><span class="s2">Random Forest Regression Feature Importance Plot: "</span><span class="p">)</span>
<span class="n">pyplot</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">20</span><span class="p">,</span> <span class="mi">3</span><span class="p">))</span>
<span class="n">pyplot</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="n">featuresNames</span><span class="p">[:</span><span class="o">-</span><span class="mi">1</span><span class="p">],</span> <span class="nb">list</span><span class="p">(</span><span class="n">rfImportance</span><span class="p">))</span>
<span class="n">pyplot</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>

<span class="nb">print</span><span class="p">(</span><span class="s2">"</span><span class="se">\n\n</span><span class="s2">Gradient Boosting Regression Feature Importance Plot: "</span><span class="p">)</span>
<span class="n">pyplot</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">20</span><span class="p">,</span> <span class="mi">3</span><span class="p">))</span>
<span class="n">pyplot</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="n">featuresNames</span><span class="p">[:</span><span class="o">-</span><span class="mi">1</span><span class="p">],</span> <span class="nb">list</span><span class="p">(</span><span class="n">gbImportance</span><span class="p">))</span>
<span class="n">pyplot</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>Random Forest Regression Feature Importance: 
Feature:        fixed acidity, Score: 0.05458
Feature:     volatile acidity, Score: 0.09749
Feature:          citric acid, Score: 0.05529
Feature:       residual sugar, Score: 0.04788
Feature:            chlorides, Score: 0.06904
Feature:  free sulfur dioxide, Score: 0.05178
Feature: total sulfur dioxide, Score: 0.08317
Feature:              density, Score: 0.05652
Feature:                   pH, Score: 0.05768
Feature:            sulphates, Score: 0.15882
Feature:              alcohol, Score: 0.26774


Gradient Boosting Regression Feature Importance: 
Feature:        fixed acidity, Score: 0.06297
Feature:     volatile acidity, Score: 0.10438
Feature:          citric acid, Score: 0.04191
Feature:       residual sugar, Score: 0.02639
Feature:            chlorides, Score: 0.06071
Feature:  free sulfur dioxide, Score: 0.03230
Feature: total sulfur dioxide, Score: 0.08289
Feature:              density, Score: 0.05654
Feature:                   pH, Score: 0.05041
Feature:            sulphates, Score: 0.17765
Feature:              alcohol, Score: 0.30386


Random Forest Regression Feature Importance Plot: 
</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>

Gradient Boosting Regression Feature Importance Plot: 
</pre>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=2c527065-7b91-4ca6-aaf0-bb8e6fa7b669">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Evaluation-of-Classification-model">Evaluation of Classification model<a class="anchor-link" href="#Evaluation-of-Classification-model">¶</a></h4>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=2deb2586-cc01-471a-980f-2bc1643a8658">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>As we can see from the below graphs, our Neural Network performs how it should perform meaning that our model did not overfit, or underfit the training data and we have almost the same accuracy scores for both of train and test sets. The training loss and test loss are the same too meaning that the model's loss would be around the same for the unseen data.</p>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=68b4a8fe-b47c-4c01-a341-057d481334f7">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [19]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Got this code from Stack Overflow</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">history</span><span class="o">.</span><span class="n">history</span><span class="p">[</span><span class="s1">'accuracy'</span><span class="p">])</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">history</span><span class="o">.</span><span class="n">history</span><span class="p">[</span><span class="s1">'val_accuracy'</span><span class="p">])</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">'Training Accuracy Vs. Validation Accuracy'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">'accuracy'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">'epoch'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">([</span><span class="s1">'train'</span><span class="p">,</span> <span class="s1">'test'</span><span class="p">],</span> <span class="n">loc</span><span class="o">=</span><span class="s1">'upper left'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>

<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">history</span><span class="o">.</span><span class="n">history</span><span class="p">[</span><span class="s1">'loss'</span><span class="p">])</span>
<span class="n">plt</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">history</span><span class="o">.</span><span class="n">history</span><span class="p">[</span><span class="s1">'val_loss'</span><span class="p">])</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">'Training loss Vs. Validation loss'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">'loss'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">'epoch'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">legend</span><span class="p">([</span><span class="s1">'train'</span><span class="p">,</span> <span class="s1">'val'</span><span class="p">],</span> <span class="n">loc</span><span class="o">=</span><span class="s1">'upper left'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">show</span><span class="p">()</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,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
"/>
</div>
</div>
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedImage jp-OutputArea-output" tabindex="0">
<img alt="No description has been provided for this image" class="jp-needs-light-background" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAYgAAAEWCAYAAAB8LwAVAAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjQuMywgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy/MnkTPAAAACXBIWXMAAAsTAAALEwEAmpwYAAA3U0lEQVR4nO3deXwU9f348dd7N5ts7jskECBccslpRBBvKwW1auuF9WxtqVX7U2utWr9Va/tttYettvWsVq1UpR71vr8qoqIcBrklcgYChEAg9/n+/TEDLHETAmQzOd7Px2Mfmf3MZ2beO7vZ987nM/MZUVWMMcaY5nxeB2CMMaZzsgRhjDEmLEsQxhhjwrIEYYwxJixLEMYYY8KyBGGMMSYsSxDmoInI6yJyaXvXPcAYThCRovZeb1ciImtF5Bvu9C9E5B9tqXsQ2zlWRFYebJytrDdPRFREotp73ebQWILoYUSkIuTRJCLVIc8vPJB1qeo0VX28vet2ViKyQkS+H6b8GhGZfwjrfVBEnghTPlpEakUkra3rUtXfquoPDjaWZttXERkcsu4PVXVoe6zbdA2WIHoYVU3Y/QDWA98KKZu5u579mgvrceCSMOUXu/MO1mPAd0Qkvln5JcArqrr9ENZtzEGzBGGAvU01InKjiGwG/ikiqSLyioiUiMgOdzo3ZJn3ReQH7vRlIjJHRP7o1l0jItMOsu4AEZktIuUi8o6I/F1Enmzj6xjubqtMRJaKyBkh804VkWXuejeKyM/c8gz3tZWJyHYR+VBEwv1v/As4RkT6h24PGA08FfLaVrvbWNOWozJV/QTYCJwdsl4/8F3gcREZJCL/JyKlIrJNRGaKSEoLr//20H0lIheLyDp32Vua1Z0gIp+4r7tYRP4mItHuvNlutUXu0eX5zZvz9rOvH3Pft1fdffGpiAza375wl+0tIi+570WhiPywWczzRWSXiGwRkbvd8qCIPOm+zjIRmScivdqyPdMySxAmVDaQBvQHZuB8Pv7pPu8HVAN/a2X5o4CVQAbwe+AREZGDqPtv4DMgHbgd5xf6folIAHgZeAvIAn4CzBSR3c0ijwA/UtVE4HDg/9zy64EiIBPoBfwC+NoYNKpaBLzXLJ5LgNdUdZt7BHAvMM3dxtFAQVtiB55g36OTbwAB4HVAgN8BvYHhQF+c/dIqERkB3O/G2xtnf+aGVGkErsN5DyYBJwNXuq/1OLfOGPfo8plm697fvga4APgVkAoUAv+7v5hdT+G8H72Bc4DfisjJ7rx7gHtUNQkYBMxyyy8FknH2TTpwBc7n1RwCSxAmVBNwm6rWqmq1qpaq6nOqWqWq5Tj/4Me3svw6VX1YVRtxmlxycL5w21xXRPoBRwK3qmqdqs4BXmpj/BOBBOBOd9n/A17B+aICqAdGiEiSqu5Q1YUh5TlAf1Wtd9vaWxqk7HHcBOEeZVzIvs1LTcDhIhKrqsWqurSNsf8LOD7kCO0S4N9uPIWq+rb7vpQAd9P6+7DbOThNVLNVtRb4pRsfAKq6QFXnqmqDqq4FHmzjemH/+xrgeVX9TFUbgJnA2P2tVET6AscAN6pqjaoWAP9gb1KuBwaLSIaqVqjq3JDydGCwqja6r21XG1+LaYElCBOqRFVrdj8RkThxOlDXicguYDaQ4jZ/hLN594SqVrmTCQdYtzewPaQMYEMb4+8NbFDVppCydUAfd/ps4FRgnYh8ICKT3PI/4PzCfcttHrqplW08D+SIyETgBCAOeNV9HZXA+Ti/Xovd5pVhbQlcVdfj7N+LRCQBOAs38YhIlog87TaL7QKexPnVvz+9Cdl3bnylu5+LyGFu09pmd72/beN696y7lX0NIe8xUEXLn4Xm693u/iAJt97LgcOAFW4z0ulu+b+AN4GnRWSTiPzePcoxh8AShAnV/Ffz9cBQ4Cj3kH53s0NLzUbtoRhIE5G4kLK+bVx2E9C3Wf9BP5z2fVR1nqqeidMk8l/c5glVLVfV61V1IPAt4KchTRr7cBPXszi/8C8GnlbVupD5b6rqKThHJCuAh9sYO+ztBD8bWBNyhPM7nPdmtPs+XETb3oNiQvadu0/TQ+bf78Y4xF3vL9q4XtjPvj4Em3De/8Rw61XVVap6Ac57eBfwrIjEu0dav1LVEThNe6cT/oQCcwAsQZjWJOK045aJc6rlbZHeoKquA+YDt4tItPsr/1ttXPxToBL4uYgEROQEd9mn3XVdKCLJqloP7MJpg0dETheRwW4fyO7yxla28zjOkcLZhDQviUgvETnD7YuoBSr2s57mnsP5Qv8V+zZbJbrrKhORPsANbVzfs8DpInKM2/l8B/v+zyfivN4K90jnx82W3wIMbGHdLe7rNsYWlqpuAD4Gfud2PI/GOWqYCSAiF4lIpnvkUuYu1igiJ4rIKPfodhdOk9OB7HsThiUI05q/ALHANmAu8EYHbfdCnE7TUuA3wDM4X7itcn/JnwFMw4n5PuASVV3hVrkYWOs2p1yB80scYAjwDs6X8CfAfar6fiubmg3sBDaq6ryQch/OUdcmYDtOe/6VsOcis4r9xF/J3iQxM2TWr4Dx7jZfxWnm2i+3/+MqnE7/YmAHTufvbj/DOVOqHOdI55lmq7gd5yyqMhE5r9m697evD8UFQB7OfnwBp1/sbXfeVGCpuy/vAaa7zaLZOAlxF7Ac+ACnKc4cArEbBpnOTkSeAVaoasSPYIwxe9kRhOl0RORIcc7994nIVOBMnD4DY0wHsqtlTWeUjdOMko7TJPJjVf3c25CM6XmsickYY0xY1sRkjDEmrG7VxJSRkaF5eXleh2GMMV3GggULtqlqZrh53SpB5OXlMX/+QY+6bIwxPY6IrGtpnjUxGWOMCStiRxDuoFtP4JyR0gQ8pKr3NKtzA85FUbtjGQ5kqup2EVmLcwFPI9CgqvmRitUYY8zXRbKJqQG4XlUXuuOqLBCRt1V12e4KqvoHnIHSEJFvAdc1uznKiaq6LYIxGmOMaUHEEoSqFuNc3o+qlovIcpwRGZe1sMgFuDddaU/19fUUFRVRU1Oz/8pdWDAYJDc3l0DABrA0xrSPDumkFpE8YBzOAF/h5sfhjLFydUix4gy/rMCDqvpQC8vOwLm5Df369fva/KKiIhITE8nLy6Ple9d0bapKaWkpRUVFDBgwwOtwjDHdRMQ7qd2x7Z8Drm3lBh7fAj5q1rw0WVXH4wwGdpWIHBduQVV9SFXzVTU/M/PrZ2rV1NSQnp7ebZMDgIiQnp7e7Y+SjDEdK6IJwr1hx3PATFVtbQTK6TRrXlLVTe7frTgjOk44hDgOdtEuoye8RmNMx4pYgnDH1n8EWK6qd7dSLxlnWOQXQ8rid98wxB1bfwqwJBJxNjUpxVvL2VVuv76NMSZUJI8gJuOMv3+SiBS4j1NF5AoRuSKk3reBt9yx8HfrBcwRkUU4N69/VVUjci8CEdhSUsGOnZFJEGVlZdx3330HvNypp55KWVlZ+wdkjDFtFMmzmObQhtsXqupjwGPNylYDYyISWDMiQmwwQFVNfUTWvztBXHnllfuUNzY24ve3dGtneO211yISjzHGtFW3GmrjYKg2kUoZZbU+VDPavS3/pptu4quvvmLs2LEEAgESEhLIycmhoKCAZcuWcdZZZ7FhwwZqamq45pprmDFjBrB32JCKigqmTZvGMcccw8cff0yfPn148cUXiY2Nbdc4jTGmuR6VIK69/XUKlm7+WnlDdSWNKgSCsfh8B5Ygxo7M5i+3T2tx/p133smSJUsoKCjg/fff57TTTmPJkiV7Tkd99NFHSUtLo7q6miOPPJKzzz6b9PT0fdaxatUqnnrqKR5++GHOO+88nnvuOS666KJwmzPGmHbToxJEi8SHaBNNTXrACeJATZgwYZ9rFe69915eeOEFADZs2MCqVau+liAGDBjA2LFjATjiiCNYu3ZtRGM0xhjoYQmipV/6VVuKqNlRQk3KIHpnJ0U0hvj4+D3T77//Pu+88w6ffPIJcXFxnHDCCWGvZYiJidkz7ff7qa6ujmiMxhgDNporAP5gLD5R6iLwxZuYmEh5eXnYeTt37iQ1NZW4uDhWrFjB3Llz2337xhhzsHrUEURL/DFOh29jbfsniPT0dCZPnszhhx9ObGwsvXr12jNv6tSpPPDAA4wePZqhQ4cyceLEdt++McYcrG51T+r8/HxtfsOg5cuXM3z48FaX06Ymdq5axPaGePoPH4zf1zUPrNryWo0xJpSILGjpdgpd85uwnYnPB1HRxEgDNTUNXodjjDGdgiUIlz8mlmhfQ8QumDPGmK7GEoQrEBtHQBqoqa7zOhRjjOkULEG4dndU11dXeRyJMcZ0DpYgXL7oIABNdTV0p457Y4w5WJYgXL5ANCp+AtRT39DkdTjGGOM5SxAuEUECMURLA9XV3nVUJyQkeLZtY4wJZQkiRCAY5yQIO5PJGGPsSupQUcFY/LuaKK+uARLbZZ033ngj/fv333M/iNtvvx0RYfbs2ezYsYP6+np+85vfcOaZZ7bL9owxpr30qASx5G83srNwcYvztamRxpoq6gmwMS7YpnUmDx7F4Vff1eL86dOnc+211+5JELNmzeKNN97guuuuIykpiW3btjFx4kTOOOMMu6+0MaZT6VEJYr/EbXFTRVXb5Qt73LhxbN26lU2bNlFSUkJqaio5OTlcd911zJ49G5/Px8aNG9myZQvZ2dmHvD1jjGkvEUsQItIXeALIBpqAh1T1nmZ1TgBeBNa4Rc+r6h3uvKnAPYAf+Ieq3nmoMbX2S3+3ssLFlNf5Sek3iMSEmP3Wb4tzzjmHZ599ls2bNzN9+nRmzpxJSUkJCxYsIBAIkJeXF3aYb2OM8VIkjyAagOtVdaGIJAILRORtVV3WrN6Hqnp6aIGI+IG/A6cARcA8EXkpzLLtzh+MI6ahksrq+nZLENOnT+eHP/wh27Zt44MPPmDWrFlkZWURCAR47733WLduXbtsxxhj2lPEzmJS1WJVXehOlwPLgT5tXHwCUKiqq1W1Dnga6JBe3EBsvHMmU1X7/aIfOXIk5eXl9OnTh5ycHC688ELmz59Pfn4+M2fOZNiwYe22LWOMaS8d0gchInnAOODTMLMnicgiYBPwM1VdipNINoTUKQKOamHdM4AZAP369TvkWCM15MbixXs7xzMyMvjkk0/C1quoqGjX7RpjzMGK+HUQIpIAPAdcq6q7ms1eCPRX1THAX4H/7l4szKrCjn+hqg+par6q5mdmZh5yvP5gHAC+xloaGu2KamNMzxXRBCEiAZzkMFNVn28+X1V3qWqFO/0aEBCRDJwjhr4hVXNxjjAizhcVAH+AGKn39IpqY4zxWsQShDjniD4CLFfVu1uok+3WQ0QmuPGUAvOAISIyQESigenASwcby4EOvucPxhHja6CyquskCBtg0BjT3iLZBzEZuBhYLCIFbtkvgH4AqvoAcA7wYxFpAKqB6ep80zWIyNXAmzinuT7q9k0csGAwSGlpKenp6W2+riEQG09j5U52VNcAnX9sJFWltLSUYLBtF/cZY0xbdPt7UtfX11NUVHRA1xk01lZTW1ZChSaQlZ3W3mFGRDAYJDc3l0Ag4HUoxpgupLV7Unf7K6kDgQADBgw4oGVqd5Tw5nUn8Oi243j8o2dJTrJf5saYnsdGcw0jJjUTkrIZFLOFhUuKvQ7HGGM8YQmiBWnDxjI4ZgsLvuiQk6eMMabTsQTRgqzD8+kTXUbBwkKvQzHGGE9YgmhB8mFjAdj0xfzWKxpjTDdlCaIFKYeNAyCpcg3rN5Z5G4wxxnjAEkQLYlIz8afmMCRmCx/N27D/BYwxppuxBNGKzFFHMSy2mI/mr/c6FGOM6XCWIFqRPuooMqN28cW8JV6HYowxHc4SRCvSRjojjDdt+ILyilqPozHGmI5lCaIVyYNHQ1QMQ2M2MndhkdfhGGNMh7IE0QpfIJrkw8YxLGj9EMaYnscSxH5kjpnEoOBW5s77yutQjDGmQ1mC2I+0kUcRRSMlSxbQ0NDodTjGGNNhLEHsR+rICQD0Zz2LV2z1OBpjjOk4liD2IyYlg+jsAQwLbrJ+CGNMj2IJog16jTmakXHFfPSZJQhjTM9hCaIN0g4/ikRfFUs/+9zu/WyM6TEsQbRBqnvBXEZVIcu+LPE4GmOM6RgRSxAi0ldE3hOR5SKyVESuCVPnQhH5wn18LCJjQuatFZHFIlIgIp6OuZ3Yfyi+uCSGBTfy7kervQzFGGM6TCSPIBqA61V1ODARuEpERjSrswY4XlVHA78GHmo2/0RVHdvSDbU7ivh8ZIyayLikYt6ds8bLUIwxpsNELEGoarGqLnSny4HlQJ9mdT5W1R3u07lAbqTiOVQZ44+nl2xj0WeL7XoIY0yP0CF9ECKSB4wDPm2l2uXA6yHPFXhLRBaIyIxW1j1DROaLyPySksj1D2SOPwGAgU2FzLf7VBtjeoCIJwgRSQCeA65V1V0t1DkRJ0HcGFI8WVXHA9NwmqeOC7esqj6kqvmqmp+ZmdnO0e+VNHAkUUlpjI5db81MxpgeIaIJQkQCOMlhpqo+30Kd0cA/gDNVtXR3uapucv9uBV4AJkQy1v0Rn4+s8SdwRNJG3p1j4zIZY7q/SJ7FJMAjwHJVvbuFOv2A54GLVfXLkPJ4EUncPQ1MATy/a0/G+ONJZidrv1hEdXW91+EYY0xERUVw3ZOBi4HFIlLglv0C6Aegqg8AtwLpwH1OPqHBPWOpF/CCWxYF/FtV34hgrG2SOf54AIZHreWj+ev5xrGDPI7IGGMiJ2IJQlXnALKfOj8AfhCmfDUw5utLeCuu9wCCvfoxpnID78xZbQnCGNOt2ZXUB0BEyDriBMYmFPHO7EKvwzHGmIiyBHGAMsYfT1Cr2blqERuLw56UZYwx3YIliAOUMc7phxgdu55X3v1yP7WNMabrsgRxgIJpWSQOGMHEtE28/M5Kr8MxxpiIsQRxELImnMIQ/zo+/mgFVdV1XodjjDERYQniIGQfPQ2fNjLc/xXvfGijuxpjuidLEAchdeQEAompTE5Zy8vvWD+EMaZ7sgRxEHz+KHpN/Cb5CWt57d0VNDU1eR2SMca0O0sQByn76GkEGytI2fUlC74o9jocY4xpd5YgDlLmkScjUQEmJKy2s5mMMd2SJYiDFIhPIn3MMRyXtp4X37IEYYzpfixBHILso6eR3rSVksIVrCiM3M2KjDHGC5YgDkH20dMAmBC/mmdeXupxNMYY074sQRyCuOz+JA4YwSk5G3n6pSWoqtchGWNMu7EEcYhyjjmN3IbVFK9ZzxfLt3gdjjHGtBtLEIco5/hvI9rEpMSvePolz296Z4wx7cYSxCFKGjiS+NxBnN5ngzUzGWO6FUsQh0hE6H3cWeTWraJ0YzGfFWz0OiRjjGkXliDaQc7xZyLayDHJX/H0i9bMZIzpHiKWIESkr4i8JyLLRWSpiFwTpo6IyL0iUigiX4jI+JB5U0VkpTvvpkjF2R6Sh4whod9hnNVnDc+8vISGhkavQzLGmEMWySOIBuB6VR0OTASuEpERzepMA4a4jxnA/QAi4gf+7s4fAVwQZtlOQ0ToO+UCsmtW0bS9iDc/+MrrkIwx5pBFLEGoarGqLnSny4HlQJ9m1c4EnlDHXCBFRHKACUChqq5W1Trgabdup9XnG+eBCKf2KuTRZz73OhxjjDlkHdIHISJ5wDjg02az+gAbQp4XuWUtlYdb9wwRmS8i80tKvBvuIq5XXzLGHsc301by0tsr2LqtwrNYjDGmPUQ8QYhIAvAccK2q7mo+O8wi2kr51wtVH1LVfFXNz8zMPLRgD1HulOnEVm9hcNRGnnz+C09jMcaYQxXRBCEiAZzkMFNVnw9TpQjoG/I8F9jUSnmn1vu4M/AH4zh/wDoeeeZzuybCGNOlRfIsJgEeAZar6t0tVHsJuMQ9m2kisFNVi4F5wBARGSAi0cB0t26nFhWXSM6x32KsLGbVKrsmwhjTtUXyCGIycDFwkogUuI9TReQKEbnCrfMasBooBB4GrgRQ1QbgauBNnM7tWaraJYZLzT1lOr66Co5JWccjTy/0OhxjjDlo0p2aQfLz83X+/PmexqCNjbxz4WjWVSZy3aoz2DjvpyQlBj2NyRhjWiIiC1Q1P9w8u5K6nYnfT//Tv0dWxTKS6zbzxHOLvA7JGGMOiiWICOh36iVIVIBLB33F3x77jKamJq9DMsaYA2YJIgKCaVn0Pu4MJvg+Z+3qzbzz4WqvQzLGmANmCSJC8s78IVJXwWk5a/jrY595HY4xxhwwSxARkjZqEokDRnBO9jJefXclq9dt9zokY4w5IJYgIkREyDvjcuJ3rWZo7Fbue2Ke1yEZY8wBsQQRQbmnnE9UXCI/HlbII898TkVlrdchGWNMm1mCiKBAfBL9T7+MvIr5BCq38vC/7cI5Y0zX0aYEISLXiEiSOyTGIyKyUESmRDq47mDg2T9GRLhyeCF/euhj6uoavA7JGGPapK1HEN93R2KdAmQC3wPujFhU3UhsVi59Tjqb8Q2fUra1hH//d7HXIRljTJu0NUHsHn77VOCfqrqI8ENymzAGnff/oL6a7w1ZzV33f2QXzhljuoS2JogFIvIWToJ4U0QSAfuWa6PkwaPIzD+Jk2PmUVi4mZff/tLrkIwxZr/amiAuB24CjlTVKiCA08xk2mjw9GvwVZVyTt467rxvjt0rwhjT6bU1QUwCVqpqmYhcBPwPsDNyYXU/GeNPIPmwcZyb+hnzFq7j3Tk2/IYxpnNra4K4H6gSkTHAz4F1wBMRi6obEhGGXnoTUeXFfKfvWn75x/fsKMIY06m1NUE0qPNtdiZwj6reAyRGLqzuqdekqSQfNo7pGc5RxBvvF3odkjHGtKitCaJcRG7GuUPcqyLix+mHMAdARBh6mXMUcU7/ddxqRxHGmE6srQnifKAW53qIzUAf4A8Ri6ob6zVxKilDx3F+2qd8/sUGXn57pdchGWNMWG1KEG5SmAkki8jpQI2qWh/EQXD6Im7GX17M+XlrufVP79l1EcaYTqmtQ22cB3wGnAucB3wqIufsZ5lHRWSriCxpYf4NIlLgPpaISKOIpLnz1orIYneetzeZjoCsid8kdXg+56Z8wvLlRcx6eanXIRljzNe0tYnpFpxrIC5V1UuACcAv97PMY8DUlmaq6h9UdayqjgVuBj5Q1dCbJpzozg97M+2uTEQYPuMOfBVb+eFhhfzi9+9SW2tjNBljOpe2Jgifqm4NeV66v2VVdTbQ1rvkXAA81ca63ULG2GPoNfGbTIn6kG1Fxdz/L7tfhDGmc2lrgnhDRN4UkctE5DLgVeC19ghAROJwjjSeCylW4C0RWSAiM/az/AwRmS8i80tKStojpA4z/Ie3Q10l149aya/vmU3ZzmqvQzLGmD3a2kl9A/AQMBoYAzykqje2UwzfAj5q1rw0WVXHA9OAq0TkuFZie0hV81U1PzMzs51C6hhJA0fS95vfZVzth0RVbOau+z/yOiRjjNmjzTcMUtXnVPWnqnqdqr7QjjFMp1nzkqpucv9uBV7A6fPoloZ97xZ8Pj+/HLuUv/xjLus3lnkdkjHGAPtJECJSLiK7wjzKRWTXoW5cRJKB44EXQ8ri3dFiEZF4nHtQhD0TqjuIzcpl0HlX069sLsNjNnD9r9/yOiRjjAH239GcqKpJYR6JqprU2rIi8hTwCTBURIpE5HIRuUJErgip9m3gLVWtDCnrBcwRkUU4p9a+qqpvHNzL6xqGfPd6YrNyuXHwXJ5/dQnvfPiV1yEZYwzSnYZ6yM/P1/nzu+ZlE5vef4H5v7qUZxtOZ17U0Sx68wqio6O8DssY082JyIKWLidocx+Eiayc488iY9xxnJMwm42rN3Dvo596HZIxpoezBNFJiAiH/+QPSF0lt4xewq/+8gEbiw+5m8cYYw6aJYhOJGnAcAZ850cMr5xDX9nET25tl0tNjDHmoFiC6GSGXnoz0SkZ3DpyHv99YznPv77M65CMMT2UJYhOJpCQzIgZdxBXupzvDdvA1f/zml1hbYzxhCWITqjvlAtIHz2Zs6LfpmbHVm783Tteh2SM6YEsQXRC4vMx+vp7kPpqfj9hMQ/NXMD7n6zxOixjTA9jCaKTSux3GEMuvJ6sLR9x+oBtfO/6FymvqPU6LGNMD2IJohMbfMFPSeh3GD/KeIfNG0v42W9sGA5jTMexBNGJ+aNjGPOzv9K0YxN/Pu5LHpq5gDffL/Q6LGNMD2EJopNLHzWJgedcRe+iNzlzyA4uv+FFdpTZWU3GmMizBNEFDP/hbST2H8YPEl+hcvs2fvDzl+hOY2gZYzonSxBdgD86yPhbHkYrd/DXyYt5/vXl/O2xz7wOyxjTzVmC6CKSh4xh6GU3k7RhNtdN3MH1v36TeQUbvQ7LGNONWYLoQgZfcB1poyZxcsUsRveq47wr/2NXWRtjIsYSRBfi80dxxP88gi86mjsGvc3m4u18/2cvWn+EMSYiLEF0MbFZuYz7+f00bFzOg1NW88IbK7jnkbleh2WM6YYsQXRB2ZNPZeDZPybly5f4f5MrueF/3+aDT9Z6HZYxppuJWIIQkUdFZKuILGlh/gkislNECtzHrSHzporIShEpFJGbIhVjVzZ8xh2kDBvPlJ1PMql/PedcMYu1G3Z4HZYxphuJ5BHEY8DU/dT5UFXHuo87AETED/wdmAaMAC4QkRERjLNL8kfHcOQdM/HHxnFz9osEGis58/Knqayq8zo0Y0w3EbEEoaqzge0HsegEoFBVV6tqHfA0cGa7BtdNxGb24chfPUnDtiIePHoeS1du4bKf/pempiavQzPGdANe90FMEpFFIvK6iIx0y/oAG0LqFLllJoz0UZM4/Ce/R1fN4R+nFfHsq8u47U/vex2WMaYb8DJBLAT6q+oY4K/Af91yCVO3xfM4RWSGiMwXkfklJSXtH2UXkHfG5fQ/43LSls/iVyeX8Zt7Z/PEswVeh2WM6eI8SxCquktVK9zp14CAiGTgHDH0DamaC2xqZT0PqWq+quZnZmZGNObOSkQY9f/+QNaEbzBuw+Ncll/LD37+ErPnrvU6NGNMF+ZZghCRbBERd3qCG0spMA8YIiIDRCQamA685FWcXYXPH8URtz5GYt5wzql7gkn96vj2D59h5VfbvA7NGNNFRfI016eAT4ChIlIkIpeLyBUicoVb5RxgiYgsAu4FpqujAbgaeBNYDsxS1aWRirM7CcQncdTvZhGIS+Cm9GdJi6pg2iVPsnlrudehGWO6IOlOwzTk5+fr/PnzvQ7Dc2VfFvDRNdPwZeRx4WdTGDCoN+/PuozEhBivQzPGdDIiskBV88PN8/osJhMBKYeN5YhbH6V+03IeO2EBi5dt4twrZlFf3+h1aMaYLsQSRDeVPWkao66+C76czb9OX8ubHxQy48aXbWA/Y0ybWYLoxgZ8+0cMPPdqYpe+wP2nbeGx/xRw6x/f8zosY0wXYQmimxt5xW/InXIBvVf+m1+fVMpv7p3Ng09aP40xZv8sQXRz4vMx9oa/0WvSVEZveIKrj9rFlbe8yktvrfA6NGNMJ2cJogfwRQXIv+1x0g6fyJSdj3POiHKmX/Uscxdu2P/CxpgeyxJED+GPieWo3z5DYr+hXKxPcnT2dqZdMpOCpcVeh2aM6aQsQfQggYQUJv7+eWKzenNtwlOMTtzMNy54giUrtngdmjGmE7IE0cME07OZfPerxGZkc0PyMwwPFnPyBU+worBnDnRojGmZJYgeKJiRw+Q/v0ZsZjY3ps9iUNQGTjr/cQrXlHodmjGmE7EE0UMFM3I4+u5Xic3oxc0Z/6Ef6zhp+uN221JjzB6WIHqw2MzeHH33q8RlZHNLxn/oX7eSE89/nA2bdnodmjGmE7AE0cPFZvZm8l9eJzF3IDekP8vg6oUcf+4/rbnJGGMJwrgd1/e8RtrII/lJ6ouMr/uYyd95lIWLW7xPkzGmB7AEYQDnFNhJv3+BXpOmcknCG5wVP4cTzvsn//fRaq9DM8Z4xBKE2cMfE8uRv3qS3CkXcFrgPa7JeY/TL3mC/7xi92sypieK8joA07n4ogKMu/F+YjP7wMw/ctfAHVx+dTVri87gZz86GvcuscaYHsCOIMzXiM/H8B/cyribHySPddx32PPc8/tnOPeKWZRX1HodnjGmg1iCMC3qO+UCjr77ZTLiG/nroFls+vBlJnzrYbvq2pgeImIJQkQeFZGtIrKkhfkXisgX7uNjERkTMm+tiCwWkQIRsZsXeCh91CSOf3A26YOHcVOvlziu+lUmnP4gz722zOvQjDERFskjiMeAqa3MXwMcr6qjgV8DDzWbf6Kqjm3pZtqm48Rm5TL5njfod+olnBb7Ef+b+xxXXPUIN/72bRoa7D7XxnRXEUsQqjob2N7K/I9Vdfe4DnOB3EjFYg6dPzrI2Bv+xtgb72dgYDMPDJrJR/96lG9e9CQlpZVeh2eMiYDO0gdxOfB6yHMF3hKRBSIyo7UFRWSGiMwXkfklJdY2Hmn9pl7I8f+YQ9ZhI/h59quMWf0Ak6bdy7tz7HoJY7obUdXIrVwkD3hFVQ9vpc6JwH3AMapa6pb1VtVNIpIFvA38xD0iaVV+fr7On29dFh2hqaGeL5+4iy+f/COlTcncs+kkjpt+Lnfe/A3iYqO9Ds8Y00YisqClpnxPjyBEZDTwD+DM3ckBQFU3uX+3Ai8AE7yJ0LTEFxVg2Pf/h8n3vEHf3DTu6PMcgddu59ipf+LTz4u8Ds8Y0w48SxAi0g94HrhYVb8MKY8XkcTd08AUIOyZUMZ76aMmcuKjcxl62c0cn/IVN8ifue3ia7jpt29SVV3ndXjGmEMQydNcnwI+AYaKSJGIXC4iV4jIFW6VW4F04L5mp7P2AuaIyCLgM+BVVX0jUnGaQ+ePjmHopTdz4qOfkDNqPFdmvk36yz/h9FNu4o33VnkdnjHmIEW0D6KjWR+E91SVDW/+m0X33YqWl/Bh+VC2j/0+v/nfi8jpleh1eMaYZjptH4TpfkSEflMvZNozixh04Q1MTlnDaYU389szzuDPf36Z2toGr0M0xrSRJQgTEVGxCYz8wS/55lOLyDhxOifFfU7ufy/lhlPOYNasj+lOR67GdFeWIExExWb24bjbHmDKkwuJG/tNTvJ/ROPfzuCmaWfz4fuLvA7PGNMKSxCmQ8T3Gchp9zzFCQ9/RNTgiUyqeYfi207kjtPP4uP3F3odnjEmDEsQpkOlDD6ccx99haMf+JjaAcczquI9im8/mbtOn8ZHr77rdXjGmBB2FpPxVMlXK3ntt7cS/9XbREsDxTGDGHbuFRxz0SX4Y2K9Ds+Ybq+1s5gsQZhOYXvxZp793Z34Cp4ny19GDUGiRk3hmO//mMwxdic7YyLFEoTpMnburOKpvz7GxreeYpQsJehroDahN4Omnc+gKWeTNGiUJQtj2pElCNPlNDY28errBbz98MP02jybw2OL8IniS8ul//GnkZl/EhljjyEqzi6+M+ZQWIIwXdqSFVt48OF3WP3uixwRvZLRcUVESz34o0gbcSSZR5xIZv6JpAw7Ap8/yutwjelSLEGYbqG8opb/vLKUf82aT+mSuYyNW8+xmcVkNRQhKP5gPKnD80k7fAKpI48idcSRRCemeh22MZ2aJQjT7RSuKeWJ5xbxn1eXsXH1BkbHreekvmUcnrCFYNlq0CYAEvOGkzriSFKGjidl2HiSBo7EFxXwOHpjOg9LEKZbW76qhBfeWM7zry9nweJiglLHyYOqObl/OYP8G4jaupyGijIAfIEYkgYdTsqw8aQMHU/qsCNI6DsE8fu9fRHGeMQShOkx1hWV8d83V/DG+4XM/nQdVdX1+P1wyuhYpgyuZUTCVuLKCtm1ahGNNc69tP2xCaQMGeMmjXGkDB1PXO8BdraU6REsQZgeqba2gbkLi3hnzmre/vAr5i3aRFOTEhcbYPIRfTh5uI8xqdvJqltP5VcF7CxcTFN9LQCBpFRSDhu3p2kqZeh4ghk5ljRMt2MJwhigbGc173+ylnfmrGbOvPV8sXwLquD3C+MPz+HYI3ozIbeW/v6NxGz7kp2rCihfvRRtagQgJq0XKcPGkzxoFAn9DiOh7xAS+g0hKjbB41dmzMGzBGFMGDt31fDxgg3M+Ww9c+at59OCImprnWQQFxtgzIhejB+aRn52BXn+TcTvKqR8VQEVRYXQ1LRnPcHMPm7CGExiv8P2JI9gZh874jCdniUIY9qgrq6BZatKKFi6mc+XbqZg6WYKlm1mV7nT7OT3C8MGZXDEiAyO7NfIYcmV9JJtNJasoWLDKio2rKKhctee9fmD8cT3HkBc7zz37wDic/KI6zOAuKy++ALRXr1UY/awBGHMQWpqamLthjI+X7qZz5cUU7BsM58v2cymLeV76vTrk8ywQRkMyUtleI4wIH4XmZQQU15E9ea1VG1aS2XxWprqavau2OcjNjOXuJz+xGX3Iy7b/ZuTR1x2P4LpOXZmlekQniQIEXkUOB3YqqqHh5kvwD3AqUAVcJmqLnTnTXXn+YF/qOqdbdmmJQjTUbZuq9hzhFGwdDNfri5l1drte442AAIBHwP7pXLYgHSG5KUyJFPpG1dOhmwnrmYrdSXrqdq8nuot66nZVrzP+iUqQGxWLnHZ/YnN7E0wszexmX2cvxm9CWb2ITo53ZqwzCHzKkEcB1QAT7SQIE4FfoKTII4C7lHVo0TED3wJnAIUAfOAC1R12f62aQnCeElV2bqt0kkWa0r5ck0pq9Zsd5NH6Z7+jd16ZcYzoG8qebkpDOwdx8DUWvoEK0mTHcTWllBXssFJICWbqC3dvKezfDdfIIZgZg7BjL1JIzazt/M803keTOtlRyKmVa0liIgNXKOqs0Ukr5UqZ+IkDwXmikiKiOQAeUChqq4GEJGn3br7TRDGeElE6JWZQK/MBI49qv8+85qamti8tYK1RWWs2VDG2g1lrNmwg7VFZXxWsJFnX9tJQ0NTyLp89MkeRV7usfTtnUTu6Hj6pzSRE1tFelQFSbqTQE0ptds2UVOyiR0rFlDz4ct7TtPdw+cjmNaLmNQsYlIz3b9ZRKdm7vM8JjWLmOR0SyZmH16ObNYH2BDyvMgtC1d+VEsrEZEZwAyAfv36tX+UxrQDn89H7+wkemcncXT+1z+njY1NbNy8y00cZU4iWb83gTy/edfXjkD8/ihyskaSmzOJ3Jwkcgcn0jdN6R1bTaq/nMSmnQTrtiMVJdSVlVC7Yyvla1dQu2MrTfV1Xw9ShOjk9JCk4SaQtCxiUjK/9tw62bs/LxNEuMZTbaU8LFV9CHgInCam9gnNmI7l9/vo1yeFfn1SOG7i1+erKqU7qigq3sXGzeUUFe/a+9i8iyUrt/L6e6uorKpvtqQQCGTTK2MwvTLiyc5KILtvPH1SfWTH15EZrCU1qooEKgg27EIrS6nbUUJtWQk7ls+jdnvJnivOmwskpOx7FJLmTEcnpxNITCU6KY3opFRnOjkNfzDe+ky6GC8TRBHQN+R5LrAJiG6h3JgeS0TISIsnIy2esSNzwtZRVXaV17K5pILNWyucv+5ji/t305ZyFi4uZmtpJY2NX/89FRvMIjtrINmZCWSmxZM6LEhaAmTG1JIWqCLJV0W8lhPbsItA3U581TtorCxl5+ol1C0ood4d8yocXyDaSRaJqQSSnATiJJJ9pwNuYtld5g/GWWLxiJcJ4iXgareP4Shgp6oWi0gJMEREBgAbgenAdz2M05guQURITgqSnBRk6KCMVus2NTVRuqO6xUSyucTpLylYVsOOndWUVzRvkooBstwHREf7SU0Okp4URe/EJrLiG8mIrSctpp7kQC2J/hripYpgUxWNjZXU1eyiqmw1WrWT+oodNNVWtxjr7sQSSEgmkJBMVHySO51CwJ2OSkjeMx1ISCEqPomouAT3kWj3CTlIEdtrIvIUcAKQISJFwG1AAEBVHwBewzmDqRDnNNfvufMaRORq4E2c01wfVdWlkYrTmJ7I5/ORmR5PZno8o4b32m/9hoZGynbVULazhh07naSxY2cNZbvCT68sq+bTohq3XGhqigGSW4hFyEj00TsZchIbyYxvICVQT1JUNQm+GuKlmlitIqapmkBZNYFtm/DVr8JXVwk1u6CxebNamG1EB/cmjNjEFqadZPK16Wb1/MF4xOc70F3eJdmFcsaYiGpqaqKism7fxBIyvWNntZtc9k5XVNZRUVVHZVU9le7flgSkgThfLQm+WuJ9tcT7a0mMqiM52ERydCNJ0Q0kBBqI99cT568n1ldHjNQRo7UEtIaophr8DdX4GmqQlrs79+EPxu8/ycQl4I9NICoYhz8mFv/X/sYTFRuHPxjvPI+J9STxeHKaqzHGgHO0kpQYJCkxSP/clINaR1NTE9U1DXuSRWVVHZXV9VRU1u0tq65zn++dX1lVR2llHeur9yYaJ/HsrVdd0wCAoMSIk0Bifbv/1hErzt+gWxbnrycxqoGEQD1x/gbi/FXE+XYSlDqCUks0tURrLQENc6bY/gSCSEwcvphY/NFx+INxRMXGEYiNdx7x8UTFxuOPicMfjHX+xgQJJKbQ95TpB7VvW2MJwhjT6fl8PuLjoomPa/9Taxsbm6gKSSCV1W4i2Z183HkVlU4yqal1HtU19eysDX2+d7qmtoGa6lqa6qrQ2hqa6qqhvgapryHGV0+MNBDjqyco9SF/G4iReoLufOfvToK+bfvUD/rqifY1ECMNe15DhSTxXUsQxhjTvvx+H4kJMSQmxER8W6pKXV0j1TX1+ySW6pp6ausaqa1roCYk0dTWNe6ZrqhtoDRkfm1tPXU1NTRUVxEfE5kzeSxBGGNMBxERYmKiiInpGl+9PaMr3hhjzAGzBGGMMSYsSxDGGGPCsgRhjDEmLEsQxhhjwrIEYYwxJixLEMYYY8KyBGGMMSasbjVYnztU+LqDXDwD2NaO4bQXi+vAddbYLK4DY3EduIOJrb+qZoab0a0SxKEQkfktjWjoJYvrwHXW2CyuA2NxHbj2js2amIwxxoRlCcIYY0xYliD2esjrAFpgcR24zhqbxXVgLK4D166xWR+EMcaYsOwIwhhjTFiWIIwxxoTV4xOEiEwVkZUiUigiN3kYR18ReU9ElovIUhG5xi2/XUQ2ikiB+zjVo/jWishiN4b5blmaiLwtIqvcv6kdHNPQkP1SICK7RORaL/aZiDwqIltFZElIWYv7R0Rudj9zK0Xkmx7E9gcRWSEiX4jICyKS4pbniUh1yL57oIPjavG966h91kJcz4TEtFZECtzyjtxfLX1HRO5zpqo99gH4ga+AgUA0sAgY4VEsOcB4dzoR+BIYAdwO/KwT7Ku1QEazst8DN7nTNwF3efxebgb6e7HPgOOA8cCS/e0f931dBMQAA9zPoL+DY5sCRLnTd4XElhdaz4N9Fva968h9Fi6uZvP/BNzqwf5q6TsiYp+znn4EMQEoVNXVqloHPA2c6UUgqlqsqgvd6XJgOdDHi1gOwJnA4+7048BZ3oXCycBXqnqwV9IfElWdDWxvVtzS/jkTeFpVa1V1DVCI81nssNhU9S1V3X3X+7lAbqS2fyBxtaLD9llrcYmIAOcBT0Vi261p5TsiYp+znp4g+gAbQp4X0Qm+lEUkDxgHfOoWXe02BTza0c04IRR4S0QWiMgMt6yXqhaD8+EFsjyKDWA6+/7TdoZ91tL+6Wyfu+8Dr4c8HyAin4vIByJyrAfxhHvvOss+OxbYoqqrQso6fH81+46I2OespycICVPm6Xm/IpIAPAdcq6q7gPuBQcBYoBjn8NYLk1V1PDANuEpEjvMojq8RkWjgDOA/blFn2Wct6TSfOxG5BWgAZrpFxUA/VR0H/BT4t4gkdWBILb13nWWfXcC+P0Q6fH+F+Y5osWqYsgPaZz09QRQBfUOe5wKbPIoFEQngvPEzVfV5AFXdoqqNqtoEPEwEmyJao6qb3L9bgRfcOLaISI4bew6w1YvYcJLWQlXd4sbYKfYZLe+fTvG5E5FLgdOBC9VttHabI0rd6QU47daHdVRMrbx3nu8zEYkCvgM8s7uso/dXuO8IIvg56+kJYh4wREQGuL9CpwMveRGI27b5CLBcVe8OKc8JqfZtYEnzZTsgtngRSdw9jdPBuQRnX13qVrsUeLGjY3Pt86uuM+wzV0v75yVguojEiMgAYAjwWUcGJiJTgRuBM1S1KqQ8U0T87vRAN7bVHRhXS++d5/sM+AawQlWLdhd05P5q6TuCSH7OOqL3vTM/gFNxzgb4CrjFwziOwTn8+wIocB+nAv8CFrvlLwE5HsQ2EOdsiEXA0t37CUgH3gVWuX/TPIgtDigFkkPKOnyf4SSoYqAe55fb5a3tH+AW9zO3EpjmQWyFOO3Tuz9rD7h1z3bf40XAQuBbHRxXi+9dR+2zcHG55Y8BVzSr25H7q6XviIh9zmyoDWOMMWH19CYmY4wxLbAEYYwxJixLEMYYY8KyBGGMMSYsSxDGGGPCsgRhTCcgIieIyCtex2FMKEsQxhhjwrIEYcwBEJGLROQzd+z/B0XELyIVIvInEVkoIu+KSKZbd6yIzJW991xIdcsHi8g7IrLIXWaQu/oEEXlWnPs0zHSvnDXGM5YgjGkjERkOnI8zcOFYoBG4EIjHGQtqPPABcJu7yBPAjao6Gufq4N3lM4G/q+oY4Gicq3bBGZ3zWpxx/AcCkyP8koxpVZTXARjThZwMHAHMc3/cx+IMjNbE3gHcngSeF5FkIEVVP3DLHwf+445p1UdVXwBQ1RoAd32fqTvOj3vHsjxgTsRflTEtsARhTNsJ8Liq3rxPocgvm9Vrbfya1pqNakOmG7H/T+Mxa2Iypu3eBc4RkSzYcy/g/jj/R+e4db4LzFHVncCOkBvIXAx8oM74/UUicpa7jhgRievIF2FMW9kvFGPaSFWXicj/4NxZz4cz2udVQCUwUkQWADtx+inAGXr5ATcBrAa+55ZfDDwoIne46zi3A1+GMW1mo7kac4hEpEJVE7yOw5j2Zk1MxhhjwrIjCGOMMWHZEYQxxpiwLEEYY4wJyxKEMcaYsCxBGGOMCcsShDHGmLD+Pw9ZEJpoGKSjAAAAAElFTkSuQmCC
"/>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=e2a56f69-fcfc-4762-9fdb-dae93337b1f3">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>The Neural Network model we have trained, has the scores of:</p>
<ul>
<li>Accuracy: 0.59</li>
<li>Precision (weighted): 0.56</li>
<li>Recall (weighted): 0.59</li>
</ul>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell" id="cell-id=71a20889-f45a-4a47-b1dd-ed97130c5fad">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [20]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="n">y_predict</span> <span class="o">=</span> <span class="n">nnModel</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">X_test</span><span class="p">)</span>
<span class="n">y_predict_num</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">argmax</span><span class="p">(</span><span class="n">y_predict</span><span class="p">,</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>

<span class="c1"># Got this code from https://machinelearningmastery.com/how-to-calculate-precision-recall-f1-and-more-for-deep-learning-models/</span>
<span class="c1"># accuracy: (tp + tn) / (p + n)</span>
<span class="n">accuracy</span> <span class="o">=</span> <span class="n">accuracy_score</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">y_predict_num</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">'Accuracy: </span><span class="si">%f</span><span class="s1">'</span> <span class="o">%</span> <span class="n">accuracy</span><span class="p">)</span>
<span class="c1"># precision tp / (tp + fp)</span>
<span class="n">precision</span> <span class="o">=</span> <span class="n">precision_score</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">y_predict_num</span><span class="p">,</span> <span class="n">average</span><span class="o">=</span><span class="s1">'weighted'</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">'Precision: </span><span class="si">%f</span><span class="s1">'</span> <span class="o">%</span> <span class="n">precision</span><span class="p">)</span>
<span class="c1"># recall: tp / (tp + fn)</span>
<span class="n">recall</span> <span class="o">=</span> <span class="n">recall_score</span><span class="p">(</span><span class="n">y_test</span><span class="p">,</span> <span class="n">y_predict_num</span><span class="p">,</span> <span class="n">average</span><span class="o">=</span><span class="s1">'weighted'</span><span class="p">)</span>
<span class="nb">print</span><span class="p">(</span><span class="s1">'Recall: </span><span class="si">%f</span><span class="s1">'</span> <span class="o">%</span> <span class="n">recall</span><span class="p">)</span>
</pre></div>
</div>
</div>
</div>
</div>
<div class="jp-Cell-outputWrapper">
<div class="jp-Collapser jp-OutputCollapser jp-Cell-outputCollapser">
</div>
<div class="jp-OutputArea jp-Cell-outputArea">
<div class="jp-OutputArea-child">
<div class="jp-OutputPrompt jp-OutputArea-prompt"></div>
<div class="jp-RenderedText jp-OutputArea-output" data-mime-type="text/plain" tabindex="0">
<pre>Accuracy: 0.593750
Precision: 0.559540
Recall: 0.593750
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell" id="cell-id=cc93c002">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h3 id="Conclusion">Conclusion<a class="anchor-link" href="#Conclusion">¶</a></h3><p>The scores of our regression models:</p>
<ul>
<li>Random Forest scores:<ul>
<li>R^2: 0.52</li>
<li>RMSE: 0.56</li>
<li>MAE: 0.43</li>
</ul>
</li>
<li>Gradient Boosting scores:<ul>
<li>R^2: 0.49</li>
<li>RMSE: 0.58</li>
<li>MAE: 0.45</li>
</ul>
</li>
</ul>
<p>The scores of our classification model (NN):</p>
<ul>
<li>Accuracy: 0.59</li>
<li>Precision: 0.56</li>
<li>Recall: 0.59</li>
</ul>
<p>By comparing the performance scores, we can conclude that the Neural Network model performs much better than the other two regression models. Since the <code>wine quality</code> dataset contains lots of features and moderate correlations between many of the features, the relationships between different attributes of the dataset is hard to obtain and regression models are not good at finding complex relationships. But, the Neural Network models can be very useful to obtain these relationships as they are very good at very complex tasks. However, the Neural Network models need a very large amount of data which we do not have and due to that our classification model's performance scores were not as high as it could have been.</p>
</div>
</div>
</div>
</div>
</main>
</body>
</html>

</details>