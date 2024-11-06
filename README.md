<!DOCTYPE html>

<html lang="en">
<head><meta charset="utf-8"/>
<meta content="width=device-width, initial-scale=1.0" name="viewport"/>
<title>DO_DOAN_BINH_MINH_MINH_3_Notebook_Pima_Indians_Diabetes_Analysis_Template (2)</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>
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
    const mermaid = (await import("https://cdnjs.cloudflare.com/ajax/libs/mermaid/10.7.0/mermaid.esm.min.mjs")).default;
    const parser = new DOMParser();

    mermaid.initialize({
      maxTextSize: 100000,
      maxEdges: 100000,
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
        let { svg } = await mermaid.render(id, raw, el);
        svg = cleanMermaidSvg(svg);
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


    /**
     * Post-process to ensure mermaid diagrams contain only valid SVG and XHTML.
     */
    function cleanMermaidSvg(svg) {
      return svg.replace(RE_VOID_ELEMENT, replaceVoidElement);
    }


    /**
     * A regular expression for all void elements, which may include attributes and
     * a slash.
     *
     * @see https://developer.mozilla.org/en-US/docs/Glossary/Void_element
     *
     * Of these, only `<br>` is generated by Mermaid in place of `\n`,
     * but _any_ "malformed" tag will break the SVG rendering entirely.
     */
    const RE_VOID_ELEMENT =
      /<\s*(area|base|br|col|embed|hr|img|input|link|meta|param|source|track|wbr)\s*([^>]*?)\s*>/gi;

    /**
     * Ensure a void element is closed with a slash, preserving any attributes.
     */
    function replaceVoidElement(match, tag, rest) {
      rest = rest.trim();
      if (!rest.endsWith('/')) {
        rest = `${rest} /`;
      }
      return `<${tag} ${rest}>`;
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
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h1 id="Foundations-of-Data-Science-Project---Diabetes-Analysis">Foundations of Data Science Project - Diabetes Analysis<a class="anchor-link" href="#Foundations-of-Data-Science-Project---Diabetes-Analysis">¶</a></h1><hr/>
<h2 id="Context">Context<a class="anchor-link" href="#Context">¶</a></h2><hr/>
<p>Diabetes is one of the most frequent diseases worldwide and the number of diabetic patients are growing over the years. The main cause of diabetes remains unknown, yet scientists believe that both genetic factors and environmental lifestyle play a major role in diabetes.</p>
<p>A few years ago research was done on a tribe in America which is called the Pima tribe (also known as the Pima Indians). In this tribe, it was found that the ladies are prone to diabetes very early. Several constraints were placed on the selection of these instances from a larger database. In particular, all patients were females at least 21 years old of Pima Indian heritage.</p>
<hr/>
<h2 id="Objective">Objective<a class="anchor-link" href="#Objective">¶</a></h2><hr/>
<p>Here, we are analyzing different aspects of Diabetes in the Pima Indians tribe by doing Exploratory Data Analysis.</p>
<hr/>
<h2 id="Data-Dictionary">Data Dictionary<a class="anchor-link" href="#Data-Dictionary">¶</a></h2><hr/>
<p>The dataset has the following information:</p>
<ul>
<li>Pregnancies: Number of times pregnant</li>
<li>Glucose: Plasma glucose concentration over 2 hours in an oral glucose tolerance test</li>
<li>BloodPressure: Diastolic blood pressure (mm Hg)</li>
<li>SkinThickness: Triceps skin fold thickness (mm)</li>
<li>Insulin: 2-Hour serum insulin (mu U/ml)</li>
<li>BMI: Body mass index (weight in kg/(height in m)^2)</li>
<li>DiabetesPedigreeFunction: A function that scores the likelihood of diabetes based on family history.</li>
<li>Age: Age in years</li>
<li>Outcome: Class variable (0: a person is not diabetic or 1: a person is diabetic)</li>
</ul>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q-1:-Import-the-necessary-libraries-and-briefly-explain-the-use-of-each-library-(3-Marks)">Q 1: Import the necessary libraries and briefly explain the use of each library (3 Marks)<a class="anchor-link" href="#Q-1:-Import-the-necessary-libraries-and-briefly-explain-the-use-of-each-library-(3-Marks)">¶</a></h2>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [50]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate library name</span>

<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>

<span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>

<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>

<span class="kn">import</span> <span class="nn">matplotlib.pyplot</span> <span class="k">as</span> <span class="nn">plt</span>


<span class="o">%</span><span class="k">matplotlib</span> inline
</pre></div>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Write-your-Answer-here:">Write your Answer here:<a class="anchor-link" href="#Write-your-Answer-here:">¶</a></h4><p>seaborn create chart
matplot create chart
numpy caculate number
pandas analyze data</p>
</div>
</div>
</div>
</div>Ans 1:<div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [19]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>

<span class="n">file_id</span> <span class="o">=</span> <span class="s2">"1Yc4C_HsrPcsjZKpH0nNdfGT8slrCLzGj"</span>
<span class="n">url</span> <span class="o">=</span> <span class="sa">f</span><span class="s2">"https://drive.google.com/uc?export=download&amp;id=</span><span class="si">{</span><span class="n">file_id</span><span class="si">}</span><span class="s2">"</span>
</pre></div>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>read file from cloud</p>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q-2:-Read-the-given-dataset-(2-Marks)">Q 2: Read the given dataset (2 Marks)<a class="anchor-link" href="#Q-2:-Read-the-given-dataset-(2-Marks)">¶</a></h2>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [21]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate function name</span>
<span class="n">pima</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="n">url</span><span class="p">,</span> <span class="n">on_bad_lines</span><span class="o">=</span><span class="s2">"skip"</span><span class="p">)</span>
<span class="n">pima</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
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
<div class="jp-OutputPrompt jp-OutputArea-prompt">Out[21]:</div>
<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html" tabindex="0">
<div class="colab-df-container" id="df-1d823afd-f6b6-4950-b7d7-1f5f88b6cbd3">
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
<th>Pregnancies</th>
<th>Glucose</th>
<th>BloodPressure</th>
<th>SkinThickness</th>
<th>Insulin</th>
<th>BMI</th>
<th>DiabetesPedigreeFunction</th>
<th>Age</th>
<th>Outcome</th>
</tr>
</thead>
<tbody>
<tr>
<th>0</th>
<td>6</td>
<td>148</td>
<td>72</td>
<td>35</td>
<td>79</td>
<td>33.6</td>
<td>0.627</td>
<td>50</td>
<td>1</td>
</tr>
<tr>
<th>1</th>
<td>1</td>
<td>85</td>
<td>66</td>
<td>29</td>
<td>79</td>
<td>26.6</td>
<td>0.351</td>
<td>31</td>
<td>0</td>
</tr>
<tr>
<th>2</th>
<td>8</td>
<td>183</td>
<td>64</td>
<td>20</td>
<td>79</td>
<td>23.3</td>
<td>0.672</td>
<td>32</td>
<td>1</td>
</tr>
<tr>
<th>3</th>
<td>1</td>
<td>89</td>
<td>66</td>
<td>23</td>
<td>94</td>
<td>28.1</td>
<td>0.167</td>
<td>21</td>
<td>0</td>
</tr>
<tr>
<th>4</th>
<td>0</td>
<td>137</td>
<td>40</td>
<td>35</td>
<td>168</td>
<td>43.1</td>
<td>2.288</td>
<td>33</td>
<td>1</td>
</tr>
</tbody>
</table>
</div>
<div class="colab-df-buttons">
<div class="colab-df-container">
<button class="colab-df-convert" onclick="convertToInteractive('df-1d823afd-f6b6-4950-b7d7-1f5f88b6cbd3')" style="display:none;" title="Convert this dataframe to an interactive table.">
<svg height="24px" viewbox="0 -960 960 960" xmlns="http://www.w3.org/2000/svg">
<path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"></path>
</svg>
</button>
<style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>
<script>
      const buttonEl =
        document.querySelector('#df-1d823afd-f6b6-4950-b7d7-1f5f88b6cbd3 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-1d823afd-f6b6-4950-b7d7-1f5f88b6cbd3');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
</div>
<div id="df-8b1c5afc-269c-4afa-80ff-e80692cb3339">
<button class="colab-df-quickchart" onclick="quickchart('df-8b1c5afc-269c-4afa-80ff-e80692cb3339')" style="display:none;" title="Suggest charts">
<svg height="24px" viewbox="0 0 24 24" width="24px" xmlns="http://www.w3.org/2000/svg">
<g>
<path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"></path>
</g>
</svg>
</button>
<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>
<script>
    async function quickchart(key) {
      const quickchartButtonEl =
        document.querySelector('#' + key + ' button');
      quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
      quickchartButtonEl.classList.add('colab-df-spinner');
      try {
        const charts = await google.colab.kernel.invokeFunction(
            'suggestCharts', [key], {});
      } catch (error) {
        console.error('Error during call to suggestCharts:', error);
      }
      quickchartButtonEl.classList.remove('colab-df-spinner');
      quickchartButtonEl.classList.add('colab-df-quickchart-complete');
    }
    (() => {
      let quickchartButtonEl =
        document.querySelector('#df-8b1c5afc-269c-4afa-80ff-e80692cb3339 button');
      quickchartButtonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';
    })();
  </script>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>read csv by read url</p>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q3.-Show-the-last-10-records-of-the-dataset.-How-many-columns-are-there?-(2-Marks)">Q3. Show the last 10 records of the dataset. How many columns are there? (2 Marks)<a class="anchor-link" href="#Q3.-Show-the-last-10-records-of-the-dataset.-How-many-columns-are-there?-(2-Marks)">¶</a></h2>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [23]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove ______ and write the appropriate number in the function</span>

<span class="nb">print</span><span class="p">(</span><span class="n">pima</span><span class="o">.</span><span class="n">tail</span><span class="p">(</span><span class="mi">10</span><span class="p">))</span>
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
<pre>     Pregnancies  Glucose  BloodPressure  SkinThickness  Insulin   BMI  \
758            1      106             76             20       79  37.5   
759            6      190             92             20       79  35.5   
760            2       88             58             26       16  28.4   
761            9      170             74             31       79  44.0   
762            9       89             62             20       79  22.5   
763           10      101             76             48      180  32.9   
764            2      122             70             27       79  36.8   
765            5      121             72             23      112  26.2   
766            1      126             60             20       79  30.1   
767            1       93             70             31       79  30.4   

     DiabetesPedigreeFunction  Age  Outcome  
758                     0.197   26        0  
759                     0.278   66        1  
760                     0.766   22        0  
761                     0.403   43        1  
762                     0.142   33        0  
763                     0.171   63        0  
764                     0.340   27        0  
765                     0.245   30        0  
766                     0.349   47        1  
767                     0.315   23        0  
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>tail is read from the last rows</p>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [24]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="n">num_columns</span> <span class="o">=</span> <span class="n">pima</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">1</span><span class="p">]</span>
<span class="nb">print</span><span class="p">(</span><span class="n">num_columns</span><span class="p">)</span>
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
<pre>9
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>shapes is see how many columns are there</p>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Write-your-Answer-here:">Write your Answer here:<a class="anchor-link" href="#Write-your-Answer-here:">¶</a></h4>
</div>
</div>
</div>
</div>Ans 3:
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q4.-Show-the-first-10-records-of-the-dataset-(2-Marks)">Q4. Show the first 10 records of the dataset (2 Marks)<a class="anchor-link" href="#Q4.-Show-the-first-10-records-of-the-dataset-(2-Marks)">¶</a></h2>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [26]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate function name and the number of rows to get in the output</span>

<span class="n">pima</span><span class="o">.</span><span class="n">head</span><span class="p">(</span><span class="mi">10</span><span class="p">)</span>
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
<div class="jp-OutputPrompt jp-OutputArea-prompt">Out[26]:</div>
<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html" tabindex="0">
<div class="colab-df-container" id="df-a60c8f82-be5a-462d-ae86-47c7eff76d50">
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
<th>Pregnancies</th>
<th>Glucose</th>
<th>BloodPressure</th>
<th>SkinThickness</th>
<th>Insulin</th>
<th>BMI</th>
<th>DiabetesPedigreeFunction</th>
<th>Age</th>
<th>Outcome</th>
</tr>
</thead>
<tbody>
<tr>
<th>0</th>
<td>6</td>
<td>148</td>
<td>72</td>
<td>35</td>
<td>79</td>
<td>33.600000</td>
<td>0.627</td>
<td>50</td>
<td>1</td>
</tr>
<tr>
<th>1</th>
<td>1</td>
<td>85</td>
<td>66</td>
<td>29</td>
<td>79</td>
<td>26.600000</td>
<td>0.351</td>
<td>31</td>
<td>0</td>
</tr>
<tr>
<th>2</th>
<td>8</td>
<td>183</td>
<td>64</td>
<td>20</td>
<td>79</td>
<td>23.300000</td>
<td>0.672</td>
<td>32</td>
<td>1</td>
</tr>
<tr>
<th>3</th>
<td>1</td>
<td>89</td>
<td>66</td>
<td>23</td>
<td>94</td>
<td>28.100000</td>
<td>0.167</td>
<td>21</td>
<td>0</td>
</tr>
<tr>
<th>4</th>
<td>0</td>
<td>137</td>
<td>40</td>
<td>35</td>
<td>168</td>
<td>43.100000</td>
<td>2.288</td>
<td>33</td>
<td>1</td>
</tr>
<tr>
<th>5</th>
<td>5</td>
<td>116</td>
<td>74</td>
<td>20</td>
<td>79</td>
<td>25.600000</td>
<td>0.201</td>
<td>30</td>
<td>0</td>
</tr>
<tr>
<th>6</th>
<td>3</td>
<td>78</td>
<td>50</td>
<td>32</td>
<td>88</td>
<td>31.000000</td>
<td>0.248</td>
<td>26</td>
<td>1</td>
</tr>
<tr>
<th>7</th>
<td>10</td>
<td>115</td>
<td>69</td>
<td>20</td>
<td>79</td>
<td>35.300000</td>
<td>0.134</td>
<td>29</td>
<td>0</td>
</tr>
<tr>
<th>8</th>
<td>2</td>
<td>197</td>
<td>70</td>
<td>45</td>
<td>543</td>
<td>30.500000</td>
<td>0.158</td>
<td>53</td>
<td>1</td>
</tr>
<tr>
<th>9</th>
<td>8</td>
<td>125</td>
<td>96</td>
<td>20</td>
<td>79</td>
<td>31.992578</td>
<td>0.232</td>
<td>54</td>
<td>1</td>
</tr>
</tbody>
</table>
</div>
<div class="colab-df-buttons">
<div class="colab-df-container">
<button class="colab-df-convert" onclick="convertToInteractive('df-a60c8f82-be5a-462d-ae86-47c7eff76d50')" style="display:none;" title="Convert this dataframe to an interactive table.">
<svg height="24px" viewbox="0 -960 960 960" xmlns="http://www.w3.org/2000/svg">
<path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"></path>
</svg>
</button>
<style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>
<script>
      const buttonEl =
        document.querySelector('#df-a60c8f82-be5a-462d-ae86-47c7eff76d50 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-a60c8f82-be5a-462d-ae86-47c7eff76d50');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
</div>
<div id="df-4ff87cf1-c45a-4be9-9d7d-8610ed69feb0">
<button class="colab-df-quickchart" onclick="quickchart('df-4ff87cf1-c45a-4be9-9d7d-8610ed69feb0')" style="display:none;" title="Suggest charts">
<svg height="24px" viewbox="0 0 24 24" width="24px" xmlns="http://www.w3.org/2000/svg">
<g>
<path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"></path>
</g>
</svg>
</button>
<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>
<script>
    async function quickchart(key) {
      const quickchartButtonEl =
        document.querySelector('#' + key + ' button');
      quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
      quickchartButtonEl.classList.add('colab-df-spinner');
      try {
        const charts = await google.colab.kernel.invokeFunction(
            'suggestCharts', [key], {});
      } catch (error) {
        console.error('Error during call to suggestCharts:', error);
      }
      quickchartButtonEl.classList.remove('colab-df-spinner');
      quickchartButtonEl.classList.add('colab-df-quickchart-complete');
    }
    (() => {
      let quickchartButtonEl =
        document.querySelector('#df-4ff87cf1-c45a-4be9-9d7d-8610ed69feb0 button');
      quickchartButtonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';
    })();
  </script>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>using head to see first 5 rows
type 10 to see 10 rows</p>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q5.-What-do-you-understand-by-the-dimension-of-the-dataset?-Find-the-dimension-of-the-pima-dataframe.-(3-Marks)">Q5. What do you understand by the dimension of the dataset? Find the dimension of the <code>pima</code> dataframe. (3 Marks)<a class="anchor-link" href="#Q5.-What-do-you-understand-by-the-dimension-of-the-dataset?-Find-the-dimension-of-the-pima-dataframe.-(3-Marks)">¶</a></h2>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [25]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate function name</span>

<span class="n">pima</span><span class="o">.</span><span class="n">shape</span>
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
<div class="jp-OutputPrompt jp-OutputArea-prompt">Out[25]:</div>
<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain" tabindex="0">
<pre>(768, 9)</pre>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>there are 768 row and 9 columns</p>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Write-your-Answer-here:">Write your Answer here:<a class="anchor-link" href="#Write-your-Answer-here:">¶</a></h4>
</div>
</div>
</div>
</div>Ans 5:
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q6.-What-do-you-understand-by-the-size-of-the-dataset?-Find-the-size-of-the-pima-dataframe.-(3-Marks)">Q6. What do you understand by the size of the dataset? Find the size of the <code>pima</code> dataframe. (3 Marks)<a class="anchor-link" href="#Q6.-What-do-you-understand-by-the-size-of-the-dataset?-Find-the-size-of-the-pima-dataframe.-(3-Marks)">¶</a></h2>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [27]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate function name</span>

<span class="n">pima</span><span class="o">.</span><span class="n">size</span>
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
<div class="jp-OutputPrompt jp-OutputArea-prompt">Out[27]:</div>
<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain" tabindex="0">
<pre>6912</pre>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>count items from a given dataset</p>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Write-your-Answer-here:">Write your Answer here:<a class="anchor-link" href="#Write-your-Answer-here:">¶</a></h4>
</div>
</div>
</div>
</div>Ans 6:
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q7.-What-are-the-data-types-of-all-the-variables-in-the-data-set?-(2-Marks)">Q7. What are the data types of all the variables in the data set? (2 Marks)<a class="anchor-link" href="#Q7.-What-are-the-data-types-of-all-the-variables-in-the-data-set?-(2-Marks)">¶</a></h2><p><strong>Hint: Use the info() function to get all the information about the dataset.</strong></p>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [28]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate function name</span>

<span class="n">pima</span><span class="o">.</span><span class="n">info</span><span class="p">()</span>
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
RangeIndex: 768 entries, 0 to 767
Data columns (total 9 columns):
 #   Column                    Non-Null Count  Dtype  
---  ------                    --------------  -----  
 0   Pregnancies               768 non-null    int64  
 1   Glucose                   768 non-null    int64  
 2   BloodPressure             768 non-null    int64  
 3   SkinThickness             768 non-null    int64  
 4   Insulin                   768 non-null    int64  
 5   BMI                       768 non-null    float64
 6   DiabetesPedigreeFunction  768 non-null    float64
 7   Age                       768 non-null    int64  
 8   Outcome                   768 non-null    int64  
dtypes: float64(2), int64(7)
memory usage: 54.1 KB
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>see type of columns</p>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Write-your-Answer-here:">Write your Answer here:<a class="anchor-link" href="#Write-your-Answer-here:">¶</a></h4>
</div>
</div>
</div>
</div>Ans 7:
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q8.-What-do-we-mean-by-missing-values?-Are-there-any-missing-values-in-the-pima-dataframe?-(4-Marks)">Q8. What do we mean by missing values? Are there any missing values in the <code>pima</code> dataframe? (4 Marks)<a class="anchor-link" href="#Q8.-What-do-we-mean-by-missing-values?-Are-there-any-missing-values-in-the-pima-dataframe?-(4-Marks)">¶</a></h2>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [30]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate function name</span>

<span class="n">pima</span><span class="o">.</span><span class="n">isnull</span><span class="p">()</span><span class="o">.</span><span class="n">values</span><span class="o">.</span><span class="n">any</span><span class="p">()</span>
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
<div class="jp-OutputPrompt jp-OutputArea-prompt">Out[30]:</div>
<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain" tabindex="0">
<pre>False</pre>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>there are no missing value</p>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Write-your-Answer-here:">Write your Answer here:<a class="anchor-link" href="#Write-your-Answer-here:">¶</a></h4>
</div>
</div>
</div>
</div>Ans 8:
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q9.-What-do-the-summary-statistics-of-the-data-represent?-Find-the-summary-statistics-for-all-variables-except-'Outcome'-in-the-pima-data.-Take-one-column/variable-from-the-output-table-and-explain-all-its-statistical-measures.-(5-Marks)">Q9. What do the summary statistics of the data represent? Find the summary statistics for all variables except 'Outcome' in the <code>pima</code> data. Take one column/variable from the output table and explain all its statistical measures. (5 Marks)<a class="anchor-link" href="#Q9.-What-do-the-summary-statistics-of-the-data-represent?-Find-the-summary-statistics-for-all-variables-except-'Outcome'-in-the-pima-data.-Take-one-column/variable-from-the-output-table-and-explain-all-its-statistical-measures.-(5-Marks)">¶</a></h2>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [31]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate function name</span>

<span class="n">pima</span><span class="o">.</span><span class="n">iloc</span><span class="p">[:,</span> <span class="mi">0</span><span class="p">:</span><span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">describe</span><span class="p">()</span>
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
<div class="jp-OutputPrompt jp-OutputArea-prompt">Out[31]:</div>
<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html" tabindex="0">
<div class="colab-df-container" id="df-e4ee7dbb-efed-49f1-9db9-9bc7592e8c26">
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
<th>Pregnancies</th>
<th>Glucose</th>
<th>BloodPressure</th>
<th>SkinThickness</th>
<th>Insulin</th>
<th>BMI</th>
<th>DiabetesPedigreeFunction</th>
<th>Age</th>
</tr>
</thead>
<tbody>
<tr>
<th>count</th>
<td>768.000000</td>
<td>768.000000</td>
<td>768.000000</td>
<td>768.000000</td>
<td>768.000000</td>
<td>768.000000</td>
<td>768.000000</td>
<td>768.000000</td>
</tr>
<tr>
<th>mean</th>
<td>3.845052</td>
<td>121.675781</td>
<td>72.250000</td>
<td>26.447917</td>
<td>118.270833</td>
<td>32.450805</td>
<td>0.471876</td>
<td>33.240885</td>
</tr>
<tr>
<th>std</th>
<td>3.369578</td>
<td>30.436252</td>
<td>12.117203</td>
<td>9.733872</td>
<td>93.243829</td>
<td>6.875374</td>
<td>0.331329</td>
<td>11.760232</td>
</tr>
<tr>
<th>min</th>
<td>0.000000</td>
<td>44.000000</td>
<td>24.000000</td>
<td>7.000000</td>
<td>14.000000</td>
<td>18.200000</td>
<td>0.078000</td>
<td>21.000000</td>
</tr>
<tr>
<th>25%</th>
<td>1.000000</td>
<td>99.750000</td>
<td>64.000000</td>
<td>20.000000</td>
<td>79.000000</td>
<td>27.500000</td>
<td>0.243750</td>
<td>24.000000</td>
</tr>
<tr>
<th>50%</th>
<td>3.000000</td>
<td>117.000000</td>
<td>72.000000</td>
<td>23.000000</td>
<td>79.000000</td>
<td>32.000000</td>
<td>0.372500</td>
<td>29.000000</td>
</tr>
<tr>
<th>75%</th>
<td>6.000000</td>
<td>140.250000</td>
<td>80.000000</td>
<td>32.000000</td>
<td>127.250000</td>
<td>36.600000</td>
<td>0.626250</td>
<td>41.000000</td>
</tr>
<tr>
<th>max</th>
<td>17.000000</td>
<td>199.000000</td>
<td>122.000000</td>
<td>99.000000</td>
<td>846.000000</td>
<td>67.100000</td>
<td>2.420000</td>
<td>81.000000</td>
</tr>
</tbody>
</table>
</div>
<div class="colab-df-buttons">
<div class="colab-df-container">
<button class="colab-df-convert" onclick="convertToInteractive('df-e4ee7dbb-efed-49f1-9db9-9bc7592e8c26')" style="display:none;" title="Convert this dataframe to an interactive table.">
<svg height="24px" viewbox="0 -960 960 960" xmlns="http://www.w3.org/2000/svg">
<path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"></path>
</svg>
</button>
<style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>
<script>
      const buttonEl =
        document.querySelector('#df-e4ee7dbb-efed-49f1-9db9-9bc7592e8c26 button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-e4ee7dbb-efed-49f1-9db9-9bc7592e8c26');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
</div>
<div id="df-dbe6aadc-000a-4e16-a972-d7a5d7d509c1">
<button class="colab-df-quickchart" onclick="quickchart('df-dbe6aadc-000a-4e16-a972-d7a5d7d509c1')" style="display:none;" title="Suggest charts">
<svg height="24px" viewbox="0 0 24 24" width="24px" xmlns="http://www.w3.org/2000/svg">
<g>
<path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"></path>
</g>
</svg>
</button>
<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>
<script>
    async function quickchart(key) {
      const quickchartButtonEl =
        document.querySelector('#' + key + ' button');
      quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
      quickchartButtonEl.classList.add('colab-df-spinner');
      try {
        const charts = await google.colab.kernel.invokeFunction(
            'suggestCharts', [key], {});
      } catch (error) {
        console.error('Error during call to suggestCharts:', error);
      }
      quickchartButtonEl.classList.remove('colab-df-spinner');
      quickchartButtonEl.classList.add('colab-df-quickchart-complete');
    }
    (() => {
      let quickchartButtonEl =
        document.querySelector('#df-dbe6aadc-000a-4e16-a972-d7a5d7d509c1 button');
      quickchartButtonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';
    })();
  </script>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>describe each columns</p>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span> 
</pre></div>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Write-your-Answer-here:">Write your Answer here:<a class="anchor-link" href="#Write-your-Answer-here:">¶</a></h4>
</div>
</div>
</div>
</div>Ans 9:
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q-10.-Plot-the-distribution-plot-for-the-variable-'BloodPressure'.-Write-detailed-observations-from-the-plot.-(2-Marks)">Q 10. Plot the distribution plot for the variable 'BloodPressure'. Write detailed observations from the plot. (2 Marks)<a class="anchor-link" href="#Q-10.-Plot-the-distribution-plot-for-the-variable-'BloodPressure'.-Write-detailed-observations-from-the-plot.-(2-Marks)">¶</a></h2>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [33]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate library name</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>

<span class="n">sns</span><span class="o">.</span><span class="n">displot</span><span class="p">(</span><span class="n">pima</span><span class="p">[</span><span class="s1">'BloodPressure'</span><span class="p">],</span> <span class="n">kind</span><span class="o">=</span><span class="s1">'kde'</span><span class="p">)</span>

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
<img alt="No description has been provided for this image" class="" src="data:image/png;base64,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eTKUSiUiIyOxcuVKhzDS6/V4/PHHER4eDpVKhZtuugmHDh1yOMcnn3yCYcOGwdfXFzNmzEBhYWGHnxUeHo7IyEj88Ic/xNq1a3HixAmcPXvW3tL+9NNPMWHCBCiVSnz11VewWCzIyspCfHw8fH19kZSUhPfff99+vrq6OsyfPx9hYWHw9fVFQkIC3njjDQCAwWDAkiVLEBkZCZVKhUGDBtn3mO7otn99fT0kEgk+//xzAOhxTURikotdABF1XVNTE9555x0MHToUISEhaG5udni9tLQUt912Gx588EG8/fbbOHXqFB5++GGoVCo8++yzAICnn34aH3zwAd566y0MGjQIL774ItLT03H27FkEBwejpKQEd911Fx577DE88sgjOHz4MH7961/fsDZfX18A1jC1WblyJf7whz9g8ODBGDBgALKysvDOO+9gy5YtSEhIwJdffon7778fYWFhmD59Op555hmcOHECn376KUJDQ3H27Fm0trYCAF599VV8+OGH+Oc//4nY2FiUlJSgpKSk21/D7tZEJCpxN+EioutZuHChIJPJBH9/f8Hf318AIERGRgp5eXmCIAj2bf2OHDkiCIIgrF69Whg+fLhgsVjs59i8ebMQEBAgmM1moampSfDx8RHeffdd++sGg0GIiooSXnzxRUEQBGHVqlXCqFGjHOpYsWKFAECoq6sTBOHyVoO2v5eVlQlTp04VoqOjBb1eb399165d9nO0tbUJfn5+wv79+x3OvXjxYvs+wD/96U+FRYsWdfi1WLp0qfCjH/3I4dpsrv46CIIg1NXVOWxv2NOaiMTEljSRi5sxYwZee+01ANbbwX/+859x66234uDBg9cce/LkSaSmpkIikdifmzZtGpqamnDx4kXU19fDaDRi2rRp9td9fHwwefJknDx50n6OlJQUh/OmpqZ2WNvAgQMhCAJaWlqQlJSEDz74AAqFwv76xIkT7X8+e/YsWlpa8OMf/9jhHAaDAePGjQMA/PKXv8ScOXOQn5+PW265BRkZGZg6dSoA6yC6H//4xxg+fDhmzZqFn/zkJ7jllltu/AW8SndrIhITQ5rIxfn7+2Po0KH2v//tb3+DRqPBX//6Vzz00EMiVgb873//g1qtRnh4OAIDA6953d/f3/7npqYmAMDHH3+M6Ohoh+OUSiUA4NZbb0VRURE++eQTZGdnY+bMmXjsscfwhz/8AePHj8eFCxfw6aef4rPPPsO9996LtLQ0vP/++5BKrcNrBEGwn9NoNHZYc3drIhITQ5rIzUgkEkilUntf7ZVGjhyJDz74AIIg2FvTX3/9NQIDAzFw4ECEhIRAoVDg66+/xqBBgwBYw+zQoUN44okn7Of48MMPHc77zTffdFhLfHw8goKCulT3qFGjoFQqUVxcfN2+3rCwMCxcuBALFy7ED37wAzz11FP4wx/+AABQq9WYO3cu5s6di7vvvhuzZs1CbW0twsLCAADl5eX2FnBX5o53tSYisTCkiVycXq9HRUUFAOvt7k2bNqGpqQk//elPrzn2V7/6FTZu3IilS5diyZIlKCgowLp165CZmQmpVAp/f3/88pe/xFNPPYXg4GDExsbixRdfREtLCxYvXgwA+MUvfoENGzbgqaeewkMPPYS8vDy8+eabvb6OwMBAPPnkk1i+fDksFgtuuukmNDQ04Ouvv4ZarcbChQuxdu1aTJgwAaNHj4Zer8fu3bsxcuRIAMDLL7+MyMhIjBs3DlKpFDt27IBWq0VQUBCkUimmTJmC9evXIz4+HlVVVVizZo1TaiISlch94kR0HQsXLhQA2B+BgYHCpEmThPfff18QhI4HTH3++efCpEmTBIVCIWi1WmHFihWC0Wi0v97a2iosXbpUCA0NFZRKpTBt2jTh4MGDDp/70UcfCUOHDhWUSqXwgx/8QPj73/9+3YFjV+vsdYvFImzcuFEYPny44OPjI4SFhQnp6enCF198IQiCIDz33HPCyJEjBV9fXyE4OFi44447hPPnzwuCIAhbt24VkpOTBX9/f0GtVgszZ84U8vPz7ec+ceKEkJqaKvj6+grJycnCf//73w4HjnW3JiIxSQThik4cIiIichlczISIiMhFMaSJiIhcFEOaiIjIRTGkiYiIXBRDmoiIyEUxpImIiFwUQ5qIiMhFMaSJiIhcFEOaiIjIRTGkiYiIXBRDmoiIyEX9f1+s8dJ0J7npAAAAAElFTkSuQmCC
"/>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>using seaborn to create chart</p>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Write-your-Answer-here:">Write your Answer here:<a class="anchor-link" href="#Write-your-Answer-here:">¶</a></h4>
</div>
</div>
</div>
</div>Ans 10:
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>:## Q 11. What is the 'BMI' of the person having the highest 'Glucose'? (2 Marks)</p>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [49]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate function name</span>

<span class="n">pima</span><span class="p">[</span><span class="n">pima</span><span class="p">[</span><span class="s1">'Glucose'</span><span class="p">]</span> <span class="o">==</span> <span class="n">pima</span><span class="p">[</span><span class="s1">'Glucose'</span><span class="p">]</span><span class="o">.</span><span class="n">max</span><span class="p">()][</span><span class="s1">'BMI'</span><span class="p">]</span>
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
<div class="jp-OutputPrompt jp-OutputArea-prompt">Out[49]:</div>
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
<th>BMI</th>
</tr>
</thead>
<tbody>
<tr>
<th>661</th>
<td>42.9</td>
</tr>
</tbody>
</table>
</div><br/><label><b>dtype:</b> float64</label>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Write-your-Answer-here:">Write your Answer here:<a class="anchor-link" href="#Write-your-Answer-here:">¶</a></h4><p>we using max to see the highest value in glucose columns and show respectively value</p>
</div>
</div>
</div>
</div>Ans 11:
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q12.">Q12.<a class="anchor-link" href="#Q12.">¶</a></h2><h3 id="12.1-What-is-the-mean-of-the-variable-'BMI'?">12.1 What is the mean of the variable 'BMI'?<a class="anchor-link" href="#12.1-What-is-the-mean-of-the-variable-'BMI'?">¶</a></h3><h3 id="12.2-What-is-the-median-of-the-variable-'BMI'?">12.2 What is the median of the variable 'BMI'?<a class="anchor-link" href="#12.2-What-is-the-median-of-the-variable-'BMI'?">¶</a></h3><h3 id="12.3-What-is-the-mode-of-the-variable-'BMI'?">12.3 What is the mode of the variable 'BMI'?<a class="anchor-link" href="#12.3-What-is-the-mode-of-the-variable-'BMI'?">¶</a></h3><h3 id="12.4-Are-the-three-measures-of-central-tendency-equal?">12.4 Are the three measures of central tendency equal?<a class="anchor-link" href="#12.4-Are-the-three-measures-of-central-tendency-equal?">¶</a></h3><h3 id="(4-Marks)">(4 Marks)<a class="anchor-link" href="#(4-Marks)">¶</a></h3>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [32]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate function name</span>

<span class="n">m1</span> <span class="o">=</span> <span class="n">pima</span><span class="p">[</span><span class="s1">'BMI'</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()</span>  <span class="c1"># mean</span>
<span class="nb">print</span><span class="p">(</span><span class="n">m1</span><span class="p">)</span>

<span class="n">m2</span> <span class="o">=</span> <span class="n">pima</span><span class="p">[</span><span class="s1">'BMI'</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">()</span>  <span class="c1"># median</span>
<span class="nb">print</span><span class="p">(</span><span class="n">m2</span><span class="p">)</span>

<span class="n">m3</span> <span class="o">=</span> <span class="n">pima</span><span class="p">[</span><span class="s1">'BMI'</span><span class="p">]</span><span class="o">.</span><span class="n">mode</span><span class="p">()[</span><span class="mi">0</span><span class="p">]</span>  <span class="c1"># mode</span>
<span class="nb">print</span><span class="p">(</span><span class="n">m3</span><span class="p">)</span>
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
<pre>32.45080515543619
32.0
32.0
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Write-your-Answer-here:">Write your Answer here:<a class="anchor-link" href="#Write-your-Answer-here:">¶</a></h4>
</div>
</div>
</div>
</div>Ans 12:

mean is average

median = middle number

mode is number appears most often in the set
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q13.-How-many-women's-'Glucose'-levels-are-above-the-mean-level-of-'Glucose'?-(2-Marks)">Q13. How many women's 'Glucose' levels are above the mean level of 'Glucose'? (2 Marks)<a class="anchor-link" href="#Q13.-How-many-women's-'Glucose'-levels-are-above-the-mean-level-of-'Glucose'?-(2-Marks)">¶</a></h2>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [36]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate function name</span>

<span class="n">pima</span><span class="p">[</span><span class="n">pima</span><span class="p">[</span><span class="s1">'Glucose'</span><span class="p">]</span> <span class="o">&gt;</span> <span class="n">pima</span><span class="p">[</span><span class="s1">'Glucose'</span><span class="p">]</span><span class="o">.</span><span class="n">mean</span><span class="p">()]</span><span class="o">.</span><span class="n">shape</span><span class="p">[</span><span class="mi">0</span><span class="p">]</span>
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
<div class="jp-OutputPrompt jp-OutputArea-prompt">Out[36]:</div>
<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain" tabindex="0">
<pre>343</pre>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Write-your-Answer-here:">Write your Answer here:<a class="anchor-link" href="#Write-your-Answer-here:">¶</a></h4>
</div>
</div>
</div>
</div>Ans 13:

using mean to see the average number and see how many value in glucose bigger than that


<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q14.-How-many-women-have-their-'BloodPressure'-equal-to-the-median-of-'BloodPressure'-and-their-'BMI'-less-than-the-median-of-'BMI'?-(2-Marks)">Q14. How many women have their 'BloodPressure' equal to the median of 'BloodPressure' and their 'BMI' less than the median of 'BMI'? (2 Marks)<a class="anchor-link" href="#Q14.-How-many-women-have-their-'BloodPressure'-equal-to-the-median-of-'BloodPressure'-and-their-'BMI'-less-than-the-median-of-'BMI'?-(2-Marks)">¶</a></h2>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate column name</span>

<span class="n">pima</span><span class="p">[(</span><span class="n">pima</span><span class="p">[</span><span class="s1">'BloodPressure'</span><span class="p">]</span> <span class="o">==</span> <span class="n">pima</span><span class="p">[</span><span class="s1">'BloodPressure'</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())</span> <span class="o">&amp;</span> <span class="p">(</span><span class="n">pima</span><span class="p">[</span><span class="s1">'BMI'</span><span class="p">]</span> <span class="o">&lt;</span> <span class="n">pima</span><span class="p">[</span><span class="s1">'BMI'</span><span class="p">]</span><span class="o">.</span><span class="n">median</span><span class="p">())]</span>
</pre></div>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Write-your-Answer-here:">Write your Answer here:<a class="anchor-link" href="#Write-your-Answer-here:">¶</a></h4><p>caculate median of BloodPressure to see  then see how many women have bmi &lt; median bmi</p>
</div>
</div>
</div>
</div>Ans 14:
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q15.-Create-a-pairplot-for-the-variables-'Glucose',-'SkinThickness',-and-'DiabetesPedigreeFunction'.-Write-your-observations-from-the-plot.-(3-Marks)">Q15. Create a pairplot for the variables 'Glucose', 'SkinThickness', and 'DiabetesPedigreeFunction'. Write your observations from the plot. (3 Marks)<a class="anchor-link" href="#Q15.-Create-a-pairplot-for-the-variables-'Glucose',-'SkinThickness',-and-'DiabetesPedigreeFunction'.-Write-your-observations-from-the-plot.-(3-Marks)">¶</a></h2>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [37]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate function name</span>

<span class="n">sns</span><span class="o">.</span><span class="n">pairplot</span><span class="p">(</span><span class="n">data</span> <span class="o">=</span> <span class="n">pima</span><span class="p">,</span> <span class="nb">vars</span> <span class="o">=</span> <span class="p">[</span><span class="s1">'Glucose'</span><span class="p">,</span> <span class="s1">'SkinThickness'</span><span class="p">,</span> <span class="s1">'DiabetesPedigreeFunction'</span><span class="p">],</span> <span class="n">hue</span> <span class="o">=</span> <span class="s1">'Outcome'</span><span class="p">)</span>
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
<img alt="No description has been provided for this image" class="" src="data:image/png;base64,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KBSsWrWqqsOQpGrtVvmkRo0afPTRR3f1mO3ateOll166o7iuN3XqVBo1anTHcUn3p9u9Fzxo59OQIUPo1auX5XVF8ueD7sbPTHrwyIKNdFelpKQwduxYIiMj0Wq1+Pn50apVK7744gvy8/OrOjxJqjYuX77MyJEjCQ0NRaPR4O/vT+fOndmxY0eFtt+zZw8jRoyoUNqpU6eiUChu+ldRycnJdO3atcLppQfPkCFDLOeVWq3Gz8+Pjh078vXXX2MymSzpquJcOnv2LAqFgoMHD97V/daoUcPynvV6PU2aNGH58uV39Rg//PADb7/99l3d59+1YMECm9eRr776qlKOX973+PHHH7NgwYJKiUGqnlRVHYB0/zh9+jStWrXC3d2d6dOnExMTg0aj4ciRI8ydO5egoCAef/zxqg5TkqqFPn36UFxczDfffENERASpqals2rSJ9PT0Cm3v4+NT4WO9+uqrPP/885bXzZo1Y8SIETz33HO3Hbe/v/9tbyM9eLp06cL8+fMxGo2kpqayfv16xo4dy/fff89PP/2ESqW6786lt956i+eee47s7GxmzZpF//79CQoKomXLlndl/56enne8D4PBgFqtvgvRgKurKwkJCVbL3Nzc7sq+/66qPr5U9WSNjXTXvPDCC6hUKvbu3Uu/fv2oU6cOERER9OzZk7Vr19KjR48y22zZsgWFQkFmZqZl2cGDB1EoFJw9e9aybMeOHbRr1w4nJyc8PDzo3LkzGRkZABQVFfHiiy/i6+uLVquldevW7Nmzx7JtRkYGAwcOxMfHB51OR1RUFPPnz7esv3DhAv369cPd3R1PT0969uxpdWxJutsyMzPZtm0b//73v3nkkUcICwujefPmTJo0qdzC/5QpUwgICODw4cNA2aZopb+W9u7dGycnJ6Kiovjpp58AcHZ2xt/f3/Ln4OCAi4uL1bJSJpOJCRMm4Onpib+/P1OnTrWK48bmQxcvXmTAgAF4enqi1+uJjY1l165dNt9DYmIiERERjB49GiEECxYswN3dnV9++YU6derg7OxMly5dSE5Ottruq6++ok6dOmi1WmrXrs3nn39uWVdcXMzo0aMJCAhAq9USFhbGjBkzABBCMHXqVEutWGBgIC+++OLNvxzpriithQwKCqJJkya8/vrr/Pjjj6xbt87yi/qN59LEiROpVasWTk5OREREMHny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
"/>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>create multiple chart by using seaborn (matplot cant do that)</p>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Write-your-Answer-here:">Write your Answer here:<a class="anchor-link" href="#Write-your-Answer-here:">¶</a></h4>
</div>
</div>
</div>
</div>Ans 15:<div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span> 
</pre></div>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q16.-Plot-the-scatterplot-between-'Glucose'-and-'Insulin'.-Write-your-observations-from-the-plot.-(4-Marks)">Q16. Plot the scatterplot between 'Glucose' and 'Insulin'. Write your observations from the plot. (4 Marks)<a class="anchor-link" href="#Q16.-Plot-the-scatterplot-between-'Glucose'-and-'Insulin'.-Write-your-observations-from-the-plot.-(4-Marks)">¶</a></h2>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [38]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate function name</span>

<span class="n">sns</span><span class="o">.</span><span class="n">scatterplot</span><span class="p">(</span><span class="n">x</span> <span class="o">=</span> <span class="s1">'Glucose'</span><span class="p">,</span> <span class="n">y</span> <span class="o">=</span> <span class="s1">'Insulin'</span><span class="p">,</span> <span class="n">data</span> <span class="o">=</span> <span class="n">pima</span><span class="p">)</span>
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
<img alt="No description has been provided for this image" class="" src="data:image/png;base64,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qalBQUEBysrKPP4ZjUbV9SCi6GGwQ0Qx88ILL8DhcGD48OH45z//if379+PAgQN47bXX8PXXX0Or1fq8pqysDMXFxXjooYdQU1ODf//733j66ac9trnvvvvw5ZdfYubMmdi1axe+/vprLFmyBA0NDcjMzMStt96Ke+65B6tXr8a+fftw8803w2KxYMaMGQCA+fPn491330VtbS327t2LVatWoX///gCAKVOmwGQy4aqrrsLGjRtx6NAhfPbZZ7j99tvx/fffR/6gEVHwBCKiGDp27JhQVVUllJaWCmlpaUJWVpZw3nnnCU899ZTQ2toqCIIgABBWrlzpfs2mTZuEwYMHC+np6cKYMWOEt956SwAgHDp0yL3NZ599JowaNUrQ6/VCbm6uMGHCBKGxsVEQBEFoa2sTbrvtNsFkMgl6vV6orKwUvvjiC/drFyxYIPTv318wGAxCjx49hKuuuko4ePCg+/njx48LN954o/v1Z599tnDzzTcLZrM5oseKiEKjEQRJxzcRERFRkmE3FhERESU1BjtERESU1BjsEBERUVJjsENERERJjcEOERERJTUGO0RERJTUGOwQERFRUmOwQ0REREmNwQ4RERElNQY7RERElNQY7BAREVFS+/+P2Vq926rhAQAAAABJRU5ErkJggg==
"/>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Write-your-Answer-here:">Write your Answer here:<a class="anchor-link" href="#Write-your-Answer-here:">¶</a></h4>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>using scatterplot by using sns</p>
</div>
</div>
</div>
</div>Ans 16:
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q-17.-Plot-the-boxplot-for-the-'Age'-variable.-Are-there-outliers?-(2-Marks)">Q 17. Plot the boxplot for the 'Age' variable. Are there outliers? (2 Marks)<a class="anchor-link" href="#Q-17.-Plot-the-boxplot-for-the-'Age'-variable.-Are-there-outliers?-(2-Marks)">¶</a></h2>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [39]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate function and column name</span>

<span class="n">plt</span><span class="o">.</span><span class="n">boxplot</span><span class="p">(</span><span class="n">pima</span><span class="p">[</span><span class="s1">'Age'</span><span class="p">])</span>

<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">'Boxplot of Age'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">'Age'</span><span class="p">)</span>
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
<img alt="No description has been provided for this image" class="" src="data:image/png;base64,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n376SaWlpTWeV5Lmzp2r66+/XgcOHFBeXp7y8vLUvn17lZeXa+HChW41eHh4KCoqyu39LVu2dHu9f/9+HTp0SG+//baaNWvmdt1///2S/rshGcB/cfwaaCA8PDwUHx+v1157Tbm5uWrTpk2N5/jss88kSceOHVNubu5Jv5wbitzcXK1fv16S1KpVq5P6582bp4cffrhGc1bdg6Z///4aMGDAKce0a9euhpUC9R9BBmhATpw4IUk6fPiwJOnyyy/X8uXLVVJS4rYqs23bNld/lW+++UYvvvii7r//fm3atEkPPvigvv32WwUFBbl9RmVlpb7//nvXKowkbd++XZJOe9+XZs2aqXHjxsrJyTmpb9u2bfLw8FBERIQknXIV6HSq6j/dvJdccon8/f2rPV+VefPmydvbW++8847bRmdJWr16tV5//XXt3r1bLVq00OWXX67Kykrt3LnTLfTk5eW5va9Zs2YKCAhQRUUF96IBaoCvloAG4vjx4/r888/l4+Pj+uro9ttvV0VFhd544w23sZMnT5bD4VBiYqLrvSkpKQoPD9drr72m9PR0FRUVafjw4af8rF/PZ1mW3njjDXl7e+uWW2455XhPT0/deuut+uijj9y+fioqKtL8+fPVtWtXBQYGSpIreBw6dOiMP3NYWJiuvfZazZkzx2385s2b9fnnn+v2228/4xynMm/ePHXr1k133323evfu7XY98cQTkuS6X0/37t0lSdOnT3ebY+rUqW6vPT09lZycrA8++ECbN28+6TP3799/VrUC9R0rMkA9lZGR4VpZ2bdvn+bPn6/c3Fw9/fTTrlDQo0cPxcfH65lnnlF+fr6uueYaff755/roo480bNgwXXHFFZKksWPHatOmTVqxYoUCAgLUrl07Pf/883r22WfVu3dvt0DQqFEjffrppxowYIA6duyojIwMffzxxxo1apSaNWt22nrHjh2rZcuWqWvXrnr00Ufl5eWlt956S2VlZZowYYJr3LXXXitPT0+NHz9excXF8vX11c0336zmzZufct6//vWvSkxMVFxcnAYOHKijR49q6tSpCgoKOqtnPa1bt055eXluG5p/7dJLL1WHDh00b948PfXUU4qNjVVycrKmTJmiAwcOqFOnTsrMzHStUv16hWncuHFauXKlOnbsqIceekhXXXWVDh48qI0bN2r58uU6ePBgjesF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
"/>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>there are some outliner and we using box plot to see mean, Q1, Q2, Q3</p>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Write-your-Answer-here:">Write your Answer here:<a class="anchor-link" href="#Write-your-Answer-here:">¶</a></h4>
</div>
</div>
</div>
</div>Ans 17:
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q18.-Plot-histograms-for-the-'Age'-variable-to-understand-the-number-of-women-in-different-age-groups-given-whether-they-have-diabetes-or-not.-Explain-both-histograms-and-compare-them.-(5-Marks)">Q18. Plot histograms for the 'Age' variable to understand the number of women in different age groups given whether they have diabetes or not. Explain both histograms and compare them. (5 Marks)<a class="anchor-link" href="#Q18.-Plot-histograms-for-the-'Age'-variable-to-understand-the-number-of-women-in-different-age-groups-given-whether-they-have-diabetes-or-not.-Explain-both-histograms-and-compare-them.-(5-Marks)">¶</a></h2>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [40]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate function and column name</span>

<span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">pima</span><span class="p">[</span><span class="n">pima</span><span class="p">[</span><span class="s1">'Outcome'</span><span class="p">]</span> <span class="o">==</span> <span class="mi">1</span><span class="p">][</span><span class="s1">'Age'</span><span class="p">],</span> <span class="n">bins</span> <span class="o">=</span> <span class="mi">5</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">'Distribution of Age for Women who has Diabetes'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">'Age'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">'Frequency'</span><span class="p">)</span>
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
<img alt="No description has been provided for this image" class="" src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAjIAAAHHCAYAAACle7JuAAAAOXRFWHRTb2Z0d2FyZQBNYXRwbG90bGliIHZlcnNpb24zLjguMCwgaHR0cHM6Ly9tYXRwbG90bGliLm9yZy81sbWrAAAACXBIWXMAAA9hAAAPYQGoP6dpAAA/IklEQVR4nO3dd3wU1f7/8fdCKgkktDQpiXRI6Ih0hAgCegFBUOFLEcSroDQLeEVAQIpSBQkoUlXaBcFCk6YgHaRclV4NJCikIgGS8/vDR/bHkgBJSNgMvp6Pxz50z8ye+ezJsHln5syszRhjBAAAYEF5nF0AAABAVhFkAACAZRFkAACAZRFkAACAZRFkAACAZRFkAACAZRFkAACAZRFkAACAZRFkAACAZRFkHjDDhg2TzWa7L9tq3LixGjdubH++adMm2Ww2LV269L5sv1u3bgoODr4v28qqhIQE9ezZUwEBAbLZbOrXr5+zS8q01atXq2rVqvLw8JDNZlNMTIyzS8Jd2Gw29enTJ0e3cerUKdlsNn344Yc5up2cci+flcHBwXryySezuSJkFUEmF5szZ45sNpv94eHhoaCgIDVv3lxTpkxRfHx8tmwnMjJSw4YN088//5wt/WWn3FxbRrz//vuaM2eOXn75Zc2fP1//93//d9fXJCcnKygoSDabTatWrboPVd7en3/+qQ4dOsjT01PTpk3T/Pnz5eXllSPbWrx4sWw2m5YvX55mWZUqVWSz2bRx48Y0y0qUKKG6devmSE2whvv1WZlTrly5omHDhmnTpk3OLsWSCDIW8N5772n+/PmaPn26Xn31VUlSv379FBYWpgMHDjis+8477+ivv/7KVP+RkZEaPnx4psPC2rVrtXbt2ky9JrPuVNsnn3yiw4cP5+j279WGDRv06KOPaujQoercubNq1KiRodecP39ewcHB+vzzz+9Dlbe3a9cuxcfHa8SIEerRo4c6d+4sV1fXHNlW/fr1JUlbtmxxaI+Li9OhQ4fk4uKirVu3Oiw7e/aszp49a38t/tly+rMyp1y5ckXDhw8nyGSRi7MLwN21aNFCNWvWtD8fPHiwNmzYoCeffFL/+te/9Ouvv8rT01OS5OLiIheXnP2xXrlyRfny5ZObm1uObuducuoXanaKjo5WxYoVM/WaBQsWqHr16uratavefvttJSYm5thRkLuJjo6WJPn6+mZbn7d7P0FBQQoJCUkTZLZt2yZjjJ555pk0y1KfE2Qg5b7PStwfHJGxqCZNmmjIkCE6ffq0FixYYG9P77zvunXrVL9+ffn6+srb21vlypXT22+/LenveS21atWSJHXv3t1+aHbOnDmS/p4HExoaqj179qhhw4bKly+f/bW3zpFJlZycrLffflsBAQHy8vLSv/71L509e9ZhneDgYHXr1i3Na2/u8261pTdHJjExUQMHDlTx4sXl7u6ucuXK6cMPP9StX/KeOofgq6++UmhoqNzd3VWpUiWtXr06/QG/RXR0tHr06CF/f395eHioSpUqmjt3rn156nyhkydP6ttvv7XXfurUqTv2+9dff2n58uV69tln1aFDB/31119asWJFuusuWbJEFStWlIeHh0JDQ7V8+fJ0xyQlJUWTJk1SpUqV5OHhIX9/f7300ku6fPnyHWtp3LixunbtKkmqVauWbDabw89syZIlqlGjhjw9PVWkSBF17txZv//+u0Mf3bp1k7e3t44fP66WLVsqf/786tSp0223Wb9+fe3bt8/hL+WtW7eqUqVKatGihbZv366UlBSHZTabTfXq1ZMk3bhxQyNGjFCpUqXk7u6u4OBgvf3220pKSnLYTuoch02bNqlmzZry9PRUWFiY/S/iZcuWKSwsTB4eHqpRo4b27duXptbffvtN7du3V6FCheTh4aGaNWtq5cqVDuuknvLYunWrBgwYoKJFi8rLy0tt27bVxYsX7zD60sqVK2Wz2RyOJPz3v/+VzWbT008/7bBuhQoV1LFjxzR9ZGT/3rdvn1q0aKECBQrI29tbTZs21fbt2+9Y261mzpxpH/NatWpp165dDssPHDigbt266eGHH5aHh4cCAgL0wgsv6M8//3RYLz4+Xv369VNwcLDc3d3l5+enxx9/XHv37s1UPTfLzGfl7Nmz1aRJE/n5+cnd3V0VK1bU9OnTb9v32rVr7fPHKlasqGXLlqVZJyYmRv369bN/JpUuXVpjx46178enTp1S0aJFJUnDhw+3f1YMGzbM3kdG9rXr169r+PDhKlOmjDw8PFS4cGHVr19f69aty/SYWY5BrjV79mwjyezatSvd5WfPnjWSTPv27e1tQ4cONTf/WA8dOmTc3NxMzZo1zeTJk01ERIR5/fXXTcOGDY0xxly4cMG89957RpLp1auXmT9/vpk/f745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Mqv7WmpI++GHH3TixAlVr15dXl5eatCggaZMmaKEhATt27dPo0aNyvT7yC4Z2U6HDh30008/6Y033lDVqlXl7e2tlJQUPfHEEw5/VHXo0EENGjTQ8uXLtXbtWn3wwQcaO3asli1bphYtWmS5xox8Vh4/flxNmzZV+fLlNWHCBBUvXlxubm767rvvNHHixCwd0U5JSdHjjz+uN998M93lqcHnTq+XMravNWzYUMePH9eKFSu0du1affrpp5o4caIiIiLUs2fPTNduJQQZC5s/f74k3XYHT5UnTx41bdpUTZs21YQJE/T+++/rP//5jzZu3Kjw8PBsvxPwrYc2jTE6duyYKleubG8rWLBguneIPX36tMMvpszUVrJkSX3//feKj493+Mvrt99+sy/PDiVLltSBAweUkpLi8Av6XrZz8uRJ/fTTT+rTp48aNWrksCwlJUX/93//py+++ELvvPOOvf9jx46l6efWtlKlSun7779XvXr1si2Qpm7/8OHDatKkicOyw4cP3/M433w/ma1btzrcDblGjRpyd3fXpk2btGPHDrVs2dKhrpSUFB09etR+dEySoqKiFBMTk20//9T909XV1f6XdU4pUaKESpQooR9//FEnTpywn7Zp2LChBgwYoCVLlig5OVkNGzbMdN9FixZVvnz50r0X02+//aY8efKkOTqVFZcvX9b69es1fPhwvfvuu/b2250CCQwM1CuvvKJXXnlF0dHRql69ukaNGnVPQSYjn5Vff/21kpKStHLlSoejTLc7/Zp6tOTmz6gjR45Ikv3KwVKlSikhIeGu+8ntPucyu68VKlRI3bt3V/fu3ZWQkKCGDRtq2LBhD3yQ4dSSRW3YsEEjRoxQSEjIHS9nvXTpUpq2qlWrSpL9ktTUe3pk163n582b53AueunSpTp//rzDB1GpUqW0fft2Xbt2zd72zTffpDmUnZnaWrZsqeTkZE2dOtWhfeLEibLZbPf0QXjrdi5cuKBFixbZ227cuKGPPvpI3t7eaYJIRqQeMXnzzTfVvn17h0eHDh3UqFEj+zpBQUEKDQ3VvHnzlJCQYO9j8+bNOnjwoEO/HTp0UHJyskaMGJFmmzdu3MjSz7xmzZry8/NTRESEw2XNq1at0q+//qpWrVplus9b+/fw8NDnn3+u33//3eGIjLu7u6pXr65p06YpMTHR4f4xqaFm0qRJDv1NmDBBku65rlR+fn5q3LixZsyYofPnz6dZfrfLqjOrQYMG2rBhg3bu3GkPMlWrVlX+/Pk1ZswYeXp6ZuhGi7fKmzevmjVrphUrVjic9o2KitIXX3yh+vXrq0CBAvdcf+oRm1uPBN36c0pOTk5z+sbPz09BQUFpLp/PjIx+VqZXZ2xsrGbPnp3u+pGRkQ53oY6Li9O8efNUtWpVBQQESPr739+2bdu0Zs2aNK+PiYnRjRs3JEn58uWzt90sM/varZeye3t7q3Tp0vc0dlbBERkLWLVqlX777TfduHFDUVFR2rBhg9atW6eSJUtq5cqVDhMub/Xee+/phx9+UKtWrVSyZElFR0fr448/VrFixey/BEqVKiVfX19FREQof/788vLyUu3ate3nsDOrUKFCql+/vrp3766oqChNmjRJpUuX1osvvmhfp2fPnlq6dKmeeOIJdejQQcePH9eCBQscJidmtrannnpKjz32mP7zn//o1KlTqlKlitauXasVK1aoX79+afrOql69emnGjBnq1q2b9uzZo+DgYC1dulRbt27VpEmT7noePj2ff/65qlatetu/gP/1r3/p1Vdf1d69e1W9enW9//77at26terVq6fu3bvr8uXLmjp1qkJDQx3CTaNGjfTSSy9p9OjR+vnnn9WsWTO5urrq6NGjWrJkiSZPnqz27dtnqlZXV1eNHTtW3bt3V6NGjfTcc88pKipKkydPVnBwsPr375/p938zNzc31apVSz/++KPc3d3T/JKuW7euxo8fL8nxRnhVqlRR165dNXPmTMXExKhRo0bauXOn5s6dqzZt2uixxx67p7puNm3aNNWvX19hYWF68cUX9fDDDysqKkrbtm3TuXPntH///mzbVoMGDfT555/LZrPZ32/evHlVt25drVmzRo0bN87yzSlHjhxpv8/UK6+8IhcXF82YMUNJSUkaN25cttRfoEABNWzYUOPGjdP169f10EMPae3atTp58qTDevHx8SpWrJjat2+vKlWqyNvbW99//7127dpl/3nfzb18VjZr1kxubm566qmn9NJLLykhIUGffPKJ/Pz80g0RZcuWVY8ePbRr1y75+/vrs88+U1RUlEPweeONN7Ry5Uo9+eST6tatm2rUqKHExEQdPHhQS5cu1alTp1SkSBF5enqqYsWKWrRokcqWLatChQopNDRUoaGhGd7X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qkyZMgoJCdGQIUMUFBSkNm3aOLN0AACQCzg1yHz00UcaMmSIXnnlFUVHRysoKEgvvfSS3n33Xfs6b775phITE9WrVy/FxMSofv36Wr16tTw8PJxYOQAAyA1s5ubb6D6A4uLi5OPjo9jYWBUoUCBb+w4e9G229ofbOzWmlbNLAADcRxn9/c13LQEAAMsiyAAAAMsiyAAAAMsiyAAAAMsiyAAAAMsiyAAAAMsiyAAAAMsiyAAAAMty6p19gYzi5oP3BzceBGA1HJEBAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACWRZABAACW5eLsAgDkHsGDvnV2Cf8Ip8a0cnYJwAODIzIAAMCyCDIAAMCyCDIAAMCyCDIAAMCyCDIAAMCyCDIAAMCyCDIAAMCyCDIAAMCyCDIAAMCyCDIAAMCyCDIAAMCynB5kfv/9d3Xu3FmFCxeWp6enwsLCtHv3bvtyY4zeffddBQYGytPTU+Hh4Tp69KgTKwYAALmFU4PM5cuXVa9ePbm6umrVqlX65ZdfNH78eBUsWNC+zrhx4zRlyhRFRERox44d8vLyUvPmzXX16lUnVg4AAHIDp3779dixY1W8eHHNnj3b3hYSEmL/f2OMJk2apHfeeUetW7eWJM2bN0/+/v766quv9Oyzz973mgEAQO7h1CMyK1euVM2aNfXMM8/Iz89P1apV0yeffGJffvLkSV24cEHh4eH2Nh8fH9WuXVvbtm1Lt8+kpCTFxcU5PAAAwIPJqUHmxIkTmj59usqUKaM1a9bo5Zdf1muvvaa5c+dKki5cuCBJ8vf3d3idv7+/fdmtRo8eLR8fH/ujePHiOfsmAACA0zg1yKSkpKh69ep6//33Va1aNfXq1Usvvvii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b66PP/44R7cJAACsI1NBxmazpZkDk9E5MRmxadMmh+ceHh6aNm2apk2blm3bAAAAD45Mn1rq1q2bfTLt1atX9e9//zvNVUvLli3LvgoBAABuI1NBpmvXrg7PO3funK3FAAAAZEamgszs2bNzqg4AAIBMy9KdfQEAAHIDggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsggwAALAsF2cXAAD/NMGDvnV2Cf8Ip8a0cnYJuA84IgMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACyLIAMAACzLqUFm9OjRqlWrlvLnzy8/Pz+1adNGhw8fdljn6tWr6t27twoXLixvb2+1a9dOUVFRTqoYAADkJk4NMps3b1bv3r21fft2rVu3TtevX1ezZs2UmJhoX6d///76+uuvtWTJEm3evFmRkZF6+umnnVg1AADILVycufHVq1c7PJ8zZ478/Py0Z88eNWzYULGxsZo1a5a++OILNWnSRJI0e/ZsVahQQdu3b9ejjz7qjLIBAEAukavmyMTGxkqSChUqJEnas2ePrl+/rvDwcPs65cuXV4kSJbRt2zan1AgAAHIPpx6RuVlKSor69eunevXqKTQ0VJJ04cIFubm5ydfX12Fdf39/XbhwId1+kpKSlJSUZH8eFxeXYzUDAADnyjVHZHr37q1Dhw5p4cKF99TP6NGj5ePjY38UL148myoEAAC5Ta4IMn369NE333yjjRs3qlixYvb2gIAAXbt2TTExMQ7rR0VFKSAgIN2+Bg8erNjYWPvj7NmzOVk6AABwIqcG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
"/>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>create histogram chart by using matplotlib and show that 20-30 is most have diabetes</p>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [41]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate function and column name</span>

<span class="n">plt</span><span class="o">.</span><span class="n">hist</span><span class="p">(</span><span class="n">pima</span><span class="p">[</span><span class="n">pima</span><span class="p">[</span><span class="s1">'Outcome'</span><span class="p">]</span> <span class="o">==</span> <span class="mi">0</span><span class="p">][</span><span class="s1">'Age'</span><span class="p">],</span> <span class="n">bins</span> <span class="o">=</span> <span class="mi">5</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">title</span><span class="p">(</span><span class="s1">'Distribution of Age for Women who do not have Diabetes'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">xlabel</span><span class="p">(</span><span class="s1">'Age'</span><span class="p">)</span>
<span class="n">plt</span><span class="o">.</span><span class="n">ylabel</span><span class="p">(</span><span class="s1">'Frequency'</span><span class="p">)</span>
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
<img alt="No description has been provided for this image" class="" src="data:image/png;base64,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FEuWLJFeb2pqiu3bt+Odd96BRqOBjY0NIiMjMW3aNGOtEhEREVUz1e4+O8bA++w8/3ifHSKif5/n7j47RERERE8Dww4RERHJGsMOERERyRrDDhEREckaww4RERHJGsMOERERyRrDDhEREckaww4RERHJGsMOERERyRrDDhEREckaww4RERHJGsMOERERyRrDDhEREckaww4RERHJGsMOERERyRrDDhEREckaww4RERHJGsMOERERyRrDDhEREckaww4RERHJGsMOERERyRrDDhEREckaww4RERHJGsMOERERyRrDDhEREckaww4RERHJGsMOERERyRrDDhEREckaww4RERHJGsMOERERyRrDDhEREckaww4RERHJGsMOERERyRrDDhEREckaww4RERHJGsMOERERyRrDDhEREckaww4RERHJGsMOERERyRrDDhEREcmaUcNObGwsWrRoATs7Ozg7O6Nnz55ITk7W6dO+fXsoFAqdx9tvv63T59q1awgPD4e1tTWcnZ3x/vvvo7i4+FmuChEREVVTZsZc+KFDhxAVFYUWLVqguLgYkydPRufOnfHHH3/AxsZG6jd8+HBMmzZNem5tbS39v6SkBOHh4VCr1Th27BgyMzMxaNAgmJub49NPP32m60NERETVj1HDzs6dO3Wer1ixAs7Ozjh16hTatm0rtVtbW0OtVpc7j927d+OPP/7A3r174eLigqZNm2L69OmYOHEipk6dCgsLi6e6DkRERFS9VatzdvLy8gAAjo6OOu1r166Fk5MT/Pz8EB0djTt37kjTEhIS4O/vDxcXF6ktNDQU+fn5+P33359N4URERFRtGXXPzoO0Wi3GjBmDoKAg+Pn5Se1vvPEGPDw84ObmhrNnz2LixIlITk7Gpk2bAABZWVk6QQeA9DwrK6vcZRUVFaGoqEh6np+fb+jVISIiomqi2oSdqKgoJCUl4ciRIzrtI0aMkP7v7+8PV1dXBAcHIy0tDd7e3notKzY2FjExMU9ULxERET0fqsVhrJEjR2L79u04cOAA6tSp88i+LVu2BACkpqYCANRqNbKzs3X6lD6v6Dyf6Oho5OXlSY/09PQnXQUiIiKqpowadoQQGDlyJDZv3oz9+/fDy8vrsa9JTEwEALi6ugIANBoNzp07h5ycHKnPnj17YG9vD19f33LnoVQqYW9vr/MgIiIieTLq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Dhw4gB07dqBx48YwNzfXmb5p0yaDFEdERET0pPQKOw4ODnj11VcNXQsRERGRwekVdpYvX27oOoiIiIieCr3O2QGA4uJi7N27F1999RVu374NAMjIyEBBQYHBiiMiIiJ6Unrt2bl69Sq6dOmCa9euoaioCJ06dYKdnR0+++wzFBUVIS4uztB1EhEREelFrz07o0ePRvPmzfHXX3/ByspKan/11Vexb98+gxVHRERE9KT02rPz888/49ixY2W+9NPT0xN//vmnQQojIiIiMgS99uxotVqUlJSUab9+/Trs7OyeuCgiIiIiQ9Er7HTu3Bnz58+XnisUChQUFOCTTz6RzVdIEBERkTzodRjriy++QGhoKHx9fXH37l288cYbSElJgZOTE7777jtD10hERESkN73CTp06dXDmzBl8//33OHv2LAoKCjB06FD0799f54RlIiIiImPTK+wAgJmZGQYMGGDIWoiIiIgMTq+ws2rVqkdOHzRokF7FEBERERmaXmFn9OjROs/v37+PO3fuwMLCAtbW1gw7REREVG3odTXWX3/9pfMoKChAcnIyWrduzROUiYiIqFrR+7uxHubj44NZs2aV2etDREREZEwGCzvAPyctZ2RkGHKWRERERE9Er3N2tm3bpvNcCIHMzEwsWrQIQUFBBimMiIiIyBD0Cjs9e/bUea5QKFCrVi107NgRX3zxhSHqIiIiIjIIvcKOVqs1dB1ERERET4VBz9khIiIiqm702rMzbty4SvedO3euPosgIiIiMgi9ws7p06dx+vRp3L9/Hw0aNAAAXLx4EaampmjWrJnUT6FQGKZKIiIiIj3pFXa6d+8OOzs7rFy5EjVq1ADwz40GhwwZgjZt2mD8+PEGLZKIiIhIX3qds/PFF18gNjZWCjoAUKNGDcyYMYNXYxEREVG1olfYyc/Px40bN8q037hxA7dv337iooiIiIgMRa+w8+qrr2LIkCHYtGkTrl+/juvXr+O///0vhg4dil69ehm6RiIiIiK96XXOTlxcHCZMmIA33ngD9+/f/2dGZmYYOnQo5syZY9ACiYiIiJ6EXmHH2toaS5YswZw5c5CWlgYA8Pb2ho2NjUGLIyIiInpST3RTwczMTGRmZsLHxwc2NjYQQhiqLiIiIiKD0Cvs3Lx5E8HBwahfvz66du2KzMxMAMDQoUN52TkRERFVK3qFnbFj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
"/>
</div>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [ ]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="n">same</span> <span class="n">but</span> <span class="n">using</span> <span class="n">outcome</span> <span class="o">=</span><span class="mi">0</span>
</pre></div>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Write-your-Answer-here:">Write your Answer here:<a class="anchor-link" href="#Write-your-Answer-here:">¶</a></h4>
</div>
</div>
</div>
</div>Ans 18:
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q-19.-What-is-the-Interquartile-Range-of-all-the-variables?-Why-is-this-used?-Which-plot-visualizes-the-same?-(5-Marks)">Q 19. What is the Interquartile Range of all the variables? Why is this used? Which plot visualizes the same? (5 Marks)<a class="anchor-link" href="#Q-19.-What-is-the-Interquartile-Range-of-all-the-variables?-Why-is-this-used?-Which-plot-visualizes-the-same?-(5-Marks)">¶</a></h2>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [42]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate variable name</span>

<span class="n">Q1</span> <span class="o">=</span> <span class="n">pima</span><span class="o">.</span><span class="n">quantile</span><span class="p">(</span><span class="mf">0.25</span><span class="p">)</span>
<span class="n">Q3</span> <span class="o">=</span> <span class="n">pima</span><span class="o">.</span><span class="n">quantile</span><span class="p">(</span><span class="mf">0.75</span><span class="p">)</span>
<span class="n">IQR</span> <span class="o">=</span> <span class="n">Q3</span> <span class="o">-</span><span class="n">Q1</span>
<span class="nb">print</span><span class="p">(</span><span class="n">IQR</span><span class="p">)</span>
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
<pre>Pregnancies                  5.0000
Glucose                     40.5000
BloodPressure               16.0000
SkinThickness               12.0000
Insulin                     48.2500
BMI                          9.1000
DiabetesPedigreeFunction     0.3825
Age                         17.0000
Outcome                      1.0000
dtype: float64
</pre>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>caculate IQR by Q3-Q1</p>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Write-your-Answer-here:">Write your Answer here:<a class="anchor-link" href="#Write-your-Answer-here:">¶</a></h4>
</div>
</div>
</div>
</div>Ans 19:
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h2 id="Q-20.-Find-and-visualize-the-correlation-matrix.-Write-your-observations-from-the-plot.-(3-Marks)">Q 20. Find and visualize the correlation matrix. Write your observations from the plot. (3 Marks)<a class="anchor-link" href="#Q-20.-Find-and-visualize-the-correlation-matrix.-Write-your-observations-from-the-plot.-(3-Marks)">¶</a></h2>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [43]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate function name and run the code</span>

<span class="n">corr_matrix</span> <span class="o">=</span> <span class="n">pima</span><span class="o">.</span><span class="n">iloc</span><span class="p">[</span> <span class="p">:</span> <span class="p">,</span><span class="mi">0</span> <span class="p">:</span> <span class="mi">8</span><span class="p">]</span><span class="o">.</span><span class="n">corr</span><span class="p">()</span>

<span class="n">corr_matrix</span>
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
<div class="jp-OutputPrompt jp-OutputArea-prompt">Out[43]:</div>
<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html" tabindex="0">
<div class="colab-df-container" id="df-d089e5bb-b4a1-4360-8e11-953bbb289e6e">
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
<th>Pregnancies</th>
<th>Glucose</th>
<th>BloodPressure</th>
<th>SkinThickness</th>
<th>Insulin</th>
<th>BMI</th>
<th>DiabetesPedigreeFunction</th>
<th>Age</th>
</tr>
</thead>
<tbody>
<tr>
<th>Pregnancies</th>
<td>1.000000</td>
<td>0.128022</td>
<td>0.208987</td>
<td>0.009393</td>
<td>-0.018780</td>
<td>0.021546</td>
<td>-0.033523</td>
<td>0.544341</td>
</tr>
<tr>
<th>Glucose</th>
<td>0.128022</td>
<td>1.000000</td>
<td>0.219765</td>
<td>0.158060</td>
<td>0.396137</td>
<td>0.231464</td>
<td>0.137158</td>
<td>0.266673</td>
</tr>
<tr>
<th>BloodPressure</th>
<td>0.208987</td>
<td>0.219765</td>
<td>1.000000</td>
<td>0.130403</td>
<td>0.010492</td>
<td>0.281222</td>
<td>0.000471</td>
<td>0.326791</td>
</tr>
<tr>
<th>SkinThickness</th>
<td>0.009393</td>
<td>0.158060</td>
<td>0.130403</td>
<td>1.000000</td>
<td>0.245410</td>
<td>0.532552</td>
<td>0.157196</td>
<td>0.020582</td>
</tr>
<tr>
<th>Insulin</th>
<td>-0.018780</td>
<td>0.396137</td>
<td>0.010492</td>
<td>0.245410</td>
<td>1.000000</td>
<td>0.189919</td>
<td>0.158243</td>
<td>0.037676</td>
</tr>
<tr>
<th>BMI</th>
<td>0.021546</td>
<td>0.231464</td>
<td>0.281222</td>
<td>0.532552</td>
<td>0.189919</td>
<td>1.000000</td>
<td>0.153508</td>
<td>0.025748</td>
</tr>
<tr>
<th>DiabetesPedigreeFunction</th>
<td>-0.033523</td>
<td>0.137158</td>
<td>0.000471</td>
<td>0.157196</td>
<td>0.158243</td>
<td>0.153508</td>
<td>1.000000</td>
<td>0.033561</td>
</tr>
<tr>
<th>Age</th>
<td>0.544341</td>
<td>0.266673</td>
<td>0.326791</td>
<td>0.020582</td>
<td>0.037676</td>
<td>0.025748</td>
<td>0.033561</td>
<td>1.000000</td>
</tr>
</tbody>
</table>
</div>
<div class="colab-df-buttons">
<div class="colab-df-container">
<button class="colab-df-convert" onclick="convertToInteractive('df-d089e5bb-b4a1-4360-8e11-953bbb289e6e')" style="display:none;" title="Convert this dataframe to an interactive table.">
<svg height="24px" viewbox="0 -960 960 960" xmlns="http://www.w3.org/2000/svg">
<path d="M120-120v-720h720v720H120Zm60-500h600v-160H180v160Zm220 220h160v-160H400v160Zm0 220h160v-160H400v160ZM180-400h160v-160H180v160Zm440 0h160v-160H620v160ZM180-180h160v-160H180v160Zm440 0h160v-160H620v160Z"></path>
</svg>
</button>
<style>
    .colab-df-container {
      display:flex;
      gap: 12px;
    }

    .colab-df-convert {
      background-color: #E8F0FE;
      border: none;
      border-radius: 50%;
      cursor: pointer;
      display: none;
      fill: #1967D2;
      height: 32px;
      padding: 0 0 0 0;
      width: 32px;
    }

    .colab-df-convert:hover {
      background-color: #E2EBFA;
      box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
      fill: #174EA6;
    }

    .colab-df-buttons div {
      margin-bottom: 4px;
    }

    [theme=dark] .colab-df-convert {
      background-color: #3B4455;
      fill: #D2E3FC;
    }

    [theme=dark] .colab-df-convert:hover {
      background-color: #434B5C;
      box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
      filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
      fill: #FFFFFF;
    }
  </style>
<script>
      const buttonEl =
        document.querySelector('#df-d089e5bb-b4a1-4360-8e11-953bbb289e6e button.colab-df-convert');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      async function convertToInteractive(key) {
        const element = document.querySelector('#df-d089e5bb-b4a1-4360-8e11-953bbb289e6e');
        const dataTable =
          await google.colab.kernel.invokeFunction('convertToInteractive',
                                                    [key], {});
        if (!dataTable) return;

        const docLinkHtml = 'Like what you see? Visit the ' +
          '<a target="_blank" href=https://colab.research.google.com/notebooks/data_table.ipynb>data table notebook</a>'
          + ' to learn more about interactive tables.';
        element.innerHTML = '';
        dataTable['output_type'] = 'display_data';
        await google.colab.output.renderOutput(dataTable, element);
        const docLink = document.createElement('div');
        docLink.innerHTML = docLinkHtml;
        element.appendChild(docLink);
      }
    </script>
</div>
<div id="df-2e81a688-7399-491c-9b63-8ceaf76938fb">
<button class="colab-df-quickchart" onclick="quickchart('df-2e81a688-7399-491c-9b63-8ceaf76938fb')" style="display:none;" title="Suggest charts">
<svg height="24px" viewbox="0 0 24 24" width="24px" xmlns="http://www.w3.org/2000/svg">
<g>
<path d="M19 3H5c-1.1 0-2 .9-2 2v14c0 1.1.9 2 2 2h14c1.1 0 2-.9 2-2V5c0-1.1-.9-2-2-2zM9 17H7v-7h2v7zm4 0h-2V7h2v10zm4 0h-2v-4h2v4z"></path>
</g>
</svg>
</button>
<style>
  .colab-df-quickchart {
      --bg-color: #E8F0FE;
      --fill-color: #1967D2;
      --hover-bg-color: #E2EBFA;
      --hover-fill-color: #174EA6;
      --disabled-fill-color: #AAA;
      --disabled-bg-color: #DDD;
  }

  [theme=dark] .colab-df-quickchart {
      --bg-color: #3B4455;
      --fill-color: #D2E3FC;
      --hover-bg-color: #434B5C;
      --hover-fill-color: #FFFFFF;
      --disabled-bg-color: #3B4455;
      --disabled-fill-color: #666;
  }

  .colab-df-quickchart {
    background-color: var(--bg-color);
    border: none;
    border-radius: 50%;
    cursor: pointer;
    display: none;
    fill: var(--fill-color);
    height: 32px;
    padding: 0;
    width: 32px;
  }

  .colab-df-quickchart:hover {
    background-color: var(--hover-bg-color);
    box-shadow: 0 1px 2px rgba(60, 64, 67, 0.3), 0 1px 3px 1px rgba(60, 64, 67, 0.15);
    fill: var(--button-hover-fill-color);
  }

  .colab-df-quickchart-complete:disabled,
  .colab-df-quickchart-complete:disabled:hover {
    background-color: var(--disabled-bg-color);
    fill: var(--disabled-fill-color);
    box-shadow: none;
  }

  .colab-df-spinner {
    border: 2px solid var(--fill-color);
    border-color: transparent;
    border-bottom-color: var(--fill-color);
    animation:
      spin 1s steps(1) infinite;
  }

  @keyframes spin {
    0% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
      border-left-color: var(--fill-color);
    }
    20% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    30% {
      border-color: transparent;
      border-left-color: var(--fill-color);
      border-top-color: var(--fill-color);
      border-right-color: var(--fill-color);
    }
    40% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-top-color: var(--fill-color);
    }
    60% {
      border-color: transparent;
      border-right-color: var(--fill-color);
    }
    80% {
      border-color: transparent;
      border-right-color: var(--fill-color);
      border-bottom-color: var(--fill-color);
    }
    90% {
      border-color: transparent;
      border-bottom-color: var(--fill-color);
    }
  }
</style>
<script>
    async function quickchart(key) {
      const quickchartButtonEl =
        document.querySelector('#' + key + ' button');
      quickchartButtonEl.disabled = true;  // To prevent multiple clicks.
      quickchartButtonEl.classList.add('colab-df-spinner');
      try {
        const charts = await google.colab.kernel.invokeFunction(
            'suggestCharts', [key], {});
      } catch (error) {
        console.error('Error during call to suggestCharts:', error);
      }
      quickchartButtonEl.classList.remove('colab-df-spinner');
      quickchartButtonEl.classList.add('colab-df-quickchart-complete');
    }
    (() => {
      let quickchartButtonEl =
        document.querySelector('#df-2e81a688-7399-491c-9b63-8ceaf76938fb button');
      quickchartButtonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';
    })();
  </script>
</div>
<div id="id_67073897-e5e1-4292-945d-f4f858a1b340">
<style>
      .colab-df-generate {
        background-color: #E8F0FE;
        border: none;
        border-radius: 50%;
        cursor: pointer;
        display: none;
        fill: #1967D2;
        height: 32px;
        padding: 0 0 0 0;
        width: 32px;
      }

      .colab-df-generate:hover {
        background-color: #E2EBFA;
        box-shadow: 0px 1px 2px rgba(60, 64, 67, 0.3), 0px 1px 3px 1px rgba(60, 64, 67, 0.15);
        fill: #174EA6;
      }

      [theme=dark] .colab-df-generate {
        background-color: #3B4455;
        fill: #D2E3FC;
      }

      [theme=dark] .colab-df-generate:hover {
        background-color: #434B5C;
        box-shadow: 0px 1px 3px 1px rgba(0, 0, 0, 0.15);
        filter: drop-shadow(0px 1px 2px rgba(0, 0, 0, 0.3));
        fill: #FFFFFF;
      }
    </style>
<button class="colab-df-generate" onclick="generateWithVariable('corr_matrix')" style="display:none;" title="Generate code using this dataframe.">
<svg height="24px" viewbox="0 0 24 24" width="24px" xmlns="http://www.w3.org/2000/svg">
<path d="M7,19H8.4L18.45,9,17,7.55,7,17.6ZM5,21V16.75L18.45,3.32a2,2,0,0,1,2.83,0l1.4,1.43a1.91,1.91,0,0,1,.58,1.4,1.91,1.91,0,0,1-.58,1.4L9.25,21ZM18.45,9,17,7.55Zm-12,3A5.31,5.31,0,0,0,4.9,8.1,5.31,5.31,0,0,0,1,6.5,5.31,5.31,0,0,0,4.9,4.9,5.31,5.31,0,0,0,6.5,1,5.31,5.31,0,0,0,8.1,4.9,5.31,5.31,0,0,0,12,6.5,5.46,5.46,0,0,0,6.5,12Z"></path>
</svg>
</button>
<script>
      (() => {
      const buttonEl =
        document.querySelector('#id_67073897-e5e1-4292-945d-f4f858a1b340 button.colab-df-generate');
      buttonEl.style.display =
        google.colab.kernel.accessAllowed ? 'block' : 'none';

      buttonEl.onclick = () => {
        google.colab.notebook.generateWithVariable('corr_matrix');
      }
      })();
    </script>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>we using corr to see the correlation between columns</p>
</div>
</div>
</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In [44]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
<div class="cm-editor cm-s-jupyter">
<div class="highlight hl-ipython3"><pre><span></span><span class="c1"># Remove _____ &amp; write the appropriate function name</span>

<span class="n">plt</span><span class="o">.</span><span class="n">figure</span><span class="p">(</span><span class="n">figsize</span> <span class="o">=</span> <span class="p">(</span><span class="mi">8</span><span class="p">,</span> <span class="mi">8</span><span class="p">))</span>
<span class="n">sns</span><span class="o">.</span><span class="n">heatmap</span><span class="p">(</span><span class="n">corr_matrix</span><span class="p">,</span> <span class="n">annot</span> <span class="o">=</span> <span class="kc">True</span><span class="p">)</span>

<span class="c1"># Display the plot</span>
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
<img alt="No description has been provided for this image" class="" src="data:image/png;base64,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CUpKSnB1dUWDBg3QrFkz+Pr64urVq6hSpYqiq0ZERERE/2eYASGUKlUKHh4e3w8kIiIiou/jbXjzxQwIERERERHJDTMgRERERESyxNvw5osZECIiIiIikht2QIiIiIiISG44BIuIiIiISJY4CT1fzIAQEREREZHcMANCRERERCRL2VmKrkGRxgwIERERERHJDTMgRERERESyxDkg+WIGhIiIiIiI5IYdECIiIiIikhsOwSIiIiIikiU+CT1fzIAQEREREZHcMANCRERERCRLnISeL2ZAiIiIiIhIbtgBISIiIiIiueEQLCIiIiIiWeIk9HwxA0JERERERHLDDAgRERERkSwxA5IvZkCIiIiIiEhumAEhIiIiIpIhkShL0VUo0pgBISIiIiIiuWEHhIiIiIiI5IZDsIiIiIiIZImT0PPFDAgREREREckNMyBERERERLIkYgYkP8yAEBERERGR3LADQkREREREcsMhWEREREREssRJ6PliBoSIiIiIiOSGGRCi72hTy07RVVCI6967FF0FhbCtP03RVVCIhvoVFF0FhRiRaaDoKijEFWG6oqugECHaCYqugkJsSjRUdBUUYq0id85J6PliBoSIiIiIiOSGGRAiIiIiIlniHJB8MQNCRERERERyww4IERERERHJDYdgERERERHJEieh54sZECIiIiIikhtmQIiIiIiIZImT0PPFDAgREREREckNOyBERERERCQ3HIJFRERERCRLHIKVL2ZAiIiIiIhIbpgBISIiIiKSJd6GN1/MgBARERERkdwwA0JEREREJEucA5IvZkCIiIiIiEhu2AEhIiIiIiK54RAsIiIiIiJZ4iT0fDEDQkREREREcsMMCBERERGRLHESer6YASEiIiIiIrlhB4SIiIiIiOSGQ7CIiIiIiGSJk9DzxQwIERERERHJDTMgRERERESyxEno+WIGhIiIiIiI5IYZECIiIiIiWWIGJF/MgBARERERkdywA0JERERERHLDIVhERERERLIkEim6BkUaMyBERERERCQ3zIAQEREREckSJ6HnixkQkimBQIDTp08ruhpEREREVEQxA0IF9vbtWzg7O+PcuXN49eoVdHV1YWlpiSFDhsDGxgYaGhqKrmKR1tOmOwba94OBsQFC/UKxft4m+HsFSo0tW7EMRk4djko1K8K8lBk2Om3BcZdTEjE9hlmj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zIAQEREREZHcMANCRERERCRDnAOSN2ZAiIiIiIhIbtgBISIiIiIiueEQLCIiIiIiGeKd0PPGDAgREREREckNMyBERERERDKUxUnoeWIGhIiIiIiI5IYdECIiIiIikhsOwSIiIiIikiFOQs8bMyBERERERCQ3zIAQfUPchyShQxBEoGa80CEI4lhcsNAhCMJTr7LQIQgkTegABNG51l9ChyCIix7bhQ5BEGXMuwgdQpHDSeh5YwaEiIiIiIjkhhkQIiIiIiIZ4hyQvDEDQkREREREcsMOCBERERERyQ2HYBERERERyVBmFieh54UZECIiIiIikhtmQIiIiIiIZIj5j7wxA0JERERERHLDDggREREREckNh2AREREREclQJgdh5YkZECIiIiKiImrbtm0wMzODqqoqGjRoADc3t1zr7tq1C82aNYOuri50dXVhaWmZZ/3csANCRERERCRDWQL+70ccPXoU06dPx+LFi/H48WPUrFkT7du3R3R0tNT6Li4uGDhwIG7evAlXV1eULl0a7dq1w6tXr37ouOyAEBEREREVQevXr8eYMWMwYsQIVK1aFXZ2dlBXV4eDg4PU+gcPHsRff/0FCwsLVKlSBbt370ZmZiacnZ1/6LicA0JEREREJEOZAh47NTUVqampEmUqKipQUVGRKPv48SPc3d0xd+5ccZmCggIsLS3h6ur6Xcd6//490tLSoKen90MxMgNCRERERFRI2NjYQFtbW+JhY2OTo15sbCwyMjJgbGwsUW5sbIzIyMjvOtbs2bNRokQJWFpa/lCMzIAQERERERUSc+fOxfTp0yXKvs5+yMKqVatw5MgRuLi4QFVV9Ye2ZQeEiIiIiEiGhFyGV9pwK2kMDAygqKiIqKgoifKoqCiYmJjkue0///yDVatW4fr166hRo8YPx8ghWERERERERUyxYsVQp04diQnknyaUN2rUKNft1qxZg//9739wcnJC3bp1f+rYzIAQEREREcnQjy6HK5Tp06dj2LBhqFu3LurXr4+NGzciOTkZI0aMAAAMHToUJUuWFM8hWb16NRYtWoRDhw7BzMxMPFdEQ0MDGhoa331cdkCIiIiIiIqg/v37IyYmBosWLUJkZCQsLCzg5OQknpgeFhYGBYXPA6ZsbW3x8eNH9OnTR2I/ixcvxpIlS777uOyAEBEREREVURMnTsTEiROlvubi4iLxPCQkRCbHZAeEiIiIiEiGhLwPyO+Ak9CJiIiIiEhumAEhIiIiIpKhrKzfYxK6UJgBISIiIiIiuWEGhIiIiIhIhoS8EeHvgBkQIiIiIiKSG3ZAiIiIiIhIbjgEi4iIiIhIhrgMb96YASEiIiIiIrlhBoSIiIiISIayOAk9T/mSARGJRDhz5sx311+yZAksLCzyI5QCafjw4ejRo4f4ecuWLTF16lTB4vkdfP03IyIiIqLf0w91QIYPHw6RSASRSARlZWUYGxujbdu2cHBwQGbm59FuERER6Nixo8yDzUtISAhEIhE8PT1lul8zMzNxm4sXL47atWvj+PHjMj3GqVOn8L///U+m+/xZjo6O4vZ++di9e7dcjp/bedy0aRMcHR3lEoMsLVk8E+Ghj/EuIRBXLh+BuXm5b24zYfwwBD7/F0mJQbh/9zzq1bWQeH37ttXwf3YP7xICEfHKG6dOOqBy5QpS96Wnp4uQ4EdI//gK2tpasmjSD+sxrBuOuB7A1cBL2H5+C6pYVM61rlmlsli6czGOuB6Ay8vr6DOqV577HvT3ALi8vI6JSybIOmwJY8Za4YnvbUS/eYYbLqdQp06NPOv36NkRjx5fQ/SbZ3B1u4x27VvmqDN/wVQ8D/oXUbG+OHthPypUMJN4XVdXG7sdNuBlhBfCXnli6/ZVKF5cXerxypcvi1eR3gh75SlRfvHyISQmB+d4HD9p/yPN/yFdh3XB3vuOOB9wFpvObUBli0q51i1bqQwW7piPvfcdcSX8MnqO6iG1nr6JPqw3zcJx76M4F3AGdte2o2KNivnUgp9TdNvdFfvu78WFgHPYfG7jN9pdFgt3LMC++3txNdxJarutpg3B1XAniYf9zV352IL89cjzCf62XoxW3QajWpOOcL59X+iQfsjw0QPh5n0NLyI9cPH6EVjUrp5n/S7d2+OO2wW8iPTAjXtn0Lptc4nXZ8z5G3fcLiDo1SM8C3HF0TP2qJXL52mxYsq4ducUIuJ98Wf1KjJrExUMP5wB6dChAyIiIhASEoLLly+jVatWmDJlCrp06YL09HQAgImJCVRUVGQerFCWLVuGiIgIeHh4oF69eujfvz/u35fdh4ienh40NTV/aR9paWkyigbQ0tJCRESExGPw4MEy2//P0NbWho6OjqAx/KhZM//CxL9H4q+Jc9C4aVckv3+PSxcO5vlvo2/fbvhn7WL8b/l61GvQAV7evrh08SAMDfXFdR4/9sboMdNRrUZLdOo8CCKRCJcvHoaCQs5/zrt2/oMnT3zzpX3fo1XXlvhr0Xg4btiPMR3HI8g3GGsPrIKOvo7U+ipqqogIi8BOm914E/Umz31XrlkZXQd3RqBvUD5E/lmv3p2xctU8rLLZjGZNuuLJk2c4dXYvDL44J1+q36A2HBw3Yd++Y2jauAsunr+KQ0fs8EfVzz/Mpk4fh3EThmPq5AVo3bIX3ie/x6mzjlBRKSaus9thA6r8URE9ug5Fvz6j0aRJfWzeujLH8ZSUlODguAmu9x/leG3IoAkwL19f/Khftz3S09Nx+vQlGfxlcmrRtTnGLhyLgxsP4u9OkxDs+wIr9i+Htr621PrZ5zsSDqv24E3UW6l1NLQ1sP7UOmSkp2PB0IUY03ocdv5vN5ISkvKlDT+jKLd73MIxOLDxAP7qNBHBvsFYuX8FdHJttwoiwyLhsMoh13YDQIh/CPrXHih+TOs1I7+akO8+fEhBZfPymD/jL6FD+WHdenbAkhWzsW71drRv0Qe+Pn44fGon9A30pNavW98CtvZrcWj/KbRr3htOl5yx5+AWVP7DXFwnODAE82atQKvGPdC9gxXCw17hyKld0NfXzbG/hctmIioiOt/al98ykSXY43fwwx0QFRUVmJiYoGTJkqhduzbmzZuHs2fP4vLly+Ir1F8PwZo9ezYqVaoEdXV1lC9fHgsXLpT6g3nHjh0oXbo01NXV0a9fPyQkJEi8vnv3bvzxxx9QVVVFlSpVsH37dvFr5cplX1muVasWRCIRWrZs+V3bffz4ERMnToSpqSlUVVVRtmxZ2NjYSBxXU1MTJiYmqFSpErZt2wY1NTWcP38eABAeHo5+/fpBR0cHenp66N69O0JCQsTbZmRkYPr06dDR0YG+vj6sra2RlSX55vh6CFZERAQ6d+4MNTU1lCtXDocOHYKZmRk2btworiMSiWBra4tu3bqhePHiWLFiBQDg7NmzqF27NlRVVVG+fHksXbpU3DEEgPj4eIwePRqGhobQ0tJC69at4eXlJRGPSCSCiYmJxENNTQ2Ojo45OgFnzpyBSCQSP/80nG7//v0wMzODtrY2BgwYgHfv3onrZGZmYs2aNTA3N4eKigrKlCkjjj+38/j1EKzU1FRMnjwZRkZGUFVVRdOmTfHw4UPx6y4uLhCJRHB2dkbdunWhrq6Oxo0bw9/fH/IyedJorLTZhPPnr+LJk2cYPmIKSpQwRvfu7XPdZtqUMdhtfwh79x3Ds2cB+OvvOXj//gNGDB8grrPb/iDu3H2A0NCX8PD0waLFa1CmTEmYmZWW2Ne4sUOho62F9Rt25Fsbv6Xv2N64ePgSnI5dQWhAGNbP2YiUlFR0GtBBan1/L3/YLd+JG+dckPYx9061mroqFmyZi3+sN+T7D7KJk0Zh756jOLj/BPz9AjF18gJ8+PABVkP7Sq0/4a/huH7tNjZv3IXn/kFY/r8N8PJ8irHjhorr/PX3CKxdsxWXLl7HUx8/jBszE6amxujStR0AoFLlCmjbriUm/TUXjx554V/XR5g1cwl69+kCExMjieMtXDwDz58H4dSpizliiYtLQHRUrPjRunVTvH//AWdO5U8HpNeYnnA6fBlXj11DWEAYNs/dgtSUVLTv305q/edez7F7hT1unbuV6/nuN6EvYiNisG7GBvh7PkdUeBQe336MiNCIfGnDzyiq7e49phcuH3YSt3uTuN3SP+Oeez3HrhW74ZJHuwEgIz0DcTFx4kdiXGJ+NSHfNWtUD5PHDoNliyZCh/LDxv09HAf3HsfRg6fx3D8I1tOW4sP7FAwcIj0zPXq8FW5evwvbLQ4IeB6MNSu24ImXL0aO+XwB8/SJi7hzyxVhoS/x3C8QS+avhpa2Jv74UzIz3tqyGVq0aoxlC9fmaxtJODKZA9K6dWvUrFkTp06dkvq6pqYmHB0d4evri02bNmHXrl3YsGGDRJ3AwEAcO3YM58+fh5OTEzw8PPDXX5+vGBw8eBCLFi3CihUr8OzZM6xcuRILFy7E3r17AQBubm4AgOvXryMiIkIcy7e227x5M86dO4djx47B398fBw8ehJmZWa5tVVJSgrKyMj5+/Ii0tDS0b98empqauHPnDu7duwcNDQ106NABHz9+BACsW7cOjo6OcHBwwN27d/H27VucPn06z7/n0KFD8fr1a7i4uODkyZPYuXMnoqNzXgVYsmQJevbsiSdPnmDkyJG4c+cOhg4diilTpsDX1xc7duyAo6Oj+Mc9APTt2xfR0dG4fPky3N3dUbt2bbRp0wZv3+Z+NepHBQUF4cyZM7hw4QIuXLiAW7duYdWqVeLX586di1WrVmHhwoXw9fXFoUOHYGxsDCD38/g1a2trnDx5Env37sXjx49hbm6O9u3b52jH/PnzsW7dOjx69AhKSkoYOXKkzNqZl3LlysDU1BjON+6KyxIT38HNzQMNG9SRuo2ysjJq164B5xt3xGVZWVlwvnEXDRtK30ZdXQ3Dh/ZHcHAowsNfi8v/+KMiFsyfiuEjp0gMj5QnJWUlVK5eCe53HovLsrKy4H7nMarWrvpL+56yYjL+dX4A97uPv135FygrK8OiVjXcvHlPXJaVlQWXm/dQv34tqdvUb1AbLl/UBwDn63dQv0F2fTOz0jAxMZKok5j4Do8eeorr1G9QG3FxCfDweCKuc/PGPWRmZqJuPQtxWfMWjdCjZ0fMmLb4u9pjNawfTp64gPfvP3xX/R+hpKyEitUr4vFdT3FZVlYWPO54omqdP356vw3bNsRz7wDMt52Hox6Hse3yVnQcKL0DK4Si3m6Pux7isux2e+CPX2g3AJQsVxKHHx3E3rt7MGezNQxLGP5quPSDlJWVUcOiKu7c+ldclpWVhTu3XFGnvoXUberWs8CdW64SZS437qFO/Zq5HmPIsH5ISEiEr4+fuNzAUB9rNy3FpHFz8P6D7D+r5CUrK0uwx+9AZqtgValSBd7e3lJfW7Bggfi/zczMMHPmTBw5cgTW1tbi8pSUFOzbtw8lS5YEAGzZsgWdO3fGunXrYGJigsWLF2PdunXo1Su7512uXDnxj+xhw4bB0DD7A0pfXx8mJibi/X5ru7CwMFSsWBFNmzaFSCRC2bJlc23jx48fsW7dOiQkJKB169Y4evQoMjMzsXv3bnEWYM+ePdDR0YGLiwvatWuHjRs3Yu7cueLj29nZ4cqVK7kew8/PD9evX8fDhw9Rt25dANkZnIoVc477HTRoEEaMGCF+PnLkSMyZMwfDhg0DAJQvXx7/+9//YG1tjcWLF+Pu3btwc3NDdHS0eBjQP//8gzNnzuDEiRMYO3YsACAhIQEaGhri/WpoaCAyMjLXmL+WmZkJR0dH8bAyKysrODs7Y8WKFXj37h02bdqErVu3iuOsUKECmjZtCgC5nscvJScnw9bWFo6OjuK5Rrt27cK1a9dgb2+PWbNmieuuWLECLVq0AADMmTMHnTt3RkpKClRVVb+7PT/DxDj7KnVUVIxEeVR0bI4r2J8YGOhBSUkJ0VGxEuXR0TGo8tUcj/HjhmGVzXxoaBSHn38gOnQaKM4qFitWDAf2b8fsucsRHv4a5cvl/p7OT9p62lBUUsTbmDiJ8rjYOJQxL53LVt/WultLVKpeEeM75/+QBn19XSgpKSEm+utzEotKlaTPuzE2NkC0lPrGxtnvbaP//l9aHSOj7NeMjQwRGyM5BC0jIwNxcfHi/ejp6cB2x1qMGTUN7959OwtUp04N/PlnZUycMPubdX+Glp4WFJUUES/lfJc2L/XT+zUtY4IuQzrj1O5TOLL1KCrVrIQJy8YjLS0d109c/9Wwf1lRb3dcTLxEeVxsPEr/wr9vPw8/rJ2+Di+DXkLPWA9Dpg7G+pP/YKzleHxI/n1/jP5u9PR1pH72xUS/gXnF8lK3MTQ2QEz0m6/qx8LIyECizLJ9C9jZr4OauiqiImPQv8dovH0bL3590/aV2L/nKLw8n6JUmRKyaRAVODLrgGRlZUkMxfnS0aNHsXnzZgQFBSEpKQnp6enQ0pKcEFumTBlx5wMAGjVqhMzMTPj7+0NTUxNBQUEYNWoUxowZI66Tnp4ObW3pY02B7B+q39pu+PDhaNu2LSpXrowOHTqgS5cuaNdOMm0+e/ZsLFiwACkpKdDQ0MCqVavQuXNnzJo1C4GBgTnmb6SkpCAoKAgJCQmIiIhAgwYNxK8pKSmhbt26ufZQ/f39oaSkhNq1a4vLzM3Noaubc3zkpw7KJ15eXrh3755ExiMjIwMpKSl4//49vLy8kJSUBH19ybHrHz58QFDQ53H0mpqaePz485VlaXML8mJmZibxNzE1NRVncJ49e4bU1FS0adPmh/b5paCgIKSlpaFJk88pbWVlZdSvXx/Pnj2TqFujxufJbaampgCA6OholClTRuq+U1NTkZqaKlGW13v7k4EDe8J222rx827dh+ZR+9cdOnwK151vw9TECNOnj8fhQ3Zo3qIHUlNTsXL5XPj5BeDQIenZo9+ZoakhJi79GzMHWeNjquzmPf2ONm+1wfFj53D/3sNvV0Z29sPHxw/u7tIvFBVUIgURArwDsGd1dtY66GkQzCqXRechnQrED/H8UlTb/dDl81ymF34v4OfhhwOu+9CiS3M4Hc394h39Pu7dcYNls17Q09fB4GF9sdNxPTq1GYA3sW8xatwQaGioY/P633fhAfo+MuuAPHv2TDx+/0uurq4YPHgwli5divbt20NbWxtHjhzBunXrvnvfSUnZV/d27dol8WMeABQVFX9pu9q1a+PFixe4fPkyrl+/jn79+sHS0hInTpwQ1501axaGDx8ODQ0NGBsbi3+MJiUloU6dOjh48GCOY3+6kp+fihcvLvE8KSkJS5cuFWdbvqSqqoqkpCSYmprCxcUlx+tfzu1QUFCAubl5jjoKCgo5Ok7S5vIoKytLPBeJROJhQGpqarm2Jz98Gcun85bXkCQbGxssXbpUokykoAGRYt4rSJ0/fxVubp+HInyaTGxsbIjIyM/D54yNDODp9VTqPmJj3yI9PR1GxpJXi4yMDBH5VSYlMfEdEhPfITDwBf598Bix0b7o0aMDjh49i5atmqB6tSro3auzRLujIp7AZtVmLF32/f/2fkXC2wRkpGdAz1Cy86xroIu30XG5bJW3yjUqQs9QF7su24nLFJUUUaNBdfQc3gNty3eU6ZCzN2/ikJ6eDkOjr8+JQY7s1idRUTmv+H1ZP/q//zcyMkBUZIxEnU8LBkRFx+SY5K6oqAhdXR3xfpq3aIROndtg8pTRALLPs6KiIt4mPMfkSfNxYN/n1frU1dXQu09XrFwuOfRVlhLfJiIjPQM6Us53XMzPnW8AeBv9FqEBYRJl4YHhaNqpYIypL+rt1jXUkSjXNdDJkfX8FcmJyXj54hVKmPFKuDy9fRMv9bPP0Eg/R/b2k5ioWBga6X9VP2dG+MP7Dwh5EYaQF2F4/Mgb99wvY5BVb2zZsAtNmzdAnfoWCI32lNjG6eYxnDp+AVMmzPv1xskJ74SeN5nMAblx4waePHmC3r1753jt/v37KFu2LObPn4+6deuiYsWKCA0NzVEvLCwMr19/HsP+77//QkFBAZUrV4axsTFKlCiB4OBgmJubSzw+dXqKFcv+wZeRkSHex/dsB2Sv+tS/f3/s2rULR48excmTJyXmEhgYGMDc3BwmJiYSV8Jr166NgIAAGBkZ5di/trY2tLW1YWpqigcPHoi3SU9Ph7u7e65/y8qVKyM9PR0eHp9/zAYGBiIu7tsf6LVr14a/v3+OWMzNzaGgoIDatWsjMjISSkpKOV43MDD45v4NDQ3x7t07JCcni8t+dNnjihUrQk1NDc7OzlJfl3Yev1ahQgUUK1YM9+59HkOflpaGhw8fomrVX5tbMHfuXCQkJEg8RArfXqEsKSkZQUEh4oev73NEREShdaum4jqamhqoX78W/n0g/fynpaXh8WNviW1EIhFat2qKf//N/T3zaalklWLZw+r69R+D2nXbok69dqhTrx3GjpsJAGjZqhe22zp+z59BJtLT0uH/5DlqN/2czROJRKjTtBZ8H//cylzudz0wos1ojG4/Tvzw8/TH9dPOGN1+nMznu6SlpcHTwwctWzYWl4lEIrRo2Viiw/kltweP0eKL+gDQqnUTuD3Irh8SEo7IyGiJOpqaGqhbz0Jcx+3BY+jqasPCopq4TouWjaCgoIBHDz0BAJate6NJoy7ix4r/bUBi4js0adQFF85JXinu0asTVFSK4eiRMz/9t/iW9LR0BDwJQK0mFuIykUgEi6YW8HV/lvuG3+D7yBelK0gOZSpZviSiXxaM1XGKerstpLT72S+0+2uq6qowLWuKt9Gym6dI35aWlgZvT180bdFQXCYSidC0eUO4u3lK3ebRQ0+J+gDQvGUjuLt5Sa3/iYKCCMX+u2i3YPZKtGnaE5bNesGyWS8M6TseADB+5Ays+t+mX2gRFTQ/nAFJTU1FZGQkMjIyEBUVBScnJ9jY2KBLly4YOjTnsJOKFSsiLCwMR44cQb169XDx4kWpk7BVVVUxbNgw/PPPP0hMTMTkyZPRr18/8TyApUuXYvLkydDW1kaHDh2QmpqKR48eIS4uDtOnT4eRkRHU1NTg5OSEUqVKQVVVFdra2t/cbv369TA1NUWtWrWgoKCA48ePw8TE5LuWfB08eDDWrl2L7t27Y9myZShVqhRCQ0Nx6tQpWFtbo1SpUpgyZQpWrVqFihUrokqVKli/fj3i4+Nz3WeVKlVgaWmJsWPHwtbWFsrKypgxYwbU1NS+OQxo0aJF6NKlC8qUKYM+ffpAQUEBXl5e8PHxwfLly2FpaYlGjRqhR48eWLNmDSpVqoTXr1/j4sWL6NmzZ44hXV9r0KAB1NXVMW/ePEyePBkPHjz44XtzqKqqYvbs2bC2tkaxYsXQpEkTxMTE4OnTpxg1alSu5/FLxYsXx4QJEzBr1izo6emhTJkyWLNmDd6/f49Ro0b9UDxfU1FRybFM7rf+7rnZvGU35s2djIDAYISEhGPpkll4/ToKZ89+/nF41ekozpy9LO4YbNi0C3vsN8D9sTcePvTA5EljULy4Ghz3HgWQPbm9X99uuHbtFmJi36BUyRKwtv4bHz6k4LJTdqcuOFiyg2+gn71k4jO/ACQkyHc1meM7T2LuBmv4e/njmac/+ozuBVU1VVw+6gQAmLtxNmIjY7FrVfZ9KZSUlWBWsaz4vw1MDWBetQI+vP+AVyGv8SH5A174h0gcI+VDChLjEnOUy8rWLfaw2/kPPDye4NEjL/z19wioq6vjwP7sLOmOXf/g9esoLF2cvVqL7XZHXL5yGBMnj8IVp5vo06cratWujsmT5ov3uX3bHsyynoigwBCEhr7EgoXTEBERhQvnrwIAnvsH4dpVF2zethLTJi+AkrIy/lm3FCdPXBBn1J77Sy4/XKt2dWRmZuGZ7/McbRg6tB8unr8qMc46P5zadRoz18/Ac+8A+Hv6o+eoHlBVU8HVY9cAALM2zEBs5BvsWe0IIPscl6mYPRxSuZgS9E30Ub5qeaS8/4DXIdmrPZ3afQYbTq/DgIn9cfvCbVS2qIxOgzpi4+zN+dqWH1FU231y1ynMWj8TAd4B8PP0R69RPaGqpoorx7Lfx7M2zMSbyDdwWL0HQM52G5gY5Gj3mAWj8e/1B4h+GQ19Yz0MnW6FzIwM3DzrIkgbf9X79x8Q9vLzxdVXr6Pg9zwI2lqaMM1lPmBBsWObIzbZ2sDLwwee7k8wZsJQqBdXw5GD2b/hNtvZIPJ1NFYuy86s7rbbj1MX92LcxOFwvnIL3Xt3Qs1a1TBravYiGWrqapg6YxyuXL6B6KhY6OnpYPiYQTAxNcb5M9nfi69eSq7ylpz8HgAQ8iIcEa+j5NV0meCd0PP2wx0QJycnmJqaQklJCbq6uqhZsyY2b96MYcOGSZ0r0K1bN0ybNg0TJ05EamoqOnfujIULF2LJkiUS9czNzdGrVy906tQJb9++RZcuXSSWyx09ejTU1dWxdu1azJo1C8WLF0f16tXFy9cqKSlh8+bNWLZsGRYtWoRmzZrBxcXlm9tpampizZo1CAgIgKKiIurVq4dLly5917wHdXV13L59G7Nnz0avXr3w7t07lCxZEm3atBHPcZkxYwYiIiLEf5+RI0eiZ8+eOZYY/tK+ffswatQoNG/eHCYmJrCxscHTp0+/OXG6ffv2uHDhApYtW4bVq1dDWVkZVapUwejRn4doXLp0CfPnz8eIESMQExMDExMTNG/eXLwKVV709PRw4MABzJo1C7t27UKbNm2wZMkS8eT177Vw4UIoKSlh0aJFeP36NUxNTTF+fPZVjtzO49dWrVqFzMxMWFlZ4d27d6hbty6uXLkida6MUNb+sx3Fi6vDbvsa6Oho4d69h+jcdYjEHJPy5cvC4Is11Y8fPwdDAz0sWTQTJiaG8PJ6is5dhohT2CkpqWjapD4mTxoNXV1tREXF4s7df9GsRXfExOR93wwh3DzvAh19bYyYORx6hroI9A2CtdVcxMXGAwCMSxoh64ushYGxPnZf/bxs8IDx/TBgfD94unphal9h7gVw6uRFGBjoYd6CaTA2NsAT72fo3WO4eHJmqVIlJDIvbg8eY9SIqVi4aAYWL5mJoKAQDBowXqJjsHH9DhRXV8PmrSuhra0FV9dH6N1jBFJTP4rrjB45Df+sX4pzFw8gMzML5846wXqm5PDA72FesRwaN6mH7l3zd14SANw6fxvaetoYOmMIdA31EOwbhPlWCxH/3/k2LGmEzC+Gceob68H2yjbx877j+6Dv+D7wcvWGdb/syfLPvZ5j2Zj/YcSc4Rg8ZRAiwyNht2QHbp65me/t+V5stxV0DXUR7BuM+VYLxO02KmkkMWxX31gfdlc+f69/2e5Z/bIXpTE0NcC8rXOgqaOJhLcJePrwKaZ0n4aEt7l/ZxZkPn4BGDnp88IPa7bsBAB072iJFQsK9v1Nzp12gr6BHqznTYKhkQGePvHDoN7jxAtklCxlKvHZ98jNE3+NtsbsBZMxd+FUvAgKxYjBk+D/LBAAkJmRAfNK5dB34Cbo6esi7m08PD180KOjFZ77BQrSRhKOKOt3Wa+rCHv58iVKly6N69ev/9Lkbfo5SsVKfrtSIdTU6NeW0vxdPY4LFjoEQTTSy/0O9VT4FNWrsxc9tn+7UiFUxryL0CEIIiJeuBvxWpbO/Z5f+e16eMFfsEFmk9BJdm7cuIGkpCRUr14dERERsLa2hpmZGZo3by50aEREREREv4QdkAIoLS0N8+bNQ3BwMDQ1NdG4cWMcPHgwx+pSRERERES/G3ZACqD27dujfXvhUndERERE9PM4wyFvMlmGl4iIiIiI6HswA0JEREREJEOZRXShh+/FDAgREREREckNOyBERERERCQ3HIJFRERERCRDRfVeO9+LGRAiIiIiIpIbZkCIiIiIiGQok8vw5okZECIiIiIikhtmQIiIiIiIZIj5j7wxA0JERERERHLDDggREREREckNh2AREREREckQ74SeN2ZAiIiIiIhIbpgBISIiIiKSIWZA8sYMCBERERERyQ07IEREREREJDccgkVEREREJENZvBN6npgBISIiIiIiuWEGhIiIiIhIhjgJPW/MgBARERERkdwwA0JEREREJENZzIDkiRkQIiIiIiKSG3ZAiIiIiIhIbjgEi4iIiIhIhrgMb96YASEiIiIiIrlhBoSIiIiISIa4DG/emAEhIiIiIiK5YQeEiIiIiIjkhkOwiIiIiIhkiJPQ88YMCBERERERyQ0zIETfEPBHVaFDEMSWBH2hQxBEF30ToUMQxOqEh0KHIIhiCkXzazA9M0PoEARRxryL0CEIIizwgtAhFDmchJ43ZkCIiIiIiEhuiualHyIiIiKifJLFDEiemAEhIiIiIiK5YQeEiIiIiIjkhkOwiIiIiIhkKJPL8OaJGRAiIiIiIpIbZkCIiIiIiGSIk9DzxgwIERERERHJDTsgREREREQkNxyCRUREREQkQ5yEnjdmQIiIiIiISG6YASEiIiIikiFOQs8bMyBERERERCQ3zIAQEREREckQ54DkjRkQIiIiIiKSG3ZAiIiIiIhIbjgEi4iIiIhIhjgJPW/MgBARERERkdwwA0JEREREJEOchJ43ZkCIiIiIiEhu2AEhIiIiIiK54RAsIiIiIiIZ4iT0vDEDQkREREREcsMMCBERERGRDGVlZQodQoHGDAgREREREckNMyBERERERDKUyTkgeWIGhIiIiIiI5IYdECIiIiIikhsOwSIiIiIikqEs3gk9T8yAEBERERGR3DADQkREREQkQ5yEnjdmQIiIiIiISG7YAaECy9XVFYqKiujcubPQociMZv9uKHVpP8q6XYTpgc0oVq1yrnU1urVDOa9rEo+ybhdzra+/YArKeV2D1uCe+RH6L2li1Q4L7m7Bav99mHJmOcrUrJBr3YYDWmPisSVY7rUby712Y/yB+Tnqrw85IvXRamyX/G7KD7EYaokx9zZg6nMHDD67BCY1y+dat2KHuhhyYRkmPtmBKX67MfTyClTt1USiTuNpvTDixhpM8duNiU92oO+hOTCxyP1vKQ8jRw+Cu7czwqO84eR8DLVqV8+zfrceHXD/4WWER3nj1v1zsGzbXPyakpISFi6diVv3zyHktQee+N3BVrvVMDYxktjHtJnjcfHqYYRGeCIw9GG+tOtbho0eiH+9riIo4jHOXzsMi2+0u0v3drj14DyCIh7j+r3TaN22mcTr02f/hVsPziPg5UM8fXEfR07vRq06kvssX6EsHA5uwZPAu/ALfYDTl/ejcdP6Mm9bXkaMHoSH3s4IjfLCZeej3zzfXXu0x92HlxAa5QWX++fQ5qvzvWDpDLjcP4cXrx/Dy+82ttitynG+AcCyXQtcdj6KkEhP+Ic+gOPBrTJvW16Gjx4IN+9reBHpgYvXj3zH+W6PO24X8CLSAzfunUHrL9oNADPm/I07bhcQ9OoRnoW44ugZe9SqU0PqvooVU8a1O6cQEe+LP6tXkVmb8tMjzyf423oxWnUbjGpNOsL59n2hQ6IChh0QKrDs7e0xadIk3L59G69fvxY6nF9WvH0L6M8ch/gdB/B6wAR89A+Gia0NFPR0ct0m810ywlr3Ez/COwyWWk+9dROoVP8D6dGx+RT9z7Po0gjdF1jhyqYTWN95Ll77hmLsvrnQ0NeSWr9Cw6p4fO4etg/8Hzb3WoT4iDcYt38etI11xXUW1xsn8Tg8yxaZmZnwuuwmr2Z9U+WuDdBy4WC4bjyN/Z0XIPpZGPocmA31XNqdEp+Mf7ecw6GeS+HYfh58jt9Gh3/Gwqz55x86b4Mj4LxoLxzbzcXh3suQEB6LvgdmQ01PU17NktCjV0csWzkX/6zehjbNe+Kpjx+OnbaHgYGe1Pr16tfCDvt1OLj/BFo364HLF52x99A2VPmjIgBATV0VNWpWxfq1tmjTvBeGD5kI84rlcOCIrcR+lJWVce6MExztD+d7G6Xp1rMDFi+3xvrV29GhZV/4+vjj4Mkd0M+l3XXrW2Db7rU4fOAU2rfogysXb8D+wBZU/sNcXCc4KBQLrFegTZOe6NnRCuFhr3Do1C7o6X9+3+89sh1KSoro130kOrbKPu7eI9tgaGSQ720GgO69OmLpyjlYt3ob2jbvhac+/jhyeneu57tu/Vqws1+HQ/tPwLJZT1y+eB2Oh7ZKOd/bYdm8N0YOmQTziuWw78h2if107tYOW3euxuGDp9C6SQ90bTcIp05cyPf2ftKtZwcsWTEb61ZvR/sWfeDr44fDp3bmeb5t7dfi0P5TaNe8N5wuOWPPwa/Od2AI5s1agVaNe6B7h+zzfeTULuh/cb4/WbhsJqIiovOtffnhw4cUVDYvj/kz/hI6FMFkZWUJ9vgdiLJ+l0ipSElKSoKpqSkePXqExYsXo0aNGpg3b5749XPnzmHGjBkIDw9Ho0aNMHz4cAwfPhxxcXHQ0dEBANy9exdz587Fo0ePYGBggJ49e8LGxgbFixf/oVhe1GwrkzaZHtiMj0+f443Nf1fuRCKUvnoIiYfPIMHhaI76Gt3aQW/WBIQ1yzujoWikjxIHtiBywlwYb1mOxIOnkHjw9C/HuyVB/5f3AQBTzixHuFcQTi3eAwAQiURY5LoNd/Y64YbtuW9uL1IQYYWXPU4t3oNHp+5IrTNi5wyoFFeD3eDlvxxviUzZTI0bfHYJIr2C4bxoX3aBSIRxDzbBw/Ea3Laf/659WF1cjuAbnri37oTU14tpqGGy7y4cG2iDsHtPfyne1Qk/nklwcj4Gz8dPMGfW/wBkn1sv31vYvXM/Nm/YlaP+rj0boK6uhsH9x4vLLl8/Cp8nfpg1bbHUY1jUro5rN0/A4s+WePUyQuK1AYN6YrnNPJiXrffDsX9STOHHz/f5a4fh5eGDBdYrAGS3+6GPM/bsOoRtG3fnqG9r/w/Ui6th2IC/P+/j6iE89fHDnOnLpB5DQ7M4/MPc0L/7SNy9/QC6ejrwCbqHnp2s4Ob6GABQXEMdz8MfYkCPUbhz698fakN6ZsYP1QeAy85H4fHYB/O+ON8evi6w33kAW6Sc75171kNdXR1Dvjjfl64fgc8TP1hPWyL1GBa1q+HKzROo/WcrvHoZAUVFRTx64oy1NltwaP/JH475awqiH7/uevH6EXg+foL5X5xv96c34LDzILZKOd92Duugrq6GoQM+//i+cO0wnj7xw+zpS6UeQ0OzOALCH6Jvt5G4e/vzuWxt2QxLVlhj9NCpuPXgPCyb9cLTJ34/3IawQPl12L5WrUlHbLJZiDbNG8v92MoGuWed81tJ3T8FO/aruF/7PpAHZkCoQDp27BiqVKmCypUrY8iQIXBwcBD36l+8eIE+ffqgR48e8PLywrhx4zB//nyJ7YOCgtChQwf07t0b3t7eOHr0KO7evYuJEycK0RxASQkqf1TCh38ffy7LysKHfx9DpUbVXDdTUFdD6csHUPrKQRhtXArlCmUlK4hEMFwxGwmOx5EWFJpPwf88RWVFlKpWDs/vPRGXZWVl4fm9JzCrXem79lFMTQWKykp4H58s9XUNA21UbVULbkdvyiRmWVBQVoRx9XIIvfvFl0BWFsLuPkWJ2ua5b/iFMk3+hF4FE7x0k/5jQ0FZETUGtUJKQjJifOV/7pWVlVHT4k/ccvk8tCIrKwu3Xe6jbr1aUrepW88Ct11cJcpuOt9F3XoWuR5HS0sDmZmZSEhIlEncv0pZWRk1LKrizhftyMrKwt1b/6JOvZpSt6lT3wJ3XCQ7CC437qFOLu1WVlbG4GF9kZCQiKc+/gCAuLfxCHwejD79u0NNXQ2KiooYMrwfYqJj4e3pK5vG5SG73X/iTo7z7Zrr+atTzwK3XSSH3tx0vveN860pcb5r1KyKEiVNkJmZhet3TsHb/zYOndgpzqLkN/H5/qKDl5WVhTu3XFGnvoXUberWs8CdW5Lvc5cb91CnvvT3h7KyMoYM64eEhET4+nz+925gqI+1m5Zi0rg5eP/hw683huQqMytLsMfvgKtgUYFkb2+PIUOGAAA6dOiAhIQE3Lp1Cy1btsSOHTtQuXJlrF27FgBQuXJl+Pj4YMWKFeLtbWxsMHjwYEydOhUAULFiRWzevBktWrSAra0tVFVV5doeRV1tiJQUkfEmTqI8400clMuVlrpNWkg4Yhf/g48BL6CgURzaw/qgxN5NeNlrNDL+G2qlPaI/kJGJxEO/nvHID8V1taCopIh3sQkS5e9iEmBUoeR37aPLnEFIiIqT6MR8qV7v5khNToH3lYIz/EpNTxMKSopI/qrdybEJ0Ktgmut2xTTVMN5tCxSLKSErIxPXFzgi9I6PRJ3ybSzQZetEKKsVQ1J0PE4MXo0PcUn50o686OnrQklJCTHRbyTKo2PewLyS9KuORsYGiP5qmGBMzBsYGUsfQqSiUgyLls7EqRMXkfROegdU3vT0daCkpITYGMl2x8S8QYWK5aRuY2hkgJiv6sfGvIGhkWSW0bJ9C2zf/Q/U1FURFRmDgT3HIO5tvPj1AT1Hw/7AZjwPd0NmZiZiY95icJ9xcumc5Xa+Y2JiUbGS9HYbGRtIrZ/X+V6wdCZOf3G+y/73+Thzzt9YPH81wsNeYcLEETh1cR8a1+mA+LgEqfuSlU/nO+br9230G5hXlP4+N5TW7uhYGH01VM6yfQvY2a8Tn+/+PUbj7Rfne9P2ldi/5yi8PJ+iVJkSsmkQUQHBDAgVOP7+/nBzc8PAgQMBZE9U7N+/P+zt7cWv16snOeSifn3JiZheXl5wdHSEhoaG+NG+fXtkZmbixYsXuR47NTUViYmJEo/UzEwZt/D7pHo/Q9KF6/joH4QUd29ETV+KjLh4aPbNnpRf7I+K0BrcEzEL1woSnzy0ntANtbo2xp5x65Cemia1Tv1+LeF+5m6ur/9OPialYF+H+TjQdRHurj2OlgsHo3TDPyTqhN9/hn0d5uNQz6UIcfFG1+0Tc51X8jtTUlLCbsdNEIlEmDVd+vCswubeHTe0a94b3dsPhovzXdjtWScxz2DF2gWIjX2Lnp2GonObAbhy6Qb2Ht6W6w/634mSkhJ2OW6ESARYT18iLv80ZGrTuh24eO4qvD2fYspfc5GVlYWuPToIE6yM3LvjBstmvdC13SDcdL6LnY7rxed71Lgh0NBQx+b1OYe2ERUG7IBQgWNvb4/09HSUKFECSkpKUFJSgq2tLU6ePImEhO+72pWUlIRx48bB09NT/PDy8kJAQAAqVMh91SAbGxtoa2tLPGyjc++wfK+MuARkpWdA8asJhor6usiIjctlq6+kZ+CjXxCUS2dnDlRrV4Oing5KOx2EmbsTzNydoFzSBHozxqHUpf2/HLMsJMclIiM9A5oG2hLlmobaeBcTn+e2Lcd0QZsJ3WFntRIRfmFS65SrVwXGFUriwdEbsgpZJj68fYfM9AwU/6rdxQ20kRyTx3s4KwvxoVGI8Q3Do12X8fzSQ9T/u6tElbQPqYgPjUKERxCuWO9GZkYmqg1okR/NyNPbN3FIT0/PcRXfyFAf0VHSF0OIjsp5FdhQSv3szsdGlCpdAn26jyww2Q8AePsmHunp6TAwlGy3oaF+jqvkn8REx8Lwq/oGhvo5rpJ/eP8BIS/C8PiRN2ZOXoSM9AwMtOoFAGjavAEs27fAX6Nm4tEDD/h4P8O8mf9DSkoq+g7sIbsG5iK3821oaJDn+f6e+tmdjw0oVboE+nUfJXG+o6JiAAD+foHiso8f0xAWEo5SpXLPJsrKp/P99UR/QyP9HNm8T2KktdsoZ/bvy/M9Y9JCpKdnYJBVbwDZ57tOfQuERnsiPNYbro+dAABON49hk+1KWTWP8lGWgP/7HbADQgVKeno69u3bh3Xr1uXoPJQoUQKHDx9G5cqV8ejRI4ntHj6UnEBbu3Zt+Pr6wtzcPMejWLFiuR5/7ty5SEhIkHhMMJI+vOAHG4bUZ8+h2uCLsfEiEdQa1EKq93eO31ZQgHJFM2TEZv9oSbpwHa/6jsOr/uPFj/ToWCTsPY6oCXN/PWYZyEjLwEufF6jYuJq4TCQSoWLjagh5/DzX7VqN64q2k3ph5zAbvHwSnGu9Bv1bIdw7CK+fSe+gCCUzLQNRT16gTJMvJiGKRCjT5E+8fhyY+4ZfESmIoFRM+Zfr5Ie0tDR4eT5F8xaNPsciEqFZi0Z49NBD6jaPHnqiWYuGEmUtWjXGo4ee4uefOh/lK5RFn+7DERcXnx/h/7S0tDR4e/qi6RftEIlEaNq8Adwfekndxt3NU6I+ADRv1QjuX7RbGpGCSPx5paauBgDIzJT8cZGZmQkFBdGPNuOHZbf7KZrlON8NJc7fl9wfekrUB6Sf712OG1C+Qln07T4ix/n28vRBSkoqzL8Y3qakpITSZUriZXj+r46Y+/luCHc3T6nbPHoo5Xy3bAR3N+nvj08UFEQoppJ9vhfMXok2TXvCslkvWDbrhSF9syfyjx85A6v+t+kXWkRUMHAOCBUoFy5cQFxcHEaNGgVtbcmrx71794a9vT2OHTuG9evXY/bs2Rg1ahQ8PT3h6OgIIPuLAQBmz56Nhg0bYuLEiRg9ejSKFy8OX19fXLt2DVu35r5+vIqKClRUVCTK3ijIpp+euP8kDP5njY9PnyPVxx9aQ3pCpKaKd2euAAAMllsjIzoWcZsdAAA644Yg1fsZ0sJeQUFTA9rD+0HJ1BjvTl0GAGQmvENmwjuJY2SlpSMj9i3SQl/KJGZZuLX7Igaum4DwJ8EI8wxEi1GdUExdBW7HbwEABq77C4lRb3FxzREAQOvx3dBhWl8cmLIFb1/GQNMw+32QmpyCj+9TxftV0VBDzU4NcG7FAfk36js82n0ZHdeNQ9STF4jwDEKdUR2grK4Cn2PZ7e64YRySIuNwZ/UxAED9v7siyvsF4kOjoFhMGeVb1UTVXk1wfb4jAEBZTQUNJnVH0DV3JEfHQ01PExZD20LDWBf+Fx8I0ka7bXuwxXY1PD188NjdG+P+Ggb14mo4fOAUAGCr3WpERkRh+dL1AICdtvtw9tJ+TJg4Ateu3ELP3p1gUasaZkxZBCD7h6XDvs2oUbMqBvcfB0VFRXHGJC4uAWlp2cPsSpYyha6uNkqWKgFFRUVU++/eCC+Cw5Cc/D7f271r+15s2L4S3h5P4fH4CcZMsIJacTUc/W/1uU22KxEREY1VyzYCAOx3HMCJC44Y9/cwXL96G917dUQNi2qwnroEQHbnYsqMsbh6+SaiomKgp6eL4aMHwsTUGBfOZn8+PHLzREJ8IjZuX4mNa22R8iEFg4b1QemypeB89Xa+txkA7LY5YrPtKnh6+MDD3Rtj/zvfR/4731vsViEyIhorxOd7P85c2ofxE0fg+hUX9OjdGTVr/YmZX5xv+32bUL1mVQzpPx4KioriTEP8f+c76V0y9jkcway5k/DqVSRehr3G31NGAgDOnXGSS7t3bHPEJlsbeHn4wNP9CcZMGJrd7v/O92Y7G0S+jsbKZRsAALvt9uPUxb0YN3E4nK/cQvfenVCzVjXMmpo9lFBNXQ1TZ4zDlcs3EB0VCz09HQwfMwgmpsY4/9/3wdcrvn16X4e8CEfE6yi5tPtXvH//AWEvP3cQX72Ogt/zIGhracJUyn1eCiMuMps3dkCoQLG3t4elpWWOzgeQ3QFZs2YN3r17hxMnTmDGjBnYtGkTGjVqhPnz52PChAnizkONGjVw69YtzJ8/H82aNUNWVhYqVKiA/v37y7tJYslXbkFBVwe6fw2DooEuUv2DEPXXPGT+N+lQycQI+OLqpoKmBgwWTYOigS4yEpPw0TcAEcOmIC24YF3t/xbPC67Q0NNCh2l9oWWog1fPQrFz2Cok/TdBW7ekgcQHdeMhbaGkoozhdtMl9nNl4wlc2fh5OdpaXRtnLwN67p58GvKD/M8/gLqeFppM7w11Q23E+IbihNUavI/NnjCsVcIAWV+cb2U1FVguHw4NUz2kp3zE28DXuDTVFv7nszsXmZmZ0Ktgij/7TIGariZS4pMQ6RWMI32W483zV4K08cypy9DX18PseZNhZGwInyfP0L/XaPGE61KlTJH1xRyqh24eGD96JuYumIr5i6YjOCgEwwb9Db9nAQAA0xLG6Ni5DQDA5Z7kEs3dO1vh/t3shQbmzJuMAYN7iV+7efdsjjr56dxpJ+gZ6GHmvIkwNDLA0yd+GNJnnHhieolSphKZikdunpg4xhrW8ydj9sKpeBEcilFDJsH/WXY2LDMjAxUqlsPOAd2hp6+LuLfx8PLwQa9OQ/HcLwhA9ipYg/uMw+wFU3DsrAOUlJTw3C8QIwdPhO9/K2Xlt7P/nW/reZNgZGyIp0+eYWCvMeLzXbJUia/a7YEJo2dizoKpmLdoGl4EhWD4oIkS57vDf+f75r2zEsfq2Xmo+FwuXbgW6RkZ2LZjNVRVVfHY3Qu9uw5HQrx8VkY7d9oJ+gbZ7f50vgf1/ny+S5YyReYX7/NHbp74a7Q1Zi+YjLkLp+JFUChGDJY83+aVyqHvwE3i8+3p4YMeHa3w3O/7M6QFmY9fAEZOmi1+vmbLTgBA946WWLFghlBhUQHC+4BQobBixQrY2dkhPDxc5vuW1X1Afjeyug/I70ZW9wH53fzMfUAKg5+5D0hh8DP3ASkMfuY+IIWBkPcBEZKQ9wEx1K4s2LFjEuRzUeJXFM1PXvrtbd++HfXq1YO+vj7u3buHtWvXCnePDyIiIiL6buyA0G8pICAAy5cvx9u3b1GmTBnMmDEDc+cWjInXRERERJQ7dkDot7RhwwZs2LBB6DCIiIiIcuAMh7wVzcGQREREREQkCGZAiIiIiIhkKJMZkDwxA0JERERERHLDDggREREREckNh2AREREREckQJ6HnjRkQIiIiIiKSG3ZAiIiIiIhkKBNZgj1+1LZt22BmZgZVVVU0aNAAbm5uedY/fvw4qlSpAlVVVVSvXh2XLl364WOyA0JEREREVAQdPXoU06dPx+LFi/H48WPUrFkT7du3R3R0tNT69+/fx8CBAzFq1Ch4eHigR48e6NGjB3x8fH7ouKIsDlIjytOLmm2FDkEQWxL0hQ5BECUyi+bUuNUJD4UOQRDFFIrm+U7PzBA6BEEoiIrmddewwAtChyAIZYPygh1bq7hwx05MDv7uug0aNEC9evWwdetWAEBmZiZKly6NSZMmYc6cOTnq9+/fH8nJybhw4fN7qmHDhrCwsICdnd13H7do/kskIiIiIiqEUlNTkZiYKPFITU3NUe/jx49wd3eHpaWluExBQQGWlpZwdXWVum9XV1eJ+gDQvn37XOvnhh0QIiIiIqJCwsbGBtra2hIPGxubHPViY2ORkZEBY2NjiXJjY2NERkZK3XdkZOQP1c9N0cw9ExERERHlEyHvhD537lxMnz5dokxFRUWgaKRjB4SIiIiIqJBQUVH5rg6HgYEBFBUVERUVJVEeFRUFExMTqduYmJj8UP3ccAgWEREREZEMZQn4v+9VrFgx1KlTB87OzuKyzMxMODs7o1GjRlK3adSokUR9ALh27Vqu9XPDDAgRERERURE0ffp0DBs2DHXr1kX9+vWxceNGJCcnY8SIEQCAoUOHomTJkuI5JFOmTEGLFi2wbt06dO7cGUeOHMGjR4+wc+fOHzouOyBEREREREVQ//79ERMTg0WLFiEyMhIWFhZwcnISTzQPCwuDgsLnAVONGzfGoUOHsGDBAsybNw8VK1bEmTNnUK1atR86Lu8DQvQNvA9I0cL7gBQtvA9I0cL7gBQtQt4HRE2trGDH/vAhVLBjf6+i+S+RiIiIiIgEUTQv/RARERER5RMOMMobMyBERERERCQ3zIAQEREREcnQjyyHWxQxA0JERERERHLDDggREREREckNh2AREREREckQJ6HnjRkQIiIiIiKSG2ZAiIiIiIhkiBmQvDEDQkREREREcsMOCBERERERyQ2HYBERERERyRAHYOWNGRAiIiIiIpIbURZnyRAVSKmpqbCxscHcuXOhoqIidDhyw3az3UUB2812FwVFtd30beyAEBVQiYmJ0NbWRkJCArS0tIQOR27Ybra7KGC72e6ioKi2m76NQ7CIiIiIiEhu2AEhIiIiIiK5YQeEiIiIiIjkhh0QogJKRUUFixcvLnIT99hutrsoYLvZ7qKgqLabvo2T0ImIiIiISG6YASEiIiIiIrlhB4SIiIiIiOSGHRAiIiIiIpIbdkCIiIiIiEhu2AEhIiIiIiK5YQeEiAqE9PR0XL9+HTt27MC7d+8AAK9fv0ZSUpLAkVF+y8jIgKenJ+Li4oQOhYhk4OPHj/D390d6errQoVABxQ4IUQESHh6Oly9fip+7ublh6tSp2Llzp4BR5b/Q0FBUr14d3bt3x99//42YmBgAwOrVqzFz5kyBoyNZmzp1Kuzt7QFkdz5atGiB2rVro3Tp0nBxcRE2OCIZ+/jxI16+fImwsDCJR2H0/v17jBo1Curq6vjzzz/F7Zw0aRJWrVolcHRUkCgJHQARfTZo0CCMHTsWVlZWiIyMRNu2bfHnn3/i4MGDiIyMxKJFi4QOMV9MmTIFdevWhZeXF/T19cXlPXv2xJgxYwSMLP/duXMHO3bsQFBQEE6cOIGSJUti//79KFeuHJo2bSp0ePnixIkTGDJkCADg/PnzePHiBfz8/LB//37Mnz8f9+7dEzjC/BEVFYWZM2fC2dkZ0dHR+Po2XBkZGQJFlj/OnTv3XfW6deuWz5EIIyAgACNHjsT9+/clyrOysiASiQrd+QaAuXPnwsvLCy4uLujQoYO43NLSEkuWLMGcOXMEjI4KEnZAiAoQHx8f1K9fHwBw7NgxVKtWDffu3cPVq1cxfvz4QtsBuXPnDu7fv49ixYpJlJuZmeHVq1cCRZX/Tp48CSsrKwwePBgeHh5ITU0FACQkJGDlypW4dOmSwBHmj9jYWJiYmAAALl26hL59+6JSpUoYOXIkNm3aJHB0+Wf48OEICwvDwoULYWpqCpFIJHRI+apHjx7frFNYf4gD2edbSUkJFy5cKBLnGwDOnDmDo0ePomHDhhLt/fPPPxEUFCRgZFTQsANCVICkpaVBRUUFAHD9+nXxlcEqVaogIiJCyNDyVWZmptQfIS9fvoSmpqYAEcnH8uXLYWdnh6FDh+LIkSPi8iZNmmD58uUCRpa/jI2N4evrC1NTUzg5OcHW1hZA9vANRUVFgaPLP3fv3sWdO3dgYWEhdChykZmZKXQIgvL09IS7uzuqVKkidChyExMTAyMjoxzlycnJRaIDRt+Pc0CICpA///wTdnZ2uHPnDq5duyZOYb9+/VpiaFJh065dO2zcuFH8XCQSISkpCYsXL0anTp2ECyyf+fv7o3nz5jnKtbW1ER8fL/+A5GTEiBHo168fqlWrBpFIBEtLSwDAgwcPCvWPtdKlS+cYdkWFV9WqVREbGyt0GHJVt25dXLx4Ufz8U6dj9+7daNSokVBhUQHEDAhRAbJ69Wr07NkTa9euxbBhw1CzZk0A2WOpPw3NKozWrVuH9u3bo2rVqkhJScGgQYMQEBAAAwMDHD58WOjw8o2JiQkCAwNhZmYmUX737l2UL19emKDkYMmSJahWrRrCw8PRt29fcdZPUVGxUI8R37hxI+bMmYMdO3bkOOeF0e3bt7+rnrROeGGwevVqWFtbY+XKlahevTqUlZUlXtfS0hIosvyzcuVKdOzYEb6+vkhPT8emTZvg6+uL+/fv49atW0KHRwWIKIuXY4gKlIyMDCQmJkJXV1dcFhISAnV1damp7cIiPT0dR48ehZeXF5KSklC7dm0MHjwYampqQoeWb2xsbHDgwAE4ODigbdu2uHTpEkJDQzFt2jQsXLgQkyZNEjpEuYmPj4eOjo7QYeQrXV1dvH//Hunp6VBXV8/xg/Tt27cCRZY/FBQUxFfAc/upUZjngCgoZA8y+XroUWGehA4AQUFBWLVqlcRn+ezZs1G9enWhQ6MChB0QogImPT0dLi4uCAoKwqBBg6CpqYnXr19DS0sLGhoaQodHMpSVlYWVK1fCxsYG79+/BwCoqKhg5syZ+N///idwdPln9erVMDMzQ//+/QEA/fr1w8mTJ2FqaopLly6hRo0aAkeYP/bu3Zvn68OGDZNTJPKhr68PTU1NDB8+HFZWVjAwMJBaT1tbW86Ryce3rvi3aNFCTpEQFTzsgBAVIKGhoejQoQPCwsKQmpqK58+fo3z58pgyZQpSU1NhZ2cndIj5Yu/evTAwMEDnzp0BANbW1ti5cyeqVq2Kw4cPo2zZsgJHKHsZGRm4d+8eatSoAXV1dQQGBiIpKQlVq1Yt9B3NcuXK4eDBg2jcuDGuXbuGfv364ejRozh27BjCwsJw9epVoUMkGfj48SNOnz4NBwcH3LlzB506dcKoUaPQoUMHTkgupBITE6WWi0QiqKio5FjpkIoudkCICpAePXpAU1MT9vb20NfXh5eXF8qXLw8XFxeMGTMGAQEBQoeYLypXrgxbW1u0bt0arq6uaNOmDTZu3IgLFy5ASUkJp06dEjrEfKGqqopnz56hXLlyQociV2pqanj+/DlKly6NKVOmICUlBTt27MDz58/RoEGDQnVH9MTERPFY/9x+nH1SGOcEfBIWFgZHR0fs3bsXqampGDZsGJYuXQolpcI9FTU+Ph729vZ49uwZgOyFRkaOHFlosz5fDruTplSpUhg+fDgWL14sHqJGRRPPPlEBcufOHSxYsKDI3Q8jPDwc5ubmALLXke/Tpw/Gjh0LGxsb3LlzR+Do8k+1atUQHBwsdBhyp6uri/DwcACAk5OTeBWsrKysQjcuXldXF9HR0QAAHR0d6Orq5nh8Ki/MypQpg0WLFuH69euoVKkSVq1a9c0O2e/u0aNHqFChAjZs2IC3b9/i7du3WL9+PSpUqIDHjx8LHV6+cHR0RIkSJTBv3jycOXMGZ86cwbx581CyZEnY2tpi7Nix2Lx5M++KTlwFi6ggKar3w9DQ0MCbN29QpkwZXL16FdOnTweQnSH48OGDwNHln+XLl4vne9SpUwfFixeXeL2wXhHv1asXBg0ahIoVK+LNmzfo2LEjAMDDw0PcES0sbty4AT09PQDAzZs3BY5GGKmpqTh58iQcHBzg6uqKzp074+LFi+K/S2E1bdo0dOvWDbt27RJnetLT0zF69GhMnTr1u1cJ+53s3bsX69atQ79+/cRlXbt2RfXq1bFjxw44OzujTJkyWLFiBebNmydgpCQ0DsEiKkD69+8PbW1t7Ny5E5qamvD29oahoSG6d++OMmXKYM+ePUKHmC8GDx4MPz8/1KpVC4cPH0ZYWBj09fVx7tw5zJs3Dz4+PkKHmC++HILw5bCFwr5KTlpaGjZt2oTw8HAMHz4ctWrVAgBs2LABmpqaGD16tMARkiy4ublhz549OHLkCMzMzDBixAgMGTKk0Hc8PlFTU4OHh0eOe9v4+vqibt264oUnChM1NTV4e3ujYsWKEuUBAQGoWbMm3r9/jxcvXuDPP/8slO2n78cMCFEBUlTvh7Ft2zYsWLAA4eHhOHnypPimi+7u7hg4cKDA0eWfonpFXFlZGTNnzsxRPm3aNAGiyV/e3t7fXbewrf7VsGFDlClTBpMnT0adOnUAZN/j5mvdunWTd2hyoaWlhbCwsBwdkPDw8EKb0S5dujTs7e1zDLGyt7dH6dKlAQBv3rwp9EMO6duYASEqYNLT03HkyBF4e3sXmfthUNGzf/9+7NixA8HBwXB1dUXZsmWxceNGlCtXDt27dxc6PJn5NCn3W1+1hTHj9T2TjAtjuz+ZPHkyTp8+jX/++QeNGzcGANy7dw+zZs1C7969sXHjRmEDzAfnzp1D3759UaVKFdSrVw9A9lyYZ8+e4eTJk+jSpQtsbW0REBCA9evXCxwtCYkdECIqEIraajHAt+8UXVjvEG1ra4tFixZh6tSpWLFiBXx8fFC+fHnxKkmFKTMUGhr63XUL43LTRdnHjx8xa9Ys2NnZIT09HUB29m/ChAlYtWoVVFRUBI4wf4SEhMDOzg7Pnz8HkL3K4bhx45CUlIRq1aoJHB0VFOyAEAns3Llz6NixI5SVlXHu3Lk86xbWoQqPHj1C+/btoaamhvr16wMAHj58iA8fPuDq1auoXbu2wBHmD2lXiL+cC1JYrwxXrVoVK1euFC87/Wm5aR8fH7Rs2RKxsbFCh0gy9ObNG/GwyvDwcOzatQspKSno2rUrmjVrJnB0+e/9+/cICgoCAFSoUAHq6uoCRyQ/iYmJOHz4MBwcHPDo0aNC+5lGP44dECKBKSgoIDIyEkZGRnkOWSjMQxWaNWsGc3NzqavFBAcHF8rVYgAgISFB4nlaWho8PDywcOFCrFixAm3atBEosvylpqYGPz8/lC1bVqIDEhAQgBo1ahTalc/27duX5+tDhw6VUyTy8eTJE3Tt2hXh4eGoWLEijhw5gg4dOiA5ORkKCgpITk7GiRMn0KNHD6FDJRm7ffs27O3tcfLkSZQoUQK9evVC7969xcOyiNgBISLBFcXVYvJy69YtTJ8+He7u7kKHki+qVq0KGxsbdO/eXaIDsmXLFuzZs6fQ3iPh64m3aWlpeP/+PYoVKwZ1dXW8fftWoMjyR8eOHaGkpIQ5c+Zg//79uHDhAtq3b49du3YBACZNmgR3d3f8+++/AkcqO7169YKjoyO0tLTQq1evPOsWthusRkZGwtHREfb29khMTES/fv1gZ2cHLy8vVK1aVejwqIDhKlhEJLiiuFpMXoyNjeHv7y90GPlm+vTp+Pvvv5GSkoKsrCy4ubnh8OHDsLGxwe7du4UOL99Iu8N7QEAAJkyYgFmzZgkQUf56+PAhbty4gRo1aqBmzZrYuXMn/vrrL3Gmd9KkSWjYsKHAUcqWtra2eBillpZWnncFL0y6du2K27dvo3Pnzti4cSM6dOgARUVF2NnZCR0aFVDMgBAVIJMnT4a5uTkmT54sUb5161YEBgYWylVTgKK5WgyQc4nWrKwsREREYNWqVUhPT5e6ZGlhcfDgQSxZskQ8Nr5EiRJYunQpRo0aJXBk8vfo0SMMGTIEfn5+QociU18OLwUgke0CgKioKJQoUaLQDi0tSpSUlDB58mRMmDBB4h4gysrKzICQVMyAEBUgJ0+elDoRvXHjxli1alWh/SH+zz//QCQSYejQoVJXiymsLCwspC7R2rBhQzg4OAgUlXwMHjwYgwcPxvv375GUlCT+kVoUKSkp4fXr10KHkS++zgAUlYwAALRu3RqnTp2Cjo6ORHliYiJ69OiBGzduCBNYPrh79y7s7e1Rp04d/PHHH7CyssKAAQOEDosKMGZAiAoQVVVV+Pj4wNzcXKI8MDAQ1apVQ0pKikCRyUdRWy3m6yVaFRQUYGhoCFVVVYEiovz09cWFTxmvrVu3onTp0rh8+bJAkeUPBQUFdOzYUbzc7Pnz59G6dWsUL14cAJCamgonJ6dCmwH5OgP0SXR0NEqWLIm0tDSBIss/ycnJOHr0KBwcHODm5oaMjAysX78eI0eOLJLDaSl37IAQFSDVqlXD+PHjMXHiRInyLVu2wNbWFr6+vgJFlr8SEhKQkZEBPT09ifK3b99CSUkJWlpaAkUmf/Hx8TmumBY2UVFRmDlzJpydnREdHZ0jA1SYf5B+SSQSwdDQEK1bt8a6detgamoqUGT5Y8SIEd9Vb8+ePfkciXx9GlppYWGBGzduSHyuZWRkwMnJCTt27EBISIhAEcqHv78/7O3tsX//fsTHx6Nt27bfXGqeig52QIgKEAcHB0ycOBGzZs1C69atAQDOzs5Yt24dNm7ciDFjxggcYf7o2LEjunbtir/++kui3M7ODufOncOlS5cEiix/rV69GmZmZujfvz8AoF+/fjhx4gRMTU1x6dIl1KxZU+AI80fHjh0RFhaGiRMnwtTUNMewnMJ0J3QqehQUFMTvaWk/sdTU1LBlyxaMHDlS3qEJIiMjA+fPn4eDgwM7ICTGDghRAWNra4sVK1aIx4SbmZlhyZIlhe4eAV/S09PDvXv38Mcff0iU+/n5oUmTJnjz5o1AkeWvcuXK4eDBg2jcuDGuXbuGfv364ejRozh27BjCwsJw9epVoUPMF5qamrhz5w4sLCyEDkVQGRkZePLkCcqWLZtjiV76fYWGhiIrKwvly5eHm5sbDA0Nxa8VK1YMRkZGUFRUFDBCIuFxEjpRATNhwgRMmDABMTExUFNTg4aGhtAh5bvU1FTx5PMvpaWlFdqb0gHZ6+aXLl0aAHDhwgX069cP7dq1g5mZGRo0aCBwdPmndOnSUq8MF3ZTp05F9erVMWrUKGRkZKB58+ZwdXWFuro6Lly4gJYtWwodIslA2bJlAQCZmZkCR0JUcOV+22UiEpShoWGR6HwAQP369bFz584c5XZ2dqhTp44AEcmHrq4uwsPDAQBOTk6wtLQEkD1so7DOgwCAjRs3Ys6cOYV+DPzXTpw4IR5Wd/78eYSEhMDPzw/Tpk3D/PnzBY6OZM3GxkbqanYODg5YvXq1ABERFRwcgkVUgBTVybn37t2DpaUl6tWrhzZt2gDInvvy8OFDXL16Fc2aNRM4wvwxceJEXLhwARUrVoSHhwdCQkKgoaGBI0eOYM2aNYX6juDv379Heno61NXVoaysLPF6Ybsj+CeqqqoIDAxEqVKlMHbsWKirq2Pjxo148eIFatasicTERKFDJBkyMzPDoUOHxPc2+uTBgwcYMGAAXrx4IVBkRMLjECyiAmT48OEICwvDwoULpU7OLayaNGkCV1dXrF27FseOHYOamhpq1KgBe3t7iZtaFTYbNmyAmZkZwsPDsWbNGnHGKyIiIseE/MJkw4YNRea9/SVjY2P4+vrC1NQUTk5OsLW1BZC9/DTnBBQ+kZGRUlc2MzQ0REREhAARERUc7IAQFSB3794tspNzLSwscPDgQaHDkCtlZWXMnDkzR/m0adMEiEZ+hg8fnutrhXnOz4gRI9CvXz/xxYVPQ+4ePHiAKlWqCBwdyVrp0qVx7949lCtXTqL83r17KFGihEBRERUM7IAQFSBFdXJuWFhYnq+XKVNGTpHI1969e2FgYIDOnTsDAKytrbFz505UrVoVhw8fFk9mLWwmT56MzZs35yhPTk5Gly5dcPPmTQGiyn9LlixBtWrVEB4ejr59+4pv0KeoqIg5c+YIHB3J2pgxYzB16lSkpaVJLKtubW2NGTNmCBwdkbA4B4SoALl69SrWrVuHHTt2wMzMTOhw5ObLdfOlKaxzXypXrgxbW1u0bt0arq6usLS0xIYNG3DhwgUoKSnh1KlTQoeYLypUqIAhQ4Zg6dKl4rLk5GR06NABAHDnzh2hQiOSmaysLMyZMwebN2/Gx48fAWTPA5o9ezYWLVokcHREwmIHhKgAKaqTc728vCSep6WlwcPDA+vXr8eKFSvQq1cvgSLLX+rq6vDz80OZMmUwe/ZsREREYN++fXj69ClatmyJmJgYoUPMF0FBQWjWrBmsra0xdepUvHv3Du3bt4eSkhIuX76M4sWLCx1ivnF2dhYvMvH1Mq3SVkyi319SUhKePXsGNTU1VKxYUZz5IirKOASLqADZuHGj0CEIQtodv+vWrYsSJUpg7dq1hbYDoqGhgTdv3qBMmTK4evUqpk+fDiD7KmlhngtRoUIFODk5oVWrVlBQUMDhw4ehoqKCixcvFurOx9KlS7Fs2TLUrVu3SC0yUdRpaGigXr16QodBVKAwA0JEBVZgYCBq1qyJ5ORkoUPJF4MHD4afnx9q1aqFw4cPIywsDPr6+jh37hzmzZsHHx8foUPMV66urmjbti0aNGiACxcuQE1NTeiQ8pWpqSnWrFkDKysroUMhOUhOTsaqVatyzXgFBwcLFBmR8JgBISqgUlJSxOOGP9HS0hIomvz19f0PsrKyEBERgSVLlhTqZXi3bduGBQsWIDw8HCdPnoS+vj4AwN3dHQMHDhQ4OtmqVauW1Cv+KioqeP36NZo0aSIuK6z3P/n48WOOe0JQ4TV69GjcunULVlZWzHgRXxullwAAH9hJREFUfYUZEKICJDk5GbNnz8axY8fw5s2bHK8X1snY0iahZ2VloXTp0jhy5AgaNWokUGQkK19OOP+WxYsX52Mkwpk9ezY0NDSwcOFCoUMhOdDR0cHFixclOtdElI0ZEKICxNraGjdv3oStrS2srKywbds2vHr1Cjt27MCqVauEDi/ffL3sqoKCAgwNDWFubg4lpcL9MXXnzh3s2LEDwcHBOH78OEqWLIn9+/ejXLlyaNq0qdDhyUxh7VT8iJSUFOzcuRPXr19HjRo1ciwysX79eoEio/ygq6sLPT09ocMgKpCYASEqQMqUKYN9+/ahZcuW0NLSwuPHj2Fubo79+/fj8OHDuHTpktAhkgydPHkSVlZWGDx4MPbv3w9fX1+UL18eW7duxaVLlwrt+X748CEyMzPRoEEDifIHDx5AUVERdevWFSiy/NWqVas8Xy+s9z8pqg4cOICzZ89i7969UFdXFzocogKFHRCiAkRDQwO+vr4oU6YMSpUqhVOnTqF+/fp48eIFqlevjqSkJKFDlJlz5859d91u3brlYyTCqVWrFqZNm4ahQ4dCU1MTXl5eKF++PDw8PNCxY0dERkYKHWK+qF+/PqytrdGnTx+J8lOnTmH16tV48OCBQJERyU6tWrUQFBSErKwsmJmZ5ch4Fda5TkTfo3CPbSD6zZQvXx4vXrxAmTJlUKVKFRw7dgz169fH+fPnoaOjI3R4MtWjR4/vqicSiQrt3Bd/f380b948R7m2tjbi4+PlH5Cc+Pr6onbt2jnKa9WqBV9fXwEiyl/fs4y0SCTCyZMn5RANycv3fsYRFUXsgBAVICNGjICXlxdatGiBOXPmoGvXrti6dSvS0tIK3fjwr5ekLIpMTEwQGBiY4673d+/eRfny5YUJSg5UVFQQFRWVo40RERGFcs6Ptra20CGQADjviSh3HIJFVICFhobC3d0d5ubmqFGjhtDhyFxKSgquX7+OLl26AADmzp2L1NRU8etKSkpYtmwZVFVVhQoxX9nY2ODAgQNwcHBA27ZtcenSJYSGhmLatGlYuHAhJk2aJHSI+WLgwIGIiIjA2bNnxT/O4+Pj0aNHDxgZGeHYsWMCR0hERPmJHRAiEoydnR0uXryI8+fPAwA0NTXx559/im9I5+fnh1mzZonvEF7YZGVlYeXKlbCxscH79+8BZGcHZs6cif/9738CR5d/Xr16hebNm+PNmzeoVasWAMDT0xPGxsa4du0aSpcuLXCERL9O2vLiXyqsQ0uJvgc7IEQFjLOzc653znVwcBAoqvzRrFkzWFtbo2vXrgAgMREbyF5FZtu2bXB1dRUyzHyRkZGBe/fuoUaNGlBXV0dgYCCSkpJQtWpVaGhoCB1evktOTsbBgwfh5eUFNTU11KhRAwMHDswxUZfod3X27FmJ52lpafDw8MDevXuxdOlSjBo1SqDIiITHDghRAbJ06VIsW7YMdevWlXrn3NOnTwsUWf4wNTWFq6ureA6EoaEhHj58KH7+/Plz1KtXDwkJCcIFmY9UVVXx7NkzlCtXTuhQiEhODh06hKNHj+booBAVJYVvth/Rb8zOzg6Ojo6wsrISOhS5iI+Pl5jzERMTI/F6ZmamxOuFTbVq1RAcHFwkOiDnzp1Dx44doays/M0lmAvrsstEANCwYUOMHTtW6DCIBMUOCFEB8vHjRzRu3FjoMOSmVKlS8PHxQeXKlaW+7u3tjVKlSsk5KvlZvny5eL5HnTp1ULx4cYnXtbS0BIpM9nr06IHIyEgYGRnluTxpYV52mejDhw/YvHkzSpYsKXQoRILiECyiAmT27NnQ0NDAwoULhQ5FLqZMmYLr16/D3d09x0pXHz58QN26dWFpaYlNmzYJFGH+UlBQEP/3l8PtsrKy+EOc6Denq6ub49/1u3fvoK6ujgMHDjDTR0UaOyBEBciUKVOwb98+1KhRAzVq1MgxIbew3QskKioKFhYWKFasGCZOnIhKlSoByL5B39atW5Geng4PDw8YGxsLHGn+uHXrVp6vt2jRQk6REJGs7d27V+K5goICDA0N0aBBA+jq6goUFVHBwA4IUQHSqlWrXF8TiUS4ceOGHKORjxcvXmDChAm4du0aPn0ciUQitG3bFtu3by+0N+TLyspCYGAgPn78iMqVKxfKG/DlpSit9kZFi4ODAwYPHgwVFRWhQyEqsNgBIaIC4e3btwgMDAQAmJubQ09PT+CI8s+LFy/QrVs3+Pr6AsieC3Py5EnUrVtX4Mjko6it9kZFi6KiIiIiImBkZAQAKFGiBO7fvy9e3Y+I2AEhIpK7Pn364OnTp1i0aBFUVVXxzz//ICUlBe7u7kKHJhempqZYs2ZNkVntjYoWBQUF8YILQM77GxERV8EiKlB69uwp9c65IpEIqqqqMDc3x6BBg3JdNYp+D3fv3sWJEyfQtGlTANnLcpYqVQrJyck5VsIqjIraam9ERCRJ4dtViEhetLW1cePGDTx+/BgikQgikQgeHh64ceMG0tPTcfToUdSsWRP37t0TOlT6BdHR0ahYsaL4uampKdTU1BAdHS1gVPIzevRoHDp0SOgwiPLFp8/u3J4TETMgRAWKiYkJBg0ahK1bt4qXaM3MzMSUKVOgqamJI0eOYPz48Zg9ezbu3r0rcLT0s0QiEZKSkqCmpiYuU1BQwLt375CYmCguK0z3AZk+fbr4vzMzM7Fz505cv369SKz2RkVLVlYWKlWqJO50JCUloVatWhLLbgPZ896IiirOASEqQAwN/9/enQdVfZ1/HP9cCCLKUjc0uAyiNNrEuMdoFkZkFNyiMq0T97U2OmolIdqqEbRuUaNR2xDR1GWMNVXjlhS3uEui1gUdgxA3kEhswasiirL8/rC5E4om/bXfe88V3q+/uOd7//gww+h97jnPc2rp8OHDjnG030tLS1OHDh30z3/+U2fOnNErr7wiu91uJiT+Zx4eHmW+Ef3+7o8f/lye7gH5sQlvP1Rep72h4vj38buPM3jwYCcnAdwXOyCAGyksLFRqamqZAiQ1NdXxYbRy5cps5z/h9u7dazqCy1XE3xkVE4UF8NMoQAA3MnDgQA0fPly///3v1bZtW0nSsWPHNGvWLA0aNEjSw8vrnn32WZMx8T+qqBcM/vt4UqC8s9vt2rBhgy5cuKDY2FhVr15dJ06cUO3atVW3bl3T8QBjOIIFuJGioiLNmTNHS5cu1XfffSdJql27tsaOHauJEyfK09NTGRkZ8vDwUL169QynxX/jhz0eP6U89YBIZceTAuVZSkqKIiIiFBAQoMuXL+v8+fMKCQnRlClTlJGRodWrV5uOCBhDAQK4qe8/qJa3D6EV3aP6Px6nPPWASBQgqFgiIiLUqlUrvfvuu6XuAjly5Ij69euny5cvm44IGMMRLMDNFBYWat++fbpw4YL69esnSfr222/l7+8vX19fw+nwv/phL8Tly5c1adIkDRkyRO3bt5ckJScna9WqVZo9e7apiE61fPnyn/w7HjdunIvSAM5z7Ngxffjhh2XW69atq+zsbAOJAPfBDgjgRq5cuaLIyEhlZGSooKBAaWlpCgkJ0fjx41VQUKCEhATTEWGhTp06acSIEXr99ddLrX/88cdatmyZ9u3bZyaYk3x/dNDT0/Ox77HZbLp48aILUwHOERgYqB07dqhly5aldkB27dqlYcOGKTMz03REwBgKEMCN9OrVS35+flqxYoVq1Kjh+A9r3759GjlypNLT001HhIWqVKmi06dPl7qUUHo4drlFixbKz883lMw5OIKFimTEiBHKycnRJ598ourVqyslJUWenp7q1auXXn31VS1atMh0RMAYbkIH3MjBgwc1ZcoUVapUqdR6cHCwsrKyDKWCs9SvX1+JiYll1pcvX6769esbSORcjI9GRbJgwQLl5eUpMDBQd+/eVVhYmBo3biw/Pz/NnDnTdDzAKHpAADdSXFz8yMbjq1evys/Pz0AiONPChQsVHR2tv/3tb2rXrp0k6ejRo0pPT9fGjRsNp7MeG+6oSAICArRr1y4dOnRIKSkpysvLU6tWrRQREWE6GmAcR7AAN9K3b18FBARo2bJl8vPzU0pKimrVqqXXXntNDRo00J///GfTEWGxq1ev6k9/+pNSU1MlSU2bNtVvfvObcrkDEh8fr9jYWFWpUsV0FMCl7t27J29vb3YBgX+hAAHcSGZmpiIjI1VSUqL09HS1adNG6enpqlmzpg4cOMDZeZQbdrtdR48e1fXr11VcXFzq2feXbgJPsuLiYs2cOVMJCQn67rvvHENFpk6dquDgYA0fPtx0RMAYChDAzRQWFmr9+vU6ffq0Y8u+f//+8vHxMR0NTmC327VixQp9/fXXkqRnn31Ww4YNU0BAgOFkzrNt2zb1799feXl58vf3L/WtsM1mU25ursF0gDWmT5+uVatWafr06Ro5cqTOnj2rkJAQrV+/XosWLVJycrLpiIAxFCCAm3jw4IGaNGmi7du3q2nTpqbjwAWOHz+uLl26yMfHRy+88IKkh3cH3L17Vzt37lSrVq0MJ3SOn//85+ratatmzZrFcSyUW40bN9aHH36oTp06lRrDm5qaqvbt2+vGjRumIwLG0IQOuAkvLy/du3fPdAy40IQJE9SzZ08lJibqqace/nNcWFioESNG6Le//a0OHDhgOKFzZGVlady4cRQfKNeysrLUuHHjMuvFxcV68OCBgUSA+2AML+BGxowZo7lz56qwsNB0FLjA8ePHNXHiREfxIUlPPfWU3n77bR0/ftxgMufq0qVLuf79AEn6xS9+oYMHD5ZZ37Bhg1q2bGkgEeA+2AEB3MixY8e0Z88e7dy5U82aNVPVqlVLPd+0aZOhZHAGf39/ZWRkqEmTJqXWMzMzy/XY5W7duik2Nlbnzp1Ts2bN5OXlVep5z549DSUDrPPOO+9o8ODBysrKUnFxsTZt2qTz589r9erV2r59u+l4gFH0gABuZOjQoT/6nDG85cu4ceP06aefav78+erQoYMk6fDhw4qNjVV0dHS5vSnZw+Pxm+82m+2Rd+EAT6KDBw9q+vTppYaKvPPOO+rcubPpaIBR7IAAbqC4uFjz5s1TWlqa7t+/r/DwcMXFxTH5qpybP3++bDabBg0a5Dh25+XlpTfeeENz5swxnM55/n3sLlDeFBYWatasWRo2bJh27dplOg7gdtgBAdzAjBkzFBcXp4iICPn4+GjHjh16/fXX9dFHH5mOBhfIz8/XhQsXJEmNGjWiORsoB3x9fXX27FkFBwebjgK4HQoQwA2Ehobqrbfe0qhRoyRJu3fvVrdu3XT37t0fPa6C8uPq1auSpHr16hlO4hyLFy/Wr3/9a1WuXFmLFy/+0feOGzfORakA53nttdfUp08fDR482HQUwO1QgABuwNvbW998843q16/vWKtcubK++eabcvuBFA+PIv3hD3/QggULlJeXJ0ny8/PTm2++qcmTJ5er4rNhw4Y6fvy4atSooYYNGz72fTabTRcvXnRhMsA5EhISFB8fr/79+6t169ZlhoowbAEVGQUI4AY8PT2VnZ2tWrVqOdb8/PyUkpLyox/W8GT73e9+pxUrVig+Pl4vvfSSJOnQoUOKi4vTyJEjNXPmTMMJAfy3GLYAPB4FCOAGPDw8FBUVJW9vb8fatm3bFB4eXupbM8bwli9BQUFKSEgo803oli1bNHr0aGVlZRlK5lxnz57Vc88998hnmzdvVq9evVwbCADgUkzBAtzAo84IDxgwwEASuFJubm6ZO0AkqUmTJsrNzTWQyDW6dOmiQ4cOldnd27hxowYNGqQ7d+4YSgYAcAUKEMANcL9HxdS8eXMtXbq0TFP20qVL1bx5c0OpnG/EiBGKiIjQ4cOHVadOHUnS+vXrNWzYMK1cudJsOMAijxu2YLPZVLlyZTVu3FivvvqqPD09XZwMMI8jWABgyP79+9WtWzc1aNBA7du3lyQlJycrMzNTn3/+uV555RXDCZ1n7Nix2rt3rw4cOKCkpCSNGDFCa9asUXR0tOlogCUaNmyof/zjH8rPz1e1atUkSTdu3FCVKlXk6+ur69evKyQkRHv37i01gASoCMrPiBUAeMKEhYUpLS1NvXv3lt1ul91uV58+fXT+/PlyXXxI0pIlS9S8eXO9+OKLGjlypNatW0fxgXJl1qxZatu2rdLT05WTk6OcnBylpaWpXbt2ev/995WRkaE6depowoQJpqMCLscOCADA6bZu3Vpm7cGDB5owYYI6d+5cqhGf8aQoDxo1aqSNGzeqRYsWpdZPnjyp6OhoXbx4UUeOHFF0dLSuXbtmJiRgCAUIALhQSkrKf/ze559/3olJXOs/vdOE8aQoL6pUqaIDBw6oTZs2pdaPHTumsLAw5efn6/Lly3ruuecc9wABFQVN6ADgQi1atJDNZtNPffdT3j6IFxcXm44AuFTHjh01atQoLV++XC1btpT0cPfjjTfeUHh4uCTpzJkz3PWECokCBABc6NKlS6YjGJOcnKycnBx1797dsbZ69WpNmzZNd+7cUa9evbRkyZJS9+EAT6oVK1Zo4MCBat26tby8vCRJhYWF6tSpk1asWCFJ8vX11YIFC0zGBIzgCBYAGJKTk6MaNWpIkjIzM5WYmKi7d++qZ8+e5bIJPTIyUh07dtTEiRMlPfz2t1WrVhoyZIiaNm2qefPmadSoUYqLizMbFLBQamqq0tLSJEnPPPOMnnnmGcOJAPMoQADAxc6cOaMePXooMzNToaGh+stf/qLIyEjduXNHHh4eunPnjjZs2FDubgR/+umntW3bNseZ+MmTJ2v//v06dOiQJOmvf/2rpk2bpnPnzpmMCQBwMo5gAYCLvf3222rWrJnWrl2rNWvWqHv37urWrZsSExMlPbwjY86cOeWuALlx44Zq167teL1//35FRUU5Xrdt21aZmZkmogGWiImJ0YwZM1S1alXFxMT86Hvfe+89F6UC3A8FCAC42LFjx/TFF1/o+eefV/PmzbVs2TKNHj3aMSlq7NixevHFFw2ntF7t2rV16dIl1a9fX/fv39eJEycUHx/veH779m3HWXngSXTy5Ek9ePDA8fPj2Gw2V0UC3BIFCAC4WG5ururUqSPpYRNq1apVHTclS1K1atV0+/ZtU/GcpmvXrpo0aZLmzp2rzZs3q0qVKqV6XVJSUtSoUSODCYH/zd69ex/5M4DSKEAAwIB//wa0InwjOmPGDPXp00dhYWHy9fXVqlWrVKlSJcfzjz76SJ07dzaYEADgCjShA4CLeXh4KCoqyjFudtu2bQoPD1fVqlUlSQUFBUpKSipX94D80M2bN+Xr6ytPT89S67m5ufL19S1VlABPkj59+vzH7920aZMTkwDujR0QAHCxwYMHl3o9YMCAMu8ZNGiQq+K4XEBAwCPXq1ev7uIkgLV++LddUlKiTz/9VAEBAY7Jb3//+99lt9v/X4UKUB6xAwIAAGCxiRMnKjc3VwkJCY7dvqKiIo0ePVr+/v6aN2+e4YSAORQgAAAAFqtVq5YOHTpU5uLB8+fPq0OHDsrJyTGUDDDPw3QAAACA8qawsFCpqall1lNTU1VcXGwgEeA+6AEBAACw2NChQzV8+HBduHBBL7zwgiTpq6++0pw5czR06FDD6QCzOIIFAABgseLiYs2fP1/vv/++rl27Jkl6+umnNX78eL355ptlpsABFQkFCAAAgBPdunVLkuTv7284CeAe6AEBAABwgsLCQu3evVvr1q1zXDb67bffKi8vz3AywCx2QAAAACx25coVRUZGKiMjQwUFBUpLS1NISIjGjx+vgoICJSQkmI4IGMMOCAAAgMXGjx+vNm3a6MaNG/Lx8XGs9+7dW3v27DGYDDCPKVgAAAAWO3jwoI4cOaJKlSqVWg8ODlZWVpahVIB7YAcEAADAYsXFxSoqKiqzfvXqVfn5+RlIBLgPChAAAACLde7cWYsWLXK8ttlsysvL07Rp09S1a1dzwQA3QBM6AACAxa5evaouXbqopKRE6enpatOmjdLT01WzZk0dOHBAgYGBpiMCxlCAAAAAOEFhYaHWr1+v06dPKy8vT61atVL//v1LNaUDFREFCAAAgIW+/PJLbdu2Tffv31d4eLiioqJMRwLcCgUIAACARTZs2KC+ffvKx8dHXl5eunXrlubOnau33nrLdDTAbVCAAAAAWKR169Zq27at/vjHP8rT01OzZ8/WvHnzlJubazoa4DYoQAAAACzi6+urU6dOqXHjxpKk+/fvq2rVqsrKyqLxHPgXxvACAABYJD8/X/7+/o7XlSpVUuXKlZWXl2cwFeBeuAkdAADAQsuXL5evr6/jdWFhoVauXKmaNWs61saNG2ciGuAWOIIFAABgkeDgYNlsth99j81m08WLF12UCHA/FCAAAAAAXIYeEAAAABew2+2mIwBugQIEAADAYnPnztX69esdr3/5y1+qevXqqlu3rk6fPm0wGWAeBQgAAIDFEhISVL9+fUnSrl27tHv3biUlJSkqKkqxsbGG0wFmMQULAADAYtnZ2Y4CZPv27frVr36lzp07Kzg4WO3atTOcDjCLHRAAAACLVatWTZmZmZKkpKQkRURESJJKSkpUVFRkMhpgHDsgAAAAFuvTp4/69eun0NBQ5eTkKCoqSpJ08uRJxy3pQEVFAQIAAGCxhQsXKjg4WJmZmXr33XcdFxNeu3ZNo0ePNpwOMIt7QAAAAAC4DD0gAAAATrBmzRq9/PLLCgoK0pUrVyRJixYt0pYtWwwnA8yiAAEAALDYBx98oJiYGEVFRclutzsaz3/2s59p0aJFZsMBhlGAAAAAWGzJkiVKTEzU5MmT5enp6Vhv06aNzpw5YzAZYB4FCAAAgMUuXbqkli1blln39vbWnTt3DCQC3AcFCAAAgMUaNmyoU6dOlVlPSkpS06ZNXR8IcCOM4QUAALBYTEyMxowZo3v37qmkpERHjx7VunXrNHv2bC1fvtx0PMAoxvACAAA4wdq1axUXF6cLFy5IkoKCghQfH6/hw4cbTgaYRQECAADgRPn5+crLy1NgYKDpKIBboAcEAADAYuHh4bLb7ZKkKlWqOIqPW7duKTw83GAywDx2QAAAACzm4eGh7OzsMrse169fV926dfXgwQNDyQDzaEIHAACwSEpKiuPnc+fOKTs72/G6qKhISUlJqlu3rologNtgBwQAAMAiHh4estlskqRHfcTy8fHRkiVLNGzYMFdHA9wGBQgAAIBFrly5opKSEoWEhOjo0aOqVauW41mlSpUUGBhY6mZ0oCKiAAEAAADgMkzBAgAAcII1a9bopZdeUlBQkK5cuSJJWrhwobZs2WI4GWAWBQgAAIDFPvjgA8XExKhr166y2+0qKiqSJFWrVk2LFi0yGw4wjAIEAADAYkuWLFFiYqImT55cquejTZs2OnPmjMFkgHkUIAAAABa7dOmSWrZsWWbd29tbd+7cMZAIcB8UIAAAABZr2LChTp06VWY9KSlJTZs2dX0gwI1wESEAAIDFYmJiNGbMGN27d08lJSU6evSo1q1bp9mzZ2v58uWm4wFGMYYXAADACdauXau4uDhduHBBkhQUFKT4+HgNHz7ccDLALAoQAAAAJ8rPz1deXp4CAwNNRwHcAkewAAAAnOT69es6f/68JMlms5W6GR2oqGhCBwAAsNjt27c1cOBABQUFKSwsTGFhYQoKCtKAAQN08+ZN0/EAoyhAAAAALDZixAh99dVX+uyzz2S322W327V9+3YdP35co0aNMh0PMIoeEAAAAItVrVpVO3bs0Msvv1xq/eDBg4qMjOQuEFRo7IAAAABYrEaNGgoICCizHhAQoGrVqhlIBLgPChAAAACLTZkyRTExMcrOznasZWdnKzY2VlOnTjWYDDCPI1gAAAAWaNmypWw2m+N1enq6CgoK1KBBA0lSRkaGvL29FRoaqhMnTpiKCRjHGF4AAAAL9OrVy3QE4InADggAAAAAl6EHBAAAAIDLcAQLAADAYkVFRVq4cKE++eQTZWRk6P79+6We5+bmGkoGmMcOCAAAgMXi4+P13nvvqW/fvrp586ZiYmLUp08feXh4KC4uznQ8wCh6QAAAACzWqFEjLV68WN26dZOfn59OnTrlWPvyyy/18ccfm44IGMMOCAAAgMWys7PVrFkzSZKvr69u3rwpSerevbs+++wzk9EA4yhAAAAALFavXj1du3ZN0sPdkJ07d0qSjh07Jm9vb5PRAOMoQAAAACzWu3dv7dmzR5I0duxYTZ06VaGhoRo0aJCGDRtmOB1gFj0gAAAATpacnKzk5GSFhoaqR48epuMARlGAAAAAAHAZ7gEBAACwwNatWxUVFSUvLy9t3br1R9/bs2dPF6UC3A87IAAAABbw8PBQdna2AgMD5eHx+DZbm82moqIiFyYD3AsFCAAAAACX4QgWAACAhYqLi7Vy5Upt2rRJly9fls1mU0hIiKKjozVw4EDZbDbTEQGj2AEBAACwSElJiXr06KHPP/9czZs3V5MmTVRSUqKvv/5aZ86cUc+ePbV582bTMQGj2AEBAACwyMqVK3XgwAHt2bNHHTt2LPXsiy++UK9evbR69WoNGjTIUELAPHZAAAAALNK5c2eFh4dr0qRJj3w+a9Ys7d+/Xzt27HBxMsB9cBM6AACARVJSUhQZGfnY51FRUTp9+rQLEwHuhwIEAADAIrm5uapdu/Zjn9euXVs3btxwYSLA/VCAAAAAWKSoqEhPPfX4FltPT08VFha6MBHgfmhCBwAAsEhJSYmGDBkib2/vRz4vKChwcSLA/VCAAAAAWGTw4ME/+R4mYKGiYwoWAAAAAJehBwQAAACAy1CAAAAAAHAZChAAAAAALkMBAgAAAMBlKEAAAAAAuAwFCAAAAACXoQABAAAA4DIUIAAAAABc5v8ApbqMoyP/GMUAAAAASUVORK5CYII=
"/>
</div>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<p>create a heatmap to easily see, and visualization</p>
</div>
</div>
</div>
</div>
<div class="jp-Cell jp-MarkdownCell jp-Notebook-cell">
<div class="jp-Cell-inputWrapper" tabindex="0">
<div class="jp-Collapser jp-InputCollapser jp-Cell-inputCollapser">
</div>
<div class="jp-InputArea jp-Cell-inputArea"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput" data-mime-type="text/markdown">
<h4 id="Write-your-Answer-here:">Write your Answer here:<a class="anchor-link" href="#Write-your-Answer-here:">¶</a></h4>
</div>
</div>
</div>
</div>Ans 20:
</main>
</body>
</html>
