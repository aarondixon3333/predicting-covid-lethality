<!DOCTYPE html>
<html>
<head><meta charset="utf-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Final Project</title><script src="https://cdnjs.cloudflare.com/ajax/libs/require.js/2.1.10/require.min.js"></script>




<style type="text/css">
    pre { line-height: 125%; }
td.linenos pre { color: #000000; background-color: #f0f0f0; padding-left: 5px; padding-right: 5px; }
span.linenos { color: #000000; background-color: #f0f0f0; padding-left: 5px; padding-right: 5px; }
td.linenos pre.special { color: #000000; background-color: #ffffc0; padding-left: 5px; padding-right: 5px; }
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

/*
 * Webkit scrollbar styling
 */

/* use standard opaque scrollbars for most nodes */

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar,
[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-corner {
  background: var(--jp-scrollbar-background-color);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-thumb {
  background: rgb(var(--jp-scrollbar-thumb-color));
  border: var(--jp-scrollbar-thumb-margin) solid transparent;
  background-clip: content-box;
  border-radius: var(--jp-scrollbar-thumb-radius);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-track:horizontal {
  border-left: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
  border-right: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
}

[data-jp-theme-scrollbars='true'] ::-webkit-scrollbar-track:vertical {
  border-top: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
  border-bottom: var(--jp-scrollbar-endpad) solid
    var(--jp-scrollbar-background-color);
}

/* for code nodes, use a transparent style of scrollbar */

[data-jp-theme-scrollbars='true'] .CodeMirror-hscrollbar::-webkit-scrollbar,
[data-jp-theme-scrollbars='true'] .CodeMirror-vscrollbar::-webkit-scrollbar,
[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-corner,
[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-corner {
  background-color: transparent;
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-thumb,
[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-thumb {
  background: rgba(var(--jp-scrollbar-thumb-color), 0.5);
  border: var(--jp-scrollbar-thumb-margin) solid transparent;
  background-clip: content-box;
  border-radius: var(--jp-scrollbar-thumb-radius);
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-hscrollbar::-webkit-scrollbar-track:horizontal {
  border-left: var(--jp-scrollbar-endpad) solid transparent;
  border-right: var(--jp-scrollbar-endpad) solid transparent;
}

[data-jp-theme-scrollbars='true']
  .CodeMirror-vscrollbar::-webkit-scrollbar-track:vertical {
  border-top: var(--jp-scrollbar-endpad) solid transparent;
  border-bottom: var(--jp-scrollbar-endpad) solid transparent;
}

/*
 * Phosphor
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

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-Widget, /* </DEPRECATED> */
.lm-Widget {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  cursor: default;
}


/* <DEPRECATED> */ .p-Widget.p-mod-hidden, /* </DEPRECATED> */
.lm-Widget.lm-mod-hidden {
  display: none !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-CommandPalette, /* </DEPRECATED> */
.lm-CommandPalette {
  display: flex;
  flex-direction: column;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-CommandPalette-search, /* </DEPRECATED> */
.lm-CommandPalette-search {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-content, /* </DEPRECATED> */
.lm-CommandPalette-content {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  min-height: 0;
  overflow: auto;
  list-style-type: none;
}


/* <DEPRECATED> */ .p-CommandPalette-header, /* </DEPRECATED> */
.lm-CommandPalette-header {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}


/* <DEPRECATED> */ .p-CommandPalette-item, /* </DEPRECATED> */
.lm-CommandPalette-item {
  display: flex;
  flex-direction: row;
}


/* <DEPRECATED> */ .p-CommandPalette-itemIcon, /* </DEPRECATED> */
.lm-CommandPalette-itemIcon {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-itemContent, /* </DEPRECATED> */
.lm-CommandPalette-itemContent {
  flex: 1 1 auto;
  overflow: hidden;
}


/* <DEPRECATED> */ .p-CommandPalette-itemShortcut, /* </DEPRECATED> */
.lm-CommandPalette-itemShortcut {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-CommandPalette-itemLabel, /* </DEPRECATED> */
.lm-CommandPalette-itemLabel {
  overflow: hidden;
  white-space: nowrap;
  text-overflow: ellipsis;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-DockPanel, /* </DEPRECATED> */
.lm-DockPanel {
  z-index: 0;
}


/* <DEPRECATED> */ .p-DockPanel-widget, /* </DEPRECATED> */
.lm-DockPanel-widget {
  z-index: 0;
}


/* <DEPRECATED> */ .p-DockPanel-tabBar, /* </DEPRECATED> */
.lm-DockPanel-tabBar {
  z-index: 1;
}


/* <DEPRECATED> */ .p-DockPanel-handle, /* </DEPRECATED> */
.lm-DockPanel-handle {
  z-index: 2;
}


/* <DEPRECATED> */ .p-DockPanel-handle.p-mod-hidden, /* </DEPRECATED> */
.lm-DockPanel-handle.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-DockPanel-handle:after, /* </DEPRECATED> */
.lm-DockPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='horizontal'],
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='horizontal'] {
  cursor: ew-resize;
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='vertical'],
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='vertical'] {
  cursor: ns-resize;
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='horizontal']:after,
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='horizontal']:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}


/* <DEPRECATED> */
.p-DockPanel-handle[data-orientation='vertical']:after,
/* </DEPRECATED> */
.lm-DockPanel-handle[data-orientation='vertical']:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}


/* <DEPRECATED> */ .p-DockPanel-overlay, /* </DEPRECATED> */
.lm-DockPanel-overlay {
  z-index: 3;
  box-sizing: border-box;
  pointer-events: none;
}


/* <DEPRECATED> */ .p-DockPanel-overlay.p-mod-hidden, /* </DEPRECATED> */
.lm-DockPanel-overlay.lm-mod-hidden {
  display: none !important;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-Menu, /* </DEPRECATED> */
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


/* <DEPRECATED> */ .p-Menu-content, /* </DEPRECATED> */
.lm-Menu-content {
  margin: 0;
  padding: 0;
  display: table;
  list-style-type: none;
}


/* <DEPRECATED> */ .p-Menu-item, /* </DEPRECATED> */
.lm-Menu-item {
  display: table-row;
}


/* <DEPRECATED> */
.p-Menu-item.p-mod-hidden,
.p-Menu-item.p-mod-collapsed,
/* </DEPRECATED> */
.lm-Menu-item.lm-mod-hidden,
.lm-Menu-item.lm-mod-collapsed {
  display: none !important;
}


/* <DEPRECATED> */
.p-Menu-itemIcon,
.p-Menu-itemSubmenuIcon,
/* </DEPRECATED> */
.lm-Menu-itemIcon,
.lm-Menu-itemSubmenuIcon {
  display: table-cell;
  text-align: center;
}


/* <DEPRECATED> */ .p-Menu-itemLabel, /* </DEPRECATED> */
.lm-Menu-itemLabel {
  display: table-cell;
  text-align: left;
}


/* <DEPRECATED> */ .p-Menu-itemShortcut, /* </DEPRECATED> */
.lm-Menu-itemShortcut {
  display: table-cell;
  text-align: right;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-MenuBar, /* </DEPRECATED> */
.lm-MenuBar {
  outline: none;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-MenuBar-content, /* </DEPRECATED> */
.lm-MenuBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex-direction: row;
  list-style-type: none;
}


/* <DEPRECATED> */ .p--MenuBar-item, /* </DEPRECATED> */
.lm-MenuBar-item {
  box-sizing: border-box;
}


/* <DEPRECATED> */
.p-MenuBar-itemIcon,
.p-MenuBar-itemLabel,
/* </DEPRECATED> */
.lm-MenuBar-itemIcon,
.lm-MenuBar-itemLabel {
  display: inline-block;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-ScrollBar, /* </DEPRECATED> */
.lm-ScrollBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */
.p-ScrollBar[data-orientation='horizontal'],
/* </DEPRECATED> */
.lm-ScrollBar[data-orientation='horizontal'] {
  flex-direction: row;
}


/* <DEPRECATED> */
.p-ScrollBar[data-orientation='vertical'],
/* </DEPRECATED> */
.lm-ScrollBar[data-orientation='vertical'] {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-ScrollBar-button, /* </DEPRECATED> */
.lm-ScrollBar-button {
  box-sizing: border-box;
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-ScrollBar-track, /* </DEPRECATED> */
.lm-ScrollBar-track {
  box-sizing: border-box;
  position: relative;
  overflow: hidden;
  flex: 1 1 auto;
}


/* <DEPRECATED> */ .p-ScrollBar-thumb, /* </DEPRECATED> */
.lm-ScrollBar-thumb {
  box-sizing: border-box;
  position: absolute;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-SplitPanel-child, /* </DEPRECATED> */
.lm-SplitPanel-child {
  z-index: 0;
}


/* <DEPRECATED> */ .p-SplitPanel-handle, /* </DEPRECATED> */
.lm-SplitPanel-handle {
  z-index: 1;
}


/* <DEPRECATED> */ .p-SplitPanel-handle.p-mod-hidden, /* </DEPRECATED> */
.lm-SplitPanel-handle.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-SplitPanel-handle:after, /* </DEPRECATED> */
.lm-SplitPanel-handle:after {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  content: '';
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='horizontal'] > .p-SplitPanel-handle,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle {
  cursor: ew-resize;
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='vertical'] > .p-SplitPanel-handle,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle {
  cursor: ns-resize;
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='horizontal'] > .p-SplitPanel-handle:after,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='horizontal'] > .lm-SplitPanel-handle:after {
  left: 50%;
  min-width: 8px;
  transform: translateX(-50%);
}


/* <DEPRECATED> */
.p-SplitPanel[data-orientation='vertical'] > .p-SplitPanel-handle:after,
/* </DEPRECATED> */
.lm-SplitPanel[data-orientation='vertical'] > .lm-SplitPanel-handle:after {
  top: 50%;
  min-height: 8px;
  transform: translateY(-50%);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-TabBar, /* </DEPRECATED> */
.lm-TabBar {
  display: flex;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}


/* <DEPRECATED> */ .p-TabBar[data-orientation='horizontal'], /* </DEPRECATED> */
.lm-TabBar[data-orientation='horizontal'] {
  flex-direction: row;
}


/* <DEPRECATED> */ .p-TabBar[data-orientation='vertical'], /* </DEPRECATED> */
.lm-TabBar[data-orientation='vertical'] {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-TabBar-content, /* </DEPRECATED> */
.lm-TabBar-content {
  margin: 0;
  padding: 0;
  display: flex;
  flex: 1 1 auto;
  list-style-type: none;
}


/* <DEPRECATED> */
.p-TabBar[data-orientation='horizontal'] > .p-TabBar-content,
/* </DEPRECATED> */
.lm-TabBar[data-orientation='horizontal'] > .lm-TabBar-content {
  flex-direction: row;
}


/* <DEPRECATED> */
.p-TabBar[data-orientation='vertical'] > .p-TabBar-content,
/* </DEPRECATED> */
.lm-TabBar[data-orientation='vertical'] > .lm-TabBar-content {
  flex-direction: column;
}


/* <DEPRECATED> */ .p-TabBar-tab, /* </DEPRECATED> */
.lm-TabBar-tab {
  display: flex;
  flex-direction: row;
  box-sizing: border-box;
  overflow: hidden;
}


/* <DEPRECATED> */
.p-TabBar-tabIcon,
.p-TabBar-tabCloseIcon,
/* </DEPRECATED> */
.lm-TabBar-tabIcon,
.lm-TabBar-tabCloseIcon {
  flex: 0 0 auto;
}


/* <DEPRECATED> */ .p-TabBar-tabLabel, /* </DEPRECATED> */
.lm-TabBar-tabLabel {
  flex: 1 1 auto;
  overflow: hidden;
  white-space: nowrap;
}


/* <DEPRECATED> */ .p-TabBar-tab.p-mod-hidden, /* </DEPRECATED> */
.lm-TabBar-tab.lm-mod-hidden {
  display: none !important;
}


/* <DEPRECATED> */ .p-TabBar.p-mod-dragging .p-TabBar-tab, /* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging .lm-TabBar-tab {
  position: relative;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging[data-orientation='horizontal'] .p-TabBar-tab,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging[data-orientation='horizontal'] .lm-TabBar-tab {
  left: 0;
  transition: left 150ms ease;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging[data-orientation='vertical'] .p-TabBar-tab,
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging[data-orientation='vertical'] .lm-TabBar-tab {
  top: 0;
  transition: top 150ms ease;
}


/* <DEPRECATED> */
.p-TabBar.p-mod-dragging .p-TabBar-tab.p-mod-dragging
/* </DEPRECATED> */
.lm-TabBar.lm-mod-dragging .lm-TabBar-tab.lm-mod-dragging {
  transition: none;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ .p-TabPanel-tabBar, /* </DEPRECATED> */
.lm-TabPanel-tabBar {
  z-index: 1;
}


/* <DEPRECATED> */ .p-TabPanel-stackedPanel, /* </DEPRECATED> */
.lm-TabPanel-stackedPanel {
  z-index: 0;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/

@charset "UTF-8";
/*!

Copyright 2015-present Palantir Technologies, Inc. All rights reserved.
Licensed under the Apache License, Version 2.0.

*/
html{
  -webkit-box-sizing:border-box;
          box-sizing:border-box; }

*,
*::before,
*::after{
  -webkit-box-sizing:inherit;
          box-sizing:inherit; }

body{
  text-transform:none;
  line-height:1.28581;
  letter-spacing:0;
  font-size:14px;
  font-weight:400;
  color:#182026;
  font-family:-apple-system, "BlinkMacSystemFont", "Segoe UI", "Roboto", "Oxygen", "Ubuntu", "Cantarell", "Open Sans", "Helvetica Neue", "Icons16", sans-serif; }

p{
  margin-top:0;
  margin-bottom:10px; }

small{
  font-size:12px; }

strong{
  font-weight:600; }

::-moz-selection{
  background:rgba(125, 188, 255, 0.6); }

::selection{
  background:rgba(125, 188, 255, 0.6); }
.bp3-heading{
  color:#182026;
  font-weight:600;
  margin:0 0 10px;
  padding:0; }
  .bp3-dark .bp3-heading{
    color:#f5f8fa; }

h1.bp3-heading, .bp3-running-text h1{
  line-height:40px;
  font-size:36px; }

h2.bp3-heading, .bp3-running-text h2{
  line-height:32px;
  font-size:28px; }

h3.bp3-heading, .bp3-running-text h3{
  line-height:25px;
  font-size:22px; }

h4.bp3-heading, .bp3-running-text h4{
  line-height:21px;
  font-size:18px; }

h5.bp3-heading, .bp3-running-text h5{
  line-height:19px;
  font-size:16px; }

h6.bp3-heading, .bp3-running-text h6{
  line-height:16px;
  font-size:14px; }
.bp3-ui-text{
  text-transform:none;
  line-height:1.28581;
  letter-spacing:0;
  font-size:14px;
  font-weight:400; }

.bp3-monospace-text{
  text-transform:none;
  font-family:monospace; }

.bp3-text-muted{
  color:#5c7080; }
  .bp3-dark .bp3-text-muted{
    color:#a7b6c2; }

.bp3-text-disabled{
  color:rgba(92, 112, 128, 0.6); }
  .bp3-dark .bp3-text-disabled{
    color:rgba(167, 182, 194, 0.6); }

.bp3-text-overflow-ellipsis{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal; }
.bp3-running-text{
  line-height:1.5;
  font-size:14px; }
  .bp3-running-text h1{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h1{
      color:#f5f8fa; }
  .bp3-running-text h2{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h2{
      color:#f5f8fa; }
  .bp3-running-text h3{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h3{
      color:#f5f8fa; }
  .bp3-running-text h4{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h4{
      color:#f5f8fa; }
  .bp3-running-text h5{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h5{
      color:#f5f8fa; }
  .bp3-running-text h6{
    color:#182026;
    font-weight:600;
    margin-top:40px;
    margin-bottom:20px; }
    .bp3-dark .bp3-running-text h6{
      color:#f5f8fa; }
  .bp3-running-text hr{
    margin:20px 0;
    border:none;
    border-bottom:1px solid rgba(16, 22, 26, 0.15); }
    .bp3-dark .bp3-running-text hr{
      border-color:rgba(255, 255, 255, 0.15); }
  .bp3-running-text p{
    margin:0 0 10px;
    padding:0; }

.bp3-text-large{
  font-size:16px; }

.bp3-text-small{
  font-size:12px; }
a{
  text-decoration:none;
  color:#106ba3; }
  a:hover{
    cursor:pointer;
    text-decoration:underline;
    color:#106ba3; }
  a .bp3-icon, a .bp3-icon-standard, a .bp3-icon-large{
    color:inherit; }
  a code,
  .bp3-dark a code{
    color:inherit; }
  .bp3-dark a,
  .bp3-dark a:hover{
    color:#48aff0; }
    .bp3-dark a .bp3-icon, .bp3-dark a .bp3-icon-standard, .bp3-dark a .bp3-icon-large,
    .bp3-dark a:hover .bp3-icon,
    .bp3-dark a:hover .bp3-icon-standard,
    .bp3-dark a:hover .bp3-icon-large{
      color:inherit; }
.bp3-running-text code, .bp3-code{
  text-transform:none;
  font-family:monospace;
  border-radius:3px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2);
  background:rgba(255, 255, 255, 0.7);
  padding:2px 5px;
  color:#5c7080;
  font-size:smaller; }
  .bp3-dark .bp3-running-text code, .bp3-running-text .bp3-dark code, .bp3-dark .bp3-code{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#a7b6c2; }
  .bp3-running-text a > code, a > .bp3-code{
    color:#137cbd; }
    .bp3-dark .bp3-running-text a > code, .bp3-running-text .bp3-dark a > code, .bp3-dark a > .bp3-code{
      color:inherit; }

.bp3-running-text pre, .bp3-code-block{
  text-transform:none;
  font-family:monospace;
  display:block;
  margin:10px 0;
  border-radius:3px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
  background:rgba(255, 255, 255, 0.7);
  padding:13px 15px 12px;
  line-height:1.4;
  color:#182026;
  font-size:13px;
  word-break:break-all;
  word-wrap:break-word; }
  .bp3-dark .bp3-running-text pre, .bp3-running-text .bp3-dark pre, .bp3-dark .bp3-code-block{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#f5f8fa; }
  .bp3-running-text pre > code, .bp3-code-block > code{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:none;
    padding:0;
    color:inherit;
    font-size:inherit; }

.bp3-running-text kbd, .bp3-key{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  background:#ffffff;
  min-width:24px;
  height:24px;
  padding:3px 6px;
  vertical-align:middle;
  line-height:24px;
  color:#5c7080;
  font-family:inherit;
  font-size:12px; }
  .bp3-running-text kbd .bp3-icon, .bp3-key .bp3-icon, .bp3-running-text kbd .bp3-icon-standard, .bp3-key .bp3-icon-standard, .bp3-running-text kbd .bp3-icon-large, .bp3-key .bp3-icon-large{
    margin-right:5px; }
  .bp3-dark .bp3-running-text kbd, .bp3-running-text .bp3-dark kbd, .bp3-dark .bp3-key{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
    background:#394b59;
    color:#a7b6c2; }
.bp3-running-text blockquote, .bp3-blockquote{
  margin:0 0 10px;
  border-left:solid 4px rgba(167, 182, 194, 0.5);
  padding:0 20px; }
  .bp3-dark .bp3-running-text blockquote, .bp3-running-text .bp3-dark blockquote, .bp3-dark .bp3-blockquote{
    border-color:rgba(115, 134, 148, 0.5); }
.bp3-running-text ul,
.bp3-running-text ol, .bp3-list{
  margin:10px 0;
  padding-left:30px; }
  .bp3-running-text ul li:not(:last-child), .bp3-running-text ol li:not(:last-child), .bp3-list li:not(:last-child){
    margin-bottom:5px; }
  .bp3-running-text ul ol, .bp3-running-text ol ol, .bp3-list ol,
  .bp3-running-text ul ul,
  .bp3-running-text ol ul,
  .bp3-list ul{
    margin-top:5px; }

.bp3-list-unstyled{
  margin:0;
  padding:0;
  list-style:none; }
  .bp3-list-unstyled li{
    padding:0; }
.bp3-rtl{
  text-align:right; }

.bp3-dark{
  color:#f5f8fa; }

:focus{
  outline:rgba(19, 124, 189, 0.6) auto 2px;
  outline-offset:2px;
  -moz-outline-radius:6px; }

.bp3-focus-disabled :focus{
  outline:none !important; }
  .bp3-focus-disabled :focus ~ .bp3-control-indicator{
    outline:none !important; }

.bp3-alert{
  max-width:400px;
  padding:20px; }

.bp3-alert-body{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }
  .bp3-alert-body .bp3-icon{
    margin-top:0;
    margin-right:20px;
    font-size:40px; }

.bp3-alert-footer{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:reverse;
      -ms-flex-direction:row-reverse;
          flex-direction:row-reverse;
  margin-top:10px; }
  .bp3-alert-footer .bp3-button{
    margin-left:10px; }
.bp3-breadcrumbs{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-wrap:wrap;
      flex-wrap:wrap;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  margin:0;
  cursor:default;
  height:30px;
  padding:0;
  list-style:none; }
  .bp3-breadcrumbs > li{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center; }
    .bp3-breadcrumbs > li::after{
      display:block;
      margin:0 5px;
      background:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M10.71 7.29l-4-4a1.003 1.003 0 0 0-1.42 1.42L8.59 8 5.3 11.29c-.19.18-.3.43-.3.71a1.003 1.003 0 0 0 1.71.71l4-4c.18-.18.29-.43.29-.71 0-.28-.11-.53-.29-.71z' fill='%235C7080'/%3e%3c/svg%3e");
      width:16px;
      height:16px;
      content:""; }
    .bp3-breadcrumbs > li:last-of-type::after{
      display:none; }

.bp3-breadcrumb,
.bp3-breadcrumb-current,
.bp3-breadcrumbs-collapsed{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  font-size:16px; }

.bp3-breadcrumb,
.bp3-breadcrumbs-collapsed{
  color:#5c7080; }

.bp3-breadcrumb:hover{
  text-decoration:none; }

.bp3-breadcrumb.bp3-disabled{
  cursor:not-allowed;
  color:rgba(92, 112, 128, 0.6); }

.bp3-breadcrumb .bp3-icon{
  margin-right:5px; }

.bp3-breadcrumb-current{
  color:inherit;
  font-weight:600; }
  .bp3-breadcrumb-current .bp3-input{
    vertical-align:baseline;
    font-size:inherit;
    font-weight:inherit; }

.bp3-breadcrumbs-collapsed{
  margin-right:2px;
  border:none;
  border-radius:3px;
  background:#ced9e0;
  cursor:pointer;
  padding:1px 5px;
  vertical-align:text-bottom; }
  .bp3-breadcrumbs-collapsed::before{
    display:block;
    background:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cg fill='%235C7080'%3e%3ccircle cx='2' cy='8.03' r='2'/%3e%3ccircle cx='14' cy='8.03' r='2'/%3e%3ccircle cx='8' cy='8.03' r='2'/%3e%3c/g%3e%3c/svg%3e") center no-repeat;
    width:16px;
    height:16px;
    content:""; }
  .bp3-breadcrumbs-collapsed:hover{
    background:#bfccd6;
    text-decoration:none;
    color:#182026; }

.bp3-dark .bp3-breadcrumb,
.bp3-dark .bp3-breadcrumbs-collapsed{
  color:#a7b6c2; }

.bp3-dark .bp3-breadcrumbs > li::after{
  color:#a7b6c2; }

.bp3-dark .bp3-breadcrumb.bp3-disabled{
  color:rgba(167, 182, 194, 0.6); }

.bp3-dark .bp3-breadcrumb-current{
  color:#f5f8fa; }

.bp3-dark .bp3-breadcrumbs-collapsed{
  background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-breadcrumbs-collapsed:hover{
    background:rgba(16, 22, 26, 0.6);
    color:#f5f8fa; }
.bp3-button{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  border:none;
  border-radius:3px;
  cursor:pointer;
  padding:5px 10px;
  vertical-align:middle;
  text-align:left;
  font-size:14px;
  min-width:30px;
  min-height:30px; }
  .bp3-button > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-button > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-button::before,
  .bp3-button > *{
    margin-right:7px; }
  .bp3-button:empty::before,
  .bp3-button > :last-child{
    margin-right:0; }
  .bp3-button:empty{
    padding:0 !important; }
  .bp3-button:disabled, .bp3-button.bp3-disabled{
    cursor:not-allowed; }
  .bp3-button.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-button.bp3-align-right,
  .bp3-align-right .bp3-button{
    text-align:right; }
  .bp3-button.bp3-align-left,
  .bp3-align-left .bp3-button{
    text-align:left; }
  .bp3-button:not([class*="bp3-intent-"]){
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    color:#182026; }
    .bp3-button:not([class*="bp3-intent-"]):hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
      background-clip:padding-box;
      background-color:#ebf1f5; }
    .bp3-button:not([class*="bp3-intent-"]):active, .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#d8e1e8;
      background-image:none; }
    .bp3-button:not([class*="bp3-intent-"]):disabled, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled{
      outline:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(206, 217, 224, 0.5);
      background-image:none;
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6); }
      .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active, .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active:hover, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active, .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active:hover{
        background:rgba(206, 217, 224, 0.7); }
  .bp3-button.bp3-intent-primary{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
    .bp3-button.bp3-intent-primary:hover, .bp3-button.bp3-intent-primary:active, .bp3-button.bp3-intent-primary.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-primary:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
      background-color:#106ba3; }
    .bp3-button.bp3-intent-primary:active, .bp3-button.bp3-intent-primary.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#0e5a8a;
      background-image:none; }
    .bp3-button.bp3-intent-primary:disabled, .bp3-button.bp3-intent-primary.bp3-disabled{
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(19, 124, 189, 0.5);
      background-image:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-success{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#0f9960;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
    .bp3-button.bp3-intent-success:hover, .bp3-button.bp3-intent-success:active, .bp3-button.bp3-intent-success.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-success:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
      background-color:#0d8050; }
    .bp3-button.bp3-intent-success:active, .bp3-button.bp3-intent-success.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#0a6640;
      background-image:none; }
    .bp3-button.bp3-intent-success:disabled, .bp3-button.bp3-intent-success.bp3-disabled{
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(15, 153, 96, 0.5);
      background-image:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-warning{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#d9822b;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
    .bp3-button.bp3-intent-warning:hover, .bp3-button.bp3-intent-warning:active, .bp3-button.bp3-intent-warning.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-warning:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
      background-color:#bf7326; }
    .bp3-button.bp3-intent-warning:active, .bp3-button.bp3-intent-warning.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#a66321;
      background-image:none; }
    .bp3-button.bp3-intent-warning:disabled, .bp3-button.bp3-intent-warning.bp3-disabled{
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(217, 130, 43, 0.5);
      background-image:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button.bp3-intent-danger{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#db3737;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
    .bp3-button.bp3-intent-danger:hover, .bp3-button.bp3-intent-danger:active, .bp3-button.bp3-intent-danger.bp3-active{
      color:#ffffff; }
    .bp3-button.bp3-intent-danger:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
      background-color:#c23030; }
    .bp3-button.bp3-intent-danger:active, .bp3-button.bp3-intent-danger.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#a82a2a;
      background-image:none; }
    .bp3-button.bp3-intent-danger:disabled, .bp3-button.bp3-intent-danger.bp3-disabled{
      border-color:transparent;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(219, 55, 55, 0.5);
      background-image:none;
      color:rgba(255, 255, 255, 0.6); }
  .bp3-button[class*="bp3-intent-"] .bp3-button-spinner .bp3-spinner-head{
    stroke:#ffffff; }
  .bp3-button.bp3-large,
  .bp3-large .bp3-button{
    min-width:40px;
    min-height:40px;
    padding:5px 15px;
    font-size:16px; }
    .bp3-button.bp3-large::before,
    .bp3-button.bp3-large > *,
    .bp3-large .bp3-button::before,
    .bp3-large .bp3-button > *{
      margin-right:10px; }
    .bp3-button.bp3-large:empty::before,
    .bp3-button.bp3-large > :last-child,
    .bp3-large .bp3-button:empty::before,
    .bp3-large .bp3-button > :last-child{
      margin-right:0; }
  .bp3-button.bp3-small,
  .bp3-small .bp3-button{
    min-width:24px;
    min-height:24px;
    padding:0 7px; }
  .bp3-button.bp3-loading{
    position:relative; }
    .bp3-button.bp3-loading[class*="bp3-icon-"]::before{
      visibility:hidden; }
    .bp3-button.bp3-loading .bp3-button-spinner{
      position:absolute;
      margin:0; }
    .bp3-button.bp3-loading > :not(.bp3-button-spinner){
      visibility:hidden; }
  .bp3-button[class*="bp3-icon-"]::before{
    line-height:1;
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-weight:400;
    font-style:normal;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    color:#5c7080; }
  .bp3-button .bp3-icon, .bp3-button .bp3-icon-standard, .bp3-button .bp3-icon-large{
    color:#5c7080; }
    .bp3-button .bp3-icon.bp3-align-right, .bp3-button .bp3-icon-standard.bp3-align-right, .bp3-button .bp3-icon-large.bp3-align-right{
      margin-left:7px; }
  .bp3-button .bp3-icon:first-child:last-child,
  .bp3-button .bp3-spinner + .bp3-icon:last-child{
    margin:0 -7px; }
  .bp3-dark .bp3-button:not([class*="bp3-intent-"]){
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#394b59;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
    color:#f5f8fa; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):hover, .bp3-dark .bp3-button:not([class*="bp3-intent-"]):active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      color:#f5f8fa; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):hover{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#30404d; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-active{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#202b33;
      background-image:none; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]):disabled, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(57, 75, 89, 0.5);
      background-image:none;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-button:not([class*="bp3-intent-"]):disabled.bp3-active, .bp3-dark .bp3-button:not([class*="bp3-intent-"]).bp3-disabled.bp3-active{
        background:rgba(57, 75, 89, 0.7); }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-button-spinner .bp3-spinner-head{
      background:rgba(16, 22, 26, 0.5);
      stroke:#8a9ba8; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"])[class*="bp3-icon-"]::before{
      color:#a7b6c2; }
    .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon, .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon-standard, .bp3-dark .bp3-button:not([class*="bp3-intent-"]) .bp3-icon-large{
      color:#a7b6c2; }
  .bp3-dark .bp3-button[class*="bp3-intent-"]{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:hover{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:active, .bp3-dark .bp3-button[class*="bp3-intent-"].bp3-active{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2); }
    .bp3-dark .bp3-button[class*="bp3-intent-"]:disabled, .bp3-dark .bp3-button[class*="bp3-intent-"].bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background-image:none;
      color:rgba(255, 255, 255, 0.3); }
    .bp3-dark .bp3-button[class*="bp3-intent-"] .bp3-button-spinner .bp3-spinner-head{
      stroke:#8a9ba8; }
  .bp3-button:disabled::before,
  .bp3-button:disabled .bp3-icon, .bp3-button:disabled .bp3-icon-standard, .bp3-button:disabled .bp3-icon-large, .bp3-button.bp3-disabled::before,
  .bp3-button.bp3-disabled .bp3-icon, .bp3-button.bp3-disabled .bp3-icon-standard, .bp3-button.bp3-disabled .bp3-icon-large, .bp3-button[class*="bp3-intent-"]::before,
  .bp3-button[class*="bp3-intent-"] .bp3-icon, .bp3-button[class*="bp3-intent-"] .bp3-icon-standard, .bp3-button[class*="bp3-intent-"] .bp3-icon-large{
    color:inherit !important; }
  .bp3-button.bp3-minimal{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:none; }
    .bp3-button.bp3-minimal:hover{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(167, 182, 194, 0.3);
      text-decoration:none;
      color:#182026; }
    .bp3-button.bp3-minimal:active, .bp3-button.bp3-minimal.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(115, 134, 148, 0.3);
      color:#182026; }
    .bp3-button.bp3-minimal:disabled, .bp3-button.bp3-minimal:disabled:hover, .bp3-button.bp3-minimal.bp3-disabled, .bp3-button.bp3-minimal.bp3-disabled:hover{
      background:none;
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6); }
      .bp3-button.bp3-minimal:disabled.bp3-active, .bp3-button.bp3-minimal:disabled:hover.bp3-active, .bp3-button.bp3-minimal.bp3-disabled.bp3-active, .bp3-button.bp3-minimal.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button.bp3-minimal{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:inherit; }
      .bp3-dark .bp3-button.bp3-minimal:hover, .bp3-dark .bp3-button.bp3-minimal:active, .bp3-dark .bp3-button.bp3-minimal.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none; }
      .bp3-dark .bp3-button.bp3-minimal:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button.bp3-minimal:active, .bp3-dark .bp3-button.bp3-minimal.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button.bp3-minimal:disabled, .bp3-dark .bp3-button.bp3-minimal:disabled:hover, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled:hover{
        background:none;
        cursor:not-allowed;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-button.bp3-minimal:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal:disabled:hover.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:hover, .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button.bp3-minimal.bp3-intent-primary:disabled, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-primary:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-success{
      color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:hover, .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button.bp3-minimal.bp3-intent-success:disabled, .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-success:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:hover, .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button.bp3-minimal.bp3-intent-warning:disabled, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-warning:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button.bp3-minimal.bp3-intent-danger{
      color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:hover, .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button.bp3-minimal.bp3-intent-danger:disabled, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button.bp3-minimal.bp3-intent-danger:disabled.bp3-active, .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button.bp3-minimal.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:disabled, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button.bp3-minimal.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }

a.bp3-button{
  text-align:center;
  text-decoration:none;
  -webkit-transition:none;
  transition:none; }
  a.bp3-button, a.bp3-button:hover, a.bp3-button:active{
    color:#182026; }
  a.bp3-button.bp3-disabled{
    color:rgba(92, 112, 128, 0.6); }

.bp3-button-text{
  -webkit-box-flex:0;
      -ms-flex:0 1 auto;
          flex:0 1 auto; }

.bp3-button.bp3-align-left .bp3-button-text, .bp3-button.bp3-align-right .bp3-button-text,
.bp3-button-group.bp3-align-left .bp3-button-text,
.bp3-button-group.bp3-align-right .bp3-button-text{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto; }
.bp3-button-group{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex; }
  .bp3-button-group .bp3-button{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    position:relative;
    z-index:4; }
    .bp3-button-group .bp3-button:focus{
      z-index:5; }
    .bp3-button-group .bp3-button:hover{
      z-index:6; }
    .bp3-button-group .bp3-button:active, .bp3-button-group .bp3-button.bp3-active{
      z-index:7; }
    .bp3-button-group .bp3-button:disabled, .bp3-button-group .bp3-button.bp3-disabled{
      z-index:3; }
    .bp3-button-group .bp3-button[class*="bp3-intent-"]{
      z-index:9; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:focus{
        z-index:10; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:hover{
        z-index:11; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:active, .bp3-button-group .bp3-button[class*="bp3-intent-"].bp3-active{
        z-index:12; }
      .bp3-button-group .bp3-button[class*="bp3-intent-"]:disabled, .bp3-button-group .bp3-button[class*="bp3-intent-"].bp3-disabled{
        z-index:8; }
  .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:first-child) .bp3-button,
  .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:first-child){
    border-top-left-radius:0;
    border-bottom-left-radius:0; }
  .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:last-child){
    margin-right:-1px;
    border-top-right-radius:0;
    border-bottom-right-radius:0; }
  .bp3-button-group.bp3-minimal .bp3-button{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:none; }
    .bp3-button-group.bp3-minimal .bp3-button:hover{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(167, 182, 194, 0.3);
      text-decoration:none;
      color:#182026; }
    .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(115, 134, 148, 0.3);
      color:#182026; }
    .bp3-button-group.bp3-minimal .bp3-button:disabled, .bp3-button-group.bp3-minimal .bp3-button:disabled:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover{
      background:none;
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6); }
      .bp3-button-group.bp3-minimal .bp3-button:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button:disabled:hover.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover.bp3-active{
        background:rgba(115, 134, 148, 0.3); }
    .bp3-dark .bp3-button-group.bp3-minimal .bp3-button{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:inherit; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:hover, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:hover{
        background:rgba(138, 155, 168, 0.15); }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-active{
        background:rgba(138, 155, 168, 0.3);
        color:#f5f8fa; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled:hover, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover{
        background:none;
        cursor:not-allowed;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button:disabled:hover.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-disabled:hover.bp3-active{
          background:rgba(138, 155, 168, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary{
      color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.15);
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#106ba3; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(16, 107, 163, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
        stroke:#106ba3; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary{
        color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:hover{
          background:rgba(19, 124, 189, 0.2);
          color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-active{
          background:rgba(19, 124, 189, 0.3);
          color:#48aff0; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled{
          background:none;
          color:rgba(72, 175, 240, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-primary.bp3-disabled.bp3-active{
            background:rgba(19, 124, 189, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success{
      color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.15);
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#0d8050; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(13, 128, 80, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
        stroke:#0d8050; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success{
        color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:hover{
          background:rgba(15, 153, 96, 0.2);
          color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-active{
          background:rgba(15, 153, 96, 0.3);
          color:#3dcc91; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled{
          background:none;
          color:rgba(61, 204, 145, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-success.bp3-disabled.bp3-active{
            background:rgba(15, 153, 96, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning{
      color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.15);
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#bf7326; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(191, 115, 38, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
        stroke:#bf7326; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning{
        color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:hover{
          background:rgba(217, 130, 43, 0.2);
          color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-active{
          background:rgba(217, 130, 43, 0.3);
          color:#ffb366; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled{
          background:none;
          color:rgba(255, 179, 102, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-warning.bp3-disabled.bp3-active{
            background:rgba(217, 130, 43, 0.3); }
    .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger{
      color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:none;
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.15);
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#c23030; }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(194, 48, 48, 0.5); }
        .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled.bp3-active, .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }
      .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
        stroke:#c23030; }
      .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger{
        color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:hover{
          background:rgba(219, 55, 55, 0.2);
          color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-active{
          background:rgba(219, 55, 55, 0.3);
          color:#ff7373; }
        .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled{
          background:none;
          color:rgba(255, 115, 115, 0.5); }
          .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-button-group.bp3-minimal .bp3-button.bp3-intent-danger.bp3-disabled.bp3-active{
            background:rgba(219, 55, 55, 0.3); }
  .bp3-button-group .bp3-popover-wrapper,
  .bp3-button-group .bp3-popover-target{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-button-group.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-button-group .bp3-button.bp3-fill,
  .bp3-button-group.bp3-fill .bp3-button:not(.bp3-fixed){
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-button-group.bp3-vertical{
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column;
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch;
    vertical-align:top; }
    .bp3-button-group.bp3-vertical.bp3-fill{
      width:unset;
      height:100%; }
    .bp3-button-group.bp3-vertical .bp3-button{
      margin-right:0 !important;
      width:100%; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:first-child .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:first-child{
      border-radius:3px 3px 0 0; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:last-child .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:last-child{
      border-radius:0 0 3px 3px; }
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
    .bp3-button-group.bp3-vertical:not(.bp3-minimal) > .bp3-button:not(:last-child){
      margin-bottom:-1px; }
  .bp3-button-group.bp3-align-left .bp3-button{
    text-align:left; }
  .bp3-dark .bp3-button-group:not(.bp3-minimal) > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-dark .bp3-button-group:not(.bp3-minimal) > .bp3-button:not(:last-child){
    margin-right:1px; }
  .bp3-dark .bp3-button-group.bp3-vertical > .bp3-popover-wrapper:not(:last-child) .bp3-button,
  .bp3-dark .bp3-button-group.bp3-vertical > .bp3-button:not(:last-child){
    margin-bottom:1px; }
.bp3-callout{
  line-height:1.5;
  font-size:14px;
  position:relative;
  border-radius:3px;
  background-color:rgba(138, 155, 168, 0.15);
  width:100%;
  padding:10px 12px 9px; }
  .bp3-callout[class*="bp3-icon-"]{
    padding-left:40px; }
    .bp3-callout[class*="bp3-icon-"]::before{
      line-height:1;
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-weight:400;
      font-style:normal;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased;
      position:absolute;
      top:10px;
      left:10px;
      color:#5c7080; }
  .bp3-callout.bp3-callout-icon{
    padding-left:40px; }
    .bp3-callout.bp3-callout-icon > .bp3-icon:first-child{
      position:absolute;
      top:10px;
      left:10px;
      color:#5c7080; }
  .bp3-callout .bp3-heading{
    margin-top:0;
    margin-bottom:5px;
    line-height:20px; }
    .bp3-callout .bp3-heading:last-child{
      margin-bottom:0; }
  .bp3-dark .bp3-callout{
    background-color:rgba(138, 155, 168, 0.2); }
    .bp3-dark .bp3-callout[class*="bp3-icon-"]::before{
      color:#a7b6c2; }
  .bp3-callout.bp3-intent-primary{
    background-color:rgba(19, 124, 189, 0.15); }
    .bp3-callout.bp3-intent-primary[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-primary > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-primary .bp3-heading{
      color:#106ba3; }
    .bp3-dark .bp3-callout.bp3-intent-primary{
      background-color:rgba(19, 124, 189, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-primary[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-primary > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-primary .bp3-heading{
        color:#48aff0; }
  .bp3-callout.bp3-intent-success{
    background-color:rgba(15, 153, 96, 0.15); }
    .bp3-callout.bp3-intent-success[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-success > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-success .bp3-heading{
      color:#0d8050; }
    .bp3-dark .bp3-callout.bp3-intent-success{
      background-color:rgba(15, 153, 96, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-success[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-success > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-success .bp3-heading{
        color:#3dcc91; }
  .bp3-callout.bp3-intent-warning{
    background-color:rgba(217, 130, 43, 0.15); }
    .bp3-callout.bp3-intent-warning[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-warning > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-warning .bp3-heading{
      color:#bf7326; }
    .bp3-dark .bp3-callout.bp3-intent-warning{
      background-color:rgba(217, 130, 43, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-warning[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-warning > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-warning .bp3-heading{
        color:#ffb366; }
  .bp3-callout.bp3-intent-danger{
    background-color:rgba(219, 55, 55, 0.15); }
    .bp3-callout.bp3-intent-danger[class*="bp3-icon-"]::before,
    .bp3-callout.bp3-intent-danger > .bp3-icon:first-child,
    .bp3-callout.bp3-intent-danger .bp3-heading{
      color:#c23030; }
    .bp3-dark .bp3-callout.bp3-intent-danger{
      background-color:rgba(219, 55, 55, 0.25); }
      .bp3-dark .bp3-callout.bp3-intent-danger[class*="bp3-icon-"]::before,
      .bp3-dark .bp3-callout.bp3-intent-danger > .bp3-icon:first-child,
      .bp3-dark .bp3-callout.bp3-intent-danger .bp3-heading{
        color:#ff7373; }
  .bp3-running-text .bp3-callout{
    margin:20px 0; }
.bp3-card{
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
  background-color:#ffffff;
  padding:20px;
  -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-card.bp3-dark,
  .bp3-dark .bp3-card{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
    background-color:#30404d; }

.bp3-elevation-0{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.15), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }
  .bp3-elevation-0.bp3-dark,
  .bp3-dark .bp3-elevation-0{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), 0 0 0 rgba(16, 22, 26, 0), 0 0 0 rgba(16, 22, 26, 0); }

.bp3-elevation-1{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-1.bp3-dark,
  .bp3-dark .bp3-elevation-1{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-elevation-2{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 1px 1px rgba(16, 22, 26, 0.2), 0 2px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 1px 1px rgba(16, 22, 26, 0.2), 0 2px 6px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-2.bp3-dark,
  .bp3-dark .bp3-elevation-2{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.4), 0 2px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.4), 0 2px 6px rgba(16, 22, 26, 0.4); }

.bp3-elevation-3{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-3.bp3-dark,
  .bp3-dark .bp3-elevation-3{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }

.bp3-elevation-4{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2); }
  .bp3-elevation-4.bp3-dark,
  .bp3-dark .bp3-elevation-4{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4); }

.bp3-card.bp3-interactive:hover{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  cursor:pointer; }
  .bp3-card.bp3-interactive:hover.bp3-dark,
  .bp3-dark .bp3-card.bp3-interactive:hover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }

.bp3-card.bp3-interactive:active{
  opacity:0.9;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  -webkit-transition-duration:0;
          transition-duration:0; }
  .bp3-card.bp3-interactive:active.bp3-dark,
  .bp3-dark .bp3-card.bp3-interactive:active{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-collapse{
  height:0;
  overflow-y:hidden;
  -webkit-transition:height 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:height 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-collapse .bp3-collapse-body{
    -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-collapse .bp3-collapse-body[aria-hidden="true"]{
      display:none; }

.bp3-context-menu .bp3-popover-target{
  display:block; }

.bp3-context-menu-popover-target{
  position:fixed; }

.bp3-divider{
  margin:5px;
  border-right:1px solid rgba(16, 22, 26, 0.15);
  border-bottom:1px solid rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-divider{
    border-color:rgba(16, 22, 26, 0.4); }
.bp3-dialog-container{
  opacity:1;
  -webkit-transform:scale(1);
          transform:scale(1);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  width:100%;
  min-height:100%;
  pointer-events:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-dialog-container.bp3-overlay-enter > .bp3-dialog, .bp3-dialog-container.bp3-overlay-appear > .bp3-dialog{
    opacity:0;
    -webkit-transform:scale(0.5);
            transform:scale(0.5); }
  .bp3-dialog-container.bp3-overlay-enter-active > .bp3-dialog, .bp3-dialog-container.bp3-overlay-appear-active > .bp3-dialog{
    opacity:1;
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-property:opacity, -webkit-transform;
    transition-property:opacity, -webkit-transform;
    transition-property:opacity, transform;
    transition-property:opacity, transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-dialog-container.bp3-overlay-exit > .bp3-dialog{
    opacity:1;
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-dialog-container.bp3-overlay-exit-active > .bp3-dialog{
    opacity:0;
    -webkit-transform:scale(0.5);
            transform:scale(0.5);
    -webkit-transition-property:opacity, -webkit-transform;
    transition-property:opacity, -webkit-transform;
    transition-property:opacity, transform;
    transition-property:opacity, transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }

.bp3-dialog{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:30px 0;
  border-radius:6px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  background:#ebf1f5;
  width:500px;
  padding-bottom:20px;
  pointer-events:all;
  -webkit-user-select:text;
     -moz-user-select:text;
      -ms-user-select:text;
          user-select:text; }
  .bp3-dialog:focus{
    outline:0; }
  .bp3-dialog.bp3-dark,
  .bp3-dark .bp3-dialog{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    background:#293742;
    color:#f5f8fa; }

.bp3-dialog-header{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  border-radius:6px 6px 0 0;
  -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
  background:#ffffff;
  min-height:40px;
  padding-right:5px;
  padding-left:20px; }
  .bp3-dialog-header .bp3-icon-large,
  .bp3-dialog-header .bp3-icon{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    margin-right:10px;
    color:#5c7080; }
  .bp3-dialog-header .bp3-heading{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    margin:0;
    line-height:inherit; }
    .bp3-dialog-header .bp3-heading:last-child{
      margin-right:20px; }
  .bp3-dark .bp3-dialog-header{
    -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
    background:#30404d; }
    .bp3-dark .bp3-dialog-header .bp3-icon-large,
    .bp3-dark .bp3-dialog-header .bp3-icon{
      color:#a7b6c2; }

.bp3-dialog-body{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  margin:20px;
  line-height:18px; }

.bp3-dialog-footer{
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  margin:0 20px; }

.bp3-dialog-footer-actions{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-pack:end;
      -ms-flex-pack:end;
          justify-content:flex-end; }
  .bp3-dialog-footer-actions .bp3-button{
    margin-left:10px; }
.bp3-drawer{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:0;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  background:#ffffff;
  padding:0; }
  .bp3-drawer:focus{
    outline:0; }
  .bp3-drawer.bp3-position-top{
    top:0;
    right:0;
    left:0;
    height:50%; }
    .bp3-drawer.bp3-position-top.bp3-overlay-enter, .bp3-drawer.bp3-position-top.bp3-overlay-appear{
      -webkit-transform:translateY(-100%);
              transform:translateY(-100%); }
    .bp3-drawer.bp3-position-top.bp3-overlay-enter-active, .bp3-drawer.bp3-position-top.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer.bp3-position-top.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer.bp3-position-top.bp3-overlay-exit-active{
      -webkit-transform:translateY(-100%);
              transform:translateY(-100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer.bp3-position-bottom{
    right:0;
    bottom:0;
    left:0;
    height:50%; }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-enter, .bp3-drawer.bp3-position-bottom.bp3-overlay-appear{
      -webkit-transform:translateY(100%);
              transform:translateY(100%); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-enter-active, .bp3-drawer.bp3-position-bottom.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer.bp3-position-bottom.bp3-overlay-exit-active{
      -webkit-transform:translateY(100%);
              transform:translateY(100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer.bp3-position-left{
    top:0;
    bottom:0;
    left:0;
    width:50%; }
    .bp3-drawer.bp3-position-left.bp3-overlay-enter, .bp3-drawer.bp3-position-left.bp3-overlay-appear{
      -webkit-transform:translateX(-100%);
              transform:translateX(-100%); }
    .bp3-drawer.bp3-position-left.bp3-overlay-enter-active, .bp3-drawer.bp3-position-left.bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer.bp3-position-left.bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer.bp3-position-left.bp3-overlay-exit-active{
      -webkit-transform:translateX(-100%);
              transform:translateX(-100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer.bp3-position-right{
    top:0;
    right:0;
    bottom:0;
    width:50%; }
    .bp3-drawer.bp3-position-right.bp3-overlay-enter, .bp3-drawer.bp3-position-right.bp3-overlay-appear{
      -webkit-transform:translateX(100%);
              transform:translateX(100%); }
    .bp3-drawer.bp3-position-right.bp3-overlay-enter-active, .bp3-drawer.bp3-position-right.bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer.bp3-position-right.bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer.bp3-position-right.bp3-overlay-exit-active{
      -webkit-transform:translateX(100%);
              transform:translateX(100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
  .bp3-position-right):not(.bp3-vertical){
    top:0;
    right:0;
    bottom:0;
    width:50%; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-enter, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-appear{
      -webkit-transform:translateX(100%);
              transform:translateX(100%); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-enter-active, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-appear-active{
      -webkit-transform:translateX(0);
              transform:translateX(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-exit{
      -webkit-transform:translateX(0);
              transform:translateX(0); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right):not(.bp3-vertical).bp3-overlay-exit-active{
      -webkit-transform:translateX(100%);
              transform:translateX(100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
  .bp3-position-right).bp3-vertical{
    right:0;
    bottom:0;
    left:0;
    height:50%; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-enter, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-appear{
      -webkit-transform:translateY(100%);
              transform:translateY(100%); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-enter-active, .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-appear-active{
      -webkit-transform:translateY(0);
              transform:translateY(0);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:200ms;
              transition-duration:200ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-exit{
      -webkit-transform:translateY(0);
              transform:translateY(0); }
    .bp3-drawer:not(.bp3-position-top):not(.bp3-position-bottom):not(.bp3-position-left):not(
    .bp3-position-right).bp3-vertical.bp3-overlay-exit-active{
      -webkit-transform:translateY(100%);
              transform:translateY(100%);
      -webkit-transition-property:-webkit-transform;
      transition-property:-webkit-transform;
      transition-property:transform;
      transition-property:transform, -webkit-transform;
      -webkit-transition-duration:100ms;
              transition-duration:100ms;
      -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
              transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
      -webkit-transition-delay:0;
              transition-delay:0; }
  .bp3-drawer.bp3-dark,
  .bp3-dark .bp3-drawer{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    background:#30404d;
    color:#f5f8fa; }

.bp3-drawer-header{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  position:relative;
  border-radius:0;
  -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:0 1px 0 rgba(16, 22, 26, 0.15);
  min-height:40px;
  padding:5px;
  padding-left:20px; }
  .bp3-drawer-header .bp3-icon-large,
  .bp3-drawer-header .bp3-icon{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    margin-right:10px;
    color:#5c7080; }
  .bp3-drawer-header .bp3-heading{
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    margin:0;
    line-height:inherit; }
    .bp3-drawer-header .bp3-heading:last-child{
      margin-right:20px; }
  .bp3-dark .bp3-drawer-header{
    -webkit-box-shadow:0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:0 1px 0 rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-drawer-header .bp3-icon-large,
    .bp3-dark .bp3-drawer-header .bp3-icon{
      color:#a7b6c2; }

.bp3-drawer-body{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  overflow:auto;
  line-height:18px; }

.bp3-drawer-footer{
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  position:relative;
  -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
  padding:10px 20px; }
  .bp3-dark .bp3-drawer-footer{
    -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.4); }
.bp3-editable-text{
  display:inline-block;
  position:relative;
  cursor:text;
  max-width:100%;
  vertical-align:top;
  white-space:nowrap; }
  .bp3-editable-text::before{
    position:absolute;
    top:-3px;
    right:-3px;
    bottom:-3px;
    left:-3px;
    border-radius:3px;
    content:"";
    -webkit-transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9), box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-editable-text:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-editable-text.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
    background-color:#ffffff; }
  .bp3-editable-text.bp3-disabled::before{
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-editable-text.bp3-intent-primary .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-primary .bp3-editable-text-content{
    color:#137cbd; }
  .bp3-editable-text.bp3-intent-primary:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(19, 124, 189, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(19, 124, 189, 0.4); }
  .bp3-editable-text.bp3-intent-primary.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-success .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-success .bp3-editable-text-content{
    color:#0f9960; }
  .bp3-editable-text.bp3-intent-success:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px rgba(15, 153, 96, 0.4);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px rgba(15, 153, 96, 0.4); }
  .bp3-editable-text.bp3-intent-success.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-warning .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-warning .bp3-editable-text-content{
    color:#d9822b; }
  .bp3-editable-text.bp3-intent-warning:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px rgba(217, 130, 43, 0.4);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px rgba(217, 130, 43, 0.4); }
  .bp3-editable-text.bp3-intent-warning.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-editable-text.bp3-intent-danger .bp3-editable-text-input,
  .bp3-editable-text.bp3-intent-danger .bp3-editable-text-content{
    color:#db3737; }
  .bp3-editable-text.bp3-intent-danger:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px rgba(219, 55, 55, 0.4);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px rgba(219, 55, 55, 0.4); }
  .bp3-editable-text.bp3-intent-danger.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-editable-text:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(255, 255, 255, 0.15); }
  .bp3-dark .bp3-editable-text.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background-color:rgba(16, 22, 26, 0.3); }
  .bp3-dark .bp3-editable-text.bp3-disabled::before{
    -webkit-box-shadow:none;
            box-shadow:none; }
  .bp3-dark .bp3-editable-text.bp3-intent-primary .bp3-editable-text-content{
    color:#48aff0; }
  .bp3-dark .bp3-editable-text.bp3-intent-primary:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(72, 175, 240, 0), 0 0 0 0 rgba(72, 175, 240, 0), inset 0 0 0 1px rgba(72, 175, 240, 0.4);
            box-shadow:0 0 0 0 rgba(72, 175, 240, 0), 0 0 0 0 rgba(72, 175, 240, 0), inset 0 0 0 1px rgba(72, 175, 240, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-primary.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #48aff0, 0 0 0 3px rgba(72, 175, 240, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #48aff0, 0 0 0 3px rgba(72, 175, 240, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-success .bp3-editable-text-content{
    color:#3dcc91; }
  .bp3-dark .bp3-editable-text.bp3-intent-success:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(61, 204, 145, 0), 0 0 0 0 rgba(61, 204, 145, 0), inset 0 0 0 1px rgba(61, 204, 145, 0.4);
            box-shadow:0 0 0 0 rgba(61, 204, 145, 0), 0 0 0 0 rgba(61, 204, 145, 0), inset 0 0 0 1px rgba(61, 204, 145, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-success.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #3dcc91, 0 0 0 3px rgba(61, 204, 145, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #3dcc91, 0 0 0 3px rgba(61, 204, 145, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-warning .bp3-editable-text-content{
    color:#ffb366; }
  .bp3-dark .bp3-editable-text.bp3-intent-warning:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(255, 179, 102, 0), 0 0 0 0 rgba(255, 179, 102, 0), inset 0 0 0 1px rgba(255, 179, 102, 0.4);
            box-shadow:0 0 0 0 rgba(255, 179, 102, 0), 0 0 0 0 rgba(255, 179, 102, 0), inset 0 0 0 1px rgba(255, 179, 102, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-warning.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #ffb366, 0 0 0 3px rgba(255, 179, 102, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #ffb366, 0 0 0 3px rgba(255, 179, 102, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-danger .bp3-editable-text-content{
    color:#ff7373; }
  .bp3-dark .bp3-editable-text.bp3-intent-danger:hover::before{
    -webkit-box-shadow:0 0 0 0 rgba(255, 115, 115, 0), 0 0 0 0 rgba(255, 115, 115, 0), inset 0 0 0 1px rgba(255, 115, 115, 0.4);
            box-shadow:0 0 0 0 rgba(255, 115, 115, 0), 0 0 0 0 rgba(255, 115, 115, 0), inset 0 0 0 1px rgba(255, 115, 115, 0.4); }
  .bp3-dark .bp3-editable-text.bp3-intent-danger.bp3-editable-text-editing::before{
    -webkit-box-shadow:0 0 0 1px #ff7373, 0 0 0 3px rgba(255, 115, 115, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #ff7373, 0 0 0 3px rgba(255, 115, 115, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-editable-text-input,
.bp3-editable-text-content{
  display:inherit;
  position:relative;
  min-width:inherit;
  max-width:inherit;
  vertical-align:top;
  text-transform:inherit;
  letter-spacing:inherit;
  color:inherit;
  font:inherit;
  resize:none; }

.bp3-editable-text-input{
  border:none;
  -webkit-box-shadow:none;
          box-shadow:none;
  background:none;
  width:100%;
  padding:0;
  white-space:pre-wrap; }
  .bp3-editable-text-input::-webkit-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input::-moz-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input:-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input::-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input::placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-editable-text-input:focus{
    outline:none; }
  .bp3-editable-text-input::-ms-clear{
    display:none; }

.bp3-editable-text-content{
  overflow:hidden;
  padding-right:2px;
  text-overflow:ellipsis;
  white-space:pre; }
  .bp3-editable-text-editing > .bp3-editable-text-content{
    position:absolute;
    left:0;
    visibility:hidden; }
  .bp3-editable-text-placeholder > .bp3-editable-text-content{
    color:rgba(92, 112, 128, 0.6); }
    .bp3-dark .bp3-editable-text-placeholder > .bp3-editable-text-content{
      color:rgba(167, 182, 194, 0.6); }

.bp3-editable-text.bp3-multiline{
  display:block; }
  .bp3-editable-text.bp3-multiline .bp3-editable-text-content{
    overflow:auto;
    white-space:pre-wrap;
    word-wrap:break-word; }
.bp3-control-group{
  -webkit-transform:translateZ(0);
          transform:translateZ(0);
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:stretch;
      -ms-flex-align:stretch;
          align-items:stretch; }
  .bp3-control-group > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-control-group > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-control-group .bp3-button,
  .bp3-control-group .bp3-html-select,
  .bp3-control-group .bp3-input,
  .bp3-control-group .bp3-select{
    position:relative; }
  .bp3-control-group .bp3-input{
    z-index:2;
    border-radius:inherit; }
    .bp3-control-group .bp3-input:focus{
      z-index:14;
      border-radius:3px; }
    .bp3-control-group .bp3-input[class*="bp3-intent"]{
      z-index:13; }
      .bp3-control-group .bp3-input[class*="bp3-intent"]:focus{
        z-index:15; }
    .bp3-control-group .bp3-input[readonly], .bp3-control-group .bp3-input:disabled, .bp3-control-group .bp3-input.bp3-disabled{
      z-index:1; }
  .bp3-control-group .bp3-input-group[class*="bp3-intent"] .bp3-input{
    z-index:13; }
    .bp3-control-group .bp3-input-group[class*="bp3-intent"] .bp3-input:focus{
      z-index:15; }
  .bp3-control-group .bp3-button,
  .bp3-control-group .bp3-html-select select,
  .bp3-control-group .bp3-select select{
    -webkit-transform:translateZ(0);
            transform:translateZ(0);
    z-index:4;
    border-radius:inherit; }
    .bp3-control-group .bp3-button:focus,
    .bp3-control-group .bp3-html-select select:focus,
    .bp3-control-group .bp3-select select:focus{
      z-index:5; }
    .bp3-control-group .bp3-button:hover,
    .bp3-control-group .bp3-html-select select:hover,
    .bp3-control-group .bp3-select select:hover{
      z-index:6; }
    .bp3-control-group .bp3-button:active,
    .bp3-control-group .bp3-html-select select:active,
    .bp3-control-group .bp3-select select:active{
      z-index:7; }
    .bp3-control-group .bp3-button[readonly], .bp3-control-group .bp3-button:disabled, .bp3-control-group .bp3-button.bp3-disabled,
    .bp3-control-group .bp3-html-select select[readonly],
    .bp3-control-group .bp3-html-select select:disabled,
    .bp3-control-group .bp3-html-select select.bp3-disabled,
    .bp3-control-group .bp3-select select[readonly],
    .bp3-control-group .bp3-select select:disabled,
    .bp3-control-group .bp3-select select.bp3-disabled{
      z-index:3; }
    .bp3-control-group .bp3-button[class*="bp3-intent"],
    .bp3-control-group .bp3-html-select select[class*="bp3-intent"],
    .bp3-control-group .bp3-select select[class*="bp3-intent"]{
      z-index:9; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:focus,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:focus,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:focus{
        z-index:10; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:hover,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:hover,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:hover{
        z-index:11; }
      .bp3-control-group .bp3-button[class*="bp3-intent"]:active,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:active,
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:active{
        z-index:12; }
      .bp3-control-group .bp3-button[class*="bp3-intent"][readonly], .bp3-control-group .bp3-button[class*="bp3-intent"]:disabled, .bp3-control-group .bp3-button[class*="bp3-intent"].bp3-disabled,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"][readonly],
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"]:disabled,
      .bp3-control-group .bp3-html-select select[class*="bp3-intent"].bp3-disabled,
      .bp3-control-group .bp3-select select[class*="bp3-intent"][readonly],
      .bp3-control-group .bp3-select select[class*="bp3-intent"]:disabled,
      .bp3-control-group .bp3-select select[class*="bp3-intent"].bp3-disabled{
        z-index:8; }
  .bp3-control-group .bp3-input-group > .bp3-icon,
  .bp3-control-group .bp3-input-group > .bp3-button,
  .bp3-control-group .bp3-input-group > .bp3-input-action{
    z-index:16; }
  .bp3-control-group .bp3-select::after,
  .bp3-control-group .bp3-html-select::after,
  .bp3-control-group .bp3-select > .bp3-icon,
  .bp3-control-group .bp3-html-select > .bp3-icon{
    z-index:17; }
  .bp3-control-group:not(.bp3-vertical) > *{
    margin-right:-1px; }
  .bp3-dark .bp3-control-group:not(.bp3-vertical) > *{
    margin-right:0; }
  .bp3-dark .bp3-control-group:not(.bp3-vertical) > .bp3-button + .bp3-button{
    margin-left:1px; }
  .bp3-control-group .bp3-popover-wrapper,
  .bp3-control-group .bp3-popover-target{
    border-radius:inherit; }
  .bp3-control-group > :first-child{
    border-radius:3px 0 0 3px; }
  .bp3-control-group > :last-child{
    margin-right:0;
    border-radius:0 3px 3px 0; }
  .bp3-control-group > :only-child{
    margin-right:0;
    border-radius:3px; }
  .bp3-control-group .bp3-input-group .bp3-button{
    border-radius:3px; }
  .bp3-control-group > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-control-group.bp3-fill > *:not(.bp3-fixed){
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto; }
  .bp3-control-group.bp3-vertical{
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column; }
    .bp3-control-group.bp3-vertical > *{
      margin-top:-1px; }
    .bp3-control-group.bp3-vertical > :first-child{
      margin-top:0;
      border-radius:3px 3px 0 0; }
    .bp3-control-group.bp3-vertical > :last-child{
      border-radius:0 0 3px 3px; }
.bp3-control{
  display:block;
  position:relative;
  margin-bottom:10px;
  cursor:pointer;
  text-transform:none; }
  .bp3-control input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
  .bp3-control:hover input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#106ba3; }
  .bp3-control input:not(:disabled):active:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background:#0e5a8a; }
  .bp3-control input:disabled:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(19, 124, 189, 0.5); }
  .bp3-dark .bp3-control input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control:hover input:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#106ba3; }
  .bp3-dark .bp3-control input:not(:disabled):active:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#0e5a8a; }
  .bp3-dark .bp3-control input:disabled:checked ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(14, 90, 138, 0.5); }
  .bp3-control:not(.bp3-align-right){
    padding-left:26px; }
    .bp3-control:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-26px; }
  .bp3-control.bp3-align-right{
    padding-right:26px; }
    .bp3-control.bp3-align-right .bp3-control-indicator{
      margin-right:-26px; }
  .bp3-control.bp3-disabled{
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-control.bp3-inline{
    display:inline-block;
    margin-right:20px; }
  .bp3-control input{
    position:absolute;
    top:0;
    left:0;
    opacity:0;
    z-index:-1; }
  .bp3-control .bp3-control-indicator{
    display:inline-block;
    position:relative;
    margin-top:-3px;
    margin-right:10px;
    border:none;
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    cursor:pointer;
    width:1em;
    height:1em;
    vertical-align:middle;
    font-size:16px;
    -webkit-user-select:none;
       -moz-user-select:none;
        -ms-user-select:none;
            user-select:none; }
    .bp3-control .bp3-control-indicator::before{
      display:block;
      width:1em;
      height:1em;
      content:""; }
  .bp3-control:hover .bp3-control-indicator{
    background-color:#ebf1f5; }
  .bp3-control input:not(:disabled):active ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background:#d8e1e8; }
  .bp3-control input:disabled ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(206, 217, 224, 0.5);
    cursor:not-allowed; }
  .bp3-control input:focus ~ .bp3-control-indicator{
    outline:rgba(19, 124, 189, 0.6) auto 2px;
    outline-offset:2px;
    -moz-outline-radius:6px; }
  .bp3-control.bp3-align-right .bp3-control-indicator{
    float:right;
    margin-top:1px;
    margin-left:10px; }
  .bp3-control.bp3-large{
    font-size:16px; }
    .bp3-control.bp3-large:not(.bp3-align-right){
      padding-left:30px; }
      .bp3-control.bp3-large:not(.bp3-align-right) .bp3-control-indicator{
        margin-left:-30px; }
    .bp3-control.bp3-large.bp3-align-right{
      padding-right:30px; }
      .bp3-control.bp3-large.bp3-align-right .bp3-control-indicator{
        margin-right:-30px; }
    .bp3-control.bp3-large .bp3-control-indicator{
      font-size:20px; }
    .bp3-control.bp3-large.bp3-align-right .bp3-control-indicator{
      margin-top:0; }
  .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#137cbd;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.1)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.1), rgba(255, 255, 255, 0));
    color:#ffffff; }
  .bp3-control.bp3-checkbox:hover input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 -1px 0 rgba(16, 22, 26, 0.2);
    background-color:#106ba3; }
  .bp3-control.bp3-checkbox input:not(:disabled):active:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background:#0e5a8a; }
  .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(19, 124, 189, 0.5); }
  .bp3-dark .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-checkbox:hover input:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#106ba3; }
  .bp3-dark .bp3-control.bp3-checkbox input:not(:disabled):active:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#0e5a8a; }
  .bp3-dark .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(14, 90, 138, 0.5); }
  .bp3-control.bp3-checkbox .bp3-control-indicator{
    border-radius:3px; }
  .bp3-control.bp3-checkbox input:checked ~ .bp3-control-indicator::before{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M12 5c-.28 0-.53.11-.71.29L7 9.59l-2.29-2.3a1.003 1.003 0 0 0-1.42 1.42l3 3c.18.18.43.29.71.29s.53-.11.71-.29l5-5A1.003 1.003 0 0 0 12 5z' fill='white'/%3e%3c/svg%3e"); }
  .bp3-control.bp3-checkbox input:indeterminate ~ .bp3-control-indicator::before{
    background-image:url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 16 16'%3e%3cpath fill-rule='evenodd' clip-rule='evenodd' d='M11 7H5c-.55 0-1 .45-1 1s.45 1 1 1h6c.55 0 1-.45 1-1s-.45-1-1-1z' fill='white'/%3e%3c/svg%3e"); }
  .bp3-control.bp3-radio .bp3-control-indicator{
    border-radius:50%; }
  .bp3-control.bp3-radio input:checked ~ .bp3-control-indicator::before{
    background-image:radial-gradient(#ffffff, #ffffff 28%, transparent 32%); }
  .bp3-control.bp3-radio input:checked:disabled ~ .bp3-control-indicator::before{
    opacity:0.5; }
  .bp3-control.bp3-radio input:focus ~ .bp3-control-indicator{
    -moz-outline-radius:16px; }
  .bp3-control.bp3-switch input ~ .bp3-control-indicator{
    background:rgba(167, 182, 194, 0.5); }
  .bp3-control.bp3-switch:hover input ~ .bp3-control-indicator{
    background:rgba(115, 134, 148, 0.5); }
  .bp3-control.bp3-switch input:not(:disabled):active ~ .bp3-control-indicator{
    background:rgba(92, 112, 128, 0.5); }
  .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator{
    background:rgba(206, 217, 224, 0.5); }
    .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator::before{
      background:rgba(255, 255, 255, 0.8); }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator{
    background:#137cbd; }
  .bp3-control.bp3-switch:hover input:checked ~ .bp3-control-indicator{
    background:#106ba3; }
  .bp3-control.bp3-switch input:checked:not(:disabled):active ~ .bp3-control-indicator{
    background:#0e5a8a; }
  .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator{
    background:rgba(19, 124, 189, 0.5); }
    .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator::before{
      background:rgba(255, 255, 255, 0.8); }
  .bp3-control.bp3-switch:not(.bp3-align-right){
    padding-left:38px; }
    .bp3-control.bp3-switch:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-38px; }
  .bp3-control.bp3-switch.bp3-align-right{
    padding-right:38px; }
    .bp3-control.bp3-switch.bp3-align-right .bp3-control-indicator{
      margin-right:-38px; }
  .bp3-control.bp3-switch .bp3-control-indicator{
    border:none;
    border-radius:1.75em;
    -webkit-box-shadow:none !important;
            box-shadow:none !important;
    width:auto;
    min-width:1.75em;
    -webkit-transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:background-color 100ms cubic-bezier(0.4, 1, 0.75, 0.9); }
    .bp3-control.bp3-switch .bp3-control-indicator::before{
      position:absolute;
      left:0;
      margin:2px;
      border-radius:50%;
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
      background:#ffffff;
      width:calc(1em - 4px);
      height:calc(1em - 4px);
      -webkit-transition:left 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
      transition:left 100ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator::before{
    left:calc(100% - 1em); }
  .bp3-control.bp3-switch.bp3-large:not(.bp3-align-right){
    padding-left:45px; }
    .bp3-control.bp3-switch.bp3-large:not(.bp3-align-right) .bp3-control-indicator{
      margin-left:-45px; }
  .bp3-control.bp3-switch.bp3-large.bp3-align-right{
    padding-right:45px; }
    .bp3-control.bp3-switch.bp3-large.bp3-align-right .bp3-control-indicator{
      margin-right:-45px; }
  .bp3-dark .bp3-control.bp3-switch input ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.5); }
  .bp3-dark .bp3-control.bp3-switch:hover input ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.7); }
  .bp3-dark .bp3-control.bp3-switch input:not(:disabled):active ~ .bp3-control-indicator{
    background:rgba(16, 22, 26, 0.9); }
  .bp3-dark .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator{
    background:rgba(57, 75, 89, 0.5); }
    .bp3-dark .bp3-control.bp3-switch input:disabled ~ .bp3-control-indicator::before{
      background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator{
    background:#137cbd; }
  .bp3-dark .bp3-control.bp3-switch:hover input:checked ~ .bp3-control-indicator{
    background:#106ba3; }
  .bp3-dark .bp3-control.bp3-switch input:checked:not(:disabled):active ~ .bp3-control-indicator{
    background:#0e5a8a; }
  .bp3-dark .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator{
    background:rgba(14, 90, 138, 0.5); }
    .bp3-dark .bp3-control.bp3-switch input:checked:disabled ~ .bp3-control-indicator::before{
      background:rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-control.bp3-switch .bp3-control-indicator::before{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background:#394b59; }
  .bp3-dark .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator::before{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
  .bp3-control.bp3-switch .bp3-switch-inner-text{
    text-align:center;
    font-size:0.7em; }
  .bp3-control.bp3-switch .bp3-control-indicator-child:first-child{
    visibility:hidden;
    margin-right:1.2em;
    margin-left:0.5em;
    line-height:0; }
  .bp3-control.bp3-switch .bp3-control-indicator-child:last-child{
    visibility:visible;
    margin-right:0.5em;
    margin-left:1.2em;
    line-height:1em; }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator .bp3-control-indicator-child:first-child{
    visibility:visible;
    line-height:1em; }
  .bp3-control.bp3-switch input:checked ~ .bp3-control-indicator .bp3-control-indicator-child:last-child{
    visibility:hidden;
    line-height:0; }
  .bp3-dark .bp3-control{
    color:#f5f8fa; }
    .bp3-dark .bp3-control.bp3-disabled{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-control .bp3-control-indicator{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#394b59;
      background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
      background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0)); }
    .bp3-dark .bp3-control:hover .bp3-control-indicator{
      background-color:#30404d; }
    .bp3-dark .bp3-control input:not(:disabled):active ~ .bp3-control-indicator{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background:#202b33; }
    .bp3-dark .bp3-control input:disabled ~ .bp3-control-indicator{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(57, 75, 89, 0.5);
      cursor:not-allowed; }
    .bp3-dark .bp3-control.bp3-checkbox input:disabled:checked ~ .bp3-control-indicator, .bp3-dark .bp3-control.bp3-checkbox input:disabled:indeterminate ~ .bp3-control-indicator{
      color:rgba(167, 182, 194, 0.6); }
.bp3-file-input{
  display:inline-block;
  position:relative;
  cursor:pointer;
  height:30px; }
  .bp3-file-input input{
    opacity:0;
    margin:0;
    min-width:200px; }
    .bp3-file-input input:disabled + .bp3-file-upload-input,
    .bp3-file-input input.bp3-disabled + .bp3-file-upload-input{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(206, 217, 224, 0.5);
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6);
      resize:none; }
      .bp3-file-input input:disabled + .bp3-file-upload-input::after,
      .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after{
        outline:none;
        -webkit-box-shadow:none;
                box-shadow:none;
        background-color:rgba(206, 217, 224, 0.5);
        background-image:none;
        cursor:not-allowed;
        color:rgba(92, 112, 128, 0.6); }
        .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active, .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active:hover,
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active,
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active:hover{
          background:rgba(206, 217, 224, 0.7); }
      .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input, .bp3-dark
      .bp3-file-input input.bp3-disabled + .bp3-file-upload-input{
        -webkit-box-shadow:none;
                box-shadow:none;
        background:rgba(57, 75, 89, 0.5);
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input::after, .bp3-dark
        .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after{
          -webkit-box-shadow:none;
                  box-shadow:none;
          background-color:rgba(57, 75, 89, 0.5);
          background-image:none;
          color:rgba(167, 182, 194, 0.6); }
          .bp3-dark .bp3-file-input input:disabled + .bp3-file-upload-input::after.bp3-active, .bp3-dark
          .bp3-file-input input.bp3-disabled + .bp3-file-upload-input::after.bp3-active{
            background:rgba(57, 75, 89, 0.7); }
  .bp3-file-input.bp3-file-input-has-selection .bp3-file-upload-input{
    color:#182026; }
  .bp3-dark .bp3-file-input.bp3-file-input-has-selection .bp3-file-upload-input{
    color:#f5f8fa; }
  .bp3-file-input.bp3-fill{
    width:100%; }
  .bp3-file-input.bp3-large,
  .bp3-large .bp3-file-input{
    height:40px; }
  .bp3-file-input .bp3-file-upload-input-custom-text::after{
    content:attr(bp3-button-text); }

.bp3-file-upload-input{
  outline:none;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
  background:#ffffff;
  height:30px;
  padding:0 10px;
  vertical-align:middle;
  line-height:30px;
  color:#182026;
  font-size:14px;
  font-weight:400;
  -webkit-transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  -webkit-appearance:none;
     -moz-appearance:none;
          appearance:none;
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  position:absolute;
  top:0;
  right:0;
  left:0;
  padding-right:80px;
  color:rgba(92, 112, 128, 0.6);
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-file-upload-input::-webkit-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input::-moz-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input:-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input::-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input::placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-file-upload-input:focus, .bp3-file-upload-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-file-upload-input[type="search"], .bp3-file-upload-input.bp3-round{
    border-radius:30px;
    -webkit-box-sizing:border-box;
            box-sizing:border-box;
    padding-left:10px; }
  .bp3-file-upload-input[readonly]{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-file-upload-input:disabled, .bp3-file-upload-input.bp3-disabled{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(206, 217, 224, 0.5);
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6);
    resize:none; }
  .bp3-file-upload-input::after{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-color:#f5f8fa;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
    color:#182026;
    min-width:24px;
    min-height:24px;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    position:absolute;
    top:0;
    right:0;
    margin:3px;
    border-radius:3px;
    width:70px;
    text-align:center;
    line-height:24px;
    content:"Browse"; }
    .bp3-file-upload-input::after:hover{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
      background-clip:padding-box;
      background-color:#ebf1f5; }
    .bp3-file-upload-input::after:active, .bp3-file-upload-input::after.bp3-active{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#d8e1e8;
      background-image:none; }
    .bp3-file-upload-input::after:disabled, .bp3-file-upload-input::after.bp3-disabled{
      outline:none;
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(206, 217, 224, 0.5);
      background-image:none;
      cursor:not-allowed;
      color:rgba(92, 112, 128, 0.6); }
      .bp3-file-upload-input::after:disabled.bp3-active, .bp3-file-upload-input::after:disabled.bp3-active:hover, .bp3-file-upload-input::after.bp3-disabled.bp3-active, .bp3-file-upload-input::after.bp3-disabled.bp3-active:hover{
        background:rgba(206, 217, 224, 0.7); }
  .bp3-file-upload-input:hover::after{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#ebf1f5; }
  .bp3-file-upload-input:active::after{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#d8e1e8;
    background-image:none; }
  .bp3-large .bp3-file-upload-input{
    height:40px;
    line-height:40px;
    font-size:16px;
    padding-right:95px; }
    .bp3-large .bp3-file-upload-input[type="search"], .bp3-large .bp3-file-upload-input.bp3-round{
      padding:0 15px; }
    .bp3-large .bp3-file-upload-input::after{
      min-width:30px;
      min-height:30px;
      margin:5px;
      width:85px;
      line-height:30px; }
  .bp3-dark .bp3-file-upload-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#f5f8fa;
    color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-file-upload-input:disabled, .bp3-dark .bp3-file-upload-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(57, 75, 89, 0.5);
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-file-upload-input::after{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#394b59;
      background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
      background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
      color:#f5f8fa; }
      .bp3-dark .bp3-file-upload-input::after:hover, .bp3-dark .bp3-file-upload-input::after:active, .bp3-dark .bp3-file-upload-input::after.bp3-active{
        color:#f5f8fa; }
      .bp3-dark .bp3-file-upload-input::after:hover{
        -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
        background-color:#30404d; }
      .bp3-dark .bp3-file-upload-input::after:active, .bp3-dark .bp3-file-upload-input::after.bp3-active{
        -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
                box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
        background-color:#202b33;
        background-image:none; }
      .bp3-dark .bp3-file-upload-input::after:disabled, .bp3-dark .bp3-file-upload-input::after.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none;
        background-color:rgba(57, 75, 89, 0.5);
        background-image:none;
        color:rgba(167, 182, 194, 0.6); }
        .bp3-dark .bp3-file-upload-input::after:disabled.bp3-active, .bp3-dark .bp3-file-upload-input::after.bp3-disabled.bp3-active{
          background:rgba(57, 75, 89, 0.7); }
      .bp3-dark .bp3-file-upload-input::after .bp3-button-spinner .bp3-spinner-head{
        background:rgba(16, 22, 26, 0.5);
        stroke:#8a9ba8; }
    .bp3-dark .bp3-file-upload-input:hover::after{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#30404d; }
    .bp3-dark .bp3-file-upload-input:active::after{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#202b33;
      background-image:none; }

.bp3-file-upload-input::after{
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1); }
.bp3-form-group{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin:0 0 15px; }
  .bp3-form-group label.bp3-label{
    margin-bottom:5px; }
  .bp3-form-group .bp3-control{
    margin-top:7px; }
  .bp3-form-group .bp3-form-helper-text{
    margin-top:5px;
    color:#5c7080;
    font-size:12px; }
  .bp3-form-group.bp3-intent-primary .bp3-form-helper-text{
    color:#106ba3; }
  .bp3-form-group.bp3-intent-success .bp3-form-helper-text{
    color:#0d8050; }
  .bp3-form-group.bp3-intent-warning .bp3-form-helper-text{
    color:#bf7326; }
  .bp3-form-group.bp3-intent-danger .bp3-form-helper-text{
    color:#c23030; }
  .bp3-form-group.bp3-inline{
    -webkit-box-orient:horizontal;
    -webkit-box-direction:normal;
        -ms-flex-direction:row;
            flex-direction:row;
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start; }
    .bp3-form-group.bp3-inline.bp3-large label.bp3-label{
      margin:0 10px 0 0;
      line-height:40px; }
    .bp3-form-group.bp3-inline label.bp3-label{
      margin:0 10px 0 0;
      line-height:30px; }
  .bp3-form-group.bp3-disabled .bp3-label,
  .bp3-form-group.bp3-disabled .bp3-text-muted,
  .bp3-form-group.bp3-disabled .bp3-form-helper-text{
    color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-dark .bp3-form-group.bp3-intent-primary .bp3-form-helper-text{
    color:#48aff0; }
  .bp3-dark .bp3-form-group.bp3-intent-success .bp3-form-helper-text{
    color:#3dcc91; }
  .bp3-dark .bp3-form-group.bp3-intent-warning .bp3-form-helper-text{
    color:#ffb366; }
  .bp3-dark .bp3-form-group.bp3-intent-danger .bp3-form-helper-text{
    color:#ff7373; }
  .bp3-dark .bp3-form-group .bp3-form-helper-text{
    color:#a7b6c2; }
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-label,
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-text-muted,
  .bp3-dark .bp3-form-group.bp3-disabled .bp3-form-helper-text{
    color:rgba(167, 182, 194, 0.6) !important; }
.bp3-input-group{
  display:block;
  position:relative; }
  .bp3-input-group .bp3-input{
    position:relative;
    width:100%; }
    .bp3-input-group .bp3-input:not(:first-child){
      padding-left:30px; }
    .bp3-input-group .bp3-input:not(:last-child){
      padding-right:30px; }
  .bp3-input-group .bp3-input-action,
  .bp3-input-group > .bp3-button,
  .bp3-input-group > .bp3-icon{
    position:absolute;
    top:0; }
    .bp3-input-group .bp3-input-action:first-child,
    .bp3-input-group > .bp3-button:first-child,
    .bp3-input-group > .bp3-icon:first-child{
      left:0; }
    .bp3-input-group .bp3-input-action:last-child,
    .bp3-input-group > .bp3-button:last-child,
    .bp3-input-group > .bp3-icon:last-child{
      right:0; }
  .bp3-input-group .bp3-button{
    min-width:24px;
    min-height:24px;
    margin:3px;
    padding:0 7px; }
    .bp3-input-group .bp3-button:empty{
      padding:0; }
  .bp3-input-group > .bp3-icon{
    z-index:1;
    color:#5c7080; }
    .bp3-input-group > .bp3-icon:empty{
      line-height:1;
      font-family:"Icons16", sans-serif;
      font-size:16px;
      font-weight:400;
      font-style:normal;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased; }
  .bp3-input-group > .bp3-icon,
  .bp3-input-group .bp3-input-action > .bp3-spinner{
    margin:7px; }
  .bp3-input-group .bp3-tag{
    margin:5px; }
  .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus),
  .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus){
    color:#5c7080; }
    .bp3-dark .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus), .bp3-dark
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus){
      color:#a7b6c2; }
    .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-standard, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-large,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-standard,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:not(:hover):not(:focus) .bp3-icon-large{
      color:#5c7080; }
  .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled,
  .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled{
    color:rgba(92, 112, 128, 0.6) !important; }
    .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon-standard, .bp3-input-group .bp3-input:not(:focus) + .bp3-button.bp3-minimal:disabled .bp3-icon-large,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon-standard,
    .bp3-input-group .bp3-input:not(:focus) + .bp3-input-action .bp3-button.bp3-minimal:disabled .bp3-icon-large{
      color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-input-group.bp3-disabled{
    cursor:not-allowed; }
    .bp3-input-group.bp3-disabled .bp3-icon{
      color:rgba(92, 112, 128, 0.6); }
  .bp3-input-group.bp3-large .bp3-button{
    min-width:30px;
    min-height:30px;
    margin:5px; }
  .bp3-input-group.bp3-large > .bp3-icon,
  .bp3-input-group.bp3-large .bp3-input-action > .bp3-spinner{
    margin:12px; }
  .bp3-input-group.bp3-large .bp3-input{
    height:40px;
    line-height:40px;
    font-size:16px; }
    .bp3-input-group.bp3-large .bp3-input[type="search"], .bp3-input-group.bp3-large .bp3-input.bp3-round{
      padding:0 15px; }
    .bp3-input-group.bp3-large .bp3-input:not(:first-child){
      padding-left:40px; }
    .bp3-input-group.bp3-large .bp3-input:not(:last-child){
      padding-right:40px; }
  .bp3-input-group.bp3-small .bp3-button{
    min-width:20px;
    min-height:20px;
    margin:2px; }
  .bp3-input-group.bp3-small .bp3-tag{
    min-width:20px;
    min-height:20px;
    margin:2px; }
  .bp3-input-group.bp3-small > .bp3-icon,
  .bp3-input-group.bp3-small .bp3-input-action > .bp3-spinner{
    margin:4px; }
  .bp3-input-group.bp3-small .bp3-input{
    height:24px;
    padding-right:8px;
    padding-left:8px;
    line-height:24px;
    font-size:12px; }
    .bp3-input-group.bp3-small .bp3-input[type="search"], .bp3-input-group.bp3-small .bp3-input.bp3-round{
      padding:0 12px; }
    .bp3-input-group.bp3-small .bp3-input:not(:first-child){
      padding-left:24px; }
    .bp3-input-group.bp3-small .bp3-input:not(:last-child){
      padding-right:24px; }
  .bp3-input-group.bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:100%; }
  .bp3-input-group.bp3-round .bp3-button,
  .bp3-input-group.bp3-round .bp3-input,
  .bp3-input-group.bp3-round .bp3-tag{
    border-radius:30px; }
  .bp3-dark .bp3-input-group .bp3-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-input-group.bp3-disabled .bp3-icon{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-input-group.bp3-intent-primary .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-primary .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-primary .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #137cbd;
              box-shadow:inset 0 0 0 1px #137cbd; }
    .bp3-input-group.bp3-intent-primary .bp3-input:disabled, .bp3-input-group.bp3-intent-primary .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-primary > .bp3-icon{
    color:#106ba3; }
    .bp3-dark .bp3-input-group.bp3-intent-primary > .bp3-icon{
      color:#48aff0; }
  .bp3-input-group.bp3-intent-success .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-success .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-success .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #0f9960;
              box-shadow:inset 0 0 0 1px #0f9960; }
    .bp3-input-group.bp3-intent-success .bp3-input:disabled, .bp3-input-group.bp3-intent-success .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-success > .bp3-icon{
    color:#0d8050; }
    .bp3-dark .bp3-input-group.bp3-intent-success > .bp3-icon{
      color:#3dcc91; }
  .bp3-input-group.bp3-intent-warning .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-warning .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-warning .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #d9822b;
              box-shadow:inset 0 0 0 1px #d9822b; }
    .bp3-input-group.bp3-intent-warning .bp3-input:disabled, .bp3-input-group.bp3-intent-warning .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-warning > .bp3-icon{
    color:#bf7326; }
    .bp3-dark .bp3-input-group.bp3-intent-warning > .bp3-icon{
      color:#ffb366; }
  .bp3-input-group.bp3-intent-danger .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-danger .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input-group.bp3-intent-danger .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #db3737;
              box-shadow:inset 0 0 0 1px #db3737; }
    .bp3-input-group.bp3-intent-danger .bp3-input:disabled, .bp3-input-group.bp3-intent-danger .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-input-group.bp3-intent-danger > .bp3-icon{
    color:#c23030; }
    .bp3-dark .bp3-input-group.bp3-intent-danger > .bp3-icon{
      color:#ff7373; }
.bp3-input{
  outline:none;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
  background:#ffffff;
  height:30px;
  padding:0 10px;
  vertical-align:middle;
  line-height:30px;
  color:#182026;
  font-size:14px;
  font-weight:400;
  -webkit-transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-box-shadow 100ms cubic-bezier(0.4, 1, 0.75, 0.9);
  -webkit-appearance:none;
     -moz-appearance:none;
          appearance:none; }
  .bp3-input::-webkit-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input::-moz-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input:-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input::-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input::placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input:focus, .bp3-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-input[type="search"], .bp3-input.bp3-round{
    border-radius:30px;
    -webkit-box-sizing:border-box;
            box-sizing:border-box;
    padding-left:10px; }
  .bp3-input[readonly]{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.15); }
  .bp3-input:disabled, .bp3-input.bp3-disabled{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(206, 217, 224, 0.5);
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6);
    resize:none; }
  .bp3-input.bp3-large{
    height:40px;
    line-height:40px;
    font-size:16px; }
    .bp3-input.bp3-large[type="search"], .bp3-input.bp3-large.bp3-round{
      padding:0 15px; }
  .bp3-input.bp3-small{
    height:24px;
    padding-right:8px;
    padding-left:8px;
    line-height:24px;
    font-size:12px; }
    .bp3-input.bp3-small[type="search"], .bp3-input.bp3-small.bp3-round{
      padding:0 12px; }
  .bp3-input.bp3-fill{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:100%; }
  .bp3-dark .bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#f5f8fa; }
    .bp3-dark .bp3-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-input:disabled, .bp3-dark .bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(57, 75, 89, 0.5);
      color:rgba(167, 182, 194, 0.6); }
  .bp3-input.bp3-intent-primary{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-primary:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-primary[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #137cbd;
              box-shadow:inset 0 0 0 1px #137cbd; }
    .bp3-input.bp3-intent-primary:disabled, .bp3-input.bp3-intent-primary.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px #137cbd, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-primary:focus{
        -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-primary[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #137cbd;
                box-shadow:inset 0 0 0 1px #137cbd; }
      .bp3-dark .bp3-input.bp3-intent-primary:disabled, .bp3-dark .bp3-input.bp3-intent-primary.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-success{
    -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-success:focus{
      -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-success[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #0f9960;
              box-shadow:inset 0 0 0 1px #0f9960; }
    .bp3-input.bp3-intent-success:disabled, .bp3-input.bp3-intent-success.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-success{
      -webkit-box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), 0 0 0 0 rgba(15, 153, 96, 0), inset 0 0 0 1px #0f9960, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-success:focus{
        -webkit-box-shadow:0 0 0 1px #0f9960, 0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #0f9960, 0 0 0 1px #0f9960, 0 0 0 3px rgba(15, 153, 96, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-success[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #0f9960;
                box-shadow:inset 0 0 0 1px #0f9960; }
      .bp3-dark .bp3-input.bp3-intent-success:disabled, .bp3-dark .bp3-input.bp3-intent-success.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-warning{
    -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-warning:focus{
      -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-warning[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #d9822b;
              box-shadow:inset 0 0 0 1px #d9822b; }
    .bp3-input.bp3-intent-warning:disabled, .bp3-input.bp3-intent-warning.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), 0 0 0 0 rgba(217, 130, 43, 0), inset 0 0 0 1px #d9822b, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-warning:focus{
        -webkit-box-shadow:0 0 0 1px #d9822b, 0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #d9822b, 0 0 0 1px #d9822b, 0 0 0 3px rgba(217, 130, 43, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-warning[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #d9822b;
                box-shadow:inset 0 0 0 1px #d9822b; }
      .bp3-dark .bp3-input.bp3-intent-warning:disabled, .bp3-dark .bp3-input.bp3-intent-warning.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input.bp3-intent-danger{
    -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.15), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-danger:focus{
      -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-input.bp3-intent-danger[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px #db3737;
              box-shadow:inset 0 0 0 1px #db3737; }
    .bp3-input.bp3-intent-danger:disabled, .bp3-input.bp3-intent-danger.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none; }
    .bp3-dark .bp3-input.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), 0 0 0 0 rgba(219, 55, 55, 0), inset 0 0 0 1px #db3737, inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-danger:focus{
        -webkit-box-shadow:0 0 0 1px #db3737, 0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
                box-shadow:0 0 0 1px #db3737, 0 0 0 1px #db3737, 0 0 0 3px rgba(219, 55, 55, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
      .bp3-dark .bp3-input.bp3-intent-danger[readonly]{
        -webkit-box-shadow:inset 0 0 0 1px #db3737;
                box-shadow:inset 0 0 0 1px #db3737; }
      .bp3-dark .bp3-input.bp3-intent-danger:disabled, .bp3-dark .bp3-input.bp3-intent-danger.bp3-disabled{
        -webkit-box-shadow:none;
                box-shadow:none; }
  .bp3-input::-ms-clear{
    display:none; }
textarea.bp3-input{
  max-width:100%;
  padding:10px; }
  textarea.bp3-input, textarea.bp3-input.bp3-large, textarea.bp3-input.bp3-small{
    height:auto;
    line-height:inherit; }
  textarea.bp3-input.bp3-small{
    padding:8px; }
  .bp3-dark textarea.bp3-input{
    -webkit-box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), 0 0 0 0 rgba(19, 124, 189, 0), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background:rgba(16, 22, 26, 0.3);
    color:#f5f8fa; }
    .bp3-dark textarea.bp3-input::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input::placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark textarea.bp3-input:focus{
      -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark textarea.bp3-input[readonly]{
      -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark textarea.bp3-input:disabled, .bp3-dark textarea.bp3-input.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:rgba(57, 75, 89, 0.5);
      color:rgba(167, 182, 194, 0.6); }
label.bp3-label{
  display:block;
  margin-top:0;
  margin-bottom:15px; }
  label.bp3-label .bp3-html-select,
  label.bp3-label .bp3-input,
  label.bp3-label .bp3-select,
  label.bp3-label .bp3-slider,
  label.bp3-label .bp3-popover-wrapper{
    display:block;
    margin-top:5px;
    text-transform:none; }
  label.bp3-label .bp3-button-group{
    margin-top:5px; }
  label.bp3-label .bp3-select select,
  label.bp3-label .bp3-html-select select{
    width:100%;
    vertical-align:top;
    font-weight:400; }
  label.bp3-label.bp3-disabled,
  label.bp3-label.bp3-disabled .bp3-text-muted{
    color:rgba(92, 112, 128, 0.6); }
  label.bp3-label.bp3-inline{
    line-height:30px; }
    label.bp3-label.bp3-inline .bp3-html-select,
    label.bp3-label.bp3-inline .bp3-input,
    label.bp3-label.bp3-inline .bp3-input-group,
    label.bp3-label.bp3-inline .bp3-select,
    label.bp3-label.bp3-inline .bp3-popover-wrapper{
      display:inline-block;
      margin:0 0 0 5px;
      vertical-align:top; }
    label.bp3-label.bp3-inline .bp3-button-group{
      margin:0 0 0 5px; }
    label.bp3-label.bp3-inline .bp3-input-group .bp3-input{
      margin-left:0; }
    label.bp3-label.bp3-inline.bp3-large{
      line-height:40px; }
  label.bp3-label:not(.bp3-inline) .bp3-popover-target{
    display:block; }
  .bp3-dark label.bp3-label{
    color:#f5f8fa; }
    .bp3-dark label.bp3-label.bp3-disabled,
    .bp3-dark label.bp3-label.bp3-disabled .bp3-text-muted{
      color:rgba(167, 182, 194, 0.6); }
.bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button{
  -webkit-box-flex:1;
      -ms-flex:1 1 14px;
          flex:1 1 14px;
  width:30px;
  min-height:0;
  padding:0; }
  .bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button:first-child{
    border-radius:0 3px 0 0; }
  .bp3-numeric-input .bp3-button-group.bp3-vertical > .bp3-button:last-child{
    border-radius:0 0 3px 0; }

.bp3-numeric-input .bp3-button-group.bp3-vertical:first-child > .bp3-button:first-child{
  border-radius:3px 0 0 0; }

.bp3-numeric-input .bp3-button-group.bp3-vertical:first-child > .bp3-button:last-child{
  border-radius:0 0 0 3px; }

.bp3-numeric-input.bp3-large .bp3-button-group.bp3-vertical > .bp3-button{
  width:40px; }

form{
  display:block; }
.bp3-html-select select,
.bp3-select select{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  border:none;
  border-radius:3px;
  cursor:pointer;
  padding:5px 10px;
  vertical-align:middle;
  text-align:left;
  font-size:14px;
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
  background-color:#f5f8fa;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
  color:#182026;
  border-radius:3px;
  width:100%;
  height:30px;
  padding:0 25px 0 10px;
  -moz-appearance:none;
  -webkit-appearance:none; }
  .bp3-html-select select > *, .bp3-select select > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-html-select select > .bp3-fill, .bp3-select select > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-html-select select::before,
  .bp3-select select::before, .bp3-html-select select > *, .bp3-select select > *{
    margin-right:7px; }
  .bp3-html-select select:empty::before,
  .bp3-select select:empty::before,
  .bp3-html-select select > :last-child,
  .bp3-select select > :last-child{
    margin-right:0; }
  .bp3-html-select select:hover,
  .bp3-select select:hover{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#ebf1f5; }
  .bp3-html-select select:active,
  .bp3-select select:active, .bp3-html-select select.bp3-active,
  .bp3-select select.bp3-active{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#d8e1e8;
    background-image:none; }
  .bp3-html-select select:disabled,
  .bp3-select select:disabled, .bp3-html-select select.bp3-disabled,
  .bp3-select select.bp3-disabled{
    outline:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    background-color:rgba(206, 217, 224, 0.5);
    background-image:none;
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
    .bp3-html-select select:disabled.bp3-active,
    .bp3-select select:disabled.bp3-active, .bp3-html-select select:disabled.bp3-active:hover,
    .bp3-select select:disabled.bp3-active:hover, .bp3-html-select select.bp3-disabled.bp3-active,
    .bp3-select select.bp3-disabled.bp3-active, .bp3-html-select select.bp3-disabled.bp3-active:hover,
    .bp3-select select.bp3-disabled.bp3-active:hover{
      background:rgba(206, 217, 224, 0.7); }

.bp3-html-select.bp3-minimal select,
.bp3-select.bp3-minimal select{
  -webkit-box-shadow:none;
          box-shadow:none;
  background:none; }
  .bp3-html-select.bp3-minimal select:hover,
  .bp3-select.bp3-minimal select:hover{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(167, 182, 194, 0.3);
    text-decoration:none;
    color:#182026; }
  .bp3-html-select.bp3-minimal select:active,
  .bp3-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal select.bp3-active,
  .bp3-select.bp3-minimal select.bp3-active{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:rgba(115, 134, 148, 0.3);
    color:#182026; }
  .bp3-html-select.bp3-minimal select:disabled,
  .bp3-select.bp3-minimal select:disabled, .bp3-html-select.bp3-minimal select:disabled:hover,
  .bp3-select.bp3-minimal select:disabled:hover, .bp3-html-select.bp3-minimal select.bp3-disabled,
  .bp3-select.bp3-minimal select.bp3-disabled, .bp3-html-select.bp3-minimal select.bp3-disabled:hover,
  .bp3-select.bp3-minimal select.bp3-disabled:hover{
    background:none;
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
    .bp3-html-select.bp3-minimal select:disabled.bp3-active,
    .bp3-select.bp3-minimal select:disabled.bp3-active, .bp3-html-select.bp3-minimal select:disabled:hover.bp3-active,
    .bp3-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-html-select.bp3-minimal select.bp3-disabled.bp3-active,
    .bp3-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-disabled:hover.bp3-active,
    .bp3-select.bp3-minimal select.bp3-disabled:hover.bp3-active{
      background:rgba(115, 134, 148, 0.3); }
  .bp3-dark .bp3-html-select.bp3-minimal select, .bp3-html-select.bp3-minimal .bp3-dark select,
  .bp3-dark .bp3-select.bp3-minimal select, .bp3-select.bp3-minimal .bp3-dark select{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:none;
    color:inherit; }
    .bp3-dark .bp3-html-select.bp3-minimal select:hover, .bp3-html-select.bp3-minimal .bp3-dark select:hover,
    .bp3-dark .bp3-select.bp3-minimal select:hover, .bp3-select.bp3-minimal .bp3-dark select:hover, .bp3-dark .bp3-html-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal .bp3-dark select:active,
    .bp3-dark .bp3-select.bp3-minimal select:active, .bp3-select.bp3-minimal .bp3-dark select:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-active,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none; }
    .bp3-dark .bp3-html-select.bp3-minimal select:hover, .bp3-html-select.bp3-minimal .bp3-dark select:hover,
    .bp3-dark .bp3-select.bp3-minimal select:hover, .bp3-select.bp3-minimal .bp3-dark select:hover{
      background:rgba(138, 155, 168, 0.15); }
    .bp3-dark .bp3-html-select.bp3-minimal select:active, .bp3-html-select.bp3-minimal .bp3-dark select:active,
    .bp3-dark .bp3-select.bp3-minimal select:active, .bp3-select.bp3-minimal .bp3-dark select:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-active,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-active{
      background:rgba(138, 155, 168, 0.3);
      color:#f5f8fa; }
    .bp3-dark .bp3-html-select.bp3-minimal select:disabled, .bp3-html-select.bp3-minimal .bp3-dark select:disabled,
    .bp3-dark .bp3-select.bp3-minimal select:disabled, .bp3-select.bp3-minimal .bp3-dark select:disabled, .bp3-dark .bp3-html-select.bp3-minimal select:disabled:hover, .bp3-html-select.bp3-minimal .bp3-dark select:disabled:hover,
    .bp3-dark .bp3-select.bp3-minimal select:disabled:hover, .bp3-select.bp3-minimal .bp3-dark select:disabled:hover, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled:hover,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled:hover{
      background:none;
      cursor:not-allowed;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-html-select.bp3-minimal select:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select:disabled.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select:disabled:hover.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select:disabled:hover.bp3-active, .bp3-select.bp3-minimal .bp3-dark select:disabled:hover.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-disabled:hover.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-disabled:hover.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-disabled:hover.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-disabled:hover.bp3-active{
        background:rgba(138, 155, 168, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-primary,
  .bp3-select.bp3-minimal select.bp3-intent-primary{
    color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover,
    .bp3-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-html-select.bp3-minimal select.bp3-intent-primary:active,
    .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover,
    .bp3-select.bp3-minimal select.bp3-intent-primary:hover{
      background:rgba(19, 124, 189, 0.15);
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:active,
    .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active{
      background:rgba(19, 124, 189, 0.3);
      color:#106ba3; }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled{
      background:none;
      color:rgba(16, 107, 163, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active{
        background:rgba(19, 124, 189, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-primary .bp3-button-spinner .bp3-spinner-head{
      stroke:#106ba3; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary{
      color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:hover{
        background:rgba(19, 124, 189, 0.2);
        color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-active{
        background:rgba(19, 124, 189, 0.3);
        color:#48aff0; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled{
        background:none;
        color:rgba(72, 175, 240, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-primary.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-primary.bp3-disabled.bp3-active{
          background:rgba(19, 124, 189, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-success,
  .bp3-select.bp3-minimal select.bp3-intent-success{
    color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:hover,
    .bp3-select.bp3-minimal select.bp3-intent-success:hover, .bp3-html-select.bp3-minimal select.bp3-intent-success:active,
    .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:hover,
    .bp3-select.bp3-minimal select.bp3-intent-success:hover{
      background:rgba(15, 153, 96, 0.15);
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:active,
    .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active{
      background:rgba(15, 153, 96, 0.3);
      color:#0d8050; }
    .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled{
      background:none;
      color:rgba(13, 128, 80, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active{
        background:rgba(15, 153, 96, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-success .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-success .bp3-button-spinner .bp3-spinner-head{
      stroke:#0d8050; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success{
      color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:hover{
        background:rgba(15, 153, 96, 0.2);
        color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-active{
        background:rgba(15, 153, 96, 0.3);
        color:#3dcc91; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled{
        background:none;
        color:rgba(61, 204, 145, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-success.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-success.bp3-disabled.bp3-active{
          background:rgba(15, 153, 96, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-warning,
  .bp3-select.bp3-minimal select.bp3-intent-warning{
    color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover,
    .bp3-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-html-select.bp3-minimal select.bp3-intent-warning:active,
    .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover,
    .bp3-select.bp3-minimal select.bp3-intent-warning:hover{
      background:rgba(217, 130, 43, 0.15);
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:active,
    .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active{
      background:rgba(217, 130, 43, 0.3);
      color:#bf7326; }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled{
      background:none;
      color:rgba(191, 115, 38, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active{
        background:rgba(217, 130, 43, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-warning .bp3-button-spinner .bp3-spinner-head{
      stroke:#bf7326; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning{
      color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:hover{
        background:rgba(217, 130, 43, 0.2);
        color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-active{
        background:rgba(217, 130, 43, 0.3);
        color:#ffb366; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled{
        background:none;
        color:rgba(255, 179, 102, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-warning.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-warning.bp3-disabled.bp3-active{
          background:rgba(217, 130, 43, 0.3); }
  .bp3-html-select.bp3-minimal select.bp3-intent-danger,
  .bp3-select.bp3-minimal select.bp3-intent-danger{
    color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover,
    .bp3-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-html-select.bp3-minimal select.bp3-intent-danger:active,
    .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active{
      -webkit-box-shadow:none;
              box-shadow:none;
      background:none;
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover,
    .bp3-select.bp3-minimal select.bp3-intent-danger:hover{
      background:rgba(219, 55, 55, 0.15);
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:active,
    .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active{
      background:rgba(219, 55, 55, 0.3);
      color:#c23030; }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled,
    .bp3-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled,
    .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled{
      background:none;
      color:rgba(194, 48, 48, 0.5); }
      .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active,
      .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active{
        background:rgba(219, 55, 55, 0.3); }
    .bp3-html-select.bp3-minimal select.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head, .bp3-select.bp3-minimal select.bp3-intent-danger .bp3-button-spinner .bp3-spinner-head{
      stroke:#c23030; }
    .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger,
    .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger{
      color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:hover,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:hover, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:hover{
        background:rgba(219, 55, 55, 0.2);
        color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-active,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-active{
        background:rgba(219, 55, 55, 0.3);
        color:#ff7373; }
      .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled,
      .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled{
        background:none;
        color:rgba(255, 115, 115, 0.5); }
        .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger:disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger:disabled.bp3-active, .bp3-dark .bp3-html-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active, .bp3-html-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled.bp3-active,
        .bp3-dark .bp3-select.bp3-minimal select.bp3-intent-danger.bp3-disabled.bp3-active, .bp3-select.bp3-minimal .bp3-dark select.bp3-intent-danger.bp3-disabled.bp3-active{
          background:rgba(219, 55, 55, 0.3); }

.bp3-html-select.bp3-large select,
.bp3-select.bp3-large select{
  height:40px;
  padding-right:35px;
  font-size:16px; }

.bp3-dark .bp3-html-select select, .bp3-dark .bp3-select select{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
  background-color:#394b59;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
  color:#f5f8fa; }
  .bp3-dark .bp3-html-select select:hover, .bp3-dark .bp3-select select:hover, .bp3-dark .bp3-html-select select:active, .bp3-dark .bp3-select select:active, .bp3-dark .bp3-html-select select.bp3-active, .bp3-dark .bp3-select select.bp3-active{
    color:#f5f8fa; }
  .bp3-dark .bp3-html-select select:hover, .bp3-dark .bp3-select select:hover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#30404d; }
  .bp3-dark .bp3-html-select select:active, .bp3-dark .bp3-select select:active, .bp3-dark .bp3-html-select select.bp3-active, .bp3-dark .bp3-select select.bp3-active{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#202b33;
    background-image:none; }
  .bp3-dark .bp3-html-select select:disabled, .bp3-dark .bp3-select select:disabled, .bp3-dark .bp3-html-select select.bp3-disabled, .bp3-dark .bp3-select select.bp3-disabled{
    -webkit-box-shadow:none;
            box-shadow:none;
    background-color:rgba(57, 75, 89, 0.5);
    background-image:none;
    color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-html-select select:disabled.bp3-active, .bp3-dark .bp3-select select:disabled.bp3-active, .bp3-dark .bp3-html-select select.bp3-disabled.bp3-active, .bp3-dark .bp3-select select.bp3-disabled.bp3-active{
      background:rgba(57, 75, 89, 0.7); }
  .bp3-dark .bp3-html-select select .bp3-button-spinner .bp3-spinner-head, .bp3-dark .bp3-select select .bp3-button-spinner .bp3-spinner-head{
    background:rgba(16, 22, 26, 0.5);
    stroke:#8a9ba8; }

.bp3-html-select select:disabled,
.bp3-select select:disabled{
  -webkit-box-shadow:none;
          box-shadow:none;
  background-color:rgba(206, 217, 224, 0.5);
  cursor:not-allowed;
  color:rgba(92, 112, 128, 0.6); }

.bp3-html-select .bp3-icon,
.bp3-select .bp3-icon, .bp3-select::after{
  position:absolute;
  top:7px;
  right:7px;
  color:#5c7080;
  pointer-events:none; }
  .bp3-html-select .bp3-disabled.bp3-icon,
  .bp3-select .bp3-disabled.bp3-icon, .bp3-disabled.bp3-select::after{
    color:rgba(92, 112, 128, 0.6); }
.bp3-html-select,
.bp3-select{
  display:inline-block;
  position:relative;
  vertical-align:middle;
  letter-spacing:normal; }
  .bp3-html-select select::-ms-expand,
  .bp3-select select::-ms-expand{
    display:none; }
  .bp3-html-select .bp3-icon,
  .bp3-select .bp3-icon{
    color:#5c7080; }
    .bp3-html-select .bp3-icon:hover,
    .bp3-select .bp3-icon:hover{
      color:#182026; }
    .bp3-dark .bp3-html-select .bp3-icon, .bp3-dark
    .bp3-select .bp3-icon{
      color:#a7b6c2; }
      .bp3-dark .bp3-html-select .bp3-icon:hover, .bp3-dark
      .bp3-select .bp3-icon:hover{
        color:#f5f8fa; }
  .bp3-html-select.bp3-large::after,
  .bp3-html-select.bp3-large .bp3-icon,
  .bp3-select.bp3-large::after,
  .bp3-select.bp3-large .bp3-icon{
    top:12px;
    right:12px; }
  .bp3-html-select.bp3-fill,
  .bp3-html-select.bp3-fill select,
  .bp3-select.bp3-fill,
  .bp3-select.bp3-fill select{
    width:100%; }
  .bp3-dark .bp3-html-select option, .bp3-dark
  .bp3-select option{
    background-color:#30404d;
    color:#f5f8fa; }
  .bp3-dark .bp3-html-select::after, .bp3-dark
  .bp3-select::after{
    color:#a7b6c2; }

.bp3-select::after{
  line-height:1;
  font-family:"Icons16", sans-serif;
  font-size:16px;
  font-weight:400;
  font-style:normal;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  content:""; }
.bp3-running-text table, table.bp3-html-table{
  border-spacing:0;
  font-size:14px; }
  .bp3-running-text table th, table.bp3-html-table th,
  .bp3-running-text table td,
  table.bp3-html-table td{
    padding:11px;
    vertical-align:top;
    text-align:left; }
  .bp3-running-text table th, table.bp3-html-table th{
    color:#182026;
    font-weight:600; }
  
  .bp3-running-text table td,
  table.bp3-html-table td{
    color:#182026; }
  .bp3-running-text table tbody tr:first-child th, table.bp3-html-table tbody tr:first-child th,
  .bp3-running-text table tbody tr:first-child td,
  table.bp3-html-table tbody tr:first-child td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-running-text table th, .bp3-running-text .bp3-dark table th, .bp3-dark table.bp3-html-table th{
    color:#f5f8fa; }
  .bp3-dark .bp3-running-text table td, .bp3-running-text .bp3-dark table td, .bp3-dark table.bp3-html-table td{
    color:#f5f8fa; }
  .bp3-dark .bp3-running-text table tbody tr:first-child th, .bp3-running-text .bp3-dark table tbody tr:first-child th, .bp3-dark table.bp3-html-table tbody tr:first-child th,
  .bp3-dark .bp3-running-text table tbody tr:first-child td,
  .bp3-running-text .bp3-dark table tbody tr:first-child td,
  .bp3-dark table.bp3-html-table tbody tr:first-child td{
    -webkit-box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15); }

table.bp3-html-table.bp3-html-table-condensed th,
table.bp3-html-table.bp3-html-table-condensed td, table.bp3-html-table.bp3-small th,
table.bp3-html-table.bp3-small td{
  padding-top:6px;
  padding-bottom:6px; }

table.bp3-html-table.bp3-html-table-striped tbody tr:nth-child(odd) td{
  background:rgba(191, 204, 214, 0.15); }

table.bp3-html-table.bp3-html-table-bordered th:not(:first-child){
  -webkit-box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-html-table-bordered tbody tr td{
  -webkit-box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15);
          box-shadow:inset 0 1px 0 0 rgba(16, 22, 26, 0.15); }
  table.bp3-html-table.bp3-html-table-bordered tbody tr td:not(:first-child){
    -webkit-box-shadow:inset 1px 1px 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 1px 1px 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td{
  -webkit-box-shadow:none;
          box-shadow:none; }
  table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td:not(:first-child){
    -webkit-box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 1px 0 0 0 rgba(16, 22, 26, 0.15); }

table.bp3-html-table.bp3-interactive tbody tr:hover td{
  background-color:rgba(191, 204, 214, 0.3);
  cursor:pointer; }

table.bp3-html-table.bp3-interactive tbody tr:active td{
  background-color:rgba(191, 204, 214, 0.4); }

.bp3-dark table.bp3-html-table.bp3-html-table-striped tbody tr:nth-child(odd) td{
  background:rgba(92, 112, 128, 0.15); }

.bp3-dark table.bp3-html-table.bp3-html-table-bordered th:not(:first-child){
  -webkit-box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15);
          box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15); }

.bp3-dark table.bp3-html-table.bp3-html-table-bordered tbody tr td{
  -webkit-box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15);
          box-shadow:inset 0 1px 0 0 rgba(255, 255, 255, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered tbody tr td:not(:first-child){
    -webkit-box-shadow:inset 1px 1px 0 0 rgba(255, 255, 255, 0.15);
            box-shadow:inset 1px 1px 0 0 rgba(255, 255, 255, 0.15); }

.bp3-dark table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td{
  -webkit-box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15);
          box-shadow:inset 1px 0 0 0 rgba(255, 255, 255, 0.15); }
  .bp3-dark table.bp3-html-table.bp3-html-table-bordered.bp3-html-table-striped tbody tr:not(:first-child) td:first-child{
    -webkit-box-shadow:none;
            box-shadow:none; }

.bp3-dark table.bp3-html-table.bp3-interactive tbody tr:hover td{
  background-color:rgba(92, 112, 128, 0.3);
  cursor:pointer; }

.bp3-dark table.bp3-html-table.bp3-interactive tbody tr:active td{
  background-color:rgba(92, 112, 128, 0.4); }

.bp3-key-combo{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center; }
  .bp3-key-combo > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-key-combo > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-key-combo::before,
  .bp3-key-combo > *{
    margin-right:5px; }
  .bp3-key-combo:empty::before,
  .bp3-key-combo > :last-child{
    margin-right:0; }

.bp3-hotkey-dialog{
  top:40px;
  padding-bottom:0; }
  .bp3-hotkey-dialog .bp3-dialog-body{
    margin:0;
    padding:0; }
  .bp3-hotkey-dialog .bp3-hotkey-label{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1; }

.bp3-hotkey-column{
  margin:auto;
  max-height:80vh;
  overflow-y:auto;
  padding:30px; }
  .bp3-hotkey-column .bp3-heading{
    margin-bottom:20px; }
    .bp3-hotkey-column .bp3-heading:not(:first-child){
      margin-top:40px; }

.bp3-hotkey{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:justify;
      -ms-flex-pack:justify;
          justify-content:space-between;
  margin-right:0;
  margin-left:0; }
  .bp3-hotkey:not(:last-child){
    margin-bottom:10px; }
.bp3-icon{
  display:inline-block;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  vertical-align:text-bottom; }
  .bp3-icon:not(:empty)::before{
    content:"" !important;
    content:unset !important; }
  .bp3-icon > svg{
    display:block; }
    .bp3-icon > svg:not([fill]){
      fill:currentColor; }

.bp3-icon.bp3-intent-primary, .bp3-icon-standard.bp3-intent-primary, .bp3-icon-large.bp3-intent-primary{
  color:#106ba3; }
  .bp3-dark .bp3-icon.bp3-intent-primary, .bp3-dark .bp3-icon-standard.bp3-intent-primary, .bp3-dark .bp3-icon-large.bp3-intent-primary{
    color:#48aff0; }

.bp3-icon.bp3-intent-success, .bp3-icon-standard.bp3-intent-success, .bp3-icon-large.bp3-intent-success{
  color:#0d8050; }
  .bp3-dark .bp3-icon.bp3-intent-success, .bp3-dark .bp3-icon-standard.bp3-intent-success, .bp3-dark .bp3-icon-large.bp3-intent-success{
    color:#3dcc91; }

.bp3-icon.bp3-intent-warning, .bp3-icon-standard.bp3-intent-warning, .bp3-icon-large.bp3-intent-warning{
  color:#bf7326; }
  .bp3-dark .bp3-icon.bp3-intent-warning, .bp3-dark .bp3-icon-standard.bp3-intent-warning, .bp3-dark .bp3-icon-large.bp3-intent-warning{
    color:#ffb366; }

.bp3-icon.bp3-intent-danger, .bp3-icon-standard.bp3-intent-danger, .bp3-icon-large.bp3-intent-danger{
  color:#c23030; }
  .bp3-dark .bp3-icon.bp3-intent-danger, .bp3-dark .bp3-icon-standard.bp3-intent-danger, .bp3-dark .bp3-icon-large.bp3-intent-danger{
    color:#ff7373; }

span.bp3-icon-standard{
  line-height:1;
  font-family:"Icons16", sans-serif;
  font-size:16px;
  font-weight:400;
  font-style:normal;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  display:inline-block; }

span.bp3-icon-large{
  line-height:1;
  font-family:"Icons20", sans-serif;
  font-size:20px;
  font-weight:400;
  font-style:normal;
  -moz-osx-font-smoothing:grayscale;
  -webkit-font-smoothing:antialiased;
  display:inline-block; }

span.bp3-icon:empty{
  line-height:1;
  font-family:"Icons20";
  font-size:inherit;
  font-weight:400;
  font-style:normal; }
  span.bp3-icon:empty::before{
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased; }

.bp3-icon-add::before{
  content:""; }

.bp3-icon-add-column-left::before{
  content:""; }

.bp3-icon-add-column-right::before{
  content:""; }

.bp3-icon-add-row-bottom::before{
  content:""; }

.bp3-icon-add-row-top::before{
  content:""; }

.bp3-icon-add-to-artifact::before{
  content:""; }

.bp3-icon-add-to-folder::before{
  content:""; }

.bp3-icon-airplane::before{
  content:""; }

.bp3-icon-align-center::before{
  content:""; }

.bp3-icon-align-justify::before{
  content:""; }

.bp3-icon-align-left::before{
  content:""; }

.bp3-icon-align-right::before{
  content:""; }

.bp3-icon-alignment-bottom::before{
  content:""; }

.bp3-icon-alignment-horizontal-center::before{
  content:""; }

.bp3-icon-alignment-left::before{
  content:""; }

.bp3-icon-alignment-right::before{
  content:""; }

.bp3-icon-alignment-top::before{
  content:""; }

.bp3-icon-alignment-vertical-center::before{
  content:""; }

.bp3-icon-annotation::before{
  content:""; }

.bp3-icon-application::before{
  content:""; }

.bp3-icon-applications::before{
  content:""; }

.bp3-icon-archive::before{
  content:""; }

.bp3-icon-arrow-bottom-left::before{
  content:"↙"; }

.bp3-icon-arrow-bottom-right::before{
  content:"↘"; }

.bp3-icon-arrow-down::before{
  content:"↓"; }

.bp3-icon-arrow-left::before{
  content:"←"; }

.bp3-icon-arrow-right::before{
  content:"→"; }

.bp3-icon-arrow-top-left::before{
  content:"↖"; }

.bp3-icon-arrow-top-right::before{
  content:"↗"; }

.bp3-icon-arrow-up::before{
  content:"↑"; }

.bp3-icon-arrows-horizontal::before{
  content:"↔"; }

.bp3-icon-arrows-vertical::before{
  content:"↕"; }

.bp3-icon-asterisk::before{
  content:"*"; }

.bp3-icon-automatic-updates::before{
  content:""; }

.bp3-icon-badge::before{
  content:""; }

.bp3-icon-ban-circle::before{
  content:""; }

.bp3-icon-bank-account::before{
  content:""; }

.bp3-icon-barcode::before{
  content:""; }

.bp3-icon-blank::before{
  content:""; }

.bp3-icon-blocked-person::before{
  content:""; }

.bp3-icon-bold::before{
  content:""; }

.bp3-icon-book::before{
  content:""; }

.bp3-icon-bookmark::before{
  content:""; }

.bp3-icon-box::before{
  content:""; }

.bp3-icon-briefcase::before{
  content:""; }

.bp3-icon-bring-data::before{
  content:""; }

.bp3-icon-build::before{
  content:""; }

.bp3-icon-calculator::before{
  content:""; }

.bp3-icon-calendar::before{
  content:""; }

.bp3-icon-camera::before{
  content:""; }

.bp3-icon-caret-down::before{
  content:"⌄"; }

.bp3-icon-caret-left::before{
  content:"〈"; }

.bp3-icon-caret-right::before{
  content:"〉"; }

.bp3-icon-caret-up::before{
  content:"⌃"; }

.bp3-icon-cell-tower::before{
  content:""; }

.bp3-icon-changes::before{
  content:""; }

.bp3-icon-chart::before{
  content:""; }

.bp3-icon-chat::before{
  content:""; }

.bp3-icon-chevron-backward::before{
  content:""; }

.bp3-icon-chevron-down::before{
  content:""; }

.bp3-icon-chevron-forward::before{
  content:""; }

.bp3-icon-chevron-left::before{
  content:""; }

.bp3-icon-chevron-right::before{
  content:""; }

.bp3-icon-chevron-up::before{
  content:""; }

.bp3-icon-circle::before{
  content:""; }

.bp3-icon-circle-arrow-down::before{
  content:""; }

.bp3-icon-circle-arrow-left::before{
  content:""; }

.bp3-icon-circle-arrow-right::before{
  content:""; }

.bp3-icon-circle-arrow-up::before{
  content:""; }

.bp3-icon-citation::before{
  content:""; }

.bp3-icon-clean::before{
  content:""; }

.bp3-icon-clipboard::before{
  content:""; }

.bp3-icon-cloud::before{
  content:"☁"; }

.bp3-icon-cloud-download::before{
  content:""; }

.bp3-icon-cloud-upload::before{
  content:""; }

.bp3-icon-code::before{
  content:""; }

.bp3-icon-code-block::before{
  content:""; }

.bp3-icon-cog::before{
  content:""; }

.bp3-icon-collapse-all::before{
  content:""; }

.bp3-icon-column-layout::before{
  content:""; }

.bp3-icon-comment::before{
  content:""; }

.bp3-icon-comparison::before{
  content:""; }

.bp3-icon-compass::before{
  content:""; }

.bp3-icon-compressed::before{
  content:""; }

.bp3-icon-confirm::before{
  content:""; }

.bp3-icon-console::before{
  content:""; }

.bp3-icon-contrast::before{
  content:""; }

.bp3-icon-control::before{
  content:""; }

.bp3-icon-credit-card::before{
  content:""; }

.bp3-icon-cross::before{
  content:"✗"; }

.bp3-icon-crown::before{
  content:""; }

.bp3-icon-cube::before{
  content:""; }

.bp3-icon-cube-add::before{
  content:""; }

.bp3-icon-cube-remove::before{
  content:""; }

.bp3-icon-curved-range-chart::before{
  content:""; }

.bp3-icon-cut::before{
  content:""; }

.bp3-icon-dashboard::before{
  content:""; }

.bp3-icon-data-lineage::before{
  content:""; }

.bp3-icon-database::before{
  content:""; }

.bp3-icon-delete::before{
  content:""; }

.bp3-icon-delta::before{
  content:"Δ"; }

.bp3-icon-derive-column::before{
  content:""; }

.bp3-icon-desktop::before{
  content:""; }

.bp3-icon-diagram-tree::before{
  content:""; }

.bp3-icon-direction-left::before{
  content:""; }

.bp3-icon-direction-right::before{
  content:""; }

.bp3-icon-disable::before{
  content:""; }

.bp3-icon-document::before{
  content:""; }

.bp3-icon-document-open::before{
  content:""; }

.bp3-icon-document-share::before{
  content:""; }

.bp3-icon-dollar::before{
  content:"$"; }

.bp3-icon-dot::before{
  content:"•"; }

.bp3-icon-double-caret-horizontal::before{
  content:""; }

.bp3-icon-double-caret-vertical::before{
  content:""; }

.bp3-icon-double-chevron-down::before{
  content:""; }

.bp3-icon-double-chevron-left::before{
  content:""; }

.bp3-icon-double-chevron-right::before{
  content:""; }

.bp3-icon-double-chevron-up::before{
  content:""; }

.bp3-icon-doughnut-chart::before{
  content:""; }

.bp3-icon-download::before{
  content:""; }

.bp3-icon-drag-handle-horizontal::before{
  content:""; }

.bp3-icon-drag-handle-vertical::before{
  content:""; }

.bp3-icon-draw::before{
  content:""; }

.bp3-icon-drive-time::before{
  content:""; }

.bp3-icon-duplicate::before{
  content:""; }

.bp3-icon-edit::before{
  content:"✎"; }

.bp3-icon-eject::before{
  content:"⏏"; }

.bp3-icon-endorsed::before{
  content:""; }

.bp3-icon-envelope::before{
  content:"✉"; }

.bp3-icon-equals::before{
  content:""; }

.bp3-icon-eraser::before{
  content:""; }

.bp3-icon-error::before{
  content:""; }

.bp3-icon-euro::before{
  content:"€"; }

.bp3-icon-exchange::before{
  content:""; }

.bp3-icon-exclude-row::before{
  content:""; }

.bp3-icon-expand-all::before{
  content:""; }

.bp3-icon-export::before{
  content:""; }

.bp3-icon-eye-off::before{
  content:""; }

.bp3-icon-eye-on::before{
  content:""; }

.bp3-icon-eye-open::before{
  content:""; }

.bp3-icon-fast-backward::before{
  content:""; }

.bp3-icon-fast-forward::before{
  content:""; }

.bp3-icon-feed::before{
  content:""; }

.bp3-icon-feed-subscribed::before{
  content:""; }

.bp3-icon-film::before{
  content:""; }

.bp3-icon-filter::before{
  content:""; }

.bp3-icon-filter-keep::before{
  content:""; }

.bp3-icon-filter-list::before{
  content:""; }

.bp3-icon-filter-open::before{
  content:""; }

.bp3-icon-filter-remove::before{
  content:""; }

.bp3-icon-flag::before{
  content:"⚑"; }

.bp3-icon-flame::before{
  content:""; }

.bp3-icon-flash::before{
  content:""; }

.bp3-icon-floppy-disk::before{
  content:""; }

.bp3-icon-flow-branch::before{
  content:""; }

.bp3-icon-flow-end::before{
  content:""; }

.bp3-icon-flow-linear::before{
  content:""; }

.bp3-icon-flow-review::before{
  content:""; }

.bp3-icon-flow-review-branch::before{
  content:""; }

.bp3-icon-flows::before{
  content:""; }

.bp3-icon-folder-close::before{
  content:""; }

.bp3-icon-folder-new::before{
  content:""; }

.bp3-icon-folder-open::before{
  content:""; }

.bp3-icon-folder-shared::before{
  content:""; }

.bp3-icon-folder-shared-open::before{
  content:""; }

.bp3-icon-follower::before{
  content:""; }

.bp3-icon-following::before{
  content:""; }

.bp3-icon-font::before{
  content:""; }

.bp3-icon-fork::before{
  content:""; }

.bp3-icon-form::before{
  content:""; }

.bp3-icon-full-circle::before{
  content:""; }

.bp3-icon-full-stacked-chart::before{
  content:""; }

.bp3-icon-fullscreen::before{
  content:""; }

.bp3-icon-function::before{
  content:""; }

.bp3-icon-gantt-chart::before{
  content:""; }

.bp3-icon-geolocation::before{
  content:""; }

.bp3-icon-geosearch::before{
  content:""; }

.bp3-icon-git-branch::before{
  content:""; }

.bp3-icon-git-commit::before{
  content:""; }

.bp3-icon-git-merge::before{
  content:""; }

.bp3-icon-git-new-branch::before{
  content:""; }

.bp3-icon-git-pull::before{
  content:""; }

.bp3-icon-git-push::before{
  content:""; }

.bp3-icon-git-repo::before{
  content:""; }

.bp3-icon-glass::before{
  content:""; }

.bp3-icon-globe::before{
  content:""; }

.bp3-icon-globe-network::before{
  content:""; }

.bp3-icon-graph::before{
  content:""; }

.bp3-icon-graph-remove::before{
  content:""; }

.bp3-icon-greater-than::before{
  content:""; }

.bp3-icon-greater-than-or-equal-to::before{
  content:""; }

.bp3-icon-grid::before{
  content:""; }

.bp3-icon-grid-view::before{
  content:""; }

.bp3-icon-group-objects::before{
  content:""; }

.bp3-icon-grouped-bar-chart::before{
  content:""; }

.bp3-icon-hand::before{
  content:""; }

.bp3-icon-hand-down::before{
  content:""; }

.bp3-icon-hand-left::before{
  content:""; }

.bp3-icon-hand-right::before{
  content:""; }

.bp3-icon-hand-up::before{
  content:""; }

.bp3-icon-header::before{
  content:""; }

.bp3-icon-header-one::before{
  content:""; }

.bp3-icon-header-two::before{
  content:""; }

.bp3-icon-headset::before{
  content:""; }

.bp3-icon-heart::before{
  content:"♥"; }

.bp3-icon-heart-broken::before{
  content:""; }

.bp3-icon-heat-grid::before{
  content:""; }

.bp3-icon-heatmap::before{
  content:""; }

.bp3-icon-help::before{
  content:"?"; }

.bp3-icon-helper-management::before{
  content:""; }

.bp3-icon-highlight::before{
  content:""; }

.bp3-icon-history::before{
  content:""; }

.bp3-icon-home::before{
  content:"⌂"; }

.bp3-icon-horizontal-bar-chart::before{
  content:""; }

.bp3-icon-horizontal-bar-chart-asc::before{
  content:""; }

.bp3-icon-horizontal-bar-chart-desc::before{
  content:""; }

.bp3-icon-horizontal-distribution::before{
  content:""; }

.bp3-icon-id-number::before{
  content:""; }

.bp3-icon-image-rotate-left::before{
  content:""; }

.bp3-icon-image-rotate-right::before{
  content:""; }

.bp3-icon-import::before{
  content:""; }

.bp3-icon-inbox::before{
  content:""; }

.bp3-icon-inbox-filtered::before{
  content:""; }

.bp3-icon-inbox-geo::before{
  content:""; }

.bp3-icon-inbox-search::before{
  content:""; }

.bp3-icon-inbox-update::before{
  content:""; }

.bp3-icon-info-sign::before{
  content:"ℹ"; }

.bp3-icon-inheritance::before{
  content:""; }

.bp3-icon-inner-join::before{
  content:""; }

.bp3-icon-insert::before{
  content:""; }

.bp3-icon-intersection::before{
  content:""; }

.bp3-icon-ip-address::before{
  content:""; }

.bp3-icon-issue::before{
  content:""; }

.bp3-icon-issue-closed::before{
  content:""; }

.bp3-icon-issue-new::before{
  content:""; }

.bp3-icon-italic::before{
  content:""; }

.bp3-icon-join-table::before{
  content:""; }

.bp3-icon-key::before{
  content:""; }

.bp3-icon-key-backspace::before{
  content:""; }

.bp3-icon-key-command::before{
  content:""; }

.bp3-icon-key-control::before{
  content:""; }

.bp3-icon-key-delete::before{
  content:""; }

.bp3-icon-key-enter::before{
  content:""; }

.bp3-icon-key-escape::before{
  content:""; }

.bp3-icon-key-option::before{
  content:""; }

.bp3-icon-key-shift::before{
  content:""; }

.bp3-icon-key-tab::before{
  content:""; }

.bp3-icon-known-vehicle::before{
  content:""; }

.bp3-icon-label::before{
  content:""; }

.bp3-icon-layer::before{
  content:""; }

.bp3-icon-layers::before{
  content:""; }

.bp3-icon-layout::before{
  content:""; }

.bp3-icon-layout-auto::before{
  content:""; }

.bp3-icon-layout-balloon::before{
  content:""; }

.bp3-icon-layout-circle::before{
  content:""; }

.bp3-icon-layout-grid::before{
  content:""; }

.bp3-icon-layout-group-by::before{
  content:""; }

.bp3-icon-layout-hierarchy::before{
  content:""; }

.bp3-icon-layout-linear::before{
  content:""; }

.bp3-icon-layout-skew-grid::before{
  content:""; }

.bp3-icon-layout-sorted-clusters::before{
  content:""; }

.bp3-icon-learning::before{
  content:""; }

.bp3-icon-left-join::before{
  content:""; }

.bp3-icon-less-than::before{
  content:""; }

.bp3-icon-less-than-or-equal-to::before{
  content:""; }

.bp3-icon-lifesaver::before{
  content:""; }

.bp3-icon-lightbulb::before{
  content:""; }

.bp3-icon-link::before{
  content:""; }

.bp3-icon-list::before{
  content:"☰"; }

.bp3-icon-list-columns::before{
  content:""; }

.bp3-icon-list-detail-view::before{
  content:""; }

.bp3-icon-locate::before{
  content:""; }

.bp3-icon-lock::before{
  content:""; }

.bp3-icon-log-in::before{
  content:""; }

.bp3-icon-log-out::before{
  content:""; }

.bp3-icon-manual::before{
  content:""; }

.bp3-icon-manually-entered-data::before{
  content:""; }

.bp3-icon-map::before{
  content:""; }

.bp3-icon-map-create::before{
  content:""; }

.bp3-icon-map-marker::before{
  content:""; }

.bp3-icon-maximize::before{
  content:""; }

.bp3-icon-media::before{
  content:""; }

.bp3-icon-menu::before{
  content:""; }

.bp3-icon-menu-closed::before{
  content:""; }

.bp3-icon-menu-open::before{
  content:""; }

.bp3-icon-merge-columns::before{
  content:""; }

.bp3-icon-merge-links::before{
  content:""; }

.bp3-icon-minimize::before{
  content:""; }

.bp3-icon-minus::before{
  content:"−"; }

.bp3-icon-mobile-phone::before{
  content:""; }

.bp3-icon-mobile-video::before{
  content:""; }

.bp3-icon-moon::before{
  content:""; }

.bp3-icon-more::before{
  content:""; }

.bp3-icon-mountain::before{
  content:""; }

.bp3-icon-move::before{
  content:""; }

.bp3-icon-mugshot::before{
  content:""; }

.bp3-icon-multi-select::before{
  content:""; }

.bp3-icon-music::before{
  content:""; }

.bp3-icon-new-drawing::before{
  content:""; }

.bp3-icon-new-grid-item::before{
  content:""; }

.bp3-icon-new-layer::before{
  content:""; }

.bp3-icon-new-layers::before{
  content:""; }

.bp3-icon-new-link::before{
  content:""; }

.bp3-icon-new-object::before{
  content:""; }

.bp3-icon-new-person::before{
  content:""; }

.bp3-icon-new-prescription::before{
  content:""; }

.bp3-icon-new-text-box::before{
  content:""; }

.bp3-icon-ninja::before{
  content:""; }

.bp3-icon-not-equal-to::before{
  content:""; }

.bp3-icon-notifications::before{
  content:""; }

.bp3-icon-notifications-updated::before{
  content:""; }

.bp3-icon-numbered-list::before{
  content:""; }

.bp3-icon-numerical::before{
  content:""; }

.bp3-icon-office::before{
  content:""; }

.bp3-icon-offline::before{
  content:""; }

.bp3-icon-oil-field::before{
  content:""; }

.bp3-icon-one-column::before{
  content:""; }

.bp3-icon-outdated::before{
  content:""; }

.bp3-icon-page-layout::before{
  content:""; }

.bp3-icon-panel-stats::before{
  content:""; }

.bp3-icon-panel-table::before{
  content:""; }

.bp3-icon-paperclip::before{
  content:""; }

.bp3-icon-paragraph::before{
  content:""; }

.bp3-icon-path::before{
  content:""; }

.bp3-icon-path-search::before{
  content:""; }

.bp3-icon-pause::before{
  content:""; }

.bp3-icon-people::before{
  content:""; }

.bp3-icon-percentage::before{
  content:""; }

.bp3-icon-person::before{
  content:""; }

.bp3-icon-phone::before{
  content:"☎"; }

.bp3-icon-pie-chart::before{
  content:""; }

.bp3-icon-pin::before{
  content:""; }

.bp3-icon-pivot::before{
  content:""; }

.bp3-icon-pivot-table::before{
  content:""; }

.bp3-icon-play::before{
  content:""; }

.bp3-icon-plus::before{
  content:"+"; }

.bp3-icon-polygon-filter::before{
  content:""; }

.bp3-icon-power::before{
  content:""; }

.bp3-icon-predictive-analysis::before{
  content:""; }

.bp3-icon-prescription::before{
  content:""; }

.bp3-icon-presentation::before{
  content:""; }

.bp3-icon-print::before{
  content:"⎙"; }

.bp3-icon-projects::before{
  content:""; }

.bp3-icon-properties::before{
  content:""; }

.bp3-icon-property::before{
  content:""; }

.bp3-icon-publish-function::before{
  content:""; }

.bp3-icon-pulse::before{
  content:""; }

.bp3-icon-random::before{
  content:""; }

.bp3-icon-record::before{
  content:""; }

.bp3-icon-redo::before{
  content:""; }

.bp3-icon-refresh::before{
  content:""; }

.bp3-icon-regression-chart::before{
  content:""; }

.bp3-icon-remove::before{
  content:""; }

.bp3-icon-remove-column::before{
  content:""; }

.bp3-icon-remove-column-left::before{
  content:""; }

.bp3-icon-remove-column-right::before{
  content:""; }

.bp3-icon-remove-row-bottom::before{
  content:""; }

.bp3-icon-remove-row-top::before{
  content:""; }

.bp3-icon-repeat::before{
  content:""; }

.bp3-icon-reset::before{
  content:""; }

.bp3-icon-resolve::before{
  content:""; }

.bp3-icon-rig::before{
  content:""; }

.bp3-icon-right-join::before{
  content:""; }

.bp3-icon-ring::before{
  content:""; }

.bp3-icon-rotate-document::before{
  content:""; }

.bp3-icon-rotate-page::before{
  content:""; }

.bp3-icon-satellite::before{
  content:""; }

.bp3-icon-saved::before{
  content:""; }

.bp3-icon-scatter-plot::before{
  content:""; }

.bp3-icon-search::before{
  content:""; }

.bp3-icon-search-around::before{
  content:""; }

.bp3-icon-search-template::before{
  content:""; }

.bp3-icon-search-text::before{
  content:""; }

.bp3-icon-segmented-control::before{
  content:""; }

.bp3-icon-select::before{
  content:""; }

.bp3-icon-selection::before{
  content:"⦿"; }

.bp3-icon-send-to::before{
  content:""; }

.bp3-icon-send-to-graph::before{
  content:""; }

.bp3-icon-send-to-map::before{
  content:""; }

.bp3-icon-series-add::before{
  content:""; }

.bp3-icon-series-configuration::before{
  content:""; }

.bp3-icon-series-derived::before{
  content:""; }

.bp3-icon-series-filtered::before{
  content:""; }

.bp3-icon-series-search::before{
  content:""; }

.bp3-icon-settings::before{
  content:""; }

.bp3-icon-share::before{
  content:""; }

.bp3-icon-shield::before{
  content:""; }

.bp3-icon-shop::before{
  content:""; }

.bp3-icon-shopping-cart::before{
  content:""; }

.bp3-icon-signal-search::before{
  content:""; }

.bp3-icon-sim-card::before{
  content:""; }

.bp3-icon-slash::before{
  content:""; }

.bp3-icon-small-cross::before{
  content:""; }

.bp3-icon-small-minus::before{
  content:""; }

.bp3-icon-small-plus::before{
  content:""; }

.bp3-icon-small-tick::before{
  content:""; }

.bp3-icon-snowflake::before{
  content:""; }

.bp3-icon-social-media::before{
  content:""; }

.bp3-icon-sort::before{
  content:""; }

.bp3-icon-sort-alphabetical::before{
  content:""; }

.bp3-icon-sort-alphabetical-desc::before{
  content:""; }

.bp3-icon-sort-asc::before{
  content:""; }

.bp3-icon-sort-desc::before{
  content:""; }

.bp3-icon-sort-numerical::before{
  content:""; }

.bp3-icon-sort-numerical-desc::before{
  content:""; }

.bp3-icon-split-columns::before{
  content:""; }

.bp3-icon-square::before{
  content:""; }

.bp3-icon-stacked-chart::before{
  content:""; }

.bp3-icon-star::before{
  content:"★"; }

.bp3-icon-star-empty::before{
  content:"☆"; }

.bp3-icon-step-backward::before{
  content:""; }

.bp3-icon-step-chart::before{
  content:""; }

.bp3-icon-step-forward::before{
  content:""; }

.bp3-icon-stop::before{
  content:""; }

.bp3-icon-stopwatch::before{
  content:""; }

.bp3-icon-strikethrough::before{
  content:""; }

.bp3-icon-style::before{
  content:""; }

.bp3-icon-swap-horizontal::before{
  content:""; }

.bp3-icon-swap-vertical::before{
  content:""; }

.bp3-icon-symbol-circle::before{
  content:""; }

.bp3-icon-symbol-cross::before{
  content:""; }

.bp3-icon-symbol-diamond::before{
  content:""; }

.bp3-icon-symbol-square::before{
  content:""; }

.bp3-icon-symbol-triangle-down::before{
  content:""; }

.bp3-icon-symbol-triangle-up::before{
  content:""; }

.bp3-icon-tag::before{
  content:""; }

.bp3-icon-take-action::before{
  content:""; }

.bp3-icon-taxi::before{
  content:""; }

.bp3-icon-text-highlight::before{
  content:""; }

.bp3-icon-th::before{
  content:""; }

.bp3-icon-th-derived::before{
  content:""; }

.bp3-icon-th-disconnect::before{
  content:""; }

.bp3-icon-th-filtered::before{
  content:""; }

.bp3-icon-th-list::before{
  content:""; }

.bp3-icon-thumbs-down::before{
  content:""; }

.bp3-icon-thumbs-up::before{
  content:""; }

.bp3-icon-tick::before{
  content:"✓"; }

.bp3-icon-tick-circle::before{
  content:""; }

.bp3-icon-time::before{
  content:"⏲"; }

.bp3-icon-timeline-area-chart::before{
  content:""; }

.bp3-icon-timeline-bar-chart::before{
  content:""; }

.bp3-icon-timeline-events::before{
  content:""; }

.bp3-icon-timeline-line-chart::before{
  content:""; }

.bp3-icon-tint::before{
  content:""; }

.bp3-icon-torch::before{
  content:""; }

.bp3-icon-tractor::before{
  content:""; }

.bp3-icon-train::before{
  content:""; }

.bp3-icon-translate::before{
  content:""; }

.bp3-icon-trash::before{
  content:""; }

.bp3-icon-tree::before{
  content:""; }

.bp3-icon-trending-down::before{
  content:""; }

.bp3-icon-trending-up::before{
  content:""; }

.bp3-icon-truck::before{
  content:""; }

.bp3-icon-two-columns::before{
  content:""; }

.bp3-icon-unarchive::before{
  content:""; }

.bp3-icon-underline::before{
  content:"⎁"; }

.bp3-icon-undo::before{
  content:"⎌"; }

.bp3-icon-ungroup-objects::before{
  content:""; }

.bp3-icon-unknown-vehicle::before{
  content:""; }

.bp3-icon-unlock::before{
  content:""; }

.bp3-icon-unpin::before{
  content:""; }

.bp3-icon-unresolve::before{
  content:""; }

.bp3-icon-updated::before{
  content:""; }

.bp3-icon-upload::before{
  content:""; }

.bp3-icon-user::before{
  content:""; }

.bp3-icon-variable::before{
  content:""; }

.bp3-icon-vertical-bar-chart-asc::before{
  content:""; }

.bp3-icon-vertical-bar-chart-desc::before{
  content:""; }

.bp3-icon-vertical-distribution::before{
  content:""; }

.bp3-icon-video::before{
  content:""; }

.bp3-icon-volume-down::before{
  content:""; }

.bp3-icon-volume-off::before{
  content:""; }

.bp3-icon-volume-up::before{
  content:""; }

.bp3-icon-walk::before{
  content:""; }

.bp3-icon-warning-sign::before{
  content:""; }

.bp3-icon-waterfall-chart::before{
  content:""; }

.bp3-icon-widget::before{
  content:""; }

.bp3-icon-widget-button::before{
  content:""; }

.bp3-icon-widget-footer::before{
  content:""; }

.bp3-icon-widget-header::before{
  content:""; }

.bp3-icon-wrench::before{
  content:""; }

.bp3-icon-zoom-in::before{
  content:""; }

.bp3-icon-zoom-out::before{
  content:""; }

.bp3-icon-zoom-to-fit::before{
  content:""; }
.bp3-submenu > .bp3-popover-wrapper{
  display:block; }

.bp3-submenu .bp3-popover-target{
  display:block; }

.bp3-submenu.bp3-popover{
  -webkit-box-shadow:none;
          box-shadow:none;
  padding:0 5px; }
  .bp3-submenu.bp3-popover > .bp3-popover-content{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-submenu.bp3-popover, .bp3-submenu.bp3-popover.bp3-dark{
    -webkit-box-shadow:none;
            box-shadow:none; }
    .bp3-dark .bp3-submenu.bp3-popover > .bp3-popover-content, .bp3-submenu.bp3-popover.bp3-dark > .bp3-popover-content{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
.bp3-menu{
  margin:0;
  border-radius:3px;
  background:#ffffff;
  min-width:180px;
  padding:5px;
  list-style:none;
  text-align:left;
  color:#182026; }

.bp3-menu-divider{
  display:block;
  margin:5px;
  border-top:1px solid rgba(16, 22, 26, 0.15); }
  .bp3-dark .bp3-menu-divider{
    border-top-color:rgba(255, 255, 255, 0.15); }

.bp3-menu-item{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  border-radius:2px;
  padding:5px 7px;
  text-decoration:none;
  line-height:20px;
  color:inherit;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-menu-item > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-menu-item > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-menu-item::before,
  .bp3-menu-item > *{
    margin-right:7px; }
  .bp3-menu-item:empty::before,
  .bp3-menu-item > :last-child{
    margin-right:0; }
  .bp3-menu-item > .bp3-fill{
    word-break:break-word; }
  .bp3-menu-item:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
    background-color:rgba(167, 182, 194, 0.3);
    cursor:pointer;
    text-decoration:none; }
  .bp3-menu-item.bp3-disabled{
    background-color:inherit;
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-dark .bp3-menu-item{
    color:inherit; }
    .bp3-dark .bp3-menu-item:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
      background-color:rgba(138, 155, 168, 0.15);
      color:inherit; }
    .bp3-dark .bp3-menu-item.bp3-disabled{
      background-color:inherit;
      color:rgba(167, 182, 194, 0.6); }
  .bp3-menu-item.bp3-intent-primary{
    color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-primary::before, .bp3-menu-item.bp3-intent-primary::after,
    .bp3-menu-item.bp3-intent-primary .bp3-menu-item-label{
      color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-menu-item.bp3-intent-primary.bp3-active{
      background-color:#137cbd; }
    .bp3-menu-item.bp3-intent-primary:active{
      background-color:#106ba3; }
    .bp3-menu-item.bp3-intent-primary:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-menu-item.bp3-intent-primary:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-menu-item.bp3-intent-primary:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-primary:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-primary:active, .bp3-menu-item.bp3-intent-primary:active::before, .bp3-menu-item.bp3-intent-primary:active::after,
    .bp3-menu-item.bp3-intent-primary:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-primary.bp3-active, .bp3-menu-item.bp3-intent-primary.bp3-active::before, .bp3-menu-item.bp3-intent-primary.bp3-active::after,
    .bp3-menu-item.bp3-intent-primary.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-success{
    color:#0d8050; }
    .bp3-menu-item.bp3-intent-success .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-success::before, .bp3-menu-item.bp3-intent-success::after,
    .bp3-menu-item.bp3-intent-success .bp3-menu-item-label{
      color:#0d8050; }
    .bp3-menu-item.bp3-intent-success:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-menu-item.bp3-intent-success.bp3-active{
      background-color:#0f9960; }
    .bp3-menu-item.bp3-intent-success:active{
      background-color:#0d8050; }
    .bp3-menu-item.bp3-intent-success:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-menu-item.bp3-intent-success:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-menu-item.bp3-intent-success:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-success:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-success:active, .bp3-menu-item.bp3-intent-success:active::before, .bp3-menu-item.bp3-intent-success:active::after,
    .bp3-menu-item.bp3-intent-success:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-success.bp3-active, .bp3-menu-item.bp3-intent-success.bp3-active::before, .bp3-menu-item.bp3-intent-success.bp3-active::after,
    .bp3-menu-item.bp3-intent-success.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-warning{
    color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-warning::before, .bp3-menu-item.bp3-intent-warning::after,
    .bp3-menu-item.bp3-intent-warning .bp3-menu-item-label{
      color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-menu-item.bp3-intent-warning.bp3-active{
      background-color:#d9822b; }
    .bp3-menu-item.bp3-intent-warning:active{
      background-color:#bf7326; }
    .bp3-menu-item.bp3-intent-warning:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-menu-item.bp3-intent-warning:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-menu-item.bp3-intent-warning:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-warning:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-warning:active, .bp3-menu-item.bp3-intent-warning:active::before, .bp3-menu-item.bp3-intent-warning:active::after,
    .bp3-menu-item.bp3-intent-warning:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-warning.bp3-active, .bp3-menu-item.bp3-intent-warning.bp3-active::before, .bp3-menu-item.bp3-intent-warning.bp3-active::after,
    .bp3-menu-item.bp3-intent-warning.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item.bp3-intent-danger{
    color:#c23030; }
    .bp3-menu-item.bp3-intent-danger .bp3-icon{
      color:inherit; }
    .bp3-menu-item.bp3-intent-danger::before, .bp3-menu-item.bp3-intent-danger::after,
    .bp3-menu-item.bp3-intent-danger .bp3-menu-item-label{
      color:#c23030; }
    .bp3-menu-item.bp3-intent-danger:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-menu-item.bp3-intent-danger.bp3-active{
      background-color:#db3737; }
    .bp3-menu-item.bp3-intent-danger:active{
      background-color:#c23030; }
    .bp3-menu-item.bp3-intent-danger:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-menu-item.bp3-intent-danger:hover::before, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-menu-item.bp3-intent-danger:hover::after, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after,
    .bp3-menu-item.bp3-intent-danger:hover .bp3-menu-item-label,
    .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label, .bp3-menu-item.bp3-intent-danger:active, .bp3-menu-item.bp3-intent-danger:active::before, .bp3-menu-item.bp3-intent-danger:active::after,
    .bp3-menu-item.bp3-intent-danger:active .bp3-menu-item-label, .bp3-menu-item.bp3-intent-danger.bp3-active, .bp3-menu-item.bp3-intent-danger.bp3-active::before, .bp3-menu-item.bp3-intent-danger.bp3-active::after,
    .bp3-menu-item.bp3-intent-danger.bp3-active .bp3-menu-item-label{
      color:#ffffff; }
  .bp3-menu-item::before{
    line-height:1;
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-weight:400;
    font-style:normal;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    margin-right:7px; }
  .bp3-menu-item::before,
  .bp3-menu-item > .bp3-icon{
    margin-top:2px;
    color:#5c7080; }
  .bp3-menu-item .bp3-menu-item-label{
    color:#5c7080; }
  .bp3-menu-item:hover, .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-menu-item{
    color:inherit; }
  .bp3-menu-item.bp3-active, .bp3-menu-item:active{
    background-color:rgba(115, 134, 148, 0.3); }
  .bp3-menu-item.bp3-disabled{
    outline:none !important;
    background-color:inherit !important;
    cursor:not-allowed !important;
    color:rgba(92, 112, 128, 0.6) !important; }
    .bp3-menu-item.bp3-disabled::before,
    .bp3-menu-item.bp3-disabled > .bp3-icon,
    .bp3-menu-item.bp3-disabled .bp3-menu-item-label{
      color:rgba(92, 112, 128, 0.6) !important; }
  .bp3-large .bp3-menu-item{
    padding:9px 7px;
    line-height:22px;
    font-size:16px; }
    .bp3-large .bp3-menu-item .bp3-icon{
      margin-top:3px; }
    .bp3-large .bp3-menu-item::before{
      line-height:1;
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-weight:400;
      font-style:normal;
      -moz-osx-font-smoothing:grayscale;
      -webkit-font-smoothing:antialiased;
      margin-top:1px;
      margin-right:10px; }

button.bp3-menu-item{
  border:none;
  background:none;
  width:100%;
  text-align:left; }
.bp3-menu-header{
  display:block;
  margin:5px;
  border-top:1px solid rgba(16, 22, 26, 0.15);
  cursor:default;
  padding-left:2px; }
  .bp3-dark .bp3-menu-header{
    border-top-color:rgba(255, 255, 255, 0.15); }
  .bp3-menu-header:first-of-type{
    border-top:none; }
  .bp3-menu-header > h6{
    color:#182026;
    font-weight:600;
    overflow:hidden;
    text-overflow:ellipsis;
    white-space:nowrap;
    word-wrap:normal;
    margin:0;
    padding:10px 7px 0 1px;
    line-height:17px; }
    .bp3-dark .bp3-menu-header > h6{
      color:#f5f8fa; }
  .bp3-menu-header:first-of-type > h6{
    padding-top:0; }
  .bp3-large .bp3-menu-header > h6{
    padding-top:15px;
    padding-bottom:5px;
    font-size:18px; }
  .bp3-large .bp3-menu-header:first-of-type > h6{
    padding-top:0; }

.bp3-dark .bp3-menu{
  background:#30404d;
  color:#f5f8fa; }

.bp3-dark .bp3-menu-item.bp3-intent-primary{
  color:#48aff0; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary .bp3-icon{
    color:inherit; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary::before, .bp3-dark .bp3-menu-item.bp3-intent-primary::after,
  .bp3-dark .bp3-menu-item.bp3-intent-primary .bp3-menu-item-label{
    color:#48aff0; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active{
    background-color:#137cbd; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary:active{
    background-color:#106ba3; }
  .bp3-dark .bp3-menu-item.bp3-intent-primary:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-primary:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-primary:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item::after,
  .bp3-dark .bp3-menu-item.bp3-intent-primary:hover .bp3-menu-item-label,
  .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label,
  .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-primary.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-primary:active, .bp3-dark .bp3-menu-item.bp3-intent-primary:active::before, .bp3-dark .bp3-menu-item.bp3-intent-primary:active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-primary:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-primary.bp3-active .bp3-menu-item-label{
    color:#ffffff; }

.bp3-dark .bp3-menu-item.bp3-intent-success{
  color:#3dcc91; }
  .bp3-dark .bp3-menu-item.bp3-intent-success .bp3-icon{
    color:inherit; }
  .bp3-dark .bp3-menu-item.bp3-intent-success::before, .bp3-dark .bp3-menu-item.bp3-intent-success::after,
  .bp3-dark .bp3-menu-item.bp3-intent-success .bp3-menu-item-label{
    color:#3dcc91; }
  .bp3-dark .bp3-menu-item.bp3-intent-success:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active{
    background-color:#0f9960; }
  .bp3-dark .bp3-menu-item.bp3-intent-success:active{
    background-color:#0d8050; }
  .bp3-dark .bp3-menu-item.bp3-intent-success:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-success:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-success:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item::after,
  .bp3-dark .bp3-menu-item.bp3-intent-success:hover .bp3-menu-item-label,
  .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label,
  .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-success.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-success:active, .bp3-dark .bp3-menu-item.bp3-intent-success:active::before, .bp3-dark .bp3-menu-item.bp3-intent-success:active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-success:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-success.bp3-active .bp3-menu-item-label{
    color:#ffffff; }

.bp3-dark .bp3-menu-item.bp3-intent-warning{
  color:#ffb366; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning .bp3-icon{
    color:inherit; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning::before, .bp3-dark .bp3-menu-item.bp3-intent-warning::after,
  .bp3-dark .bp3-menu-item.bp3-intent-warning .bp3-menu-item-label{
    color:#ffb366; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active{
    background-color:#d9822b; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning:active{
    background-color:#bf7326; }
  .bp3-dark .bp3-menu-item.bp3-intent-warning:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-warning:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-warning:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item::after,
  .bp3-dark .bp3-menu-item.bp3-intent-warning:hover .bp3-menu-item-label,
  .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label,
  .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-warning.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-warning:active, .bp3-dark .bp3-menu-item.bp3-intent-warning:active::before, .bp3-dark .bp3-menu-item.bp3-intent-warning:active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-warning:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-warning.bp3-active .bp3-menu-item-label{
    color:#ffffff; }

.bp3-dark .bp3-menu-item.bp3-intent-danger{
  color:#ff7373; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger .bp3-icon{
    color:inherit; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger::before, .bp3-dark .bp3-menu-item.bp3-intent-danger::after,
  .bp3-dark .bp3-menu-item.bp3-intent-danger .bp3-menu-item-label{
    color:#ff7373; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active{
    background-color:#db3737; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger:active{
    background-color:#c23030; }
  .bp3-dark .bp3-menu-item.bp3-intent-danger:hover, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item, .bp3-dark .bp3-menu-item.bp3-intent-danger:hover::before, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::before, .bp3-dark .bp3-menu-item.bp3-intent-danger:hover::after, .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after, .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item::after,
  .bp3-dark .bp3-menu-item.bp3-intent-danger:hover .bp3-menu-item-label,
  .bp3-dark .bp3-submenu .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label,
  .bp3-submenu .bp3-dark .bp3-popover-target.bp3-popover-open > .bp3-intent-danger.bp3-menu-item .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-danger:active, .bp3-dark .bp3-menu-item.bp3-intent-danger:active::before, .bp3-dark .bp3-menu-item.bp3-intent-danger:active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-danger:active .bp3-menu-item-label, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active::before, .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active::after,
  .bp3-dark .bp3-menu-item.bp3-intent-danger.bp3-active .bp3-menu-item-label{
    color:#ffffff; }

.bp3-dark .bp3-menu-item::before,
.bp3-dark .bp3-menu-item > .bp3-icon{
  color:#a7b6c2; }

.bp3-dark .bp3-menu-item .bp3-menu-item-label{
  color:#a7b6c2; }

.bp3-dark .bp3-menu-item.bp3-active, .bp3-dark .bp3-menu-item:active{
  background-color:rgba(138, 155, 168, 0.3); }

.bp3-dark .bp3-menu-item.bp3-disabled{
  color:rgba(167, 182, 194, 0.6) !important; }
  .bp3-dark .bp3-menu-item.bp3-disabled::before,
  .bp3-dark .bp3-menu-item.bp3-disabled > .bp3-icon,
  .bp3-dark .bp3-menu-item.bp3-disabled .bp3-menu-item-label{
    color:rgba(167, 182, 194, 0.6) !important; }

.bp3-dark .bp3-menu-divider,
.bp3-dark .bp3-menu-header{
  border-color:rgba(255, 255, 255, 0.15); }

.bp3-dark .bp3-menu-header > h6{
  color:#f5f8fa; }

.bp3-label .bp3-menu{
  margin-top:5px; }
.bp3-navbar{
  position:relative;
  z-index:10;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.2);
  background-color:#ffffff;
  width:100%;
  height:50px;
  padding:0 15px; }
  .bp3-navbar.bp3-dark,
  .bp3-dark .bp3-navbar{
    background-color:#394b59; }
  .bp3-navbar.bp3-dark{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-dark .bp3-navbar{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 0 0 rgba(16, 22, 26, 0), 0 1px 1px rgba(16, 22, 26, 0.4); }
  .bp3-navbar.bp3-fixed-top{
    position:fixed;
    top:0;
    right:0;
    left:0; }

.bp3-navbar-heading{
  margin-right:15px;
  font-size:16px; }

.bp3-navbar-group{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  height:50px; }
  .bp3-navbar-group.bp3-align-left{
    float:left; }
  .bp3-navbar-group.bp3-align-right{
    float:right; }

.bp3-navbar-divider{
  margin:0 10px;
  border-left:1px solid rgba(16, 22, 26, 0.15);
  height:20px; }
  .bp3-dark .bp3-navbar-divider{
    border-left-color:rgba(255, 255, 255, 0.15); }
.bp3-non-ideal-state{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  width:100%;
  height:100%;
  text-align:center; }
  .bp3-non-ideal-state > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-non-ideal-state > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-non-ideal-state::before,
  .bp3-non-ideal-state > *{
    margin-bottom:20px; }
  .bp3-non-ideal-state:empty::before,
  .bp3-non-ideal-state > :last-child{
    margin-bottom:0; }
  .bp3-non-ideal-state > *{
    max-width:400px; }

.bp3-non-ideal-state-visual{
  color:rgba(92, 112, 128, 0.6);
  font-size:60px; }
  .bp3-dark .bp3-non-ideal-state-visual{
    color:rgba(167, 182, 194, 0.6); }

.bp3-overflow-list{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-wrap:nowrap;
      flex-wrap:nowrap;
  min-width:0; }

.bp3-overflow-list-spacer{
  -ms-flex-negative:1;
      flex-shrink:1;
  width:1px; }

body.bp3-overlay-open{
  overflow:hidden; }

.bp3-overlay{
  position:static;
  top:0;
  right:0;
  bottom:0;
  left:0;
  z-index:20; }
  .bp3-overlay:not(.bp3-overlay-open){
    pointer-events:none; }
  .bp3-overlay.bp3-overlay-container{
    position:fixed;
    overflow:hidden; }
    .bp3-overlay.bp3-overlay-container.bp3-overlay-inline{
      position:absolute; }
  .bp3-overlay.bp3-overlay-scroll-container{
    position:fixed;
    overflow:auto; }
    .bp3-overlay.bp3-overlay-scroll-container.bp3-overlay-inline{
      position:absolute; }
  .bp3-overlay.bp3-overlay-inline{
    display:inline;
    overflow:visible; }

.bp3-overlay-content{
  position:fixed;
  z-index:20; }
  .bp3-overlay-inline .bp3-overlay-content,
  .bp3-overlay-scroll-container .bp3-overlay-content{
    position:absolute; }

.bp3-overlay-backdrop{
  position:fixed;
  top:0;
  right:0;
  bottom:0;
  left:0;
  opacity:1;
  z-index:20;
  background-color:rgba(16, 22, 26, 0.7);
  overflow:auto;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-overlay-backdrop.bp3-overlay-enter, .bp3-overlay-backdrop.bp3-overlay-appear{
    opacity:0; }
  .bp3-overlay-backdrop.bp3-overlay-enter-active, .bp3-overlay-backdrop.bp3-overlay-appear-active{
    opacity:1;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-overlay-backdrop.bp3-overlay-exit{
    opacity:1; }
  .bp3-overlay-backdrop.bp3-overlay-exit-active{
    opacity:0;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-overlay-backdrop:focus{
    outline:none; }
  .bp3-overlay-inline .bp3-overlay-backdrop{
    position:absolute; }
.bp3-panel-stack{
  position:relative;
  overflow:hidden; }

.bp3-panel-stack-header{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -ms-flex-negative:0;
      flex-shrink:0;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  z-index:1;
  -webkit-box-shadow:0 1px rgba(16, 22, 26, 0.15);
          box-shadow:0 1px rgba(16, 22, 26, 0.15);
  height:30px; }
  .bp3-dark .bp3-panel-stack-header{
    -webkit-box-shadow:0 1px rgba(255, 255, 255, 0.15);
            box-shadow:0 1px rgba(255, 255, 255, 0.15); }
  .bp3-panel-stack-header > span{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-flex:1;
        -ms-flex:1;
            flex:1;
    -webkit-box-align:stretch;
        -ms-flex-align:stretch;
            align-items:stretch; }
  .bp3-panel-stack-header .bp3-heading{
    margin:0 5px; }

.bp3-button.bp3-panel-stack-header-back{
  margin-left:5px;
  padding-left:0;
  white-space:nowrap; }
  .bp3-button.bp3-panel-stack-header-back .bp3-icon{
    margin:0 2px; }

.bp3-panel-stack-view{
  position:absolute;
  top:0;
  right:0;
  bottom:0;
  left:0;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  margin-right:-1px;
  border-right:1px solid rgba(16, 22, 26, 0.15);
  background-color:#ffffff;
  overflow-y:auto; }
  .bp3-dark .bp3-panel-stack-view{
    background-color:#30404d; }

.bp3-panel-stack-push .bp3-panel-stack-enter, .bp3-panel-stack-push .bp3-panel-stack-appear{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0; }

.bp3-panel-stack-push .bp3-panel-stack-enter-active, .bp3-panel-stack-push .bp3-panel-stack-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease;
  -webkit-transition-delay:0;
          transition-delay:0; }

.bp3-panel-stack-push .bp3-panel-stack-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack-push .bp3-panel-stack-exit-active{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease;
  -webkit-transition-delay:0;
          transition-delay:0; }

.bp3-panel-stack-pop .bp3-panel-stack-enter, .bp3-panel-stack-pop .bp3-panel-stack-appear{
  -webkit-transform:translateX(-50%);
          transform:translateX(-50%);
  opacity:0; }

.bp3-panel-stack-pop .bp3-panel-stack-enter-active, .bp3-panel-stack-pop .bp3-panel-stack-appear-active{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease;
  -webkit-transition-delay:0;
          transition-delay:0; }

.bp3-panel-stack-pop .bp3-panel-stack-exit{
  -webkit-transform:translate(0%);
          transform:translate(0%);
  opacity:1; }

.bp3-panel-stack-pop .bp3-panel-stack-exit-active{
  -webkit-transform:translateX(100%);
          transform:translateX(100%);
  opacity:0;
  -webkit-transition-property:opacity, -webkit-transform;
  transition-property:opacity, -webkit-transform;
  transition-property:transform, opacity;
  transition-property:transform, opacity, -webkit-transform;
  -webkit-transition-duration:400ms;
          transition-duration:400ms;
  -webkit-transition-timing-function:ease;
          transition-timing-function:ease;
  -webkit-transition-delay:0;
          transition-delay:0; }
.bp3-popover{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  -webkit-transform:scale(1);
          transform:scale(1);
  display:inline-block;
  z-index:20;
  border-radius:3px; }
  .bp3-popover .bp3-popover-arrow{
    position:absolute;
    width:30px;
    height:30px; }
    .bp3-popover .bp3-popover-arrow::before{
      margin:5px;
      width:20px;
      height:20px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover{
    margin-top:-17px;
    margin-bottom:17px; }
    .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow{
      bottom:-11px; }
      .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(-90deg);
                transform:rotate(-90deg); }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover{
    margin-left:17px; }
    .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow{
      left:-11px; }
      .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(0);
                transform:rotate(0); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover{
    margin-top:17px; }
    .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow{
      top:-11px; }
      .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(90deg);
                transform:rotate(90deg); }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover{
    margin-right:17px;
    margin-left:-17px; }
    .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow{
      right:-11px; }
      .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow svg{
        -webkit-transform:rotate(180deg);
                transform:rotate(180deg); }
  .bp3-tether-element-attached-middle > .bp3-popover > .bp3-popover-arrow{
    top:50%;
    -webkit-transform:translateY(-50%);
            transform:translateY(-50%); }
  .bp3-tether-element-attached-center > .bp3-popover > .bp3-popover-arrow{
    right:50%;
    -webkit-transform:translateX(50%);
            transform:translateX(50%); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-top > .bp3-popover > .bp3-popover-arrow{
    top:-0.3934px; }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-right > .bp3-popover > .bp3-popover-arrow{
    right:-0.3934px; }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-left > .bp3-popover > .bp3-popover-arrow{
    left:-0.3934px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-bottom > .bp3-popover > .bp3-popover-arrow{
    bottom:-0.3934px; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:top left;
            transform-origin:top left; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:top center;
            transform-origin:top center; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:top right;
            transform-origin:top right; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:center left;
            transform-origin:center left; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:center center;
            transform-origin:center center; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:center right;
            transform-origin:center right; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-left > .bp3-popover{
    -webkit-transform-origin:bottom left;
            transform-origin:bottom left; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-center > .bp3-popover{
    -webkit-transform-origin:bottom center;
            transform-origin:bottom center; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-right > .bp3-popover{
    -webkit-transform-origin:bottom right;
            transform-origin:bottom right; }
  .bp3-popover .bp3-popover-content{
    background:#ffffff;
    color:inherit; }
  .bp3-popover .bp3-popover-arrow::before{
    -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2);
            box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2); }
  .bp3-popover .bp3-popover-arrow-border{
    fill:#10161a;
    fill-opacity:0.1; }
  .bp3-popover .bp3-popover-arrow-fill{
    fill:#ffffff; }
  .bp3-popover-enter > .bp3-popover, .bp3-popover-appear > .bp3-popover{
    -webkit-transform:scale(0.3);
            transform:scale(0.3); }
  .bp3-popover-enter-active > .bp3-popover, .bp3-popover-appear-active > .bp3-popover{
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-popover-exit > .bp3-popover{
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-popover-exit-active > .bp3-popover{
    -webkit-transform:scale(0.3);
            transform:scale(0.3);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-popover .bp3-popover-content{
    position:relative;
    border-radius:3px; }
  .bp3-popover.bp3-popover-content-sizing .bp3-popover-content{
    max-width:350px;
    padding:20px; }
  .bp3-popover-target + .bp3-overlay .bp3-popover.bp3-popover-content-sizing{
    width:350px; }
  .bp3-popover.bp3-minimal{
    margin:0 !important; }
    .bp3-popover.bp3-minimal .bp3-popover-arrow{
      display:none; }
    .bp3-popover.bp3-minimal.bp3-popover{
      -webkit-transform:scale(1);
              transform:scale(1); }
      .bp3-popover-enter > .bp3-popover.bp3-minimal.bp3-popover, .bp3-popover-appear > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1); }
      .bp3-popover-enter-active > .bp3-popover.bp3-minimal.bp3-popover, .bp3-popover-appear-active > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1);
        -webkit-transition-property:-webkit-transform;
        transition-property:-webkit-transform;
        transition-property:transform;
        transition-property:transform, -webkit-transform;
        -webkit-transition-duration:100ms;
                transition-duration:100ms;
        -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
                transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
        -webkit-transition-delay:0;
                transition-delay:0; }
      .bp3-popover-exit > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1); }
      .bp3-popover-exit-active > .bp3-popover.bp3-minimal.bp3-popover{
        -webkit-transform:scale(1);
                transform:scale(1);
        -webkit-transition-property:-webkit-transform;
        transition-property:-webkit-transform;
        transition-property:transform;
        transition-property:transform, -webkit-transform;
        -webkit-transition-duration:100ms;
                transition-duration:100ms;
        -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
                transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
        -webkit-transition-delay:0;
                transition-delay:0; }
  .bp3-popover.bp3-dark,
  .bp3-dark .bp3-popover{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-popover.bp3-dark .bp3-popover-content,
    .bp3-dark .bp3-popover .bp3-popover-content{
      background:#30404d;
      color:inherit; }
    .bp3-popover.bp3-dark .bp3-popover-arrow::before,
    .bp3-dark .bp3-popover .bp3-popover-arrow::before{
      -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4);
              box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4); }
    .bp3-popover.bp3-dark .bp3-popover-arrow-border,
    .bp3-dark .bp3-popover .bp3-popover-arrow-border{
      fill:#10161a;
      fill-opacity:0.2; }
    .bp3-popover.bp3-dark .bp3-popover-arrow-fill,
    .bp3-dark .bp3-popover .bp3-popover-arrow-fill{
      fill:#30404d; }

.bp3-popover-arrow::before{
  display:block;
  position:absolute;
  -webkit-transform:rotate(45deg);
          transform:rotate(45deg);
  border-radius:2px;
  content:""; }

.bp3-tether-pinned .bp3-popover-arrow{
  display:none; }

.bp3-popover-backdrop{
  background:rgba(255, 255, 255, 0); }

.bp3-transition-container{
  opacity:1;
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  z-index:20; }
  .bp3-transition-container.bp3-popover-enter, .bp3-transition-container.bp3-popover-appear{
    opacity:0; }
  .bp3-transition-container.bp3-popover-enter-active, .bp3-transition-container.bp3-popover-appear-active{
    opacity:1;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-transition-container.bp3-popover-exit{
    opacity:1; }
  .bp3-transition-container.bp3-popover-exit-active{
    opacity:0;
    -webkit-transition-property:opacity;
    transition-property:opacity;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-transition-container:focus{
    outline:none; }
  .bp3-transition-container.bp3-popover-leave .bp3-popover-content{
    pointer-events:none; }
  .bp3-transition-container[data-x-out-of-boundaries]{
    display:none; }

span.bp3-popover-target{
  display:inline-block; }

.bp3-popover-wrapper.bp3-fill{
  width:100%; }

.bp3-portal{
  position:absolute;
  top:0;
  right:0;
  left:0; }
@-webkit-keyframes linear-progress-bar-stripes{
  from{
    background-position:0 0; }
  to{
    background-position:30px 0; } }
@keyframes linear-progress-bar-stripes{
  from{
    background-position:0 0; }
  to{
    background-position:30px 0; } }

.bp3-progress-bar{
  display:block;
  position:relative;
  border-radius:40px;
  background:rgba(92, 112, 128, 0.2);
  width:100%;
  height:8px;
  overflow:hidden; }
  .bp3-progress-bar .bp3-progress-meter{
    position:absolute;
    border-radius:40px;
    background:linear-gradient(-45deg, rgba(255, 255, 255, 0.2) 25%, transparent 25%, transparent 50%, rgba(255, 255, 255, 0.2) 50%, rgba(255, 255, 255, 0.2) 75%, transparent 75%);
    background-color:rgba(92, 112, 128, 0.8);
    background-size:30px 30px;
    width:100%;
    height:100%;
    -webkit-transition:width 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:width 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-progress-bar:not(.bp3-no-animation):not(.bp3-no-stripes) .bp3-progress-meter{
    animation:linear-progress-bar-stripes 300ms linear infinite reverse; }
  .bp3-progress-bar.bp3-no-stripes .bp3-progress-meter{
    background-image:none; }

.bp3-dark .bp3-progress-bar{
  background:rgba(16, 22, 26, 0.5); }
  .bp3-dark .bp3-progress-bar .bp3-progress-meter{
    background-color:#8a9ba8; }

.bp3-progress-bar.bp3-intent-primary .bp3-progress-meter{
  background-color:#137cbd; }

.bp3-progress-bar.bp3-intent-success .bp3-progress-meter{
  background-color:#0f9960; }

.bp3-progress-bar.bp3-intent-warning .bp3-progress-meter{
  background-color:#d9822b; }

.bp3-progress-bar.bp3-intent-danger .bp3-progress-meter{
  background-color:#db3737; }
@-webkit-keyframes skeleton-glow{
  from{
    border-color:rgba(206, 217, 224, 0.2);
    background:rgba(206, 217, 224, 0.2); }
  to{
    border-color:rgba(92, 112, 128, 0.2);
    background:rgba(92, 112, 128, 0.2); } }
@keyframes skeleton-glow{
  from{
    border-color:rgba(206, 217, 224, 0.2);
    background:rgba(206, 217, 224, 0.2); }
  to{
    border-color:rgba(92, 112, 128, 0.2);
    background:rgba(92, 112, 128, 0.2); } }
.bp3-skeleton{
  border-color:rgba(206, 217, 224, 0.2) !important;
  border-radius:2px;
  -webkit-box-shadow:none !important;
          box-shadow:none !important;
  background:rgba(206, 217, 224, 0.2);
  background-clip:padding-box !important;
  cursor:default;
  color:transparent !important;
  -webkit-animation:1000ms linear infinite alternate skeleton-glow;
          animation:1000ms linear infinite alternate skeleton-glow;
  pointer-events:none;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-skeleton::before, .bp3-skeleton::after,
  .bp3-skeleton *{
    visibility:hidden !important; }
.bp3-slider{
  width:100%;
  min-width:150px;
  height:40px;
  position:relative;
  outline:none;
  cursor:default;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-slider:hover{
    cursor:pointer; }
  .bp3-slider:active{
    cursor:-webkit-grabbing;
    cursor:grabbing; }
  .bp3-slider.bp3-disabled{
    opacity:0.5;
    cursor:not-allowed; }
  .bp3-slider.bp3-slider-unlabeled{
    height:16px; }

.bp3-slider-track,
.bp3-slider-progress{
  top:5px;
  right:0;
  left:0;
  height:6px;
  position:absolute; }

.bp3-slider-track{
  border-radius:3px;
  overflow:hidden; }

.bp3-slider-progress{
  background:rgba(92, 112, 128, 0.2); }
  .bp3-dark .bp3-slider-progress{
    background:rgba(16, 22, 26, 0.5); }
  .bp3-slider-progress.bp3-intent-primary{
    background-color:#137cbd; }
  .bp3-slider-progress.bp3-intent-success{
    background-color:#0f9960; }
  .bp3-slider-progress.bp3-intent-warning{
    background-color:#d9822b; }
  .bp3-slider-progress.bp3-intent-danger{
    background-color:#db3737; }

.bp3-slider-handle{
  -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
          box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
  background-color:#f5f8fa;
  background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.8)), to(rgba(255, 255, 255, 0)));
  background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0));
  color:#182026;
  position:absolute;
  top:0;
  left:0;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
  cursor:pointer;
  width:16px;
  height:16px; }
  .bp3-slider-handle:hover{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#ebf1f5; }
  .bp3-slider-handle:active, .bp3-slider-handle.bp3-active{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#d8e1e8;
    background-image:none; }
  .bp3-slider-handle:disabled, .bp3-slider-handle.bp3-disabled{
    outline:none;
    -webkit-box-shadow:none;
            box-shadow:none;
    background-color:rgba(206, 217, 224, 0.5);
    background-image:none;
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
    .bp3-slider-handle:disabled.bp3-active, .bp3-slider-handle:disabled.bp3-active:hover, .bp3-slider-handle.bp3-disabled.bp3-active, .bp3-slider-handle.bp3-disabled.bp3-active:hover{
      background:rgba(206, 217, 224, 0.7); }
  .bp3-slider-handle:focus{
    z-index:1; }
  .bp3-slider-handle:hover{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 -1px 0 rgba(16, 22, 26, 0.1);
    background-clip:padding-box;
    background-color:#ebf1f5;
    z-index:2;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 1px 1px rgba(16, 22, 26, 0.2);
    cursor:-webkit-grab;
    cursor:grab; }
  .bp3-slider-handle.bp3-active{
    -webkit-box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
            box-shadow:inset 0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 2px rgba(16, 22, 26, 0.2);
    background-color:#d8e1e8;
    background-image:none;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 1px rgba(16, 22, 26, 0.1);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), inset 0 1px 1px rgba(16, 22, 26, 0.1);
    cursor:-webkit-grabbing;
    cursor:grabbing; }
  .bp3-disabled .bp3-slider-handle{
    -webkit-box-shadow:none;
            box-shadow:none;
    background:#bfccd6;
    pointer-events:none; }
  .bp3-dark .bp3-slider-handle{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
    background-color:#394b59;
    background-image:-webkit-gradient(linear, left top, left bottom, from(rgba(255, 255, 255, 0.05)), to(rgba(255, 255, 255, 0)));
    background-image:linear-gradient(to bottom, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0));
    color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle:hover, .bp3-dark .bp3-slider-handle:active, .bp3-dark .bp3-slider-handle.bp3-active{
      color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle:hover{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.4);
      background-color:#30404d; }
    .bp3-dark .bp3-slider-handle:active, .bp3-dark .bp3-slider-handle.bp3-active{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.6), inset 0 1px 2px rgba(16, 22, 26, 0.2);
      background-color:#202b33;
      background-image:none; }
    .bp3-dark .bp3-slider-handle:disabled, .bp3-dark .bp3-slider-handle.bp3-disabled{
      -webkit-box-shadow:none;
              box-shadow:none;
      background-color:rgba(57, 75, 89, 0.5);
      background-image:none;
      color:rgba(167, 182, 194, 0.6); }
      .bp3-dark .bp3-slider-handle:disabled.bp3-active, .bp3-dark .bp3-slider-handle.bp3-disabled.bp3-active{
        background:rgba(57, 75, 89, 0.7); }
    .bp3-dark .bp3-slider-handle .bp3-button-spinner .bp3-spinner-head{
      background:rgba(16, 22, 26, 0.5);
      stroke:#8a9ba8; }
    .bp3-dark .bp3-slider-handle, .bp3-dark .bp3-slider-handle:hover{
      background-color:#394b59; }
    .bp3-dark .bp3-slider-handle.bp3-active{
      background-color:#293742; }
  .bp3-dark .bp3-disabled .bp3-slider-handle{
    border-color:#5c7080;
    -webkit-box-shadow:none;
            box-shadow:none;
    background:#5c7080; }
  .bp3-slider-handle .bp3-slider-label{
    margin-left:8px;
    border-radius:3px;
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
    background:#394b59;
    color:#f5f8fa; }
    .bp3-dark .bp3-slider-handle .bp3-slider-label{
      -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
      background:#e1e8ed;
      color:#394b59; }
    .bp3-disabled .bp3-slider-handle .bp3-slider-label{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-slider-handle.bp3-start, .bp3-slider-handle.bp3-end{
    width:8px; }
  .bp3-slider-handle.bp3-start{
    border-top-right-radius:0;
    border-bottom-right-radius:0; }
  .bp3-slider-handle.bp3-end{
    margin-left:8px;
    border-top-left-radius:0;
    border-bottom-left-radius:0; }
    .bp3-slider-handle.bp3-end .bp3-slider-label{
      margin-left:0; }

.bp3-slider-label{
  -webkit-transform:translate(-50%, 20px);
          transform:translate(-50%, 20px);
  display:inline-block;
  position:absolute;
  padding:2px 5px;
  vertical-align:top;
  line-height:1;
  font-size:12px; }

.bp3-slider.bp3-vertical{
  width:40px;
  min-width:40px;
  height:150px; }
  .bp3-slider.bp3-vertical .bp3-slider-track,
  .bp3-slider.bp3-vertical .bp3-slider-progress{
    top:0;
    bottom:0;
    left:5px;
    width:6px;
    height:auto; }
  .bp3-slider.bp3-vertical .bp3-slider-progress{
    top:auto; }
  .bp3-slider.bp3-vertical .bp3-slider-label{
    -webkit-transform:translate(20px, 50%);
            transform:translate(20px, 50%); }
  .bp3-slider.bp3-vertical .bp3-slider-handle{
    top:auto; }
    .bp3-slider.bp3-vertical .bp3-slider-handle .bp3-slider-label{
      margin-top:-8px;
      margin-left:0; }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-end, .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start{
      margin-left:0;
      width:16px;
      height:8px; }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start{
      border-top-left-radius:0;
      border-bottom-right-radius:3px; }
      .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-start .bp3-slider-label{
        -webkit-transform:translate(20px);
                transform:translate(20px); }
    .bp3-slider.bp3-vertical .bp3-slider-handle.bp3-end{
      margin-bottom:8px;
      border-top-left-radius:3px;
      border-bottom-left-radius:0;
      border-bottom-right-radius:0; }

@-webkit-keyframes pt-spinner-animation{
  from{
    -webkit-transform:rotate(0deg);
            transform:rotate(0deg); }
  to{
    -webkit-transform:rotate(360deg);
            transform:rotate(360deg); } }

@keyframes pt-spinner-animation{
  from{
    -webkit-transform:rotate(0deg);
            transform:rotate(0deg); }
  to{
    -webkit-transform:rotate(360deg);
            transform:rotate(360deg); } }

.bp3-spinner{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  -webkit-box-pack:center;
      -ms-flex-pack:center;
          justify-content:center;
  overflow:visible;
  vertical-align:middle; }
  .bp3-spinner svg{
    display:block; }
  .bp3-spinner path{
    fill-opacity:0; }
  .bp3-spinner .bp3-spinner-head{
    -webkit-transform-origin:center;
            transform-origin:center;
    -webkit-transition:stroke-dashoffset 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    transition:stroke-dashoffset 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
    stroke:rgba(92, 112, 128, 0.8);
    stroke-linecap:round; }
  .bp3-spinner .bp3-spinner-track{
    stroke:rgba(92, 112, 128, 0.2); }

.bp3-spinner-animation{
  -webkit-animation:pt-spinner-animation 500ms linear infinite;
          animation:pt-spinner-animation 500ms linear infinite; }
  .bp3-no-spin > .bp3-spinner-animation{
    -webkit-animation:none;
            animation:none; }

.bp3-dark .bp3-spinner .bp3-spinner-head{
  stroke:#8a9ba8; }

.bp3-dark .bp3-spinner .bp3-spinner-track{
  stroke:rgba(16, 22, 26, 0.5); }

.bp3-spinner.bp3-intent-primary .bp3-spinner-head{
  stroke:#137cbd; }

.bp3-spinner.bp3-intent-success .bp3-spinner-head{
  stroke:#0f9960; }

.bp3-spinner.bp3-intent-warning .bp3-spinner-head{
  stroke:#d9822b; }

.bp3-spinner.bp3-intent-danger .bp3-spinner-head{
  stroke:#db3737; }
.bp3-tabs.bp3-vertical{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex; }
  .bp3-tabs.bp3-vertical > .bp3-tab-list{
    -webkit-box-orient:vertical;
    -webkit-box-direction:normal;
        -ms-flex-direction:column;
            flex-direction:column;
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start; }
    .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab{
      border-radius:3px;
      width:100%;
      padding:0 10px; }
      .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab[aria-selected="true"]{
        -webkit-box-shadow:none;
                box-shadow:none;
        background-color:rgba(19, 124, 189, 0.2); }
    .bp3-tabs.bp3-vertical > .bp3-tab-list .bp3-tab-indicator-wrapper .bp3-tab-indicator{
      top:0;
      right:0;
      bottom:0;
      left:0;
      border-radius:3px;
      background-color:rgba(19, 124, 189, 0.2);
      height:auto; }
  .bp3-tabs.bp3-vertical > .bp3-tab-panel{
    margin-top:0;
    padding-left:20px; }

.bp3-tab-list{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  -webkit-box-align:end;
      -ms-flex-align:end;
          align-items:flex-end;
  position:relative;
  margin:0;
  border:none;
  padding:0;
  list-style:none; }
  .bp3-tab-list > *:not(:last-child){
    margin-right:20px; }

.bp3-tab{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  -webkit-box-flex:0;
      -ms-flex:0 0 auto;
          flex:0 0 auto;
  position:relative;
  cursor:pointer;
  max-width:100%;
  vertical-align:top;
  line-height:30px;
  color:#182026;
  font-size:14px; }
  .bp3-tab a{
    display:block;
    text-decoration:none;
    color:inherit; }
  .bp3-tab-indicator-wrapper ~ .bp3-tab{
    -webkit-box-shadow:none !important;
            box-shadow:none !important;
    background-color:transparent !important; }
  .bp3-tab[aria-disabled="true"]{
    cursor:not-allowed;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-tab[aria-selected="true"]{
    border-radius:0;
    -webkit-box-shadow:inset 0 -3px 0 #106ba3;
            box-shadow:inset 0 -3px 0 #106ba3; }
  .bp3-tab[aria-selected="true"], .bp3-tab:not([aria-disabled="true"]):hover{
    color:#106ba3; }
  .bp3-tab:focus{
    -moz-outline-radius:0; }
  .bp3-large > .bp3-tab{
    line-height:40px;
    font-size:16px; }

.bp3-tab-panel{
  margin-top:20px; }
  .bp3-tab-panel[aria-hidden="true"]{
    display:none; }

.bp3-tab-indicator-wrapper{
  position:absolute;
  top:0;
  left:0;
  -webkit-transform:translateX(0), translateY(0);
          transform:translateX(0), translateY(0);
  -webkit-transition:height, width, -webkit-transform;
  transition:height, width, -webkit-transform;
  transition:height, transform, width;
  transition:height, transform, width, -webkit-transform;
  -webkit-transition-duration:200ms;
          transition-duration:200ms;
  -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
          transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
  pointer-events:none; }
  .bp3-tab-indicator-wrapper .bp3-tab-indicator{
    position:absolute;
    right:0;
    bottom:0;
    left:0;
    background-color:#106ba3;
    height:3px; }
  .bp3-tab-indicator-wrapper.bp3-no-animation{
    -webkit-transition:none;
    transition:none; }

.bp3-dark .bp3-tab{
  color:#f5f8fa; }
  .bp3-dark .bp3-tab[aria-disabled="true"]{
    color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-tab[aria-selected="true"]{
    -webkit-box-shadow:inset 0 -3px 0 #48aff0;
            box-shadow:inset 0 -3px 0 #48aff0; }
  .bp3-dark .bp3-tab[aria-selected="true"], .bp3-dark .bp3-tab:not([aria-disabled="true"]):hover{
    color:#48aff0; }

.bp3-dark .bp3-tab-indicator{
  background-color:#48aff0; }

.bp3-flex-expander{
  -webkit-box-flex:1;
      -ms-flex:1 1;
          flex:1 1; }
.bp3-tag{
  display:-webkit-inline-box;
  display:-ms-inline-flexbox;
  display:inline-flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  position:relative;
  border:none;
  border-radius:3px;
  -webkit-box-shadow:none;
          box-shadow:none;
  background-color:#5c7080;
  min-width:20px;
  max-width:100%;
  min-height:20px;
  padding:2px 6px;
  line-height:16px;
  color:#f5f8fa;
  font-size:12px; }
  .bp3-tag.bp3-interactive{
    cursor:pointer; }
    .bp3-tag.bp3-interactive:hover{
      background-color:rgba(92, 112, 128, 0.85); }
    .bp3-tag.bp3-interactive.bp3-active, .bp3-tag.bp3-interactive:active{
      background-color:rgba(92, 112, 128, 0.7); }
  .bp3-tag > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-tag > .bp3-fill{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-tag::before,
  .bp3-tag > *{
    margin-right:4px; }
  .bp3-tag:empty::before,
  .bp3-tag > :last-child{
    margin-right:0; }
  .bp3-tag:focus{
    outline:rgba(19, 124, 189, 0.6) auto 2px;
    outline-offset:0;
    -moz-outline-radius:6px; }
  .bp3-tag.bp3-round{
    border-radius:30px;
    padding-right:8px;
    padding-left:8px; }
  .bp3-dark .bp3-tag{
    background-color:#bfccd6;
    color:#182026; }
    .bp3-dark .bp3-tag.bp3-interactive{
      cursor:pointer; }
      .bp3-dark .bp3-tag.bp3-interactive:hover{
        background-color:rgba(191, 204, 214, 0.85); }
      .bp3-dark .bp3-tag.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-interactive:active{
        background-color:rgba(191, 204, 214, 0.7); }
    .bp3-dark .bp3-tag > .bp3-icon, .bp3-dark .bp3-tag .bp3-icon-standard, .bp3-dark .bp3-tag .bp3-icon-large{
      fill:currentColor; }
  .bp3-tag > .bp3-icon, .bp3-tag .bp3-icon-standard, .bp3-tag .bp3-icon-large{
    fill:#ffffff; }
  .bp3-tag.bp3-large,
  .bp3-large .bp3-tag{
    min-width:30px;
    min-height:30px;
    padding:0 10px;
    line-height:20px;
    font-size:14px; }
    .bp3-tag.bp3-large::before,
    .bp3-tag.bp3-large > *,
    .bp3-large .bp3-tag::before,
    .bp3-large .bp3-tag > *{
      margin-right:7px; }
    .bp3-tag.bp3-large:empty::before,
    .bp3-tag.bp3-large > :last-child,
    .bp3-large .bp3-tag:empty::before,
    .bp3-large .bp3-tag > :last-child{
      margin-right:0; }
    .bp3-tag.bp3-large.bp3-round,
    .bp3-large .bp3-tag.bp3-round{
      padding-right:12px;
      padding-left:12px; }
  .bp3-tag.bp3-intent-primary{
    background:#137cbd;
    color:#ffffff; }
    .bp3-tag.bp3-intent-primary.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-primary.bp3-interactive:hover{
        background-color:rgba(19, 124, 189, 0.85); }
      .bp3-tag.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-primary.bp3-interactive:active{
        background-color:rgba(19, 124, 189, 0.7); }
  .bp3-tag.bp3-intent-success{
    background:#0f9960;
    color:#ffffff; }
    .bp3-tag.bp3-intent-success.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-success.bp3-interactive:hover{
        background-color:rgba(15, 153, 96, 0.85); }
      .bp3-tag.bp3-intent-success.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-success.bp3-interactive:active{
        background-color:rgba(15, 153, 96, 0.7); }
  .bp3-tag.bp3-intent-warning{
    background:#d9822b;
    color:#ffffff; }
    .bp3-tag.bp3-intent-warning.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-warning.bp3-interactive:hover{
        background-color:rgba(217, 130, 43, 0.85); }
      .bp3-tag.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-warning.bp3-interactive:active{
        background-color:rgba(217, 130, 43, 0.7); }
  .bp3-tag.bp3-intent-danger{
    background:#db3737;
    color:#ffffff; }
    .bp3-tag.bp3-intent-danger.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-intent-danger.bp3-interactive:hover{
        background-color:rgba(219, 55, 55, 0.85); }
      .bp3-tag.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-tag.bp3-intent-danger.bp3-interactive:active{
        background-color:rgba(219, 55, 55, 0.7); }
  .bp3-tag.bp3-fill{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    width:100%; }
  .bp3-tag.bp3-minimal > .bp3-icon, .bp3-tag.bp3-minimal .bp3-icon-standard, .bp3-tag.bp3-minimal .bp3-icon-large{
    fill:#5c7080; }
  .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]){
    background-color:rgba(138, 155, 168, 0.2);
    color:#182026; }
    .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:hover{
        background-color:rgba(92, 112, 128, 0.3); }
      .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive.bp3-active, .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:active{
        background-color:rgba(92, 112, 128, 0.4); }
    .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]){
      color:#f5f8fa; }
      .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:hover{
          background-color:rgba(191, 204, 214, 0.3); }
        .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]).bp3-interactive:active{
          background-color:rgba(191, 204, 214, 0.4); }
      .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) > .bp3-icon, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) .bp3-icon-standard, .bp3-dark .bp3-tag.bp3-minimal:not([class*="bp3-intent-"]) .bp3-icon-large{
        fill:#a7b6c2; }
  .bp3-tag.bp3-minimal.bp3-intent-primary{
    background-color:rgba(19, 124, 189, 0.15);
    color:#106ba3; }
    .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:hover{
        background-color:rgba(19, 124, 189, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:active{
        background-color:rgba(19, 124, 189, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-primary > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-primary .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-primary .bp3-icon-large{
      fill:#137cbd; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary{
      background-color:rgba(19, 124, 189, 0.25);
      color:#48aff0; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:hover{
          background-color:rgba(19, 124, 189, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-primary.bp3-interactive:active{
          background-color:rgba(19, 124, 189, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-success{
    background-color:rgba(15, 153, 96, 0.15);
    color:#0d8050; }
    .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:hover{
        background-color:rgba(15, 153, 96, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:active{
        background-color:rgba(15, 153, 96, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-success > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-success .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-success .bp3-icon-large{
      fill:#0f9960; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success{
      background-color:rgba(15, 153, 96, 0.25);
      color:#3dcc91; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:hover{
          background-color:rgba(15, 153, 96, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-success.bp3-interactive:active{
          background-color:rgba(15, 153, 96, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-warning{
    background-color:rgba(217, 130, 43, 0.15);
    color:#bf7326; }
    .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:hover{
        background-color:rgba(217, 130, 43, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:active{
        background-color:rgba(217, 130, 43, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-warning > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-warning .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-warning .bp3-icon-large{
      fill:#d9822b; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning{
      background-color:rgba(217, 130, 43, 0.25);
      color:#ffb366; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:hover{
          background-color:rgba(217, 130, 43, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-warning.bp3-interactive:active{
          background-color:rgba(217, 130, 43, 0.45); }
  .bp3-tag.bp3-minimal.bp3-intent-danger{
    background-color:rgba(219, 55, 55, 0.15);
    color:#c23030; }
    .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive{
      cursor:pointer; }
      .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:hover{
        background-color:rgba(219, 55, 55, 0.25); }
      .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:active{
        background-color:rgba(219, 55, 55, 0.35); }
    .bp3-tag.bp3-minimal.bp3-intent-danger > .bp3-icon, .bp3-tag.bp3-minimal.bp3-intent-danger .bp3-icon-standard, .bp3-tag.bp3-minimal.bp3-intent-danger .bp3-icon-large{
      fill:#db3737; }
    .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger{
      background-color:rgba(219, 55, 55, 0.25);
      color:#ff7373; }
      .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive{
        cursor:pointer; }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:hover{
          background-color:rgba(219, 55, 55, 0.35); }
        .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive.bp3-active, .bp3-dark .bp3-tag.bp3-minimal.bp3-intent-danger.bp3-interactive:active{
          background-color:rgba(219, 55, 55, 0.45); }

.bp3-tag-remove{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  opacity:0.5;
  margin-top:-2px;
  margin-right:-6px !important;
  margin-bottom:-2px;
  border:none;
  background:none;
  cursor:pointer;
  padding:2px;
  padding-left:0;
  color:inherit; }
  .bp3-tag-remove:hover{
    opacity:0.8;
    background:none;
    text-decoration:none; }
  .bp3-tag-remove:active{
    opacity:1; }
  .bp3-tag-remove:empty::before{
    line-height:1;
    font-family:"Icons16", sans-serif;
    font-size:16px;
    font-weight:400;
    font-style:normal;
    -moz-osx-font-smoothing:grayscale;
    -webkit-font-smoothing:antialiased;
    content:""; }
  .bp3-large .bp3-tag-remove{
    margin-right:-10px !important;
    padding:5px;
    padding-left:0; }
    .bp3-large .bp3-tag-remove:empty::before{
      line-height:1;
      font-family:"Icons20", sans-serif;
      font-size:20px;
      font-weight:400;
      font-style:normal; }
.bp3-tag-input{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-orient:horizontal;
  -webkit-box-direction:normal;
      -ms-flex-direction:row;
          flex-direction:row;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  cursor:text;
  height:auto;
  min-height:30px;
  padding-right:0;
  padding-left:5px;
  line-height:inherit; }
  .bp3-tag-input > *{
    -webkit-box-flex:0;
        -ms-flex-positive:0;
            flex-grow:0;
    -ms-flex-negative:0;
        flex-shrink:0; }
  .bp3-tag-input > .bp3-tag-input-values{
    -webkit-box-flex:1;
        -ms-flex-positive:1;
            flex-grow:1;
    -ms-flex-negative:1;
        flex-shrink:1; }
  .bp3-tag-input .bp3-tag-input-icon{
    margin-top:7px;
    margin-right:7px;
    margin-left:2px;
    color:#5c7080; }
  .bp3-tag-input .bp3-tag-input-values{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-orient:horizontal;
    -webkit-box-direction:normal;
        -ms-flex-direction:row;
            flex-direction:row;
    -ms-flex-wrap:wrap;
        flex-wrap:wrap;
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center;
    -ms-flex-item-align:stretch;
        align-self:stretch;
    margin-top:5px;
    margin-right:7px;
    min-width:0; }
    .bp3-tag-input .bp3-tag-input-values > *{
      -webkit-box-flex:0;
          -ms-flex-positive:0;
              flex-grow:0;
      -ms-flex-negative:0;
          flex-shrink:0; }
    .bp3-tag-input .bp3-tag-input-values > .bp3-fill{
      -webkit-box-flex:1;
          -ms-flex-positive:1;
              flex-grow:1;
      -ms-flex-negative:1;
          flex-shrink:1; }
    .bp3-tag-input .bp3-tag-input-values::before,
    .bp3-tag-input .bp3-tag-input-values > *{
      margin-right:5px; }
    .bp3-tag-input .bp3-tag-input-values:empty::before,
    .bp3-tag-input .bp3-tag-input-values > :last-child{
      margin-right:0; }
    .bp3-tag-input .bp3-tag-input-values:first-child .bp3-input-ghost:first-child{
      padding-left:5px; }
    .bp3-tag-input .bp3-tag-input-values > *{
      margin-bottom:5px; }
  .bp3-tag-input .bp3-tag{
    overflow-wrap:break-word; }
    .bp3-tag-input .bp3-tag.bp3-active{
      outline:rgba(19, 124, 189, 0.6) auto 2px;
      outline-offset:0;
      -moz-outline-radius:6px; }
  .bp3-tag-input .bp3-input-ghost{
    -webkit-box-flex:1;
        -ms-flex:1 1 auto;
            flex:1 1 auto;
    width:80px;
    line-height:20px; }
    .bp3-tag-input .bp3-input-ghost:disabled, .bp3-tag-input .bp3-input-ghost.bp3-disabled{
      cursor:not-allowed; }
  .bp3-tag-input .bp3-button,
  .bp3-tag-input .bp3-spinner{
    margin:3px;
    margin-left:0; }
  .bp3-tag-input .bp3-button{
    min-width:24px;
    min-height:24px;
    padding:0 7px; }
  .bp3-tag-input.bp3-large{
    height:auto;
    min-height:40px; }
    .bp3-tag-input.bp3-large::before,
    .bp3-tag-input.bp3-large > *{
      margin-right:10px; }
    .bp3-tag-input.bp3-large:empty::before,
    .bp3-tag-input.bp3-large > :last-child{
      margin-right:0; }
    .bp3-tag-input.bp3-large .bp3-tag-input-icon{
      margin-top:10px;
      margin-left:5px; }
    .bp3-tag-input.bp3-large .bp3-input-ghost{
      line-height:30px; }
    .bp3-tag-input.bp3-large .bp3-button{
      min-width:30px;
      min-height:30px;
      padding:5px 10px;
      margin:5px;
      margin-left:0; }
    .bp3-tag-input.bp3-large .bp3-spinner{
      margin:8px;
      margin-left:0; }
  .bp3-tag-input.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
    background-color:#ffffff; }
    .bp3-tag-input.bp3-active.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-success{
      -webkit-box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
    .bp3-tag-input.bp3-active.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2);
              box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.2); }
  .bp3-dark .bp3-tag-input .bp3-tag-input-icon, .bp3-tag-input.bp3-dark .bp3-tag-input-icon{
    color:#a7b6c2; }
  .bp3-dark .bp3-tag-input .bp3-input-ghost, .bp3-tag-input.bp3-dark .bp3-input-ghost{
    color:#f5f8fa; }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-webkit-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-webkit-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-moz-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-moz-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost:-ms-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost:-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::-ms-input-placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::-ms-input-placeholder{
      color:rgba(167, 182, 194, 0.6); }
    .bp3-dark .bp3-tag-input .bp3-input-ghost::placeholder, .bp3-tag-input.bp3-dark .bp3-input-ghost::placeholder{
      color:rgba(167, 182, 194, 0.6); }
  .bp3-dark .bp3-tag-input.bp3-active, .bp3-tag-input.bp3-dark.bp3-active{
    -webkit-box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px #137cbd, 0 0 0 1px #137cbd, 0 0 0 3px rgba(19, 124, 189, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
    background-color:rgba(16, 22, 26, 0.3); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-primary, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-primary{
      -webkit-box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #106ba3, 0 0 0 3px rgba(16, 107, 163, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-success, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-success{
      -webkit-box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #0d8050, 0 0 0 3px rgba(13, 128, 80, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-warning, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-warning{
      -webkit-box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #bf7326, 0 0 0 3px rgba(191, 115, 38, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }
    .bp3-dark .bp3-tag-input.bp3-active.bp3-intent-danger, .bp3-tag-input.bp3-dark.bp3-active.bp3-intent-danger{
      -webkit-box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4);
              box-shadow:0 0 0 1px #c23030, 0 0 0 3px rgba(194, 48, 48, 0.3), inset 0 0 0 1px rgba(16, 22, 26, 0.3), inset 0 1px 1px rgba(16, 22, 26, 0.4); }

.bp3-input-ghost{
  border:none;
  -webkit-box-shadow:none;
          box-shadow:none;
  background:none;
  padding:0; }
  .bp3-input-ghost::-webkit-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost::-moz-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost:-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost::-ms-input-placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost::placeholder{
    opacity:1;
    color:rgba(92, 112, 128, 0.6); }
  .bp3-input-ghost:focus{
    outline:none !important; }
.bp3-toast{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:start;
      -ms-flex-align:start;
          align-items:flex-start;
  position:relative !important;
  margin:20px 0 0;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  background-color:#ffffff;
  min-width:300px;
  max-width:500px;
  pointer-events:all; }
  .bp3-toast.bp3-toast-enter, .bp3-toast.bp3-toast-appear{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px); }
  .bp3-toast.bp3-toast-enter-active, .bp3-toast.bp3-toast-appear-active{
    -webkit-transform:translateY(0);
            transform:translateY(0);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-toast.bp3-toast-enter ~ .bp3-toast, .bp3-toast.bp3-toast-appear ~ .bp3-toast{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px); }
  .bp3-toast.bp3-toast-enter-active ~ .bp3-toast, .bp3-toast.bp3-toast-appear-active ~ .bp3-toast{
    -webkit-transform:translateY(0);
            transform:translateY(0);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
            transition-timing-function:cubic-bezier(0.54, 1.12, 0.38, 1.11);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-toast.bp3-toast-exit{
    opacity:1;
    -webkit-filter:blur(0);
            filter:blur(0); }
  .bp3-toast.bp3-toast-exit-active{
    opacity:0;
    -webkit-filter:blur(10px);
            filter:blur(10px);
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:opacity, filter;
    transition-property:opacity, filter, -webkit-filter;
    -webkit-transition-duration:300ms;
            transition-duration:300ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-toast.bp3-toast-exit ~ .bp3-toast{
    -webkit-transform:translateY(0);
            transform:translateY(0); }
  .bp3-toast.bp3-toast-exit-active ~ .bp3-toast{
    -webkit-transform:translateY(-40px);
            transform:translateY(-40px);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:50ms;
            transition-delay:50ms; }
  .bp3-toast .bp3-button-group{
    -webkit-box-flex:0;
        -ms-flex:0 0 auto;
            flex:0 0 auto;
    padding:5px;
    padding-left:0; }
  .bp3-toast > .bp3-icon{
    margin:12px;
    margin-right:0;
    color:#5c7080; }
  .bp3-toast.bp3-dark,
  .bp3-dark .bp3-toast{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
    background-color:#394b59; }
    .bp3-toast.bp3-dark > .bp3-icon,
    .bp3-dark .bp3-toast > .bp3-icon{
      color:#a7b6c2; }
  .bp3-toast[class*="bp3-intent-"] a{
    color:rgba(255, 255, 255, 0.7); }
    .bp3-toast[class*="bp3-intent-"] a:hover{
      color:#ffffff; }
  .bp3-toast[class*="bp3-intent-"] > .bp3-icon{
    color:#ffffff; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button, .bp3-toast[class*="bp3-intent-"] .bp3-button::before,
  .bp3-toast[class*="bp3-intent-"] .bp3-button .bp3-icon, .bp3-toast[class*="bp3-intent-"] .bp3-button:active{
    color:rgba(255, 255, 255, 0.7) !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:focus{
    outline-color:rgba(255, 255, 255, 0.5); }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:hover{
    background-color:rgba(255, 255, 255, 0.15) !important;
    color:#ffffff !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button:active{
    background-color:rgba(255, 255, 255, 0.3) !important;
    color:#ffffff !important; }
  .bp3-toast[class*="bp3-intent-"] .bp3-button::after{
    background:rgba(255, 255, 255, 0.3) !important; }
  .bp3-toast.bp3-intent-primary{
    background-color:#137cbd;
    color:#ffffff; }
  .bp3-toast.bp3-intent-success{
    background-color:#0f9960;
    color:#ffffff; }
  .bp3-toast.bp3-intent-warning{
    background-color:#d9822b;
    color:#ffffff; }
  .bp3-toast.bp3-intent-danger{
    background-color:#db3737;
    color:#ffffff; }

.bp3-toast-message{
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  padding:11px;
  word-break:break-word; }

.bp3-toast-container{
  display:-webkit-box !important;
  display:-ms-flexbox !important;
  display:flex !important;
  -webkit-box-orient:vertical;
  -webkit-box-direction:normal;
      -ms-flex-direction:column;
          flex-direction:column;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  position:fixed;
  right:0;
  left:0;
  z-index:40;
  overflow:hidden;
  padding:0 20px 20px;
  pointer-events:none; }
  .bp3-toast-container.bp3-toast-container-top{
    top:0;
    bottom:auto; }
  .bp3-toast-container.bp3-toast-container-bottom{
    -webkit-box-orient:vertical;
    -webkit-box-direction:reverse;
        -ms-flex-direction:column-reverse;
            flex-direction:column-reverse;
    top:auto;
    bottom:0; }
  .bp3-toast-container.bp3-toast-container-left{
    -webkit-box-align:start;
        -ms-flex-align:start;
            align-items:flex-start; }
  .bp3-toast-container.bp3-toast-container-right{
    -webkit-box-align:end;
        -ms-flex-align:end;
            align-items:flex-end; }

.bp3-toast-container-bottom .bp3-toast.bp3-toast-enter:not(.bp3-toast-enter-active),
.bp3-toast-container-bottom .bp3-toast.bp3-toast-enter:not(.bp3-toast-enter-active) ~ .bp3-toast, .bp3-toast-container-bottom .bp3-toast.bp3-toast-appear:not(.bp3-toast-appear-active),
.bp3-toast-container-bottom .bp3-toast.bp3-toast-appear:not(.bp3-toast-appear-active) ~ .bp3-toast,
.bp3-toast-container-bottom .bp3-toast.bp3-toast-leave-active ~ .bp3-toast{
  -webkit-transform:translateY(60px);
          transform:translateY(60px); }
.bp3-tooltip{
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 2px 4px rgba(16, 22, 26, 0.2), 0 8px 24px rgba(16, 22, 26, 0.2);
  -webkit-transform:scale(1);
          transform:scale(1); }
  .bp3-tooltip .bp3-popover-arrow{
    position:absolute;
    width:22px;
    height:22px; }
    .bp3-tooltip .bp3-popover-arrow::before{
      margin:4px;
      width:14px;
      height:14px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip{
    margin-top:-11px;
    margin-bottom:11px; }
    .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow{
      bottom:-8px; }
      .bp3-tether-element-attached-bottom.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(-90deg);
                transform:rotate(-90deg); }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip{
    margin-left:11px; }
    .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow{
      left:-8px; }
      .bp3-tether-element-attached-left.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(0);
                transform:rotate(0); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip{
    margin-top:11px; }
    .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow{
      top:-8px; }
      .bp3-tether-element-attached-top.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(90deg);
                transform:rotate(90deg); }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip{
    margin-right:11px;
    margin-left:-11px; }
    .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow{
      right:-8px; }
      .bp3-tether-element-attached-right.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow svg{
        -webkit-transform:rotate(180deg);
                transform:rotate(180deg); }
  .bp3-tether-element-attached-middle > .bp3-tooltip > .bp3-popover-arrow{
    top:50%;
    -webkit-transform:translateY(-50%);
            transform:translateY(-50%); }
  .bp3-tether-element-attached-center > .bp3-tooltip > .bp3-popover-arrow{
    right:50%;
    -webkit-transform:translateX(50%);
            transform:translateX(50%); }
  .bp3-tether-element-attached-top.bp3-tether-target-attached-top > .bp3-tooltip > .bp3-popover-arrow{
    top:-0.22183px; }
  .bp3-tether-element-attached-right.bp3-tether-target-attached-right > .bp3-tooltip > .bp3-popover-arrow{
    right:-0.22183px; }
  .bp3-tether-element-attached-left.bp3-tether-target-attached-left > .bp3-tooltip > .bp3-popover-arrow{
    left:-0.22183px; }
  .bp3-tether-element-attached-bottom.bp3-tether-target-attached-bottom > .bp3-tooltip > .bp3-popover-arrow{
    bottom:-0.22183px; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:top left;
            transform-origin:top left; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:top center;
            transform-origin:top center; }
  .bp3-tether-element-attached-top.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:top right;
            transform-origin:top right; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:center left;
            transform-origin:center left; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:center center;
            transform-origin:center center; }
  .bp3-tether-element-attached-middle.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:center right;
            transform-origin:center right; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-left > .bp3-tooltip{
    -webkit-transform-origin:bottom left;
            transform-origin:bottom left; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-center > .bp3-tooltip{
    -webkit-transform-origin:bottom center;
            transform-origin:bottom center; }
  .bp3-tether-element-attached-bottom.bp3-tether-element-attached-right > .bp3-tooltip{
    -webkit-transform-origin:bottom right;
            transform-origin:bottom right; }
  .bp3-tooltip .bp3-popover-content{
    background:#394b59;
    color:#f5f8fa; }
  .bp3-tooltip .bp3-popover-arrow::before{
    -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2);
            box-shadow:1px 1px 6px rgba(16, 22, 26, 0.2); }
  .bp3-tooltip .bp3-popover-arrow-border{
    fill:#10161a;
    fill-opacity:0.1; }
  .bp3-tooltip .bp3-popover-arrow-fill{
    fill:#394b59; }
  .bp3-popover-enter > .bp3-tooltip, .bp3-popover-appear > .bp3-tooltip{
    -webkit-transform:scale(0.8);
            transform:scale(0.8); }
  .bp3-popover-enter-active > .bp3-tooltip, .bp3-popover-appear-active > .bp3-tooltip{
    -webkit-transform:scale(1);
            transform:scale(1);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-popover-exit > .bp3-tooltip{
    -webkit-transform:scale(1);
            transform:scale(1); }
  .bp3-popover-exit-active > .bp3-tooltip{
    -webkit-transform:scale(0.8);
            transform:scale(0.8);
    -webkit-transition-property:-webkit-transform;
    transition-property:-webkit-transform;
    transition-property:transform;
    transition-property:transform, -webkit-transform;
    -webkit-transition-duration:100ms;
            transition-duration:100ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-tooltip .bp3-popover-content{
    padding:10px 12px; }
  .bp3-tooltip.bp3-dark,
  .bp3-dark .bp3-tooltip{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 2px 4px rgba(16, 22, 26, 0.4), 0 8px 24px rgba(16, 22, 26, 0.4); }
    .bp3-tooltip.bp3-dark .bp3-popover-content,
    .bp3-dark .bp3-tooltip .bp3-popover-content{
      background:#e1e8ed;
      color:#394b59; }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow::before,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow::before{
      -webkit-box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4);
              box-shadow:1px 1px 6px rgba(16, 22, 26, 0.4); }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow-border,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow-border{
      fill:#10161a;
      fill-opacity:0.2; }
    .bp3-tooltip.bp3-dark .bp3-popover-arrow-fill,
    .bp3-dark .bp3-tooltip .bp3-popover-arrow-fill{
      fill:#e1e8ed; }
  .bp3-tooltip.bp3-intent-primary .bp3-popover-content{
    background:#137cbd;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-primary .bp3-popover-arrow-fill{
    fill:#137cbd; }
  .bp3-tooltip.bp3-intent-success .bp3-popover-content{
    background:#0f9960;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-success .bp3-popover-arrow-fill{
    fill:#0f9960; }
  .bp3-tooltip.bp3-intent-warning .bp3-popover-content{
    background:#d9822b;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-warning .bp3-popover-arrow-fill{
    fill:#d9822b; }
  .bp3-tooltip.bp3-intent-danger .bp3-popover-content{
    background:#db3737;
    color:#ffffff; }
  .bp3-tooltip.bp3-intent-danger .bp3-popover-arrow-fill{
    fill:#db3737; }

.bp3-tooltip-indicator{
  border-bottom:dotted 1px;
  cursor:help; }
.bp3-tree .bp3-icon, .bp3-tree .bp3-icon-standard, .bp3-tree .bp3-icon-large{
  color:#5c7080; }
  .bp3-tree .bp3-icon.bp3-intent-primary, .bp3-tree .bp3-icon-standard.bp3-intent-primary, .bp3-tree .bp3-icon-large.bp3-intent-primary{
    color:#137cbd; }
  .bp3-tree .bp3-icon.bp3-intent-success, .bp3-tree .bp3-icon-standard.bp3-intent-success, .bp3-tree .bp3-icon-large.bp3-intent-success{
    color:#0f9960; }
  .bp3-tree .bp3-icon.bp3-intent-warning, .bp3-tree .bp3-icon-standard.bp3-intent-warning, .bp3-tree .bp3-icon-large.bp3-intent-warning{
    color:#d9822b; }
  .bp3-tree .bp3-icon.bp3-intent-danger, .bp3-tree .bp3-icon-standard.bp3-intent-danger, .bp3-tree .bp3-icon-large.bp3-intent-danger{
    color:#db3737; }

.bp3-tree-node-list{
  margin:0;
  padding-left:0;
  list-style:none; }

.bp3-tree-root{
  position:relative;
  background-color:transparent;
  cursor:default;
  padding-left:0; }

.bp3-tree-node-content-0{
  padding-left:0px; }

.bp3-tree-node-content-1{
  padding-left:23px; }

.bp3-tree-node-content-2{
  padding-left:46px; }

.bp3-tree-node-content-3{
  padding-left:69px; }

.bp3-tree-node-content-4{
  padding-left:92px; }

.bp3-tree-node-content-5{
  padding-left:115px; }

.bp3-tree-node-content-6{
  padding-left:138px; }

.bp3-tree-node-content-7{
  padding-left:161px; }

.bp3-tree-node-content-8{
  padding-left:184px; }

.bp3-tree-node-content-9{
  padding-left:207px; }

.bp3-tree-node-content-10{
  padding-left:230px; }

.bp3-tree-node-content-11{
  padding-left:253px; }

.bp3-tree-node-content-12{
  padding-left:276px; }

.bp3-tree-node-content-13{
  padding-left:299px; }

.bp3-tree-node-content-14{
  padding-left:322px; }

.bp3-tree-node-content-15{
  padding-left:345px; }

.bp3-tree-node-content-16{
  padding-left:368px; }

.bp3-tree-node-content-17{
  padding-left:391px; }

.bp3-tree-node-content-18{
  padding-left:414px; }

.bp3-tree-node-content-19{
  padding-left:437px; }

.bp3-tree-node-content-20{
  padding-left:460px; }

.bp3-tree-node-content{
  display:-webkit-box;
  display:-ms-flexbox;
  display:flex;
  -webkit-box-align:center;
      -ms-flex-align:center;
          align-items:center;
  width:100%;
  height:30px;
  padding-right:5px; }
  .bp3-tree-node-content:hover{
    background-color:rgba(191, 204, 214, 0.4); }

.bp3-tree-node-caret,
.bp3-tree-node-caret-none{
  min-width:30px; }

.bp3-tree-node-caret{
  color:#5c7080;
  -webkit-transform:rotate(0deg);
          transform:rotate(0deg);
  cursor:pointer;
  padding:7px;
  -webkit-transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:-webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9);
  transition:transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9), -webkit-transform 200ms cubic-bezier(0.4, 1, 0.75, 0.9); }
  .bp3-tree-node-caret:hover{
    color:#182026; }
  .bp3-dark .bp3-tree-node-caret{
    color:#a7b6c2; }
    .bp3-dark .bp3-tree-node-caret:hover{
      color:#f5f8fa; }
  .bp3-tree-node-caret.bp3-tree-node-caret-open{
    -webkit-transform:rotate(90deg);
            transform:rotate(90deg); }
  .bp3-tree-node-caret.bp3-icon-standard::before{
    content:""; }

.bp3-tree-node-icon{
  position:relative;
  margin-right:7px; }

.bp3-tree-node-label{
  overflow:hidden;
  text-overflow:ellipsis;
  white-space:nowrap;
  word-wrap:normal;
  -webkit-box-flex:1;
      -ms-flex:1 1 auto;
          flex:1 1 auto;
  position:relative;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-tree-node-label span{
    display:inline; }

.bp3-tree-node-secondary-label{
  padding:0 5px;
  -webkit-user-select:none;
     -moz-user-select:none;
      -ms-user-select:none;
          user-select:none; }
  .bp3-tree-node-secondary-label .bp3-popover-wrapper,
  .bp3-tree-node-secondary-label .bp3-popover-target{
    display:-webkit-box;
    display:-ms-flexbox;
    display:flex;
    -webkit-box-align:center;
        -ms-flex-align:center;
            align-items:center; }

.bp3-tree-node.bp3-disabled .bp3-tree-node-content{
  background-color:inherit;
  cursor:not-allowed;
  color:rgba(92, 112, 128, 0.6); }

.bp3-tree-node.bp3-disabled .bp3-tree-node-caret,
.bp3-tree-node.bp3-disabled .bp3-tree-node-icon{
  cursor:not-allowed;
  color:rgba(92, 112, 128, 0.6); }

.bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content{
  background-color:#137cbd; }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content,
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon, .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon-standard, .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-icon-large{
    color:#ffffff; }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-tree-node-caret::before{
    color:rgba(255, 255, 255, 0.7); }
  .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content .bp3-tree-node-caret:hover::before{
    color:#ffffff; }

.bp3-dark .bp3-tree-node-content:hover{
  background-color:rgba(92, 112, 128, 0.3); }

.bp3-dark .bp3-tree .bp3-icon, .bp3-dark .bp3-tree .bp3-icon-standard, .bp3-dark .bp3-tree .bp3-icon-large{
  color:#a7b6c2; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-primary, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-primary, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-primary{
    color:#137cbd; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-success, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-success, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-success{
    color:#0f9960; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-warning, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-warning, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-warning{
    color:#d9822b; }
  .bp3-dark .bp3-tree .bp3-icon.bp3-intent-danger, .bp3-dark .bp3-tree .bp3-icon-standard.bp3-intent-danger, .bp3-dark .bp3-tree .bp3-icon-large.bp3-intent-danger{
    color:#db3737; }

.bp3-dark .bp3-tree-node.bp3-tree-node-selected > .bp3-tree-node-content{
  background-color:#137cbd; }
/*!

Copyright 2017-present Palantir Technologies, Inc. All rights reserved.
Licensed under the Apache License, Version 2.0.

*/
.bp3-omnibar{
  -webkit-filter:blur(0);
          filter:blur(0);
  opacity:1;
  top:20vh;
  left:calc(50% - 250px);
  z-index:21;
  border-radius:3px;
  -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
          box-shadow:0 0 0 1px rgba(16, 22, 26, 0.1), 0 4px 8px rgba(16, 22, 26, 0.2), 0 18px 46px 6px rgba(16, 22, 26, 0.2);
  background-color:#ffffff;
  width:500px; }
  .bp3-omnibar.bp3-overlay-enter, .bp3-omnibar.bp3-overlay-appear{
    -webkit-filter:blur(20px);
            filter:blur(20px);
    opacity:0.2; }
  .bp3-omnibar.bp3-overlay-enter-active, .bp3-omnibar.bp3-overlay-appear-active{
    -webkit-filter:blur(0);
            filter:blur(0);
    opacity:1;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:filter, opacity;
    transition-property:filter, opacity, -webkit-filter;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-omnibar.bp3-overlay-exit{
    -webkit-filter:blur(0);
            filter:blur(0);
    opacity:1; }
  .bp3-omnibar.bp3-overlay-exit-active{
    -webkit-filter:blur(20px);
            filter:blur(20px);
    opacity:0.2;
    -webkit-transition-property:opacity, -webkit-filter;
    transition-property:opacity, -webkit-filter;
    transition-property:filter, opacity;
    transition-property:filter, opacity, -webkit-filter;
    -webkit-transition-duration:200ms;
            transition-duration:200ms;
    -webkit-transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
            transition-timing-function:cubic-bezier(0.4, 1, 0.75, 0.9);
    -webkit-transition-delay:0;
            transition-delay:0; }
  .bp3-omnibar .bp3-input{
    border-radius:0;
    background-color:transparent; }
    .bp3-omnibar .bp3-input, .bp3-omnibar .bp3-input:focus{
      -webkit-box-shadow:none;
              box-shadow:none; }
  .bp3-omnibar .bp3-menu{
    border-radius:0;
    -webkit-box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
            box-shadow:inset 0 1px 0 rgba(16, 22, 26, 0.15);
    background-color:transparent;
    max-height:calc(60vh - 40px);
    overflow:auto; }
    .bp3-omnibar .bp3-menu:empty{
      display:none; }
  .bp3-dark .bp3-omnibar, .bp3-omnibar.bp3-dark{
    -webkit-box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
            box-shadow:0 0 0 1px rgba(16, 22, 26, 0.2), 0 4px 8px rgba(16, 22, 26, 0.4), 0 18px 46px 6px rgba(16, 22, 26, 0.4);
    background-color:#30404d; }

.bp3-omnibar-overlay .bp3-overlay-backdrop{
  background-color:rgba(16, 22, 26, 0.2); }

.bp3-select-popover .bp3-popover-content{
  padding:5px; }

.bp3-select-popover .bp3-input-group{
  margin-bottom:0; }

.bp3-select-popover .bp3-menu{
  max-width:400px;
  max-height:300px;
  overflow:auto;
  padding:0; }
  .bp3-select-popover .bp3-menu:not(:first-child){
    padding-top:5px; }

.bp3-multi-select{
  min-width:150px; }

.bp3-multi-select-popover .bp3-menu{
  max-width:400px;
  max-height:300px;
  overflow:auto; }

.bp3-select-popover .bp3-popover-content{
  padding:5px; }

.bp3-select-popover .bp3-input-group{
  margin-bottom:0; }

.bp3-select-popover .bp3-menu{
  max-width:400px;
  max-height:300px;
  overflow:auto;
  padding:0; }
  .bp3-select-popover .bp3-menu:not(:first-child){
    padding-top:5px; }
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
  --jp-icon-add: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDEzaC02djZoLTJ2LTZINXYtMmg2VjVoMnY2aDZ2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-bug: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwIDhoLTIuODFjLS40NS0uNzgtMS4wNy0xLjQ1LTEuODItMS45NkwxNyA0LjQxIDE1LjU5IDNsLTIuMTcgMi4xN0MxMi45NiA1LjA2IDEyLjQ5IDUgMTIgNWMtLjQ5IDAtLjk2LjA2LTEuNDEuMTdMOC40MSAzIDcgNC40MWwxLjYyIDEuNjNDNy44OCA2LjU1IDcuMjYgNy4yMiA2LjgxIDhINHYyaDIuMDljLS4wNS4zMy0uMDkuNjYtLjA5IDF2MUg0djJoMnYxYzAgLjM0LjA0LjY3LjA5IDFINHYyaDIuODFjMS4wNCAxLjc5IDIuOTcgMyA1LjE5IDNzNC4xNS0xLjIxIDUuMTktM0gyMHYtMmgtMi4wOWMuMDUtLjMzLjA5LS42Ni4wOS0xdi0xaDJ2LTJoLTJ2LTFjMC0uMzQtLjA0LS42Ny0uMDktMUgyMFY4em0tNiA4aC00di0yaDR2MnptMC00aC00di0yaDR2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-build: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTYiIHZpZXdCb3g9IjAgMCAyNCAyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE0LjkgMTcuNDVDMTYuMjUgMTcuNDUgMTcuMzUgMTYuMzUgMTcuMzUgMTVDMTcuMzUgMTMuNjUgMTYuMjUgMTIuNTUgMTQuOSAxMi41NUMxMy41NCAxMi41NSAxMi40NSAxMy42NSAxMi40NSAxNUMxMi40NSAxNi4zNSAxMy41NCAxNy40NSAxNC45IDE3LjQ1Wk0yMC4xIDE1LjY4TDIxLjU4IDE2Ljg0QzIxLjcxIDE2Ljk1IDIxLjc1IDE3LjEzIDIxLjY2IDE3LjI5TDIwLjI2IDE5LjcxQzIwLjE3IDE5Ljg2IDIwIDE5LjkyIDE5LjgzIDE5Ljg2TDE4LjA5IDE5LjE2QzE3LjczIDE5LjQ0IDE3LjMzIDE5LjY3IDE2LjkxIDE5Ljg1TDE2LjY0IDIxLjdDMTYuNjIgMjEuODcgMTYuNDcgMjIgMTYuMyAyMkgxMy41QzEzLjMyIDIyIDEzLjE4IDIxLjg3IDEzLjE1IDIxLjdMMTIuODkgMTkuODVDMTIuNDYgMTkuNjcgMTIuMDcgMTkuNDQgMTEuNzEgMTkuMTZMOS45NjAwMiAxOS44NkM5LjgxMDAyIDE5LjkyIDkuNjIwMDIgMTkuODYgOS41NDAwMiAxOS43MUw4LjE0MDAyIDE3LjI5QzguMDUwMDIgMTcuMTMgOC4wOTAwMiAxNi45NSA4LjIyMDAyIDE2Ljg0TDkuNzAwMDIgMTUuNjhMOS42NTAwMSAxNUw5LjcwMDAyIDE0LjMxTDguMjIwMDIgMTMuMTZDOC4wOTAwMiAxMy4wNSA4LjA1MDAyIDEyLjg2IDguMTQwMDIgMTIuNzFMOS41NDAwMiAxMC4yOUM5LjYyMDAyIDEwLjEzIDkuODEwMDIgMTAuMDcgOS45NjAwMiAxMC4xM0wxMS43MSAxMC44NEMxMi4wNyAxMC41NiAxMi40NiAxMC4zMiAxMi44OSAxMC4xNUwxMy4xNSA4LjI4OTk4QzEzLjE4IDguMTI5OTggMTMuMzIgNy45OTk5OCAxMy41IDcuOTk5OThIMTYuM0MxNi40NyA3Ljk5OTk4IDE2LjYyIDguMTI5OTggMTYuNjQgOC4yODk5OEwxNi45MSAxMC4xNUMxNy4zMyAxMC4zMiAxNy43MyAxMC41NiAxOC4wOSAxMC44NEwxOS44MyAxMC4xM0MyMCAxMC4wNyAyMC4xNyAxMC4xMyAyMC4yNiAxMC4yOUwyMS42NiAxMi43MUMyMS43NSAxMi44NiAyMS43MSAxMy4wNSAyMS41OCAxMy4xNkwyMC4xIDE0LjMxTDIwLjE1IDE1TDIwLjEgMTUuNjhaIi8+CiAgICA8cGF0aCBkPSJNNy4zMjk2NiA3LjQ0NDU0QzguMDgzMSA3LjAwOTU0IDguMzM5MzIgNi4wNTMzMiA3LjkwNDMyIDUuMjk5ODhDNy40NjkzMiA0LjU0NjQzIDYuNTA4MSA0LjI4MTU2IDUuNzU0NjYgNC43MTY1NkM1LjM5MTc2IDQuOTI2MDggNS4xMjY5NSA1LjI3MTE4IDUuMDE4NDkgNS42NzU5NEM0LjkxMDA0IDYuMDgwNzEgNC45NjY4MiA2LjUxMTk4IDUuMTc2MzQgNi44NzQ4OEM1LjYxMTM0IDcuNjI4MzIgNi41NzYyMiA3Ljg3OTU0IDcuMzI5NjYgNy40NDQ1NFpNOS42NTcxOCA0Ljc5NTkzTDEwLjg2NzIgNC45NTE3OUMxMC45NjI4IDQuOTc3NDEgMTEuMDQwMiA1LjA3MTMzIDExLjAzODIgNS4xODc5M0wxMS4wMzg4IDYuOTg4OTNDMTEuMDQ1NSA3LjEwMDU0IDEwLjk2MTYgNy4xOTUxOCAxMC44NTUgNy4yMTA1NEw5LjY2MDAxIDcuMzgwODNMOS4yMzkxNSA4LjEzMTg4TDkuNjY5NjEgOS4yNTc0NUM5LjcwNzI5IDkuMzYyNzEgOS42NjkzNCA5LjQ3Njk5IDkuNTc0MDggOS41MzE5OUw4LjAxNTIzIDEwLjQzMkM3LjkxMTMxIDEwLjQ5MiA3Ljc5MzM3IDEwLjQ2NzcgNy43MjEwNSAxMC4zODI0TDYuOTg3NDggOS40MzE4OEw2LjEwOTMxIDkuNDMwODNMNS4zNDcwNCAxMC4zOTA1QzUuMjg5MDkgMTAuNDcwMiA1LjE3MzgzIDEwLjQ5MDUgNS4wNzE4NyAxMC40MzM5TDMuNTEyNDUgOS41MzI5M0MzLjQxMDQ5IDkuNDc2MzMgMy4zNzY0NyA5LjM1NzQxIDMuNDEwNzUgOS4yNTY3OUwzLjg2MzQ3IDguMTQwOTNMMy42MTc0OSA3Ljc3NDg4TDMuNDIzNDcgNy4zNzg4M0wyLjIzMDc1IDcuMjEyOTdDMi4xMjY0NyA3LjE5MjM1IDIuMDQwNDkgNy4xMDM0MiAyLjA0MjQ1IDYuOTg2ODJMMi4wNDE4NyA1LjE4NTgyQzIuMDQzODMgNS4wNjkyMiAyLjExOTA5IDQuOTc5NTggMi4yMTcwNCA0Ljk2OTIyTDMuNDIwNjUgNC43OTM5M0wzLjg2NzQ5IDQuMDI3ODhMMy40MTEwNSAyLjkxNzMxQzMuMzczMzcgMi44MTIwNCAzLjQxMTMxIDIuNjk3NzYgMy41MTUyMyAyLjYzNzc2TDUuMDc0MDggMS43Mzc3NkM1LjE2OTM0IDEuNjgyNzYgNS4yODcyOSAxLjcwNzA0IDUuMzU5NjEgMS43OTIzMUw2LjExOTE1IDIuNzI3ODhMNi45ODAwMSAyLjczODkzTDcuNzI0OTYgMS43ODkyMkM3Ljc5MTU2IDEuNzA0NTggNy45MTU0OCAxLjY3OTIyIDguMDA4NzkgMS43NDA4Mkw5LjU2ODIxIDIuNjQxODJDOS42NzAxNyAyLjY5ODQyIDkuNzEyODUgMi44MTIzNCA5LjY4NzIzIDIuOTA3OTdMOS4yMTcxOCA0LjAzMzgzTDkuNDYzMTYgNC4zOTk4OEw5LjY1NzE4IDQuNzk1OTNaIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iOS45LDEzLjYgMy42LDcuNCA0LjQsNi42IDkuOSwxMi4yIDE1LjQsNi43IDE2LjEsNy40ICIvPgoJPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNS45TDksOS43bDMuOC0zLjhsMS4yLDEuMmwtNC45LDVsLTQuOS01TDUuMiw1Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-caret-down: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik01LjIsNy41TDksMTEuMmwzLjgtMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-left: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik0xMC44LDEyLjhMNy4xLDlsMy44LTMuOGwwLDcuNkgxMC44eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-right: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiIHNoYXBlLXJlbmRlcmluZz0iZ2VvbWV0cmljUHJlY2lzaW9uIj4KICAgIDxwYXRoIGQ9Ik03LjIsNS4yTDEwLjksOWwtMy44LDMuOFY1LjJINy4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-caret-up-empty-thin: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwb2x5Z29uIGNsYXNzPSJzdDEiIHBvaW50cz0iMTUuNCwxMy4zIDkuOSw3LjcgNC40LDEzLjIgMy42LDEyLjUgOS45LDYuMyAxNi4xLDEyLjYgIi8+Cgk8L2c+Cjwvc3ZnPgo=);
  --jp-icon-caret-up: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KCTxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSIgc2hhcGUtcmVuZGVyaW5nPSJnZW9tZXRyaWNQcmVjaXNpb24iPgoJCTxwYXRoIGQ9Ik01LjIsMTAuNUw5LDYuOGwzLjgsMy44SDUuMnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-case-sensitive: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgogIDxnIGNsYXNzPSJqcC1pY29uLWFjY2VudDIiIGZpbGw9IiNGRkYiPgogICAgPHBhdGggZD0iTTcuNiw4aDAuOWwzLjUsOGgtMS4xTDEwLDE0SDZsLTAuOSwySDRMNy42LDh6IE04LDkuMUw2LjQsMTNoMy4yTDgsOS4xeiIvPgogICAgPHBhdGggZD0iTTE2LjYsOS44Yy0wLjIsMC4xLTAuNCwwLjEtMC43LDAuMWMtMC4yLDAtMC40LTAuMS0wLjYtMC4yYy0wLjEtMC4xLTAuMi0wLjQtMC4yLTAuNyBjLTAuMywwLjMtMC42LDAuNS0wLjksMC43Yy0wLjMsMC4xLTAuNywwLjItMS4xLDAuMmMtMC4zLDAtMC41LDAtMC43LTAuMWMtMC4yLTAuMS0wLjQtMC4yLTAuNi0wLjNjLTAuMi0wLjEtMC4zLTAuMy0wLjQtMC41IGMtMC4xLTAuMi0wLjEtMC40LTAuMS0wLjdjMC0wLjMsMC4xLTAuNiwwLjItMC44YzAuMS0wLjIsMC4zLTAuNCwwLjQtMC41QzEyLDcsMTIuMiw2LjksMTIuNSw2LjhjMC4yLTAuMSwwLjUtMC4xLDAuNy0wLjIgYzAuMy0wLjEsMC41LTAuMSwwLjctMC4xYzAuMiwwLDAuNC0wLjEsMC42LTAuMWMwLjIsMCwwLjMtMC4xLDAuNC0wLjJjMC4xLTAuMSwwLjItMC4yLDAuMi0wLjRjMC0xLTEuMS0xLTEuMy0xIGMtMC40LDAtMS40LDAtMS40LDEuMmgtMC45YzAtMC40LDAuMS0wLjcsMC4yLTFjMC4xLTAuMiwwLjMtMC40LDAuNS0wLjZjMC4yLTAuMiwwLjUtMC4zLDAuOC0wLjNDMTMuMyw0LDEzLjYsNCwxMy45LDQgYzAuMywwLDAuNSwwLDAuOCwwLjFjMC4zLDAsMC41LDAuMSwwLjcsMC4yYzAuMiwwLjEsMC40LDAuMywwLjUsMC41QzE2LDUsMTYsNS4yLDE2LDUuNnYyLjljMCwwLjIsMCwwLjQsMCwwLjUgYzAsMC4xLDAuMSwwLjIsMC4zLDAuMmMwLjEsMCwwLjIsMCwwLjMsMFY5Ljh6IE0xNS4yLDYuOWMtMS4yLDAuNi0zLjEsMC4yLTMuMSwxLjRjMCwxLjQsMy4xLDEsMy4xLTAuNVY2Ljl6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-check: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkgMTYuMTdMNC44MyAxMmwtMS40MiAxLjQxTDkgMTkgMjEgN2wtMS40MS0xLjQxeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-circle-empty: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyIDJDNi40NyAyIDIgNi40NyAyIDEyczQuNDcgMTAgMTAgMTAgMTAtNC40NyAxMC0xMFMxNy41MyAyIDEyIDJ6bTAgMThjLTQuNDEgMC04LTMuNTktOC04czMuNTktOCA4LTggOCAzLjU5IDggOC0zLjU5IDgtOCA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-circle: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iOSIgY3k9IjkiIHI9IjgiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-clear: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8bWFzayBpZD0iZG9udXRIb2xlIj4KICAgIDxyZWN0IHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgZmlsbD0id2hpdGUiIC8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSI4IiBmaWxsPSJibGFjayIvPgogIDwvbWFzaz4KCiAgPGcgY2xhc3M9ImpwLWljb24zIiBmaWxsPSIjNjE2MTYxIj4KICAgIDxyZWN0IGhlaWdodD0iMTgiIHdpZHRoPSIyIiB4PSIxMSIgeT0iMyIgdHJhbnNmb3JtPSJyb3RhdGUoMzE1LCAxMiwgMTIpIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIxMCIgbWFzaz0idXJsKCNkb251dEhvbGUpIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-close: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1ub25lIGpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIGpwLWljb24zLWhvdmVyIiBmaWxsPSJub25lIj4KICAgIDxjaXJjbGUgY3g9IjEyIiBjeT0iMTIiIHI9IjExIi8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIGpwLWljb24tYWNjZW50Mi1ob3ZlciIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMTkgNi40MUwxNy41OSA1IDEyIDEwLjU5IDYuNDEgNSA1IDYuNDEgMTAuNTkgMTIgNSAxNy41OSA2LjQxIDE5IDEyIDEzLjQxIDE3LjU5IDE5IDE5IDE3LjU5IDEzLjQxIDEyeiIvPgogIDwvZz4KCiAgPGcgY2xhc3M9ImpwLWljb24tbm9uZSBqcC1pY29uLWJ1c3kiIGZpbGw9Im5vbmUiPgogICAgPGNpcmNsZSBjeD0iMTIiIGN5PSIxMiIgcj0iNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-console: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwMCAyMDAiPgogIDxnIGNsYXNzPSJqcC1pY29uLWJyYW5kMSBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMjg4RDEiPgogICAgPHBhdGggZD0iTTIwIDE5LjhoMTYwdjE1OS45SDIweiIvPgogIDwvZz4KICA8ZyBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNmZmYiPgogICAgPHBhdGggZD0iTTEwNSAxMjcuM2g0MHYxMi44aC00MHpNNTEuMSA3N0w3NCA5OS45bC0yMy4zIDIzLjMgMTAuNSAxMC41IDIzLjMtMjMuM0w5NSA5OS45IDg0LjUgODkuNCA2MS42IDY2LjV6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-copy: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTExLjksMUgzLjJDMi40LDEsMS43LDEuNywxLjcsMi41djEwLjJoMS41VjIuNWg4LjdWMXogTTE0LjEsMy45aC04Yy0wLjgsMC0xLjUsMC43LTEuNSwxLjV2MTAuMmMwLDAuOCwwLjcsMS41LDEuNSwxLjVoOCBjMC44LDAsMS41LTAuNywxLjUtMS41VjUuNEMxNS41LDQuNiwxNC45LDMuOSwxNC4xLDMuOXogTTE0LjEsMTUuNWgtOFY1LjRoOFYxNS41eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-cut: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkuNjQgNy42NGMuMjMtLjUuMzYtMS4wNS4zNi0xLjY0IDAtMi4yMS0xLjc5LTQtNC00UzIgMy43OSAyIDZzMS43OSA0IDQgNGMuNTkgMCAxLjE0LS4xMyAxLjY0LS4zNkwxMCAxMmwtMi4zNiAyLjM2QzcuMTQgMTQuMTMgNi41OSAxNCA2IDE0Yy0yLjIxIDAtNCAxLjc5LTQgNHMxLjc5IDQgNCA0IDQtMS43OSA0LTRjMC0uNTktLjEzLTEuMTQtLjM2LTEuNjRMMTIgMTRsNyA3aDN2LTFMOS42NCA3LjY0ek02IDhjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTAgMTJjLTEuMSAwLTItLjg5LTItMnMuOS0yIDItMiAyIC44OSAyIDItLjkgMi0yIDJ6bTYtNy41Yy0uMjggMC0uNS0uMjItLjUtLjVzLjIyLS41LjUtLjUuNS4yMi41LjUtLjIyLjUtLjUuNXpNMTkgM2wtNiA2IDIgMiA3LTdWM3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-download: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE5IDloLTRWM0g5djZINWw3IDcgNy03ek01IDE4djJoMTR2LTJINXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-edit: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMgMTcuMjVWMjFoMy43NUwxNy44MSA5Ljk0bC0zLjc1LTMuNzVMMyAxNy4yNXpNMjAuNzEgNy4wNGMuMzktLjM5LjM5LTEuMDIgMC0xLjQxbC0yLjM0LTIuMzRjLS4zOS0uMzktMS4wMi0uMzktMS40MSAwbC0xLjgzIDEuODMgMy43NSAzLjc1IDEuODMtMS44M3oiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-ellipses: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPGNpcmNsZSBjeD0iNSIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxMiIgY3k9IjEyIiByPSIyIi8+CiAgICA8Y2lyY2xlIGN4PSIxOSIgY3k9IjEyIiByPSIyIi8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-extension: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwLjUgMTFIMTlWN2MwLTEuMS0uOS0yLTItMmgtNFYzLjVDMTMgMi4xMiAxMS44OCAxIDEwLjUgMVM4IDIuMTIgOCAzLjVWNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAydjMuOEgzLjVjMS40OSAwIDIuNyAxLjIxIDIuNyAyLjdzLTEuMjEgMi43LTIuNyAyLjdIMlYyMGMwIDEuMS45IDIgMiAyaDMuOHYtMS41YzAtMS40OSAxLjIxLTIuNyAyLjctMi43IDEuNDkgMCAyLjcgMS4yMSAyLjcgMi43VjIySDE3YzEuMSAwIDItLjkgMi0ydi00aDEuNWMxLjM4IDAgMi41LTEuMTIgMi41LTIuNVMyMS44OCAxMSAyMC41IDExeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-fast-forward: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTQgMThsOC41LTZMNCA2djEyem05LTEydjEybDguNS02TDEzIDZ6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-file-upload: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTkgMTZoNnYtNmg0bC03LTctNyA3aDR6bS00IDJoMTR2Mkg1eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-file: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuMyA4LjJsLTUuNS01LjVjLS4zLS4zLS43LS41LTEuMi0uNUgzLjljLS44LjEtMS42LjktMS42IDEuOHYxNC4xYzAgLjkuNyAxLjYgMS42IDEuNmgxNC4yYy45IDAgMS42LS43IDEuNi0xLjZWOS40Yy4xLS41LS4xLS45LS40LTEuMnptLTUuOC0zLjNsMy40IDMuNmgtMy40VjQuOXptMy45IDEyLjdINC43Yy0uMSAwLS4yIDAtLjItLjJWNC43YzAtLjIuMS0uMy4yLS4zaDcuMnY0LjRzMCAuOC4zIDEuMWMuMy4zIDEuMS4zIDEuMS4zaDQuM3Y3LjJzLS4xLjItLjIuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-filter-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEwIDE4aDR2LTJoLTR2MnpNMyA2djJoMThWNkgzem0zIDdoMTJ2LTJINnYyeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY4YzAtMS4xLS45LTItMi0yaC04bC0yLTJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-html5: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiMwMDAiIGQ9Ik0xMDguNCAwaDIzdjIyLjhoMjEuMlYwaDIzdjY5aC0yM1Y0NmgtMjF2MjNoLTIzLjJNMjA2IDIzaC0yMC4zVjBoNjMuN3YyM0gyMjl2NDZoLTIzbTUzLjUtNjloMjQuMWwxNC44IDI0LjNMMzEzLjIgMGgyNC4xdjY5aC0yM1YzNC44bC0xNi4xIDI0LjgtMTYuMS0yNC44VjY5aC0yMi42bTg5LjItNjloMjN2NDYuMmgzMi42VjY5aC01NS42Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iI2U0NGQyNiIgZD0iTTEwNy42IDQ3MWwtMzMtMzcwLjRoMzYyLjhsLTMzIDM3MC4yTDI1NS43IDUxMiIvPgogIDxwYXRoIGNsYXNzPSJqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNmMTY1MjkiIGQ9Ik0yNTYgNDgwLjVWMTMxaDE0OC4zTDM3NiA0NDciLz4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNlYmViZWIiIGQ9Ik0xNDIgMTc2LjNoMTE0djQ1LjRoLTY0LjJsNC4yIDQ2LjVoNjB2NDUuM0gxNTQuNG0yIDIyLjhIMjAybDMuMiAzNi4zIDUwLjggMTMuNnY0Ny40bC05My4yLTI2Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tc2VsZWN0YWJsZS1pbnZlcnNlIiBmaWxsPSIjZmZmIiBkPSJNMzY5LjYgMTc2LjNIMjU1Ljh2NDUuNGgxMDkuNm0tNC4xIDQ2LjVIMjU1Ljh2NDUuNGg1NmwtNS4zIDU5LTUwLjcgMTMuNnY0Ny4ybDkzLTI1LjgiLz4KPC9zdmc+Cg==);
  --jp-icon-image: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1icmFuZDQganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGZpbGw9IiNGRkYiIGQ9Ik0yLjIgMi4yaDE3LjV2MTcuNUgyLjJ6Ii8+CiAgPHBhdGggY2xhc3M9ImpwLWljb24tYnJhbmQwIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzNGNTFCNSIgZD0iTTIuMiAyLjJ2MTcuNWgxNy41bC4xLTE3LjVIMi4yem0xMi4xIDIuMmMxLjIgMCAyLjIgMSAyLjIgMi4ycy0xIDIuMi0yLjIgMi4yLTIuMi0xLTIuMi0yLjIgMS0yLjIgMi4yLTIuMnpNNC40IDE3LjZsMy4zLTguOCAzLjMgNi42IDIuMi0zLjIgNC40IDUuNEg0LjR6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-inspector: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNEg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMThjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY2YzAtMS4xLS45LTItMi0yem0tNSAxNEg0di00aDExdjR6bTAtNUg0VjloMTF2NHptNSA1aC00VjloNHY5eiIvPgo8L3N2Zz4K);
  --jp-icon-json: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMSBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNGOUE4MjUiPgogICAgPHBhdGggZD0iTTIwLjIgMTEuOGMtMS42IDAtMS43LjUtMS43IDEgMCAuNC4xLjkuMSAxLjMuMS41LjEuOS4xIDEuMyAwIDEuNy0xLjQgMi4zLTMuNSAyLjNoLS45di0xLjloLjVjMS4xIDAgMS40IDAgMS40LS44IDAtLjMgMC0uNi0uMS0xIDAtLjQtLjEtLjgtLjEtMS4yIDAtMS4zIDAtMS44IDEuMy0yLTEuMy0uMi0xLjMtLjctMS4zLTIgMC0uNC4xLS44LjEtMS4yLjEtLjQuMS0uNy4xLTEgMC0uOC0uNC0uNy0xLjQtLjhoLS41VjQuMWguOWMyLjIgMCAzLjUuNyAzLjUgMi4zIDAgLjQtLjEuOS0uMSAxLjMtLjEuNS0uMS45LS4xIDEuMyAwIC41LjIgMSAxLjcgMXYxLjh6TTEuOCAxMC4xYzEuNiAwIDEuNy0uNSAxLjctMSAwLS40LS4xLS45LS4xLTEuMy0uMS0uNS0uMS0uOS0uMS0xLjMgMC0xLjYgMS40LTIuMyAzLjUtMi4zaC45djEuOWgtLjVjLTEgMC0xLjQgMC0xLjQuOCAwIC4zIDAgLjYuMSAxIDAgLjIuMS42LjEgMSAwIDEuMyAwIDEuOC0xLjMgMkM2IDExLjIgNiAxMS43IDYgMTNjMCAuNC0uMS44LS4xIDEuMi0uMS4zLS4xLjctLjEgMSAwIC44LjMuOCAxLjQuOGguNXYxLjloLS45Yy0yLjEgMC0zLjUtLjYtMy41LTIuMyAwLS40LjEtLjkuMS0xLjMuMS0uNS4xLS45LjEtMS4zIDAtLjUtLjItMS0xLjctMXYtMS45eiIvPgogICAgPGNpcmNsZSBjeD0iMTEiIGN5PSIxMy44IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY3g9IjExIiBjeT0iOC4yIiByPSIyLjEiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-jupyter-favicon: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMTUyIiBoZWlnaHQ9IjE2NSIgdmlld0JveD0iMCAwIDE1MiAxNjUiIHZlcnNpb249IjEuMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA3ODk0NywgMTEwLjU4MjkyNykiIGQ9Ik03NS45NDIyODQyLDI5LjU4MDQ1NjEgQzQzLjMwMjM5NDcsMjkuNTgwNDU2MSAxNC43OTY3ODMyLDE3LjY1MzQ2MzQgMCwwIEM1LjUxMDgzMjExLDE1Ljg0MDY4MjkgMTUuNzgxNTM4OSwyOS41NjY3NzMyIDI5LjM5MDQ5NDcsMzkuMjc4NDE3MSBDNDIuOTk5Nyw0OC45ODk4NTM3IDU5LjI3MzcsNTQuMjA2NzgwNSA3NS45NjA1Nzg5LDU0LjIwNjc4MDUgQzkyLjY0NzQ1NzksNTQuMjA2NzgwNSAxMDguOTIxNDU4LDQ4Ljk4OTg1MzcgMTIyLjUzMDY2MywzOS4yNzg0MTcxIEMxMzYuMTM5NDUzLDI5LjU2Njc3MzIgMTQ2LjQxMDI4NCwxNS44NDA2ODI5IDE1MS45MjExNTgsMCBDMTM3LjA4Nzg2OCwxNy42NTM0NjM0IDEwOC41ODI1ODksMjkuNTgwNDU2MSA3NS45NDIyODQyLDI5LjU4MDQ1NjEgTDc1Ljk0MjI4NDIsMjkuNTgwNDU2MSBaIiAvPgogICAgPHBhdGggdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMzczNjgsIDAuNzA0ODc4KSIgZD0iTTc1Ljk3ODQ1NzksMjQuNjI2NDA3MyBDMTA4LjYxODc2MywyNC42MjY0MDczIDEzNy4xMjQ0NTgsMzYuNTUzNDQxNSAxNTEuOTIxMTU4LDU0LjIwNjc4MDUgQzE0Ni40MTAyODQsMzguMzY2MjIyIDEzNi4xMzk0NTMsMjQuNjQwMTMxNyAxMjIuNTMwNjYzLDE0LjkyODQ4NzggQzEwOC45MjE0NTgsNS4yMTY4NDM5IDkyLjY0NzQ1NzksMCA3NS45NjA1Nzg5LDAgQzU5LjI3MzcsMCA0Mi45OTk3LDUuMjE2ODQzOSAyOS4zOTA0OTQ3LDE0LjkyODQ4NzggQzE1Ljc4MTUzODksMjQuNjQwMTMxNyA1LjUxMDgzMjExLDM4LjM2NjIyMiAwLDU0LjIwNjc4MDUgQzE0LjgzMzA4MTYsMzYuNTg5OTI5MyA0My4zMzg1Njg0LDI0LjYyNjQwNzMgNzUuOTc4NDU3OSwyNC42MjY0MDczIEw3NS45Nzg0NTc5LDI0LjYyNjQwNzMgWiIgLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-jupyter: url(data:image/svg+xml;base64,PHN2ZyB3aWR0aD0iMzkiIGhlaWdodD0iNTEiIHZpZXdCb3g9IjAgMCAzOSA1MSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgtMTYzOCAtMjI4MSkiPgogICAgPGcgY2xhc3M9ImpwLWljb24td2FybjAiIGZpbGw9IiNGMzc3MjYiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5Ljc0IDIzMTEuOTgpIiBkPSJNIDE4LjI2NDYgNy4xMzQxMUMgMTAuNDE0NSA3LjEzNDExIDMuNTU4NzIgNC4yNTc2IDAgMEMgMS4zMjUzOSAzLjgyMDQgMy43OTU1NiA3LjEzMDgxIDcuMDY4NiA5LjQ3MzAzQyAxMC4zNDE3IDExLjgxNTIgMTQuMjU1NyAxMy4wNzM0IDE4LjI2OSAxMy4wNzM0QyAyMi4yODIzIDEzLjA3MzQgMjYuMTk2MyAxMS44MTUyIDI5LjQ2OTQgOS40NzMwM0MgMzIuNzQyNCA3LjEzMDgxIDM1LjIxMjYgMy44MjA0IDM2LjUzOCAwQyAzMi45NzA1IDQuMjU3NiAyNi4xMTQ4IDcuMTM0MTEgMTguMjY0NiA3LjEzNDExWiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM5LjczIDIyODUuNDgpIiBkPSJNIDE4LjI3MzMgNS45MzkzMUMgMjYuMTIzNSA1LjkzOTMxIDMyLjk3OTMgOC44MTU4MyAzNi41MzggMTMuMDczNEMgMzUuMjEyNiA5LjI1MzAzIDMyLjc0MjQgNS45NDI2MiAyOS40Njk0IDMuNjAwNEMgMjYuMTk2MyAxLjI1ODE4IDIyLjI4MjMgMCAxOC4yNjkgMEMgMTQuMjU1NyAwIDEwLjM0MTcgMS4yNTgxOCA3LjA2ODYgMy42MDA0QyAzLjc5NTU2IDUuOTQyNjIgMS4zMjUzOSA5LjI1MzAzIDAgMTMuMDczNEMgMy41Njc0NSA4LjgyNDYzIDEwLjQyMzIgNS45MzkzMSAxOC4yNzMzIDUuOTM5MzFaIi8+CiAgICA8L2c+CiAgICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjY5LjMgMjI4MS4zMSkiIGQ9Ik0gNS44OTM1MyAyLjg0NEMgNS45MTg4OSAzLjQzMTY1IDUuNzcwODUgNC4wMTM2NyA1LjQ2ODE1IDQuNTE2NDVDIDUuMTY1NDUgNS4wMTkyMiA0LjcyMTY4IDUuNDIwMTUgNC4xOTI5OSA1LjY2ODUxQyAzLjY2NDMgNS45MTY4OCAzLjA3NDQ0IDYuMDAxNTEgMi40OTgwNSA1LjkxMTcxQyAxLjkyMTY2IDUuODIxOSAxLjM4NDYzIDUuNTYxNyAwLjk1NDg5OCA1LjE2NDAxQyAwLjUyNTE3IDQuNzY2MzMgMC4yMjIwNTYgNC4yNDkwMyAwLjA4MzkwMzcgMy42Nzc1N0MgLTAuMDU0MjQ4MyAzLjEwNjExIC0wLjAyMTIzIDIuNTA2MTcgMC4xNzg3ODEgMS45NTM2NEMgMC4zNzg3OTMgMS40MDExIDAuNzM2ODA5IDAuOTIwODE3IDEuMjA3NTQgMC41NzM1MzhDIDEuNjc4MjYgMC4yMjYyNTkgMi4yNDA1NSAwLjAyNzU5MTkgMi44MjMyNiAwLjAwMjY3MjI5QyAzLjYwMzg5IC0wLjAzMDcxMTUgNC4zNjU3MyAwLjI0OTc4OSA0Ljk0MTQyIDAuNzgyNTUxQyA1LjUxNzExIDEuMzE1MzEgNS44NTk1NiAyLjA1Njc2IDUuODkzNTMgMi44NDRaIi8+CiAgICAgIDxwYXRoIHRyYW5zZm9ybT0idHJhbnNsYXRlKDE2MzkuOCAyMzIzLjgxKSIgZD0iTSA3LjQyNzg5IDMuNTgzMzhDIDcuNDYwMDggNC4zMjQzIDcuMjczNTUgNS4wNTgxOSA2Ljg5MTkzIDUuNjkyMTNDIDYuNTEwMzEgNi4zMjYwNyA1Ljk1MDc1IDYuODMxNTYgNS4yODQxMSA3LjE0NDZDIDQuNjE3NDcgNy40NTc2MyAzLjg3MzcxIDcuNTY0MTQgMy4xNDcwMiA3LjQ1MDYzQyAyLjQyMDMyIDcuMzM3MTIgMS43NDMzNiA3LjAwODcgMS4yMDE4NCA2LjUwNjk1QyAwLjY2MDMyOCA2LjAwNTIgMC4yNzg2MSA1LjM1MjY4IDAuMTA1MDE3IDQuNjMyMDJDIC0wLjA2ODU3NTcgMy45MTEzNSAtMC4wMjYyMzYxIDMuMTU0OTQgMC4yMjY2NzUgMi40NTg1NkMgMC40Nzk1ODcgMS43NjIxNyAwLjkzMTY5NyAxLjE1NzEzIDEuNTI1NzYgMC43MjAwMzNDIDIuMTE5ODMgMC4yODI5MzUgMi44MjkxNCAwLjAzMzQzOTUgMy41NjM4OSAwLjAwMzEzMzQ0QyA0LjU0NjY3IC0wLjAzNzQwMzMgNS41MDUyOSAwLjMxNjcwNiA2LjIyOTYxIDAuOTg3ODM1QyA2Ljk1MzkzIDEuNjU4OTYgNy4zODQ4NCAyLjU5MjM1IDcuNDI3ODkgMy41ODMzOEwgNy40Mjc4OSAzLjU4MzM4WiIvPgogICAgICA8cGF0aCB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxNjM4LjM2IDIyODYuMDYpIiBkPSJNIDIuMjc0NzEgNC4zOTYyOUMgMS44NDM2MyA0LjQxNTA4IDEuNDE2NzEgNC4zMDQ0NSAxLjA0Nzk5IDQuMDc4NDNDIDAuNjc5MjY4IDMuODUyNCAwLjM4NTMyOCAzLjUyMTE0IDAuMjAzMzcxIDMuMTI2NTZDIDAuMDIxNDEzNiAyLjczMTk4IC0wLjA0MDM3OTggMi4yOTE4MyAwLjAyNTgxMTYgMS44NjE4MUMgMC4wOTIwMDMxIDEuNDMxOCAwLjI4MzIwNCAxLjAzMTI2IDAuNTc1MjEzIDAuNzEwODgzQyAwLjg2NzIyMiAwLjM5MDUxIDEuMjQ2OTEgMC4xNjQ3MDggMS42NjYyMiAwLjA2MjA1OTJDIDIuMDg1NTMgLTAuMDQwNTg5NyAyLjUyNTYxIC0wLjAxNTQ3MTQgMi45MzA3NiAwLjEzNDIzNUMgMy4zMzU5MSAwLjI4Mzk0MSAzLjY4NzkyIDAuNTUxNTA1IDMuOTQyMjIgMC45MDMwNkMgNC4xOTY1MiAxLjI1NDYyIDQuMzQxNjkgMS42NzQzNiA0LjM1OTM1IDIuMTA5MTZDIDQuMzgyOTkgMi42OTEwNyA0LjE3Njc4IDMuMjU4NjkgMy43ODU5NyAzLjY4NzQ2QyAzLjM5NTE2IDQuMTE2MjQgMi44NTE2NiA0LjM3MTE2IDIuMjc0NzEgNC4zOTYyOUwgMi4yNzQ3MSA0LjM5NjI5WiIvPgogICAgPC9nPgogIDwvZz4+Cjwvc3ZnPgo=);
  --jp-icon-jupyterlab-wordmark: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyMDAiIHZpZXdCb3g9IjAgMCAxODYwLjggNDc1Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0RTRFNEUiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDQ4MC4xMzY0MDEsIDY0LjI3MTQ5MykiPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC4wMDAwMDAsIDU4Ljg3NTU2NikiPgogICAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgwLjA4NzYwMywgMC4xNDAyOTQpIj4KICAgICAgICA8cGF0aCBkPSJNLTQyNi45LDE2OS44YzAsNDguNy0zLjcsNjQuNy0xMy42LDc2LjRjLTEwLjgsMTAtMjUsMTUuNS0zOS43LDE1LjVsMy43LDI5IGMyMi44LDAuMyw0NC44LTcuOSw2MS45LTIzLjFjMTcuOC0xOC41LDI0LTQ0LjEsMjQtODMuM1YwSC00Mjd2MTcwLjFMLTQyNi45LDE2OS44TC00MjYuOSwxNjkuOHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMTU1LjA0NTI5NiwgNTYuODM3MTA0KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuNTYyNDUzLCAxLjc5OTg0MikiPgogICAgICAgIDxwYXRoIGQ9Ik0tMzEyLDE0OGMwLDIxLDAsMzkuNSwxLjcsNTUuNGgtMzEuOGwtMi4xLTMzLjNoLTAuOGMtNi43LDExLjYtMTYuNCwyMS4zLTI4LDI3LjkgYy0xMS42LDYuNi0yNC44LDEwLTM4LjIsOS44Yy0zMS40LDAtNjktMTcuNy02OS04OVYwaDM2LjR2MTEyLjdjMCwzOC43LDExLjYsNjQuNyw0NC42LDY0LjdjMTAuMy0wLjIsMjAuNC0zLjUsMjguOS05LjQgYzguNS01LjksMTUuMS0xNC4zLDE4LjktMjMuOWMyLjItNi4xLDMuMy0xMi41LDMuMy0xOC45VjAuMmgzNi40VjE0OEgtMzEyTC0zMTIsMTQ4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzOTAuMDEzMzIyLCA1My40Nzk2MzgpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS43MDY0NTgsIDAuMjMxNDI1KSI+CiAgICAgICAgPHBhdGggZD0iTS00NzguNiw3MS40YzAtMjYtMC44LTQ3LTEuNy02Ni43aDMyLjdsMS43LDM0LjhoMC44YzcuMS0xMi41LDE3LjUtMjIuOCwzMC4xLTI5LjcgYzEyLjUtNywyNi43LTEwLjMsNDEtOS44YzQ4LjMsMCw4NC43LDQxLjcsODQuNywxMDMuM2MwLDczLjEtNDMuNywxMDkuMi05MSwxMDkuMmMtMTIuMSwwLjUtMjQuMi0yLjItMzUtNy44IGMtMTAuOC01LjYtMTkuOS0xMy45LTI2LjYtMjQuMmgtMC44VjI5MWgtMzZ2LTIyMEwtNDc4LjYsNzEuNEwtNDc4LjYsNzEuNHogTS00NDIuNiwxMjUuNmMwLjEsNS4xLDAuNiwxMC4xLDEuNywxNS4xIGMzLDEyLjMsOS45LDIzLjMsMTkuOCwzMS4xYzkuOSw3LjgsMjIuMSwxMi4xLDM0LjcsMTIuMWMzOC41LDAsNjAuNy0zMS45LDYwLjctNzguNWMwLTQwLjctMjEuMS03NS42LTU5LjUtNzUuNiBjLTEyLjksMC40LTI1LjMsNS4xLTM1LjMsMTMuNGMtOS45LDguMy0xNi45LDE5LjctMTkuNiwzMi40Yy0xLjUsNC45LTIuMywxMC0yLjUsMTUuMVYxMjUuNkwtNDQyLjYsMTI1LjZMLTQ0Mi42LDEyNS42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSg2MDYuNzQwNzI2LCA1Ni44MzcxMDQpIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMC43NTEyMjYsIDEuOTg5Mjk5KSI+CiAgICAgICAgPHBhdGggZD0iTS00NDAuOCwwbDQzLjcsMTIwLjFjNC41LDEzLjQsOS41LDI5LjQsMTIuOCw0MS43aDAuOGMzLjctMTIuMiw3LjktMjcuNywxMi44LTQyLjQgbDM5LjctMTE5LjJoMzguNUwtMzQ2LjksMTQ1Yy0yNiw2OS43LTQzLjcsMTA1LjQtNjguNiwxMjcuMmMtMTIuNSwxMS43LTI3LjksMjAtNDQuNiwyMy45bC05LjEtMzEuMSBjMTEuNy0zLjksMjIuNS0xMC4xLDMxLjgtMTguMWMxMy4yLTExLjEsMjMuNy0yNS4yLDMwLjYtNDEuMmMxLjUtMi44LDIuNS01LjcsMi45LTguOGMtMC4zLTMuMy0xLjItNi42LTIuNS05LjdMLTQ4MC4yLDAuMSBoMzkuN0wtNDQwLjgsMEwtNDQwLjgsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoODIyLjc0ODEwNCwgMC4wMDAwMDApIj4KICAgICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoMS40NjQwNTAsIDAuMzc4OTE0KSI+CiAgICAgICAgPHBhdGggZD0iTS00MTMuNywwdjU4LjNoNTJ2MjguMmgtNTJWMTk2YzAsMjUsNywzOS41LDI3LjMsMzkuNWM3LjEsMC4xLDE0LjItMC43LDIxLjEtMi41IGwxLjcsMjcuN2MtMTAuMywzLjctMjEuMyw1LjQtMzIuMiw1Yy03LjMsMC40LTE0LjYtMC43LTIxLjMtMy40Yy02LjgtMi43LTEyLjktNi44LTE3LjktMTIuMWMtMTAuMy0xMC45LTE0LjEtMjktMTQuMS01Mi45IFY4Ni41aC0zMVY1OC4zaDMxVjkuNkwtNDEzLjcsMEwtNDEzLjcsMHoiLz4KICAgICAgPC9nPgogICAgPC9nPgogICAgPGcgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOTc0LjQzMzI4NiwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDAuOTkwMDM0LCAwLjYxMDMzOSkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDQ1LjgsMTEzYzAuOCw1MCwzMi4yLDcwLjYsNjguNiw3MC42YzE5LDAuNiwzNy45LTMsNTUuMy0xMC41bDYuMiwyNi40IGMtMjAuOSw4LjktNDMuNSwxMy4xLTY2LjIsMTIuNmMtNjEuNSwwLTk4LjMtNDEuMi05OC4zLTEwMi41Qy00ODAuMiw0OC4yLTQ0NC43LDAtMzg2LjUsMGM2NS4yLDAsODIuNyw1OC4zLDgyLjcsOTUuNyBjLTAuMSw1LjgtMC41LDExLjUtMS4yLDE3LjJoLTE0MC42SC00NDUuOEwtNDQ1LjgsMTEzeiBNLTMzOS4yLDg2LjZjMC40LTIzLjUtOS41LTYwLjEtNTAuNC02MC4xIGMtMzYuOCwwLTUyLjgsMzQuNC01NS43LDYwLjFILTMzOS4yTC0zMzkuMiw4Ni42TC0zMzkuMiw4Ni42eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgICA8ZyB0cmFuc2Zvcm09InRyYW5zbGF0ZSgxMjAxLjk2MTA1OCwgNTMuNDc5NjM4KSI+CiAgICAgIDxnIHRyYW5zZm9ybT0idHJhbnNsYXRlKDEuMTc5NjQwLCAwLjcwNTA2OCkiPgogICAgICAgIDxwYXRoIGQ9Ik0tNDc4LjYsNjhjMC0yMy45LTAuNC00NC41LTEuNy02My40aDMxLjhsMS4yLDM5LjloMS43YzkuMS0yNy4zLDMxLTQ0LjUsNTUuMy00NC41IGMzLjUtMC4xLDcsMC40LDEwLjMsMS4ydjM0LjhjLTQuMS0wLjktOC4yLTEuMy0xMi40LTEuMmMtMjUuNiwwLTQzLjcsMTkuNy00OC43LDQ3LjRjLTEsNS43LTEuNiwxMS41LTEuNywxNy4ydjEwOC4zaC0zNlY2OCBMLTQ3OC42LDY4eiIvPgogICAgICA8L2c+CiAgICA8L2c+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCIgZmlsbD0iI0YzNzcyNiI+CiAgICA8cGF0aCBkPSJNMTM1Mi4zLDMyNi4yaDM3VjI4aC0zN1YzMjYuMnogTTE2MDQuOCwzMjYuMmMtMi41LTEzLjktMy40LTMxLjEtMy40LTQ4Ljd2LTc2IGMwLTQwLjctMTUuMS04My4xLTc3LjMtODMuMWMtMjUuNiwwLTUwLDcuMS02Ni44LDE4LjFsOC40LDI0LjRjMTQuMy05LjIsMzQtMTUuMSw1My0xNS4xYzQxLjYsMCw0Ni4yLDMwLjIsNDYuMiw0N3Y0LjIgYy03OC42LTAuNC0xMjIuMywyNi41LTEyMi4zLDc1LjZjMCwyOS40LDIxLDU4LjQsNjIuMiw1OC40YzI5LDAsNTAuOS0xNC4zLDYyLjItMzAuMmgxLjNsMi45LDI1LjZIMTYwNC44eiBNMTU2NS43LDI1Ny43IGMwLDMuOC0wLjgsOC0yLjEsMTEuOGMtNS45LDE3LjItMjIuNywzNC00OS4yLDM0Yy0xOC45LDAtMzQuOS0xMS4zLTM0LjktMzUuM2MwLTM5LjUsNDUuOC00Ni42LDg2LjItNDUuOFYyNTcuN3ogTTE2OTguNSwzMjYuMiBsMS43LTMzLjZoMS4zYzE1LjEsMjYuOSwzOC43LDM4LjIsNjguMSwzOC4yYzQ1LjQsMCw5MS4yLTM2LjEsOTEuMi0xMDguOGMwLjQtNjEuNy0zNS4zLTEwMy43LTg1LjctMTAzLjcgYy0zMi44LDAtNTYuMywxNC43LTY5LjMsMzcuNGgtMC44VjI4aC0zNi42djI0NS43YzAsMTguMS0wLjgsMzguNi0xLjcsNTIuNUgxNjk4LjV6IE0xNzA0LjgsMjA4LjJjMC01LjksMS4zLTEwLjksMi4xLTE1LjEgYzcuNi0yOC4xLDMxLjEtNDUuNCw1Ni4zLTQ1LjRjMzkuNSwwLDYwLjUsMzQuOSw2MC41LDc1LjZjMCw0Ni42LTIzLjEsNzguMS02MS44LDc4LjFjLTI2LjksMC00OC4zLTE3LjYtNTUuNS00My4zIGMtMC44LTQuMi0xLjctOC44LTEuNy0xMy40VjIwOC4yeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgZmlsbD0iIzYxNjE2MSIgZD0iTTE1IDlIOXY2aDZWOXptLTIgNGgtMnYtMmgydjJ6bTgtMlY5aC0yVjdjMC0xLjEtLjktMi0yLTJoLTJWM2gtMnYyaC0yVjNIOXYySDdjLTEuMSAwLTIgLjktMiAydjJIM3YyaDJ2MkgzdjJoMnYyYzAgMS4xLjkgMiAyIDJoMnYyaDJ2LTJoMnYyaDJ2LTJoMmMxLjEgMCAyLS45IDItMnYtMmgydi0yaC0ydi0yaDJ6bS00IDZIN1Y3aDEwdjEweiIvPgo8L3N2Zz4K);
  --jp-icon-keyboard: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMjAgNUg0Yy0xLjEgMC0xLjk5LjktMS45OSAyTDIgMTdjMCAxLjEuOSAyIDIgMmgxNmMxLjEgMCAyLS45IDItMlY3YzAtMS4xLS45LTItMi0yem0tOSAzaDJ2MmgtMlY4em0wIDNoMnYyaC0ydi0yek04IDhoMnYySDhWOHptMCAzaDJ2Mkg4di0yem0tMSAySDV2LTJoMnYyem0wLTNINVY4aDJ2MnptOSA3SDh2LTJoOHYyem0wLTRoLTJ2LTJoMnYyem0wLTNoLTJWOGgydjJ6bTMgM2gtMnYtMmgydjJ6bTAtM2gtMlY4aDJ2MnoiLz4KPC9zdmc+Cg==);
  --jp-icon-launcher: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkgMTlINVY1aDdWM0g1YTIgMiAwIDAwLTIgMnYxNGEyIDIgMCAwMDIgMmgxNGMxLjEgMCAyLS45IDItMnYtN2gtMnY3ek0xNCAzdjJoMy41OWwtOS44MyA5LjgzIDEuNDEgMS40MUwxOSA2LjQxVjEwaDJWM2gtN3oiLz4KPC9zdmc+Cg==);
  --jp-icon-line-form: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGZpbGw9IndoaXRlIiBkPSJNNS44OCA0LjEyTDEzLjc2IDEybC03Ljg4IDcuODhMOCAyMmwxMC0xMEw4IDJ6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-link: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTMuOSAxMmMwLTEuNzEgMS4zOS0zLjEgMy4xLTMuMWg0VjdIN2MtMi43NiAwLTUgMi4yNC01IDVzMi4yNCA1IDUgNWg0di0xLjlIN2MtMS43MSAwLTMuMS0xLjM5LTMuMS0zLjF6TTggMTNoOHYtMkg4djJ6bTktNmgtNHYxLjloNGMxLjcxIDAgMy4xIDEuMzkgMy4xIDMuMXMtMS4zOSAzLjEtMy4xIDMuMWgtNFYxN2g0YzIuNzYgMCA1LTIuMjQgNS01cy0yLjI0LTUtNS01eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-list: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiM2MTYxNjEiIGQ9Ik0xOSA1djE0SDVWNWgxNG0xLjEtMkgzLjljLS41IDAtLjkuNC0uOS45djE2LjJjMCAuNC40LjkuOS45aDE2LjJjLjQgMCAuOS0uNS45LS45VjMuOWMwLS41LS41LS45LS45LS45ek0xMSA3aDZ2MmgtNlY3em0wIDRoNnYyaC02di0yem0wIDRoNnYyaC02ek03IDdoMnYySDd6bTAgNGgydjJIN3ptMCA0aDJ2Mkg3eiIvPgo8L3N2Zz4=);
  --jp-icon-listings-info: url(data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0iaXNvLTg4NTktMSI/Pg0KPHN2ZyB2ZXJzaW9uPSIxLjEiIGlkPSJDYXBhXzEiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyIgeG1sbnM6eGxpbms9Imh0dHA6Ly93d3cudzMub3JnLzE5OTkveGxpbmsiIHg9IjBweCIgeT0iMHB4Ig0KCSB2aWV3Qm94PSIwIDAgNTAuOTc4IDUwLjk3OCIgc3R5bGU9ImVuYWJsZS1iYWNrZ3JvdW5kOm5ldyAwIDAgNTAuOTc4IDUwLjk3ODsiIHhtbDpzcGFjZT0icHJlc2VydmUiPg0KPGc+DQoJPGc+DQoJCTxnPg0KCQkJPHBhdGggc3R5bGU9ImZpbGw6IzAxMDAwMjsiIGQ9Ik00My41Miw3LjQ1OEMzOC43MTEsMi42NDgsMzIuMzA3LDAsMjUuNDg5LDBDMTguNjcsMCwxMi4yNjYsMi42NDgsNy40NTgsNy40NTgNCgkJCQljLTkuOTQzLDkuOTQxLTkuOTQzLDI2LjExOSwwLDM2LjA2MmM0LjgwOSw0LjgwOSwxMS4yMTIsNy40NTYsMTguMDMxLDcuNDU4YzAsMCwwLjAwMSwwLDAuMDAyLDANCgkJCQljNi44MTYsMCwxMy4yMjEtMi42NDgsMTguMDI5LTcuNDU4YzQuODA5LTQuODA5LDcuNDU3LTExLjIxMiw3LjQ1Ny0xOC4wM0M1MC45NzcsMTguNjcsNDguMzI4LDEyLjI2Niw0My41Miw3LjQ1OHoNCgkJCQkgTTQyLjEwNiw0Mi4xMDVjLTQuNDMyLDQuNDMxLTEwLjMzMiw2Ljg3Mi0xNi42MTUsNi44NzJoLTAuMDAyYy02LjI4NS0wLjAwMS0xMi4xODctMi40NDEtMTYuNjE3LTYuODcyDQoJCQkJYy05LjE2Mi05LjE2My05LjE2Mi0yNC4wNzEsMC0zMy4yMzNDMTMuMzAzLDQuNDQsMTkuMjA0LDIsMjUuNDg5LDJjNi4yODQsMCwxMi4xODYsMi40NCwxNi42MTcsNi44NzINCgkJCQljNC40MzEsNC40MzEsNi44NzEsMTAuMzMyLDYuODcxLDE2LjYxN0M0OC45NzcsMzEuNzcyLDQ2LjUzNiwzNy42NzUsNDIuMTA2LDQyLjEwNXoiLz4NCgkJPC9nPg0KCQk8Zz4NCgkJCTxwYXRoIHN0eWxlPSJmaWxsOiMwMTAwMDI7IiBkPSJNMjMuNTc4LDMyLjIxOGMtMC4wMjMtMS43MzQsMC4xNDMtMy4wNTksMC40OTYtMy45NzJjMC4zNTMtMC45MTMsMS4xMS0xLjk5NywyLjI3Mi0zLjI1Mw0KCQkJCWMwLjQ2OC0wLjUzNiwwLjkyMy0xLjA2MiwxLjM2Ny0xLjU3NWMwLjYyNi0wLjc1MywxLjEwNC0xLjQ3OCwxLjQzNi0yLjE3NWMwLjMzMS0wLjcwNywwLjQ5NS0xLjU0MSwwLjQ5NS0yLjUNCgkJCQljMC0xLjA5Ni0wLjI2LTIuMDg4LTAuNzc5LTIuOTc5Yy0wLjU2NS0wLjg3OS0xLjUwMS0xLjMzNi0yLjgwNi0xLjM2OWMtMS44MDIsMC4wNTctMi45ODUsMC42NjctMy41NSwxLjgzMg0KCQkJCWMtMC4zMDEsMC41MzUtMC41MDMsMS4xNDEtMC42MDcsMS44MTRjLTAuMTM5LDAuNzA3LTAuMjA3LDEuNDMyLTAuMjA3LDIuMTc0aC0yLjkzN2MtMC4wOTEtMi4yMDgsMC40MDctNC4xMTQsMS40OTMtNS43MTkNCgkJCQljMS4wNjItMS42NCwyLjg1NS0yLjQ4MSw1LjM3OC0yLjUyN2MyLjE2LDAuMDIzLDMuODc0LDAuNjA4LDUuMTQxLDEuNzU4YzEuMjc4LDEuMTYsMS45MjksMi43NjQsMS45NSw0LjgxMQ0KCQkJCWMwLDEuMTQyLTAuMTM3LDIuMTExLTAuNDEsMi45MTFjLTAuMzA5LDAuODQ1LTAuNzMxLDEuNTkzLTEuMjY4LDIuMjQzYy0wLjQ5MiwwLjY1LTEuMDY4LDEuMzE4LTEuNzMsMi4wMDINCgkJCQljLTAuNjUsMC42OTctMS4zMTMsMS40NzktMS45ODcsMi4zNDZjLTAuMjM5LDAuMzc3LTAuNDI5LDAuNzc3LTAuNTY1LDEuMTk5Yy0wLjE2LDAuOTU5LTAuMjE3LDEuOTUxLTAuMTcxLDIuOTc5DQoJCQkJQzI2LjU4OSwzMi4yMTgsMjMuNTc4LDMyLjIxOCwyMy41NzgsMzIuMjE4eiBNMjMuNTc4LDM4LjIydi0zLjQ4NGgzLjA3NnYzLjQ4NEgyMy41Nzh6Ii8+DQoJCTwvZz4NCgk8L2c+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8Zz4NCjwvZz4NCjxnPg0KPC9nPg0KPGc+DQo8L2c+DQo8L3N2Zz4NCg==);
  --jp-icon-markdown: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjN0IxRkEyIiBkPSJNNSAxNC45aDEybC02LjEgNnptOS40LTYuOGMwLTEuMy0uMS0yLjktLjEtNC41LS40IDEuNC0uOSAyLjktMS4zIDQuM2wtMS4zIDQuM2gtMkw4LjUgNy45Yy0uNC0xLjMtLjctMi45LTEtNC4zLS4xIDEuNi0uMSAzLjItLjIgNC42TDcgMTIuNEg0LjhsLjctMTFoMy4zTDEwIDVjLjQgMS4yLjcgMi43IDEgMy45LjMtMS4yLjctMi42IDEtMy45bDEuMi0zLjdoMy4zbC42IDExaC0yLjRsLS4zLTQuMnoiLz4KPC9zdmc+Cg==);
  --jp-icon-new-folder: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIwIDZoLThsLTItMkg0Yy0xLjExIDAtMS45OS44OS0xLjk5IDJMMiAxOGMwIDEuMTEuODkgMiAyIDJoMTZjMS4xMSAwIDItLjg5IDItMlY4YzAtMS4xMS0uODktMi0yLTJ6bS0xIDhoLTN2M2gtMnYtM2gtM3YtMmgzVjloMnYzaDN2MnoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-not-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI1IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDMgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMTkgMTcuMTg0NCAyLjk2OTY4IDE0LjMwMzIgMS44NjA5NCAxMS40NDA5WiIvPgogICAgPHBhdGggY2xhc3M9ImpwLWljb24yIiBzdHJva2U9IiMzMzMzMzMiIHN0cm9rZS13aWR0aD0iMiIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOS4zMTU5MiA5LjMyMDMxKSIgZD0iTTcuMzY4NDIgMEwwIDcuMzY0NzkiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDkuMzE1OTIgMTYuNjgzNikgc2NhbGUoMSAtMSkiIGQ9Ik03LjM2ODQyIDBMMCA3LjM2NDc5Ii8+Cjwvc3ZnPgo=);
  --jp-icon-notebook: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi13YXJuMCBqcC1pY29uLXNlbGVjdGFibGUiIGZpbGw9IiNFRjZDMDAiPgogICAgPHBhdGggZD0iTTE4LjcgMy4zdjE1LjRIMy4zVjMuM2gxNS40bTEuNS0xLjVIMS44djE4LjNoMTguM2wuMS0xOC4zeiIvPgogICAgPHBhdGggZD0iTTE2LjUgMTYuNWwtNS40LTQuMy01LjYgNC4zdi0xMWgxMXoiLz4KICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-palette: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTE4IDEzVjIwSDRWNkg5LjAyQzkuMDcgNS4yOSA5LjI0IDQuNjIgOS41IDRINEMyLjkgNCAyIDQuOSAyIDZWMjBDMiAyMS4xIDIuOSAyMiA0IDIySDE4QzE5LjEgMjIgMjAgMjEuMSAyMCAyMFYxNUwxOCAxM1pNMTkuMyA4Ljg5QzE5Ljc0IDguMTkgMjAgNy4zOCAyMCA2LjVDMjAgNC4wMSAxNy45OSAyIDE1LjUgMkMxMy4wMSAyIDExIDQuMDEgMTEgNi41QzExIDguOTkgMTMuMDEgMTEgMTUuNDkgMTFDMTYuMzcgMTEgMTcuMTkgMTAuNzQgMTcuODggMTAuM0wyMSAxMy40MkwyMi40MiAxMkwxOS4zIDguODlaTTE1LjUgOUMxNC4xMiA5IDEzIDcuODggMTMgNi41QzEzIDUuMTIgMTQuMTIgNCAxNS41IDRDMTYuODggNCAxOCA1LjEyIDE4IDYuNUMxOCA3Ljg4IDE2Ljg4IDkgMTUuNSA5WiIvPgogICAgPHBhdGggZmlsbC1ydWxlPSJldmVub2RkIiBjbGlwLXJ1bGU9ImV2ZW5vZGQiIGQ9Ik00IDZIOS4wMTg5NEM5LjAwNjM5IDYuMTY1MDIgOSA2LjMzMTc2IDkgNi41QzkgOC44MTU3NyAxMC4yMTEgMTAuODQ4NyAxMi4wMzQzIDEySDlWMTRIMTZWMTIuOTgxMUMxNi41NzAzIDEyLjkzNzcgMTcuMTIgMTIuODIwNyAxNy42Mzk2IDEyLjYzOTZMMTggMTNWMjBINFY2Wk04IDhINlYxMEg4VjhaTTYgMTJIOFYxNEg2VjEyWk04IDE2SDZWMThIOFYxNlpNOSAxNkgxNlYxOEg5VjE2WiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-paste: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE5IDJoLTQuMThDMTQuNC44NCAxMy4zIDAgMTIgMGMtMS4zIDAtMi40Ljg0LTIuODIgMkg1Yy0xLjEgMC0yIC45LTIgMnYxNmMwIDEuMS45IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjRjMC0xLjEtLjktMi0yLTJ6bS03IDBjLjU1IDAgMSAuNDUgMSAxcy0uNDUgMS0xIDEtMS0uNDUtMS0xIC40NS0xIDEtMXptNyAxOEg1VjRoMnYzaDEwVjRoMnYxNnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-python: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1icmFuZDAganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMEQ0N0ExIj4KICAgIDxwYXRoIGQ9Ik0xMS4xIDYuOVY1LjhINi45YzAtLjUgMC0xLjMuMi0xLjYuNC0uNy44LTEuMSAxLjctMS40IDEuNy0uMyAyLjUtLjMgMy45LS4xIDEgLjEgMS45LjkgMS45IDEuOXY0LjJjMCAuNS0uOSAxLjYtMiAxLjZIOC44Yy0xLjUgMC0yLjQgMS40LTIuNCAyLjh2Mi4ySDQuN0MzLjUgMTUuMSAzIDE0IDMgMTMuMVY5Yy0uMS0xIC42LTIgMS44LTIgMS41LS4xIDYuMy0uMSA2LjMtLjF6Ii8+CiAgICA8cGF0aCBkPSJNMTAuOSAxNS4xdjEuMWg0LjJjMCAuNSAwIDEuMy0uMiAxLjYtLjQuNy0uOCAxLjEtMS43IDEuNC0xLjcuMy0yLjUuMy0zLjkuMS0xLS4xLTEuOS0uOS0xLjktMS45di00LjJjMC0uNS45LTEuNiAyLTEuNmgzLjhjMS41IDAgMi40LTEuNCAyLjQtMi44VjYuNmgxLjdDMTguNSA2LjkgMTkgOCAxOSA4LjlWMTNjMCAxLS43IDIuMS0xLjkgMi4xaC02LjJ6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-r-kernel: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjE5NkYzIiBkPSJNNC40IDIuNWMxLjItLjEgMi45LS4zIDQuOS0uMyAyLjUgMCA0LjEuNCA1LjIgMS4zIDEgLjcgMS41IDEuOSAxLjUgMy41IDAgMi0xLjQgMy41LTIuOSA0LjEgMS4yLjQgMS43IDEuNiAyLjIgMyAuNiAxLjkgMSAzLjkgMS4zIDQuNmgtMy44Yy0uMy0uNC0uOC0xLjctMS4yLTMuN3MtMS4yLTIuNi0yLjYtMi42aC0uOXY2LjRINC40VjIuNXptMy43IDYuOWgxLjRjMS45IDAgMi45LS45IDIuOS0yLjNzLTEtMi4zLTIuOC0yLjNjLS43IDAtMS4zIDAtMS42LjJ2NC41aC4xdi0uMXoiLz4KPC9zdmc+Cg==);
  --jp-icon-react: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMTUwIDE1MCA1NDEuOSAyOTUuMyI+CiAgPGcgY2xhc3M9ImpwLWljb24tYnJhbmQyIGpwLWljb24tc2VsZWN0YWJsZSIgZmlsbD0iIzYxREFGQiI+CiAgICA8cGF0aCBkPSJNNjY2LjMgMjk2LjVjMC0zMi41LTQwLjctNjMuMy0xMDMuMS04Mi40IDE0LjQtNjMuNiA4LTExNC4yLTIwLjItMTMwLjQtNi41LTMuOC0xNC4xLTUuNi0yMi40LTUuNnYyMi4zYzQuNiAwIDguMy45IDExLjQgMi42IDEzLjYgNy44IDE5LjUgMzcuNSAxNC45IDc1LjctMS4xIDkuNC0yLjkgMTkuMy01LjEgMjkuNC0xOS42LTQuOC00MS04LjUtNjMuNS0xMC45LTEzLjUtMTguNS0yNy41LTM1LjMtNDEuNi01MCAzMi42LTMwLjMgNjMuMi00Ni45IDg0LTQ2LjlWNzhjLTI3LjUgMC02My41IDE5LjYtOTkuOSA1My42LTM2LjQtMzMuOC03Mi40LTUzLjItOTkuOS01My4ydjIyLjNjMjAuNyAwIDUxLjQgMTYuNSA4NCA0Ni42LTE0IDE0LjctMjggMzEuNC00MS4zIDQ5LjktMjIuNiAyLjQtNDQgNi4xLTYzLjYgMTEtMi4zLTEwLTQtMTkuNy01LjItMjktNC43LTM4LjIgMS4xLTY3LjkgMTQuNi03NS44IDMtMS44IDYuOS0yLjYgMTEuNS0yLjZWNzguNWMtOC40IDAtMTYgMS44LTIyLjYgNS42LTI4LjEgMTYuMi0zNC40IDY2LjctMTkuOSAxMzAuMS02Mi4yIDE5LjItMTAyLjcgNDkuOS0xMDIuNyA4Mi4zIDAgMzIuNSA0MC43IDYzLjMgMTAzLjEgODIuNC0xNC40IDYzLjYtOCAxMTQuMiAyMC4yIDEzMC40IDYuNSAzLjggMTQuMSA1LjYgMjIuNSA1LjYgMjcuNSAwIDYzLjUtMTkuNiA5OS45LTUzLjYgMzYuNCAzMy44IDcyLjQgNTMuMiA5OS45IDUzLjIgOC40IDAgMTYtMS44IDIyLjYtNS42IDI4LjEtMTYuMiAzNC40LTY2LjcgMTkuOS0xMzAuMSA2Mi0xOS4xIDEwMi41LTQ5LjkgMTAyLjUtODIuM3ptLTEzMC4yLTY2LjdjLTMuNyAxMi45LTguMyAyNi4yLTEzLjUgMzkuNS00LjEtOC04LjQtMTYtMTMuMS0yNC00LjYtOC05LjUtMTUuOC0xNC40LTIzLjQgMTQuMiAyLjEgMjcuOSA0LjcgNDEgNy45em0tNDUuOCAxMDYuNWMtNy44IDEzLjUtMTUuOCAyNi4zLTI0LjEgMzguMi0xNC45IDEuMy0zMCAyLTQ1LjIgMi0xNS4xIDAtMzAuMi0uNy00NS0xLjktOC4zLTExLjktMTYuNC0yNC42LTI0LjItMzgtNy42LTEzLjEtMTQuNS0yNi40LTIwLjgtMzkuOCA2LjItMTMuNCAxMy4yLTI2LjggMjAuNy0zOS45IDcuOC0xMy41IDE1LjgtMjYuMyAyNC4xLTM4LjIgMTQuOS0xLjMgMzAtMiA0NS4yLTIgMTUuMSAwIDMwLjIuNyA0NSAxLjkgOC4zIDExLjkgMTYuNCAyNC42IDI0LjIgMzggNy42IDEzLjEgMTQuNSAyNi40IDIwLjggMzkuOC02LjMgMTMuNC0xMy4yIDI2LjgtMjAuNyAzOS45em0zMi4zLTEzYzUuNCAxMy40IDEwIDI2LjggMTMuOCAzOS44LTEzLjEgMy4yLTI2LjkgNS45LTQxLjIgOCA0LjktNy43IDkuOC0xNS42IDE0LjQtMjMuNyA0LjYtOCA4LjktMTYuMSAxMy0yNC4xek00MjEuMiA0MzBjLTkuMy05LjYtMTguNi0yMC4zLTI3LjgtMzIgOSAuNCAxOC4yLjcgMjcuNS43IDkuNCAwIDE4LjctLjIgMjcuOC0uNy05IDExLjctMTguMyAyMi40LTI3LjUgMzJ6bS03NC40LTU4LjljLTE0LjItMi4xLTI3LjktNC43LTQxLTcuOSAzLjctMTIuOSA4LjMtMjYuMiAxMy41LTM5LjUgNC4xIDggOC40IDE2IDEzLjEgMjQgNC43IDggOS41IDE1LjggMTQuNCAyMy40ek00MjAuNyAxNjNjOS4zIDkuNiAxOC42IDIwLjMgMjcuOCAzMi05LS40LTE4LjItLjctMjcuNS0uNy05LjQgMC0xOC43LjItMjcuOC43IDktMTEuNyAxOC4zLTIyLjQgMjcuNS0zMnptLTc0IDU4LjljLTQuOSA3LjctOS44IDE1LjYtMTQuNCAyMy43LTQuNiA4LTguOSAxNi0xMyAyNC01LjQtMTMuNC0xMC0yNi44LTEzLjgtMzkuOCAxMy4xLTMuMSAyNi45LTUuOCA0MS4yLTcuOXptLTkwLjUgMTI1LjJjLTM1LjQtMTUuMS01OC4zLTM0LjktNTguMy01MC42IDAtMTUuNyAyMi45LTM1LjYgNTguMy01MC42IDguNi0zLjcgMTgtNyAyNy43LTEwLjEgNS43IDE5LjYgMTMuMiA0MCAyMi41IDYwLjktOS4yIDIwLjgtMTYuNiA0MS4xLTIyLjIgNjAuNi05LjktMy4xLTE5LjMtNi41LTI4LTEwLjJ6TTMxMCA0OTBjLTEzLjYtNy44LTE5LjUtMzcuNS0xNC45LTc1LjcgMS4xLTkuNCAyLjktMTkuMyA1LjEtMjkuNCAxOS42IDQuOCA0MSA4LjUgNjMuNSAxMC45IDEzLjUgMTguNSAyNy41IDM1LjMgNDEuNiA1MC0zMi42IDMwLjMtNjMuMiA0Ni45LTg0IDQ2LjktNC41LS4xLTguMy0xLTExLjMtMi43em0yMzcuMi03Ni4yYzQuNyAzOC4yLTEuMSA2Ny45LTE0LjYgNzUuOC0zIDEuOC02LjkgMi42LTExLjUgMi42LTIwLjcgMC01MS40LTE2LjUtODQtNDYuNiAxNC0xNC43IDI4LTMxLjQgNDEuMy00OS45IDIyLjYtMi40IDQ0LTYuMSA2My42LTExIDIuMyAxMC4xIDQuMSAxOS44IDUuMiAyOS4xem0zOC41LTY2LjdjLTguNiAzLjctMTggNy0yNy43IDEwLjEtNS43LTE5LjYtMTMuMi00MC0yMi41LTYwLjkgOS4yLTIwLjggMTYuNi00MS4xIDIyLjItNjAuNiA5LjkgMy4xIDE5LjMgNi41IDI4LjEgMTAuMiAzNS40IDE1LjEgNTguMyAzNC45IDU4LjMgNTAuNi0uMSAxNS43LTIzIDM1LjYtNTguNCA1MC42ek0zMjAuOCA3OC40eiIvPgogICAgPGNpcmNsZSBjeD0iNDIwLjkiIGN5PSIyOTYuNSIgcj0iNDUuNyIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-refresh: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDE4IDE4Ij4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTkgMTMuNWMtMi40OSAwLTQuNS0yLjAxLTQuNS00LjVTNi41MSA0LjUgOSA0LjVjMS4yNCAwIDIuMzYuNTIgMy4xNyAxLjMzTDEwIDhoNVYzbC0xLjc2IDEuNzZDMTIuMTUgMy42OCAxMC42NiAzIDkgMyA1LjY5IDMgMy4wMSA1LjY5IDMuMDEgOVM1LjY5IDE1IDkgMTVjMi45NyAwIDUuNDMtMi4xNiA1LjktNWgtMS41MmMtLjQ2IDItMi4yNCAzLjUtNC4zOCAzLjV6Ii8+CiAgICA8L2c+Cjwvc3ZnPgo=);
  --jp-icon-regex: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIwIDIwIj4KICA8ZyBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiM0MTQxNDEiPgogICAgPHJlY3QgeD0iMiIgeT0iMiIgd2lkdGg9IjE2IiBoZWlnaHQ9IjE2Ii8+CiAgPC9nPgoKICA8ZyBjbGFzcz0ianAtaWNvbi1hY2NlbnQyIiBmaWxsPSIjRkZGIj4KICAgIDxjaXJjbGUgY2xhc3M9InN0MiIgY3g9IjUuNSIgY3k9IjE0LjUiIHI9IjEuNSIvPgogICAgPHJlY3QgeD0iMTIiIHk9IjQiIGNsYXNzPSJzdDIiIHdpZHRoPSIxIiBoZWlnaHQ9IjgiLz4KICAgIDxyZWN0IHg9IjguNSIgeT0iNy41IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjg2NiAtMC41IDAuNSAwLjg2NiAtMi4zMjU1IDcuMzIxOSkiIGNsYXNzPSJzdDIiIHdpZHRoPSI4IiBoZWlnaHQ9IjEiLz4KICAgIDxyZWN0IHg9IjEyIiB5PSI0IiB0cmFuc2Zvcm09Im1hdHJpeCgwLjUgLTAuODY2IDAuODY2IDAuNSAtMC42Nzc5IDE0LjgyNTIpIiBjbGFzcz0ic3QyIiB3aWR0aD0iMSIgaGVpZ2h0PSI4Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-run: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTggNXYxNGwxMS03eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-running: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDUxMiA1MTIiPgogIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICA8cGF0aCBkPSJNMjU2IDhDMTE5IDggOCAxMTkgOCAyNTZzMTExIDI0OCAyNDggMjQ4IDI0OC0xMTEgMjQ4LTI0OFMzOTMgOCAyNTYgOHptOTYgMzI4YzAgOC44LTcuMiAxNi0xNiAxNkgxNzZjLTguOCAwLTE2LTcuMi0xNi0xNlYxNzZjMC04LjggNy4yLTE2IDE2LTE2aDE2MGM4LjggMCAxNiA3LjIgMTYgMTZ2MTYweiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-save: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTE3IDNINWMtMS4xMSAwLTIgLjktMiAydjE0YzAgMS4xLjg5IDIgMiAyaDE0YzEuMSAwIDItLjkgMi0yVjdsLTQtNHptLTUgMTZjLTEuNjYgMC0zLTEuMzQtMy0zczEuMzQtMyAzLTMgMyAxLjM0IDMgMy0xLjM0IDMtMyAzem0zLTEwSDVWNWgxMHY0eiIvPgogICAgPC9nPgo8L3N2Zz4K);
  --jp-icon-search: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjEsMTAuOWgtMC43bC0wLjItMC4yYzAuOC0wLjksMS4zLTIuMiwxLjMtMy41YzAtMy0yLjQtNS40LTUuNC01LjRTMS44LDQuMiwxLjgsNy4xczIuNCw1LjQsNS40LDUuNCBjMS4zLDAsMi41LTAuNSwzLjUtMS4zbDAuMiwwLjJ2MC43bDQuMSw0LjFsMS4yLTEuMkwxMi4xLDEwLjl6IE03LjEsMTAuOWMtMi4xLDAtMy43LTEuNy0zLjctMy43czEuNy0zLjcsMy43LTMuN3MzLjcsMS43LDMuNywzLjcgUzkuMiwxMC45LDcuMSwxMC45eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-settings: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTkuNDMgMTIuOThjLjA0LS4zMi4wNy0uNjQuMDctLjk4cy0uMDMtLjY2LS4wNy0uOThsMi4xMS0xLjY1Yy4xOS0uMTUuMjQtLjQyLjEyLS42NGwtMi0zLjQ2Yy0uMTItLjIyLS4zOS0uMy0uNjEtLjIybC0yLjQ5IDFjLS41Mi0uNC0xLjA4LS43My0xLjY5LS45OGwtLjM4LTIuNjVBLjQ4OC40ODggMCAwMDE0IDJoLTRjLS4yNSAwLS40Ni4xOC0uNDkuNDJsLS4zOCAyLjY1Yy0uNjEuMjUtMS4xNy41OS0xLjY5Ljk4bC0yLjQ5LTFjLS4yMy0uMDktLjQ5IDAtLjYxLjIybC0yIDMuNDZjLS4xMy4yMi0uMDcuNDkuMTIuNjRsMi4xMSAxLjY1Yy0uMDQuMzItLjA3LjY1LS4wNy45OHMuMDMuNjYuMDcuOThsLTIuMTEgMS42NWMtLjE5LjE1LS4yNC40Mi0uMTIuNjRsMiAzLjQ2Yy4xMi4yMi4zOS4zLjYxLjIybDIuNDktMWMuNTIuNCAxLjA4LjczIDEuNjkuOThsLjM4IDIuNjVjLjAzLjI0LjI0LjQyLjQ5LjQyaDRjLjI1IDAgLjQ2LS4xOC40OS0uNDJsLjM4LTIuNjVjLjYxLS4yNSAxLjE3LS41OSAxLjY5LS45OGwyLjQ5IDFjLjIzLjA5LjQ5IDAgLjYxLS4yMmwyLTMuNDZjLjEyLS4yMi4wNy0uNDktLjEyLS42NGwtMi4xMS0xLjY1ek0xMiAxNS41Yy0xLjkzIDAtMy41LTEuNTctMy41LTMuNXMxLjU3LTMuNSAzLjUtMy41IDMuNSAxLjU3IDMuNSAzLjUtMS41NyAzLjUtMy41IDMuNXoiLz4KPC9zdmc+Cg==);
  --jp-icon-spreadsheet: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8cGF0aCBjbGFzcz0ianAtaWNvbi1jb250cmFzdDEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNENBRjUwIiBkPSJNMi4yIDIuMnYxNy42aDE3LjZWMi4ySDIuMnptMTUuNCA3LjdoLTUuNVY0LjRoNS41djUuNXpNOS45IDQuNHY1LjVINC40VjQuNGg1LjV6bS01LjUgNy43aDUuNXY1LjVINC40di01LjV6bTcuNyA1LjV2LTUuNWg1LjV2NS41aC01LjV6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-stop: url(data:image/svg+xml;base64,PHN2ZyBoZWlnaHQ9IjI0IiB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIyNCIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICAgIDxnIGNsYXNzPSJqcC1pY29uMyIgZmlsbD0iIzYxNjE2MSI+CiAgICAgICAgPHBhdGggZD0iTTAgMGgyNHYyNEgweiIgZmlsbD0ibm9uZSIvPgogICAgICAgIDxwYXRoIGQ9Ik02IDZoMTJ2MTJINnoiLz4KICAgIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-tab: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTIxIDNIM2MtMS4xIDAtMiAuOS0yIDJ2MTRjMCAxLjEuOSAyIDIgMmgxOGMxLjEgMCAyLS45IDItMlY1YzAtMS4xLS45LTItMi0yem0wIDE2SDNWNWgxMHY0aDh2MTB6Ii8+CiAgPC9nPgo8L3N2Zz4K);
  --jp-icon-terminal: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0IiA+CiAgICA8cmVjdCBjbGFzcz0ianAtaWNvbjIganAtaWNvbi1zZWxlY3RhYmxlIiB3aWR0aD0iMjAiIGhlaWdodD0iMjAiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMikiIGZpbGw9IiMzMzMzMzMiLz4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uLWFjY2VudDIganAtaWNvbi1zZWxlY3RhYmxlLWludmVyc2UiIGQ9Ik01LjA1NjY0IDguNzYxNzJDNS4wNTY2NCA4LjU5NzY2IDUuMDMxMjUgOC40NTMxMiA0Ljk4MDQ3IDguMzI4MTJDNC45MzM1OSA4LjE5OTIyIDQuODU1NDcgOC4wODIwMyA0Ljc0NjA5IDcuOTc2NTZDNC42NDA2MiA3Ljg3MTA5IDQuNSA3Ljc3NTM5IDQuMzI0MjIgNy42ODk0NUM0LjE1MjM0IDcuNTk5NjEgMy45NDMzNiA3LjUxMTcyIDMuNjk3MjcgNy40MjU3OEMzLjMwMjczIDcuMjg1MTYgMi45NDMzNiA3LjEzNjcyIDIuNjE5MTQgNi45ODA0N0MyLjI5NDkyIDYuODI0MjIgMi4wMTc1OCA2LjY0MjU4IDEuNzg3MTEgNi40MzU1NUMxLjU2MDU1IDYuMjI4NTIgMS4zODQ3NyA1Ljk4ODI4IDEuMjU5NzcgNS43MTQ4NEMxLjEzNDc3IDUuNDM3NSAxLjA3MjI3IDUuMTA5MzggMS4wNzIyNyA0LjczMDQ3QzEuMDcyMjcgNC4zOTg0NCAxLjEyODkxIDQuMDk1NyAxLjI0MjE5IDMuODIyMjdDMS4zNTU0NyAzLjU0NDkyIDEuNTE1NjIgMy4zMDQ2OSAxLjcyMjY2IDMuMTAxNTZDMS45Mjk2OSAyLjg5ODQ0IDIuMTc5NjkgMi43MzQzNyAyLjQ3MjY2IDIuNjA5MzhDMi43NjU2MiAyLjQ4NDM4IDMuMDkxOCAyLjQwNDMgMy40NTExNyAyLjM2OTE0VjEuMTA5MzhINC4zODg2N1YyLjM4MDg2QzQuNzQwMjMgMi40Mjc3MyA1LjA1NjY0IDIuNTIzNDQgNS4zMzc4OSAyLjY2Nzk3QzUuNjE5MTQgMi44MTI1IDUuODU3NDIgMy4wMDE5NSA2LjA1MjczIDMuMjM2MzNDNi4yNTE5NSAzLjQ2NjggNi40MDQzIDMuNzQwMjMgNi41MDk3NyA0LjA1NjY0QzYuNjE5MTQgNC4zNjkxNCA2LjY3MzgzIDQuNzIwNyA2LjY3MzgzIDUuMTExMzNINS4wNDQ5MkM1LjA0NDkyIDQuNjM4NjcgNC45Mzc1IDQuMjgxMjUgNC43MjI2NiA0LjAzOTA2QzQuNTA3ODEgMy43OTI5NyA0LjIxNjggMy42Njk5MiAzLjg0OTYxIDMuNjY5OTJDMy42NTAzOSAzLjY2OTkyIDMuNDc2NTYgMy42OTcyNyAzLjMyODEyIDMuNzUxOTVDMy4xODM1OSAzLjgwMjczIDMuMDY0NDUgMy44NzY5NSAyLjk3MDcgMy45NzQ2MUMyLjg3Njk1IDQuMDY4MzYgMi44MDY2NCA0LjE3OTY5IDIuNzU5NzcgNC4zMDg1OUMyLjcxNjggNC40Mzc1IDIuNjk1MzEgNC41NzgxMiAyLjY5NTMxIDQuNzMwNDdDMi42OTUzMSA0Ljg4MjgxIDIuNzE2OCA1LjAxOTUzIDIuNzU5NzcgNS4xNDA2MkMyLjgwNjY0IDUuMjU3ODEgMi44ODI4MSA1LjM2NzE5IDIuOTg4MjggNS40Njg3NUMzLjA5NzY2IDUuNTcwMzEgMy4yNDAyMyA1LjY2Nzk3IDMuNDE2MDIgNS43NjE3MkMzLjU5MTggNS44NTE1NiAzLjgxMDU1IDUuOTQzMzYgNC4wNzIyNyA2LjAzNzExQzQuNDY2OCA2LjE4NTU1IDQuODI0MjIgNi4zMzk4NCA1LjE0NDUzIDYuNUM1LjQ2NDg0IDYuNjU2MjUgNS43MzgyOCA2LjgzOTg0IDUuOTY0ODQgNy4wNTA3OEM2LjE5NTMxIDcuMjU3ODEgNi4zNzEwOSA3LjUgNi40OTIxOSA3Ljc3NzM0QzYuNjE3MTkgOC4wNTA3OCA2LjY3OTY5IDguMzc1IDYuNjc5NjkgOC43NUM2LjY3OTY5IDkuMDkzNzUgNi42MjMwNSA5LjQwNDMgNi41MDk3NyA5LjY4MTY0QzYuMzk2NDggOS45NTUwOCA2LjIzNDM4IDEwLjE5MTQgNi4wMjM0NCAxMC4zOTA2QzUuODEyNSAxMC41ODk4IDUuNTU4NTkgMTAuNzUgNS4yNjE3MiAxMC44NzExQzQuOTY0ODQgMTAuOTg4MyA0LjYzMjgxIDExLjA2NDUgNC4yNjU2MiAxMS4wOTk2VjEyLjI0OEgzLjMzMzk4VjExLjA5OTZDMy4wMDE5NSAxMS4wNjg0IDIuNjc5NjkgMTAuOTk2MSAyLjM2NzE5IDEwLjg4MjhDMi4wNTQ2OSAxMC43NjU2IDEuNzc3MzQgMTAuNTk3NyAxLjUzNTE2IDEwLjM3ODlDMS4yOTY4OCAxMC4xNjAyIDEuMTA1NDcgOS44ODQ3NyAwLjk2MDkzOCA5LjU1MjczQzAuODE2NDA2IDkuMjE2OCAwLjc0NDE0MSA4LjgxNDQ1IDAuNzQ0MTQxIDguMzQ1N0gyLjM3ODkxQzIuMzc4OTEgOC42MjY5NSAyLjQxOTkyIDguODYzMjggMi41MDE5NSA5LjA1NDY5QzIuNTgzOTggOS4yNDIxOSAyLjY4OTQ1IDkuMzkyNTggMi44MTgzNiA5LjUwNTg2QzIuOTUxMTcgOS42MTUyMyAzLjEwMTU2IDkuNjkzMzYgMy4yNjk1MyA5Ljc0MDIzQzMuNDM3NSA5Ljc4NzExIDMuNjA5MzggOS44MTA1NSAzLjc4NTE2IDkuODEwNTVDNC4yMDMxMiA5LjgxMDU1IDQuNTE5NTMgOS43MTI4OSA0LjczNDM4IDkuNTE3NThDNC45NDkyMiA5LjMyMjI3IDUuMDU2NjQgOS4wNzAzMSA1LjA1NjY0IDguNzYxNzJaTTEzLjQxOCAxMi4yNzE1SDguMDc0MjJWMTFIMTMuNDE4VjEyLjI3MTVaIiB0cmFuc2Zvcm09InRyYW5zbGF0ZSgzLjk1MjY0IDYpIiBmaWxsPSJ3aGl0ZSIvPgo8L3N2Zz4K);
  --jp-icon-text-editor: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI0Ij4KICA8cGF0aCBjbGFzcz0ianAtaWNvbjMganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjNjE2MTYxIiBkPSJNMTUgMTVIM3YyaDEydi0yem0wLThIM3YyaDEyVjd6TTMgMTNoMTh2LTJIM3Yyem0wIDhoMTh2LTJIM3Yyek0zIDN2MmgxOFYzSDN6Ii8+Cjwvc3ZnPgo=);
  --jp-icon-trusted: url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSJub25lIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDI0IDI1Ij4KICAgIDxwYXRoIGNsYXNzPSJqcC1pY29uMiIgc3Ryb2tlPSIjMzMzMzMzIiBzdHJva2Utd2lkdGg9IjIiIHRyYW5zZm9ybT0idHJhbnNsYXRlKDIgMykiIGQ9Ik0xLjg2MDk0IDExLjQ0MDlDMC44MjY0NDggOC43NzAyNyAwLjg2Mzc3OSA2LjA1NzY0IDEuMjQ5MDcgNC4xOTkzMkMyLjQ4MjA2IDMuOTMzNDcgNC4wODA2OCAzLjQwMzQ3IDUuNjAxMDIgMi44NDQ5QzcuMjM1NDkgMi4yNDQ0IDguODU2NjYgMS41ODE1IDkuOTg3NiAxLjA5NTM5QzExLjA1OTcgMS41ODM0MSAxMi42MDk0IDIuMjQ0NCAxNC4yMTggMi44NDMzOUMxNS43NTAzIDMuNDEzOTQgMTcuMzk5NSAzLjk1MjU4IDE4Ljc1MzkgNC4yMTM4NUMxOS4xMzY0IDYuMDcxNzcgMTkuMTcwOSA4Ljc3NzIyIDE4LjEzOSAxMS40NDA5QzE3LjAzMDMgMTQuMzAzMiAxNC42NjY4IDE3LjE4NDQgOS45OTk5OSAxOC45MzU0QzUuMzMzMiAxNy4xODQ0IDIuOTY5NjggMTQuMzAzMiAxLjg2MDk0IDExLjQ0MDlaIi8+CiAgICA8cGF0aCBjbGFzcz0ianAtaWNvbjIiIGZpbGw9IiMzMzMzMzMiIHN0cm9rZT0iIzMzMzMzMyIgdHJhbnNmb3JtPSJ0cmFuc2xhdGUoOCA5Ljg2NzE5KSIgZD0iTTIuODYwMTUgNC44NjUzNUwwLjcyNjU0OSAyLjk5OTU5TDAgMy42MzA0NUwyLjg2MDE1IDYuMTMxNTdMOCAwLjYzMDg3Mkw3LjI3ODU3IDBMMi44NjAxNSA0Ljg2NTM1WiIvPgo8L3N2Zz4K);
  --jp-icon-undo: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMjQgMjQiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjUgOGMtMi42NSAwLTUuMDUuOTktNi45IDIuNkwyIDd2OWg5bC0zLjYyLTMuNjJjMS4zOS0xLjE2IDMuMTYtMS44OCA1LjEyLTEuODggMy41NCAwIDYuNTUgMi4zMSA3LjYgNS41bDIuMzctLjc4QzIxLjA4IDExLjAzIDE3LjE1IDggMTIuNSA4eiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-vega: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbjEganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjMjEyMTIxIj4KICAgIDxwYXRoIGQ9Ik0xMC42IDUuNGwyLjItMy4ySDIuMnY3LjNsNC02LjZ6Ii8+CiAgICA8cGF0aCBkPSJNMTUuOCAyLjJsLTQuNCA2LjZMNyA2LjNsLTQuOCA4djUuNWgxNy42VjIuMmgtNHptLTcgMTUuNEg1LjV2LTQuNGgzLjN2NC40em00LjQgMEg5LjhWOS44aDMuNHY3Ljh6bTQuNCAwaC0zLjRWNi41aDMuNHYxMS4xeiIvPgogIDwvZz4KPC9zdmc+Cg==);
  --jp-icon-yaml: url(data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIxNiIgdmlld0JveD0iMCAwIDIyIDIyIj4KICA8ZyBjbGFzcz0ianAtaWNvbi1jb250cmFzdDIganAtaWNvbi1zZWxlY3RhYmxlIiBmaWxsPSIjRDgxQjYwIj4KICAgIDxwYXRoIGQ9Ik03LjIgMTguNnYtNS40TDMgNS42aDMuM2wxLjQgMy4xYy4zLjkuNiAxLjYgMSAyLjUuMy0uOC42LTEuNiAxLTIuNWwxLjQtMy4xaDMuNGwtNC40IDcuNnY1LjVsLTIuOS0uMXoiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxNi41IiByPSIyLjEiLz4KICAgIDxjaXJjbGUgY2xhc3M9InN0MCIgY3g9IjE3LjYiIGN5PSIxMSIgcj0iMi4xIi8+CiAgPC9nPgo8L3N2Zz4K);
}

/* Icon CSS class declarations */

.jp-AddIcon {
  background-image: var(--jp-icon-add);
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
.jp-ConsoleIcon {
  background-image: var(--jp-icon-console);
}
.jp-CopyIcon {
  background-image: var(--jp-icon-copy);
}
.jp-CutIcon {
  background-image: var(--jp-icon-cut);
}
.jp-DownloadIcon {
  background-image: var(--jp-icon-download);
}
.jp-EditIcon {
  background-image: var(--jp-icon-edit);
}
.jp-EllipsesIcon {
  background-image: var(--jp-icon-ellipses);
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
.jp-FilterListIcon {
  background-image: var(--jp-icon-filter-list);
}
.jp-FolderIcon {
  background-image: var(--jp-icon-folder);
}
.jp-Html5Icon {
  background-image: var(--jp-icon-html5);
}
.jp-ImageIcon {
  background-image: var(--jp-icon-image);
}
.jp-InspectorIcon {
  background-image: var(--jp-icon-inspector);
}
.jp-JsonIcon {
  background-image: var(--jp-icon-json);
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
.jp-ListingsInfoIcon {
  background-image: var(--jp-icon-listings-info);
}
.jp-MarkdownIcon {
  background-image: var(--jp-icon-markdown);
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
.jp-PaletteIcon {
  background-image: var(--jp-icon-palette);
}
.jp-PasteIcon {
  background-image: var(--jp-icon-paste);
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
.jp-SpreadsheetIcon {
  background-image: var(--jp-icon-spreadsheet);
}
.jp-StopIcon {
  background-image: var(--jp-icon-stop);
}
.jp-TabIcon {
  background-image: var(--jp-icon-tab);
}
.jp-TerminalIcon {
  background-image: var(--jp-icon-terminal);
}
.jp-TextEditorIcon {
  background-image: var(--jp-icon-text-editor);
}
.jp-TrustedIcon {
  background-image: var(--jp-icon-trusted);
}
.jp-UndoIcon {
  background-image: var(--jp-icon-undo);
}
.jp-VegaIcon {
  background-image: var(--jp-icon-vega);
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

:root {
  --jp-icon-search-white: url(data:image/svg+xml;base64,PHN2ZyB2aWV3Qm94PSIwIDAgMTggMTgiIHdpZHRoPSIxNiIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIj4KICA8ZyBjbGFzcz0ianAtaWNvbjMiIGZpbGw9IiM2MTYxNjEiPgogICAgPHBhdGggZD0iTTEyLjEsMTAuOWgtMC43bC0wLjItMC4yYzAuOC0wLjksMS4zLTIuMiwxLjMtMy41YzAtMy0yLjQtNS40LTUuNC01LjRTMS44LDQuMiwxLjgsNy4xczIuNCw1LjQsNS40LDUuNCBjMS4zLDAsMi41LTAuNSwzLjUtMS4zbDAuMiwwLjJ2MC43bDQuMSw0LjFsMS4yLTEuMkwxMi4xLDEwLjl6IE03LjEsMTAuOWMtMi4xLDAtMy43LTEuNy0zLjctMy43czEuNy0zLjcsMy43LTMuN3MzLjcsMS43LDMuNywzLjcgUzkuMiwxMC45LDcuMSwxMC45eiIvPgogIDwvZz4KPC9zdmc+Cg==);
}

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

/* CSS for icons in selected items in the settings editor */
#setting-editor .jp-PluginList .jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}
#setting-editor
  .jp-PluginList
  .jp-mod-selected
  .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* CSS for icons in selected filebrowser listing items */
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable[fill] {
  fill: #fff;
}
.jp-DirListing-item.jp-mod-selected .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}

/* CSS for icons in selected tabs in the sidebar tab manager */
#tab-manager .lm-TabBar-tab.jp-mod-active .jp-icon-selectable[fill] {
  fill: #fff;
}

#tab-manager .lm-TabBar-tab.jp-mod-active .jp-icon-selectable-inverse[fill] {
  fill: var(--jp-brand-color1);
}
#tab-manager
  .lm-TabBar-tab.jp-mod-active
  .jp-icon-hover
  :hover
  .jp-icon-selectable[fill] {
  fill: var(--jp-brand-color1);
}

#tab-manager
  .lm-TabBar-tab.jp-mod-active
  .jp-icon-hover
  :hover
  .jp-icon-selectable-inverse[fill] {
  fill: #fff;
}

/**
 * TODO: come up with non css-hack solution for showing the busy icon on top
 *  of the close icon
 * CSS for complex behavior of close icon of tabs in the sidebar tab manager
 */
#tab-manager
  .lm-TabBar-tab.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon3[fill] {
  fill: none;
}
#tab-manager
  .lm-TabBar-tab.jp-mod-dirty
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: var(--jp-inverse-layout-color3);
}

#tab-manager
  .lm-TabBar-tab.jp-mod-dirty.jp-mod-active
  > .lm-TabBar-tabCloseIcon
  > :not(:hover)
  > .jp-icon-busy[fill] {
  fill: #fff;
}

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

.jp-icon-hoverShow:not(:hover) svg {
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

/* Sibling imports */

/* Override Blueprint's _reset.scss styles */
html {
  box-sizing: unset;
}

*,
*::before,
*::after {
  box-sizing: unset;
}

body {
  color: unset;
  font-family: var(--jp-ui-font-family);
}

p {
  margin-top: unset;
  margin-bottom: unset;
}

small {
  font-size: unset;
}

strong {
  font-weight: unset;
}

/* Override Blueprint's _typography.scss styles */
a {
  text-decoration: unset;
  color: unset;
}
a:hover {
  text-decoration: unset;
  color: unset;
}

/* Override Blueprint's _accessibility.scss styles */
:focus {
  outline: unset;
  outline-offset: unset;
  -moz-outline-radius: unset;
}

/* Styles for ui-components */
.jp-Button {
  border-radius: var(--jp-border-radius);
  padding: 0px 12px;
  font-size: var(--jp-ui-font-size1);
}

/* Use our own theme for hover styles */
button.jp-Button.bp3-button.bp3-minimal:hover {
  background-color: var(--jp-layout-color2);
}
.jp-Button.minimal {
  color: unset !important;
}

.jp-Button.jp-ToolbarButtonComponent {
  text-transform: none;
}

.jp-InputGroup input {
  box-sizing: border-box;
  border-radius: 0;
  background-color: transparent;
  color: var(--jp-ui-font-color0);
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.jp-InputGroup input:focus {
  box-shadow: inset 0 0 0 var(--jp-border-width)
      var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.jp-InputGroup input::placeholder,
input::placeholder {
  color: var(--jp-ui-font-color3);
}

.jp-BPIcon {
  display: inline-block;
  vertical-align: middle;
  margin: auto;
}

/* Stop blueprint futzing with our icon fills */
.bp3-icon.jp-BPIcon > svg:not([fill]) {
  fill: var(--jp-inverse-layout-color3);
}

.jp-InputGroupAction {
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
  height: 24px;
  line-height: 14px;
  padding: 0 25px 0 10px;
  text-align: left;
  -moz-appearance: none;
  -webkit-appearance: none;
}

/* Use our own theme for hover and option styles */
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

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapse {
  display: flex;
  flex-direction: column;
  align-items: stretch;
  border-top: 1px solid var(--jp-border-color2);
  border-bottom: 1px solid var(--jp-border-color2);
}

.jp-Collapse-header {
  padding: 1px 12px;
  color: var(--jp-ui-font-color1);
  background-color: var(--jp-layout-color1);
  font-size: var(--jp-ui-font-size2);
}

.jp-Collapse-header:hover {
  background-color: var(--jp-layout-color2);
}

.jp-Collapse-contents {
  padding: 0px 12px 0px 12px;
  background-color: var(--jp-layout-color1);
  color: var(--jp-ui-font-color1);
  overflow: auto;
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
  padding-bottom: 0px;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
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
  padding: 0px 9px;
  background-color: var(--jp-input-active-background);
  height: 30px;
  box-shadow: inset 0 0 0 var(--jp-border-width) var(--jp-input-border-color);
}

.lm-CommandPalette.lm-mod-focused .lm-CommandPalette-wrapper {
  box-shadow: inset 0 0 0 1px var(--jp-input-active-box-shadow-color),
    inset 0 0 0 3px var(--jp-input-active-box-shadow-color);
}

.lm-CommandPalette-wrapper::after {
  content: ' ';
  color: white;
  background-color: var(--jp-brand-color1);
  position: absolute;
  top: 4px;
  right: 4px;
  height: 30px;
  width: 10px;
  padding: 0px 10px;
  background-image: var(--jp-icon-search-white);
  background-size: 20px;
  background-repeat: no-repeat;
  background-position: center;
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
  color: var(--jp-ui-font-color3);
  font-size: var(--jp-ui-font-size1);
}

/*-----------------------------------------------------------------------------
| Results
|----------------------------------------------------------------------------*/

.lm-CommandPalette-header:first-child {
  margin-top: 0px;
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
  color: var(--jp-ui-font-color3);
}

.lm-CommandPalette-item.lm-mod-active {
  background: var(--jp-layout-color3);
}

.lm-CommandPalette-item.lm-mod-active:hover:not(.lm-mod-disabled) {
  background: var(--jp-layout-color4);
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
  color: var(--jp-ui-font-color3);
}

.lm-CommandPalette-item .lm-CommandPalette-itemIcon {
  margin: 0 4px 0 0;
  position: relative;
  width: 16px;
  top: 2px;
  flex: 0 0 auto;
}

.lm-CommandPalette-item.lm-mod-disabled .lm-CommandPalette-itemIcon {
  opacity: 0.4;
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

.lm-CommandPalette-content:empty:after {
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
  padding: 0px 8px;
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
  top: 0px;
  left: 0px;
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
  padding: 24px;
  padding-bottom: 12px;
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
}

.jp-Dialog-button {
  overflow: visible;
}

button.jp-Dialog-button:focus {
  outline: 1px solid var(--jp-brand-color1);
  outline-offset: 4px;
  -moz-outline-radius: 0px;
}

button.jp-Dialog-button:focus::-moz-focus-inner {
  border: 0;
}

.jp-Dialog-header {
  flex: 0 0 auto;
  padding-bottom: 12px;
  font-size: var(--jp-ui-font-size3);
  font-weight: 400;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-body {
  display: flex;
  flex-direction: column;
  flex: 1 1 auto;
  font-size: var(--jp-ui-font-size1);
  background: var(--jp-layout-color1);
  overflow: auto;
}

.jp-Dialog-footer {
  display: flex;
  flex-direction: row;
  justify-content: flex-end;
  flex: 0 0 auto;
  margin-left: -12px;
  margin-right: -12px;
  padding: 12px;
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
  padding: 0px 16px;
}

.jp-Dialog-body > label {
  line-height: 1.4;
  color: var(--jp-ui-font-color0);
}

.jp-Dialog-button.jp-mod-styled:not(:last-child) {
  margin-right: 12px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) 2014-2016, Jupyter Development Team.
|
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-HoverBox {
  position: fixed;
}

.jp-HoverBox.jp-mod-outofview {
  display: none;
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
When drag events occur, `p-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-IFrame {
  position: relative;
}

body.lm-mod-override-cursor .jp-IFrame:before {
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

.jp-MainAreaWidget > :focus {
  outline: none;
}

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
  --md-purple-A700: #aa00ff;

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
  --md-yellow-A200: #ffff00;
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
  --md-grey-200: #eeeeee;
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

.jp-SpinnerContent:before {
  width: 50%;
  height: 50%;
  background: #f37626;
  border-radius: 100% 0 0 0;
  position: absolute;
  top: 0;
  left: 0;
  content: '';
}

.jp-SpinnerContent:after {
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
  padding: 0px 12px;
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
  height: 28px;
  box-sizing: border-box;
  margin-bottom: 12px;
}

.jp-select-wrapper.jp-mod-focused select.jp-mod-styled {
  border: var(--jp-border-width) solid var(--jp-input-active-border-color);
  box-shadow: var(--jp-input-box-shadow);
  background-color: var(--jp-input-active-background);
}

select.jp-mod-styled:hover {
  background-color: var(--jp-layout-color1);
  cursor: pointer;
  color: var(--jp-ui-font-color0);
  background-color: var(--jp-input-hover-background);
  box-shadow: inset 0 0px 1px rgba(0, 0, 0, 0.5);
}

select.jp-mod-styled {
  flex: 1 1 auto;
  height: 32px;
  width: 100%;
  font-size: var(--jp-ui-font-size2);
  background: var(--jp-input-background);
  color: var(--jp-ui-font-color0);
  padding: 0 25px 0 8px;
  border: var(--jp-border-width) solid var(--jp-input-border-color);
  border-radius: 0px;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
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
  z-index: 1;
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
  padding: 0px;
  margin: 0px;
}

button.jp-ToolbarButtonComponent {
  background: var(--jp-layout-color1);
  border: none;
  box-sizing: border-box;
  outline: none;
  appearance: none;
  -webkit-appearance: none;
  -moz-appearance: none;
  padding: 0px 6px;
  margin: 0px;
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

button.jp-ToolbarButtonComponent span {
  padding: 0px;
  flex: 0 0 auto;
}

button.jp-ToolbarButtonComponent .jp-ToolbarButtonComponent-label {
  font-size: var(--jp-ui-font-size1);
  line-height: 100%;
  padding-left: 2px;
  color: var(--jp-ui-font-color1);
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

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Copyright (c) 2014-2017, PhosphorJS Contributors
|
| Distributed under the terms of the BSD 3-Clause License.
|
| The full license is in the file LICENSE, distributed with this software.
|----------------------------------------------------------------------------*/


/* <DEPRECATED> */ body.p-mod-override-cursor *, /* </DEPRECATED> */
body.lm-mod-override-cursor * {
  cursor: inherit !important;
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
  border-radius: 0px;
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

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* BASICS */

.CodeMirror {
  /* Set height, width, borders, and global font properties here */
  font-family: monospace;
  height: 300px;
  color: black;
  direction: ltr;
}

/* PADDING */

.CodeMirror-lines {
  padding: 4px 0; /* Vertical padding around content */
}
.CodeMirror pre.CodeMirror-line,
.CodeMirror pre.CodeMirror-line-like {
  padding: 0 4px; /* Horizontal padding of content */
}

.CodeMirror-scrollbar-filler, .CodeMirror-gutter-filler {
  background-color: white; /* The little square between H and V scrollbars */
}

/* GUTTER */

.CodeMirror-gutters {
  border-right: 1px solid #ddd;
  background-color: #f7f7f7;
  white-space: nowrap;
}
.CodeMirror-linenumbers {}
.CodeMirror-linenumber {
  padding: 0 3px 0 5px;
  min-width: 20px;
  text-align: right;
  color: #999;
  white-space: nowrap;
}

.CodeMirror-guttermarker { color: black; }
.CodeMirror-guttermarker-subtle { color: #999; }

/* CURSOR */

.CodeMirror-cursor {
  border-left: 1px solid black;
  border-right: none;
  width: 0;
}
/* Shown when moving in bi-directional text */
.CodeMirror div.CodeMirror-secondarycursor {
  border-left: 1px solid silver;
}
.cm-fat-cursor .CodeMirror-cursor {
  width: auto;
  border: 0 !important;
  background: #7e7;
}
.cm-fat-cursor div.CodeMirror-cursors {
  z-index: 1;
}
.cm-fat-cursor-mark {
  background-color: rgba(20, 255, 20, 0.5);
  -webkit-animation: blink 1.06s steps(1) infinite;
  -moz-animation: blink 1.06s steps(1) infinite;
  animation: blink 1.06s steps(1) infinite;
}
.cm-animate-fat-cursor {
  width: auto;
  border: 0;
  -webkit-animation: blink 1.06s steps(1) infinite;
  -moz-animation: blink 1.06s steps(1) infinite;
  animation: blink 1.06s steps(1) infinite;
  background-color: #7e7;
}
@-moz-keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}
@-webkit-keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}
@keyframes blink {
  0% {}
  50% { background-color: transparent; }
  100% {}
}

/* Can style cursor different in overwrite (non-insert) mode */
.CodeMirror-overwrite .CodeMirror-cursor {}

.cm-tab { display: inline-block; text-decoration: inherit; }

.CodeMirror-rulers {
  position: absolute;
  left: 0; right: 0; top: -50px; bottom: 0;
  overflow: hidden;
}
.CodeMirror-ruler {
  border-left: 1px solid #ccc;
  top: 0; bottom: 0;
  position: absolute;
}

/* DEFAULT THEME */

.cm-s-default .cm-header {color: blue;}
.cm-s-default .cm-quote {color: #090;}
.cm-negative {color: #d44;}
.cm-positive {color: #292;}
.cm-header, .cm-strong {font-weight: bold;}
.cm-em {font-style: italic;}
.cm-link {text-decoration: underline;}
.cm-strikethrough {text-decoration: line-through;}

.cm-s-default .cm-keyword {color: #708;}
.cm-s-default .cm-atom {color: #219;}
.cm-s-default .cm-number {color: #164;}
.cm-s-default .cm-def {color: #00f;}
.cm-s-default .cm-variable,
.cm-s-default .cm-punctuation,
.cm-s-default .cm-property,
.cm-s-default .cm-operator {}
.cm-s-default .cm-variable-2 {color: #05a;}
.cm-s-default .cm-variable-3, .cm-s-default .cm-type {color: #085;}
.cm-s-default .cm-comment {color: #a50;}
.cm-s-default .cm-string {color: #a11;}
.cm-s-default .cm-string-2 {color: #f50;}
.cm-s-default .cm-meta {color: #555;}
.cm-s-default .cm-qualifier {color: #555;}
.cm-s-default .cm-builtin {color: #30a;}
.cm-s-default .cm-bracket {color: #997;}
.cm-s-default .cm-tag {color: #170;}
.cm-s-default .cm-attribute {color: #00c;}
.cm-s-default .cm-hr {color: #999;}
.cm-s-default .cm-link {color: #00c;}

.cm-s-default .cm-error {color: #f00;}
.cm-invalidchar {color: #f00;}

.CodeMirror-composing { border-bottom: 2px solid; }

/* Default styles for common addons */

div.CodeMirror span.CodeMirror-matchingbracket {color: #0b0;}
div.CodeMirror span.CodeMirror-nonmatchingbracket {color: #a22;}
.CodeMirror-matchingtag { background: rgba(255, 150, 0, .3); }
.CodeMirror-activeline-background {background: #e8f2ff;}

/* STOP */

/* The rest of this file contains styles related to the mechanics of
   the editor. You probably shouldn't touch them. */

.CodeMirror {
  position: relative;
  overflow: hidden;
  background: white;
}

.CodeMirror-scroll {
  overflow: scroll !important; /* Things will break if this is overridden */
  /* 30px is the magic margin used to hide the element's real scrollbars */
  /* See overflow: hidden in .CodeMirror */
  margin-bottom: -30px; margin-right: -30px;
  padding-bottom: 30px;
  height: 100%;
  outline: none; /* Prevent dragging from highlighting the element */
  position: relative;
}
.CodeMirror-sizer {
  position: relative;
  border-right: 30px solid transparent;
}

/* The fake, visible scrollbars. Used to force redraw during scrolling
   before actual scrolling happens, thus preventing shaking and
   flickering artifacts. */
.CodeMirror-vscrollbar, .CodeMirror-hscrollbar, .CodeMirror-scrollbar-filler, .CodeMirror-gutter-filler {
  position: absolute;
  z-index: 6;
  display: none;
}
.CodeMirror-vscrollbar {
  right: 0; top: 0;
  overflow-x: hidden;
  overflow-y: scroll;
}
.CodeMirror-hscrollbar {
  bottom: 0; left: 0;
  overflow-y: hidden;
  overflow-x: scroll;
}
.CodeMirror-scrollbar-filler {
  right: 0; bottom: 0;
}
.CodeMirror-gutter-filler {
  left: 0; bottom: 0;
}

.CodeMirror-gutters {
  position: absolute; left: 0; top: 0;
  min-height: 100%;
  z-index: 3;
}
.CodeMirror-gutter {
  white-space: normal;
  height: 100%;
  display: inline-block;
  vertical-align: top;
  margin-bottom: -30px;
}
.CodeMirror-gutter-wrapper {
  position: absolute;
  z-index: 4;
  background: none !important;
  border: none !important;
}
.CodeMirror-gutter-background {
  position: absolute;
  top: 0; bottom: 0;
  z-index: 4;
}
.CodeMirror-gutter-elt {
  position: absolute;
  cursor: default;
  z-index: 4;
}
.CodeMirror-gutter-wrapper ::selection { background-color: transparent }
.CodeMirror-gutter-wrapper ::-moz-selection { background-color: transparent }

.CodeMirror-lines {
  cursor: text;
  min-height: 1px; /* prevents collapsing before first draw */
}
.CodeMirror pre.CodeMirror-line,
.CodeMirror pre.CodeMirror-line-like {
  /* Reset some styles that the rest of the page might have set */
  -moz-border-radius: 0; -webkit-border-radius: 0; border-radius: 0;
  border-width: 0;
  background: transparent;
  font-family: inherit;
  font-size: inherit;
  margin: 0;
  white-space: pre;
  word-wrap: normal;
  line-height: inherit;
  color: inherit;
  z-index: 2;
  position: relative;
  overflow: visible;
  -webkit-tap-highlight-color: transparent;
  -webkit-font-variant-ligatures: contextual;
  font-variant-ligatures: contextual;
}
.CodeMirror-wrap pre.CodeMirror-line,
.CodeMirror-wrap pre.CodeMirror-line-like {
  word-wrap: break-word;
  white-space: pre-wrap;
  word-break: normal;
}

.CodeMirror-linebackground {
  position: absolute;
  left: 0; right: 0; top: 0; bottom: 0;
  z-index: 0;
}

.CodeMirror-linewidget {
  position: relative;
  z-index: 2;
  padding: 0.1px; /* Force widget margins to stay inside of the container */
}

.CodeMirror-widget {}

.CodeMirror-rtl pre { direction: rtl; }

.CodeMirror-code {
  outline: none;
}

/* Force content-box sizing for the elements where we expect it */
.CodeMirror-scroll,
.CodeMirror-sizer,
.CodeMirror-gutter,
.CodeMirror-gutters,
.CodeMirror-linenumber {
  -moz-box-sizing: content-box;
  box-sizing: content-box;
}

.CodeMirror-measure {
  position: absolute;
  width: 100%;
  height: 0;
  overflow: hidden;
  visibility: hidden;
}

.CodeMirror-cursor {
  position: absolute;
  pointer-events: none;
}
.CodeMirror-measure pre { position: static; }

div.CodeMirror-cursors {
  visibility: hidden;
  position: relative;
  z-index: 3;
}
div.CodeMirror-dragcursors {
  visibility: visible;
}

.CodeMirror-focused div.CodeMirror-cursors {
  visibility: visible;
}

.CodeMirror-selected { background: #d9d9d9; }
.CodeMirror-focused .CodeMirror-selected { background: #d7d4f0; }
.CodeMirror-crosshair { cursor: crosshair; }
.CodeMirror-line::selection, .CodeMirror-line > span::selection, .CodeMirror-line > span > span::selection { background: #d7d4f0; }
.CodeMirror-line::-moz-selection, .CodeMirror-line > span::-moz-selection, .CodeMirror-line > span > span::-moz-selection { background: #d7d4f0; }

.cm-searching {
  background-color: #ffa;
  background-color: rgba(255, 255, 0, .4);
}

/* Used to force a border model for a node */
.cm-force-border { padding-right: .1px; }

@media print {
  /* Hide the cursor when printing */
  .CodeMirror div.CodeMirror-cursors {
    visibility: hidden;
  }
}

/* See issue #2901 */
.cm-tab-wrap-hack:after { content: ''; }

/* Help users use markselection to safely style text background */
span.CodeMirror-selectedtext { background: none; }

.CodeMirror-dialog {
  position: absolute;
  left: 0; right: 0;
  background: inherit;
  z-index: 15;
  padding: .1em .8em;
  overflow: hidden;
  color: inherit;
}

.CodeMirror-dialog-top {
  border-bottom: 1px solid #eee;
  top: 0;
}

.CodeMirror-dialog-bottom {
  border-top: 1px solid #eee;
  bottom: 0;
}

.CodeMirror-dialog input {
  border: none;
  outline: none;
  background: transparent;
  width: 20em;
  color: inherit;
  font-family: monospace;
}

.CodeMirror-dialog button {
  font-size: 70%;
}

.CodeMirror-foldmarker {
  color: blue;
  text-shadow: #b9f 1px 1px 2px, #b9f -1px -1px 2px, #b9f 1px -1px 2px, #b9f -1px 1px 2px;
  font-family: arial;
  line-height: .3;
  cursor: pointer;
}
.CodeMirror-foldgutter {
  width: .7em;
}
.CodeMirror-foldgutter-open,
.CodeMirror-foldgutter-folded {
  cursor: pointer;
}
.CodeMirror-foldgutter-open:after {
  content: "\25BE";
}
.CodeMirror-foldgutter-folded:after {
  content: "\25B8";
}

/*
  Name:       material
  Author:     Mattia Astorino (http://github.com/equinusocio)
  Website:    https://material-theme.site/
*/

.cm-s-material.CodeMirror {
  background-color: #263238;
  color: #EEFFFF;
}

.cm-s-material .CodeMirror-gutters {
  background: #263238;
  color: #546E7A;
  border: none;
}

.cm-s-material .CodeMirror-guttermarker,
.cm-s-material .CodeMirror-guttermarker-subtle,
.cm-s-material .CodeMirror-linenumber {
  color: #546E7A;
}

.cm-s-material .CodeMirror-cursor {
  border-left: 1px solid #FFCC00;
}

.cm-s-material div.CodeMirror-selected {
  background: rgba(128, 203, 196, 0.2);
}

.cm-s-material.CodeMirror-focused div.CodeMirror-selected {
  background: rgba(128, 203, 196, 0.2);
}

.cm-s-material .CodeMirror-line::selection,
.cm-s-material .CodeMirror-line>span::selection,
.cm-s-material .CodeMirror-line>span>span::selection {
  background: rgba(128, 203, 196, 0.2);
}

.cm-s-material .CodeMirror-line::-moz-selection,
.cm-s-material .CodeMirror-line>span::-moz-selection,
.cm-s-material .CodeMirror-line>span>span::-moz-selection {
  background: rgba(128, 203, 196, 0.2);
}

.cm-s-material .CodeMirror-activeline-background {
  background: rgba(0, 0, 0, 0.5);
}

.cm-s-material .cm-keyword {
  color: #C792EA;
}

.cm-s-material .cm-operator {
  color: #89DDFF;
}

.cm-s-material .cm-variable-2 {
  color: #EEFFFF;
}

.cm-s-material .cm-variable-3,
.cm-s-material .cm-type {
  color: #f07178;
}

.cm-s-material .cm-builtin {
  color: #FFCB6B;
}

.cm-s-material .cm-atom {
  color: #F78C6C;
}

.cm-s-material .cm-number {
  color: #FF5370;
}

.cm-s-material .cm-def {
  color: #82AAFF;
}

.cm-s-material .cm-string {
  color: #C3E88D;
}

.cm-s-material .cm-string-2 {
  color: #f07178;
}

.cm-s-material .cm-comment {
  color: #546E7A;
}

.cm-s-material .cm-variable {
  color: #f07178;
}

.cm-s-material .cm-tag {
  color: #FF5370;
}

.cm-s-material .cm-meta {
  color: #FFCB6B;
}

.cm-s-material .cm-attribute {
  color: #C792EA;
}

.cm-s-material .cm-property {
  color: #C792EA;
}

.cm-s-material .cm-qualifier {
  color: #DECB6B;
}

.cm-s-material .cm-variable-3,
.cm-s-material .cm-type {
  color: #DECB6B;
}


.cm-s-material .cm-error {
  color: rgba(255, 255, 255, 1.0);
  background-color: #FF5370;
}

.cm-s-material .CodeMirror-matchingbracket {
  text-decoration: underline;
  color: white !important;
}
/**
 * "
 *  Using Zenburn color palette from the Emacs Zenburn Theme
 *  https://github.com/bbatsov/zenburn-emacs/blob/master/zenburn-theme.el
 *
 *  Also using parts of https://github.com/xavi/coderay-lighttable-theme
 * "
 * From: https://github.com/wisenomad/zenburn-lighttable-theme/blob/master/zenburn.css
 */

.cm-s-zenburn .CodeMirror-gutters { background: #3f3f3f !important; }
.cm-s-zenburn .CodeMirror-foldgutter-open, .CodeMirror-foldgutter-folded { color: #999; }
.cm-s-zenburn .CodeMirror-cursor { border-left: 1px solid white; }
.cm-s-zenburn { background-color: #3f3f3f; color: #dcdccc; }
.cm-s-zenburn span.cm-builtin { color: #dcdccc; font-weight: bold; }
.cm-s-zenburn span.cm-comment { color: #7f9f7f; }
.cm-s-zenburn span.cm-keyword { color: #f0dfaf; font-weight: bold; }
.cm-s-zenburn span.cm-atom { color: #bfebbf; }
.cm-s-zenburn span.cm-def { color: #dcdccc; }
.cm-s-zenburn span.cm-variable { color: #dfaf8f; }
.cm-s-zenburn span.cm-variable-2 { color: #dcdccc; }
.cm-s-zenburn span.cm-string { color: #cc9393; }
.cm-s-zenburn span.cm-string-2 { color: #cc9393; }
.cm-s-zenburn span.cm-number { color: #dcdccc; }
.cm-s-zenburn span.cm-tag { color: #93e0e3; }
.cm-s-zenburn span.cm-property { color: #dfaf8f; }
.cm-s-zenburn span.cm-attribute { color: #dfaf8f; }
.cm-s-zenburn span.cm-qualifier { color: #7cb8bb; }
.cm-s-zenburn span.cm-meta { color: #f0dfaf; }
.cm-s-zenburn span.cm-header { color: #f0efd0; }
.cm-s-zenburn span.cm-operator { color: #f0efd0; }
.cm-s-zenburn span.CodeMirror-matchingbracket { box-sizing: border-box; background: transparent; border-bottom: 1px solid; }
.cm-s-zenburn span.CodeMirror-nonmatchingbracket { border-bottom: 1px solid; background: none; }
.cm-s-zenburn .CodeMirror-activeline { background: #000000; }
.cm-s-zenburn .CodeMirror-activeline-background { background: #000000; }
.cm-s-zenburn div.CodeMirror-selected { background: #545454; }
.cm-s-zenburn .CodeMirror-focused div.CodeMirror-selected { background: #4f4f4f; }

.cm-s-abcdef.CodeMirror { background: #0f0f0f; color: #defdef; }
.cm-s-abcdef div.CodeMirror-selected { background: #515151; }
.cm-s-abcdef .CodeMirror-line::selection, .cm-s-abcdef .CodeMirror-line > span::selection, .cm-s-abcdef .CodeMirror-line > span > span::selection { background: rgba(56, 56, 56, 0.99); }
.cm-s-abcdef .CodeMirror-line::-moz-selection, .cm-s-abcdef .CodeMirror-line > span::-moz-selection, .cm-s-abcdef .CodeMirror-line > span > span::-moz-selection { background: rgba(56, 56, 56, 0.99); }
.cm-s-abcdef .CodeMirror-gutters { background: #555; border-right: 2px solid #314151; }
.cm-s-abcdef .CodeMirror-guttermarker { color: #222; }
.cm-s-abcdef .CodeMirror-guttermarker-subtle { color: azure; }
.cm-s-abcdef .CodeMirror-linenumber { color: #FFFFFF; }
.cm-s-abcdef .CodeMirror-cursor { border-left: 1px solid #00FF00; }

.cm-s-abcdef span.cm-keyword { color: darkgoldenrod; font-weight: bold; }
.cm-s-abcdef span.cm-atom { color: #77F; }
.cm-s-abcdef span.cm-number { color: violet; }
.cm-s-abcdef span.cm-def { color: #fffabc; }
.cm-s-abcdef span.cm-variable { color: #abcdef; }
.cm-s-abcdef span.cm-variable-2 { color: #cacbcc; }
.cm-s-abcdef span.cm-variable-3, .cm-s-abcdef span.cm-type { color: #def; }
.cm-s-abcdef span.cm-property { color: #fedcba; }
.cm-s-abcdef span.cm-operator { color: #ff0; }
.cm-s-abcdef span.cm-comment { color: #7a7b7c; font-style: italic;}
.cm-s-abcdef span.cm-string { color: #2b4; }
.cm-s-abcdef span.cm-meta { color: #C9F; }
.cm-s-abcdef span.cm-qualifier { color: #FFF700; }
.cm-s-abcdef span.cm-builtin { color: #30aabc; }
.cm-s-abcdef span.cm-bracket { color: #8a8a8a; }
.cm-s-abcdef span.cm-tag { color: #FFDD44; }
.cm-s-abcdef span.cm-attribute { color: #DDFF00; }
.cm-s-abcdef span.cm-error { color: #FF0000; }
.cm-s-abcdef span.cm-header { color: aquamarine; font-weight: bold; }
.cm-s-abcdef span.cm-link { color: blueviolet; }

.cm-s-abcdef .CodeMirror-activeline-background { background: #314151; }

/*

    Name:       Base16 Default Light
    Author:     Chris Kempson (http://chriskempson.com)

    CodeMirror template by Jan T. Sott (https://github.com/idleberg/base16-codemirror)
    Original Base16 color scheme by Chris Kempson (https://github.com/chriskempson/base16)

*/

.cm-s-base16-light.CodeMirror { background: #f5f5f5; color: #202020; }
.cm-s-base16-light div.CodeMirror-selected { background: #e0e0e0; }
.cm-s-base16-light .CodeMirror-line::selection, .cm-s-base16-light .CodeMirror-line > span::selection, .cm-s-base16-light .CodeMirror-line > span > span::selection { background: #e0e0e0; }
.cm-s-base16-light .CodeMirror-line::-moz-selection, .cm-s-base16-light .CodeMirror-line > span::-moz-selection, .cm-s-base16-light .CodeMirror-line > span > span::-moz-selection { background: #e0e0e0; }
.cm-s-base16-light .CodeMirror-gutters { background: #f5f5f5; border-right: 0px; }
.cm-s-base16-light .CodeMirror-guttermarker { color: #ac4142; }
.cm-s-base16-light .CodeMirror-guttermarker-subtle { color: #b0b0b0; }
.cm-s-base16-light .CodeMirror-linenumber { color: #b0b0b0; }
.cm-s-base16-light .CodeMirror-cursor { border-left: 1px solid #505050; }

.cm-s-base16-light span.cm-comment { color: #8f5536; }
.cm-s-base16-light span.cm-atom { color: #aa759f; }
.cm-s-base16-light span.cm-number { color: #aa759f; }

.cm-s-base16-light span.cm-property, .cm-s-base16-light span.cm-attribute { color: #90a959; }
.cm-s-base16-light span.cm-keyword { color: #ac4142; }
.cm-s-base16-light span.cm-string { color: #f4bf75; }

.cm-s-base16-light span.cm-variable { color: #90a959; }
.cm-s-base16-light span.cm-variable-2 { color: #6a9fb5; }
.cm-s-base16-light span.cm-def { color: #d28445; }
.cm-s-base16-light span.cm-bracket { color: #202020; }
.cm-s-base16-light span.cm-tag { color: #ac4142; }
.cm-s-base16-light span.cm-link { color: #aa759f; }
.cm-s-base16-light span.cm-error { background: #ac4142; color: #505050; }

.cm-s-base16-light .CodeMirror-activeline-background { background: #DDDCDC; }
.cm-s-base16-light .CodeMirror-matchingbracket { color: #f5f5f5 !important; background-color: #6A9FB5 !important}

/*

    Name:       Base16 Default Dark
    Author:     Chris Kempson (http://chriskempson.com)

    CodeMirror template by Jan T. Sott (https://github.com/idleberg/base16-codemirror)
    Original Base16 color scheme by Chris Kempson (https://github.com/chriskempson/base16)

*/

.cm-s-base16-dark.CodeMirror { background: #151515; color: #e0e0e0; }
.cm-s-base16-dark div.CodeMirror-selected { background: #303030; }
.cm-s-base16-dark .CodeMirror-line::selection, .cm-s-base16-dark .CodeMirror-line > span::selection, .cm-s-base16-dark .CodeMirror-line > span > span::selection { background: rgba(48, 48, 48, .99); }
.cm-s-base16-dark .CodeMirror-line::-moz-selection, .cm-s-base16-dark .CodeMirror-line > span::-moz-selection, .cm-s-base16-dark .CodeMirror-line > span > span::-moz-selection { background: rgba(48, 48, 48, .99); }
.cm-s-base16-dark .CodeMirror-gutters { background: #151515; border-right: 0px; }
.cm-s-base16-dark .CodeMirror-guttermarker { color: #ac4142; }
.cm-s-base16-dark .CodeMirror-guttermarker-subtle { color: #505050; }
.cm-s-base16-dark .CodeMirror-linenumber { color: #505050; }
.cm-s-base16-dark .CodeMirror-cursor { border-left: 1px solid #b0b0b0; }

.cm-s-base16-dark span.cm-comment { color: #8f5536; }
.cm-s-base16-dark span.cm-atom { color: #aa759f; }
.cm-s-base16-dark span.cm-number { color: #aa759f; }

.cm-s-base16-dark span.cm-property, .cm-s-base16-dark span.cm-attribute { color: #90a959; }
.cm-s-base16-dark span.cm-keyword { color: #ac4142; }
.cm-s-base16-dark span.cm-string { color: #f4bf75; }

.cm-s-base16-dark span.cm-variable { color: #90a959; }
.cm-s-base16-dark span.cm-variable-2 { color: #6a9fb5; }
.cm-s-base16-dark span.cm-def { color: #d28445; }
.cm-s-base16-dark span.cm-bracket { color: #e0e0e0; }
.cm-s-base16-dark span.cm-tag { color: #ac4142; }
.cm-s-base16-dark span.cm-link { color: #aa759f; }
.cm-s-base16-dark span.cm-error { background: #ac4142; color: #b0b0b0; }

.cm-s-base16-dark .CodeMirror-activeline-background { background: #202020; }
.cm-s-base16-dark .CodeMirror-matchingbracket { text-decoration: underline; color: white !important; }

/*

    Name:       dracula
    Author:     Michael Kaminsky (http://github.com/mkaminsky11)

    Original dracula color scheme by Zeno Rocha (https://github.com/zenorocha/dracula-theme)

*/


.cm-s-dracula.CodeMirror, .cm-s-dracula .CodeMirror-gutters {
  background-color: #282a36 !important;
  color: #f8f8f2 !important;
  border: none;
}
.cm-s-dracula .CodeMirror-gutters { color: #282a36; }
.cm-s-dracula .CodeMirror-cursor { border-left: solid thin #f8f8f0; }
.cm-s-dracula .CodeMirror-linenumber { color: #6D8A88; }
.cm-s-dracula .CodeMirror-selected { background: rgba(255, 255, 255, 0.10); }
.cm-s-dracula .CodeMirror-line::selection, .cm-s-dracula .CodeMirror-line > span::selection, .cm-s-dracula .CodeMirror-line > span > span::selection { background: rgba(255, 255, 255, 0.10); }
.cm-s-dracula .CodeMirror-line::-moz-selection, .cm-s-dracula .CodeMirror-line > span::-moz-selection, .cm-s-dracula .CodeMirror-line > span > span::-moz-selection { background: rgba(255, 255, 255, 0.10); }
.cm-s-dracula span.cm-comment { color: #6272a4; }
.cm-s-dracula span.cm-string, .cm-s-dracula span.cm-string-2 { color: #f1fa8c; }
.cm-s-dracula span.cm-number { color: #bd93f9; }
.cm-s-dracula span.cm-variable { color: #50fa7b; }
.cm-s-dracula span.cm-variable-2 { color: white; }
.cm-s-dracula span.cm-def { color: #50fa7b; }
.cm-s-dracula span.cm-operator { color: #ff79c6; }
.cm-s-dracula span.cm-keyword { color: #ff79c6; }
.cm-s-dracula span.cm-atom { color: #bd93f9; }
.cm-s-dracula span.cm-meta { color: #f8f8f2; }
.cm-s-dracula span.cm-tag { color: #ff79c6; }
.cm-s-dracula span.cm-attribute { color: #50fa7b; }
.cm-s-dracula span.cm-qualifier { color: #50fa7b; }
.cm-s-dracula span.cm-property { color: #66d9ef; }
.cm-s-dracula span.cm-builtin { color: #50fa7b; }
.cm-s-dracula span.cm-variable-3, .cm-s-dracula span.cm-type { color: #ffb86c; }

.cm-s-dracula .CodeMirror-activeline-background { background: rgba(255,255,255,0.1); }
.cm-s-dracula .CodeMirror-matchingbracket { text-decoration: underline; color: white !important; }

/*

    Name:       Hopscotch
    Author:     Jan T. Sott

    CodeMirror template by Jan T. Sott (https://github.com/idleberg/base16-codemirror)
    Original Base16 color scheme by Chris Kempson (https://github.com/chriskempson/base16)

*/

.cm-s-hopscotch.CodeMirror {background: #322931; color: #d5d3d5;}
.cm-s-hopscotch div.CodeMirror-selected {background: #433b42 !important;}
.cm-s-hopscotch .CodeMirror-gutters {background: #322931; border-right: 0px;}
.cm-s-hopscotch .CodeMirror-linenumber {color: #797379;}
.cm-s-hopscotch .CodeMirror-cursor {border-left: 1px solid #989498 !important;}

.cm-s-hopscotch span.cm-comment {color: #b33508;}
.cm-s-hopscotch span.cm-atom {color: #c85e7c;}
.cm-s-hopscotch span.cm-number {color: #c85e7c;}

.cm-s-hopscotch span.cm-property, .cm-s-hopscotch span.cm-attribute {color: #8fc13e;}
.cm-s-hopscotch span.cm-keyword {color: #dd464c;}
.cm-s-hopscotch span.cm-string {color: #fdcc59;}

.cm-s-hopscotch span.cm-variable {color: #8fc13e;}
.cm-s-hopscotch span.cm-variable-2 {color: #1290bf;}
.cm-s-hopscotch span.cm-def {color: #fd8b19;}
.cm-s-hopscotch span.cm-error {background: #dd464c; color: #989498;}
.cm-s-hopscotch span.cm-bracket {color: #d5d3d5;}
.cm-s-hopscotch span.cm-tag {color: #dd464c;}
.cm-s-hopscotch span.cm-link {color: #c85e7c;}

.cm-s-hopscotch .CodeMirror-matchingbracket { text-decoration: underline; color: white !important;}
.cm-s-hopscotch .CodeMirror-activeline-background { background: #302020; }

/****************************************************************/
/*   Based on mbonaci's Brackets mbo theme                      */
/*   https://github.com/mbonaci/global/blob/master/Mbo.tmTheme  */
/*   Create your own: http://tmtheme-editor.herokuapp.com       */
/****************************************************************/

.cm-s-mbo.CodeMirror { background: #2c2c2c; color: #ffffec; }
.cm-s-mbo div.CodeMirror-selected { background: #716C62; }
.cm-s-mbo .CodeMirror-line::selection, .cm-s-mbo .CodeMirror-line > span::selection, .cm-s-mbo .CodeMirror-line > span > span::selection { background: rgba(113, 108, 98, .99); }
.cm-s-mbo .CodeMirror-line::-moz-selection, .cm-s-mbo .CodeMirror-line > span::-moz-selection, .cm-s-mbo .CodeMirror-line > span > span::-moz-selection { background: rgba(113, 108, 98, .99); }
.cm-s-mbo .CodeMirror-gutters { background: #4e4e4e; border-right: 0px; }
.cm-s-mbo .CodeMirror-guttermarker { color: white; }
.cm-s-mbo .CodeMirror-guttermarker-subtle { color: grey; }
.cm-s-mbo .CodeMirror-linenumber { color: #dadada; }
.cm-s-mbo .CodeMirror-cursor { border-left: 1px solid #ffffec; }

.cm-s-mbo span.cm-comment { color: #95958a; }
.cm-s-mbo span.cm-atom { color: #00a8c6; }
.cm-s-mbo span.cm-number { color: #00a8c6; }

.cm-s-mbo span.cm-property, .cm-s-mbo span.cm-attribute { color: #9ddfe9; }
.cm-s-mbo span.cm-keyword { color: #ffb928; }
.cm-s-mbo span.cm-string { color: #ffcf6c; }
.cm-s-mbo span.cm-string.cm-property { color: #ffffec; }

.cm-s-mbo span.cm-variable { color: #ffffec; }
.cm-s-mbo span.cm-variable-2 { color: #00a8c6; }
.cm-s-mbo span.cm-def { color: #ffffec; }
.cm-s-mbo span.cm-bracket { color: #fffffc; font-weight: bold; }
.cm-s-mbo span.cm-tag { color: #9ddfe9; }
.cm-s-mbo span.cm-link { color: #f54b07; }
.cm-s-mbo span.cm-error { border-bottom: #636363; color: #ffffec; }
.cm-s-mbo span.cm-qualifier { color: #ffffec; }

.cm-s-mbo .CodeMirror-activeline-background { background: #494b41; }
.cm-s-mbo .CodeMirror-matchingbracket { color: #ffb928 !important; }
.cm-s-mbo .CodeMirror-matchingtag { background: rgba(255, 255, 255, .37); }

/*
  MDN-LIKE Theme - Mozilla
  Ported to CodeMirror by Peter Kroon <plakroon@gmail.com>
  Report bugs/issues here: https://github.com/codemirror/CodeMirror/issues
  GitHub: @peterkroon

  The mdn-like theme is inspired on the displayed code examples at: https://developer.mozilla.org/en-US/docs/Web/CSS/animation

*/
.cm-s-mdn-like.CodeMirror { color: #999; background-color: #fff; }
.cm-s-mdn-like div.CodeMirror-selected { background: #cfc; }
.cm-s-mdn-like .CodeMirror-line::selection, .cm-s-mdn-like .CodeMirror-line > span::selection, .cm-s-mdn-like .CodeMirror-line > span > span::selection { background: #cfc; }
.cm-s-mdn-like .CodeMirror-line::-moz-selection, .cm-s-mdn-like .CodeMirror-line > span::-moz-selection, .cm-s-mdn-like .CodeMirror-line > span > span::-moz-selection { background: #cfc; }

.cm-s-mdn-like .CodeMirror-gutters { background: #f8f8f8; border-left: 6px solid rgba(0,83,159,0.65); color: #333; }
.cm-s-mdn-like .CodeMirror-linenumber { color: #aaa; padding-left: 8px; }
.cm-s-mdn-like .CodeMirror-cursor { border-left: 2px solid #222; }

.cm-s-mdn-like .cm-keyword { color: #6262FF; }
.cm-s-mdn-like .cm-atom { color: #F90; }
.cm-s-mdn-like .cm-number { color:  #ca7841; }
.cm-s-mdn-like .cm-def { color: #8DA6CE; }
.cm-s-mdn-like span.cm-variable-2, .cm-s-mdn-like span.cm-tag { color: #690; }
.cm-s-mdn-like span.cm-variable-3, .cm-s-mdn-like span.cm-def, .cm-s-mdn-like span.cm-type { color: #07a; }

.cm-s-mdn-like .cm-variable { color: #07a; }
.cm-s-mdn-like .cm-property { color: #905; }
.cm-s-mdn-like .cm-qualifier { color: #690; }

.cm-s-mdn-like .cm-operator { color: #cda869; }
.cm-s-mdn-like .cm-comment { color:#777; font-weight:normal; }
.cm-s-mdn-like .cm-string { color:#07a; font-style:italic; }
.cm-s-mdn-like .cm-string-2 { color:#bd6b18; } /*?*/
.cm-s-mdn-like .cm-meta { color: #000; } /*?*/
.cm-s-mdn-like .cm-builtin { color: #9B7536; } /*?*/
.cm-s-mdn-like .cm-tag { color: #997643; }
.cm-s-mdn-like .cm-attribute { color: #d6bb6d; } /*?*/
.cm-s-mdn-like .cm-header { color: #FF6400; }
.cm-s-mdn-like .cm-hr { color: #AEAEAE; }
.cm-s-mdn-like .cm-link { color:#ad9361; font-style:italic; text-decoration:none; }
.cm-s-mdn-like .cm-error { border-bottom: 1px solid red; }

div.cm-s-mdn-like .CodeMirror-activeline-background { background: #efefff; }
div.cm-s-mdn-like span.CodeMirror-matchingbracket { outline:1px solid grey; color: inherit; }

.cm-s-mdn-like.CodeMirror { background-image: url(data:image/png;base64,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); }

/*

    Name:       seti
    Author:     Michael Kaminsky (http://github.com/mkaminsky11)

    Original seti color scheme by Jesse Weed (https://github.com/jesseweed/seti-syntax)

*/


.cm-s-seti.CodeMirror {
  background-color: #151718 !important;
  color: #CFD2D1 !important;
  border: none;
}
.cm-s-seti .CodeMirror-gutters {
  color: #404b53;
  background-color: #0E1112;
  border: none;
}
.cm-s-seti .CodeMirror-cursor { border-left: solid thin #f8f8f0; }
.cm-s-seti .CodeMirror-linenumber { color: #6D8A88; }
.cm-s-seti.CodeMirror-focused div.CodeMirror-selected { background: rgba(255, 255, 255, 0.10); }
.cm-s-seti .CodeMirror-line::selection, .cm-s-seti .CodeMirror-line > span::selection, .cm-s-seti .CodeMirror-line > span > span::selection { background: rgba(255, 255, 255, 0.10); }
.cm-s-seti .CodeMirror-line::-moz-selection, .cm-s-seti .CodeMirror-line > span::-moz-selection, .cm-s-seti .CodeMirror-line > span > span::-moz-selection { background: rgba(255, 255, 255, 0.10); }
.cm-s-seti span.cm-comment { color: #41535b; }
.cm-s-seti span.cm-string, .cm-s-seti span.cm-string-2 { color: #55b5db; }
.cm-s-seti span.cm-number { color: #cd3f45; }
.cm-s-seti span.cm-variable { color: #55b5db; }
.cm-s-seti span.cm-variable-2 { color: #a074c4; }
.cm-s-seti span.cm-def { color: #55b5db; }
.cm-s-seti span.cm-keyword { color: #ff79c6; }
.cm-s-seti span.cm-operator { color: #9fca56; }
.cm-s-seti span.cm-keyword { color: #e6cd69; }
.cm-s-seti span.cm-atom { color: #cd3f45; }
.cm-s-seti span.cm-meta { color: #55b5db; }
.cm-s-seti span.cm-tag { color: #55b5db; }
.cm-s-seti span.cm-attribute { color: #9fca56; }
.cm-s-seti span.cm-qualifier { color: #9fca56; }
.cm-s-seti span.cm-property { color: #a074c4; }
.cm-s-seti span.cm-variable-3, .cm-s-seti span.cm-type { color: #9fca56; }
.cm-s-seti span.cm-builtin { color: #9fca56; }
.cm-s-seti .CodeMirror-activeline-background { background: #101213; }
.cm-s-seti .CodeMirror-matchingbracket { text-decoration: underline; color: white !important; }

/*
Solarized theme for code-mirror
http://ethanschoonover.com/solarized
*/

/*
Solarized color palette
http://ethanschoonover.com/solarized/img/solarized-palette.png
*/

.solarized.base03 { color: #002b36; }
.solarized.base02 { color: #073642; }
.solarized.base01 { color: #586e75; }
.solarized.base00 { color: #657b83; }
.solarized.base0 { color: #839496; }
.solarized.base1 { color: #93a1a1; }
.solarized.base2 { color: #eee8d5; }
.solarized.base3  { color: #fdf6e3; }
.solarized.solar-yellow  { color: #b58900; }
.solarized.solar-orange  { color: #cb4b16; }
.solarized.solar-red { color: #dc322f; }
.solarized.solar-magenta { color: #d33682; }
.solarized.solar-violet  { color: #6c71c4; }
.solarized.solar-blue { color: #268bd2; }
.solarized.solar-cyan { color: #2aa198; }
.solarized.solar-green { color: #859900; }

/* Color scheme for code-mirror */

.cm-s-solarized {
  line-height: 1.45em;
  color-profile: sRGB;
  rendering-intent: auto;
}
.cm-s-solarized.cm-s-dark {
  color: #839496;
  background-color: #002b36;
  text-shadow: #002b36 0 1px;
}
.cm-s-solarized.cm-s-light {
  background-color: #fdf6e3;
  color: #657b83;
  text-shadow: #eee8d5 0 1px;
}

.cm-s-solarized .CodeMirror-widget {
  text-shadow: none;
}

.cm-s-solarized .cm-header { color: #586e75; }
.cm-s-solarized .cm-quote { color: #93a1a1; }

.cm-s-solarized .cm-keyword { color: #cb4b16; }
.cm-s-solarized .cm-atom { color: #d33682; }
.cm-s-solarized .cm-number { color: #d33682; }
.cm-s-solarized .cm-def { color: #2aa198; }

.cm-s-solarized .cm-variable { color: #839496; }
.cm-s-solarized .cm-variable-2 { color: #b58900; }
.cm-s-solarized .cm-variable-3, .cm-s-solarized .cm-type { color: #6c71c4; }

.cm-s-solarized .cm-property { color: #2aa198; }
.cm-s-solarized .cm-operator { color: #6c71c4; }

.cm-s-solarized .cm-comment { color: #586e75; font-style:italic; }

.cm-s-solarized .cm-string { color: #859900; }
.cm-s-solarized .cm-string-2 { color: #b58900; }

.cm-s-solarized .cm-meta { color: #859900; }
.cm-s-solarized .cm-qualifier { color: #b58900; }
.cm-s-solarized .cm-builtin { color: #d33682; }
.cm-s-solarized .cm-bracket { color: #cb4b16; }
.cm-s-solarized .CodeMirror-matchingbracket { color: #859900; }
.cm-s-solarized .CodeMirror-nonmatchingbracket { color: #dc322f; }
.cm-s-solarized .cm-tag { color: #93a1a1; }
.cm-s-solarized .cm-attribute { color: #2aa198; }
.cm-s-solarized .cm-hr {
  color: transparent;
  border-top: 1px solid #586e75;
  display: block;
}
.cm-s-solarized .cm-link { color: #93a1a1; cursor: pointer; }
.cm-s-solarized .cm-special { color: #6c71c4; }
.cm-s-solarized .cm-em {
  color: #999;
  text-decoration: underline;
  text-decoration-style: dotted;
}
.cm-s-solarized .cm-error,
.cm-s-solarized .cm-invalidchar {
  color: #586e75;
  border-bottom: 1px dotted #dc322f;
}

.cm-s-solarized.cm-s-dark div.CodeMirror-selected { background: #073642; }
.cm-s-solarized.cm-s-dark.CodeMirror ::selection { background: rgba(7, 54, 66, 0.99); }
.cm-s-solarized.cm-s-dark .CodeMirror-line::-moz-selection, .cm-s-dark .CodeMirror-line > span::-moz-selection, .cm-s-dark .CodeMirror-line > span > span::-moz-selection { background: rgba(7, 54, 66, 0.99); }

.cm-s-solarized.cm-s-light div.CodeMirror-selected { background: #eee8d5; }
.cm-s-solarized.cm-s-light .CodeMirror-line::selection, .cm-s-light .CodeMirror-line > span::selection, .cm-s-light .CodeMirror-line > span > span::selection { background: #eee8d5; }
.cm-s-solarized.cm-s-light .CodeMirror-line::-moz-selection, .cm-s-ligh .CodeMirror-line > span::-moz-selection, .cm-s-ligh .CodeMirror-line > span > span::-moz-selection { background: #eee8d5; }

/* Editor styling */



/* Little shadow on the view-port of the buffer view */
.cm-s-solarized.CodeMirror {
  -moz-box-shadow: inset 7px 0 12px -6px #000;
  -webkit-box-shadow: inset 7px 0 12px -6px #000;
  box-shadow: inset 7px 0 12px -6px #000;
}

/* Remove gutter border */
.cm-s-solarized .CodeMirror-gutters {
  border-right: 0;
}

/* Gutter colors and line number styling based of color scheme (dark / light) */

/* Dark */
.cm-s-solarized.cm-s-dark .CodeMirror-gutters {
  background-color: #073642;
}

.cm-s-solarized.cm-s-dark .CodeMirror-linenumber {
  color: #586e75;
  text-shadow: #021014 0 -1px;
}

/* Light */
.cm-s-solarized.cm-s-light .CodeMirror-gutters {
  background-color: #eee8d5;
}

.cm-s-solarized.cm-s-light .CodeMirror-linenumber {
  color: #839496;
}

/* Common */
.cm-s-solarized .CodeMirror-linenumber {
  padding: 0 5px;
}
.cm-s-solarized .CodeMirror-guttermarker-subtle { color: #586e75; }
.cm-s-solarized.cm-s-dark .CodeMirror-guttermarker { color: #ddd; }
.cm-s-solarized.cm-s-light .CodeMirror-guttermarker { color: #cb4b16; }

.cm-s-solarized .CodeMirror-gutter .CodeMirror-gutter-text {
  color: #586e75;
}

/* Cursor */
.cm-s-solarized .CodeMirror-cursor { border-left: 1px solid #819090; }

/* Fat cursor */
.cm-s-solarized.cm-s-light.cm-fat-cursor .CodeMirror-cursor { background: #77ee77; }
.cm-s-solarized.cm-s-light .cm-animate-fat-cursor { background-color: #77ee77; }
.cm-s-solarized.cm-s-dark.cm-fat-cursor .CodeMirror-cursor { background: #586e75; }
.cm-s-solarized.cm-s-dark .cm-animate-fat-cursor { background-color: #586e75; }

/* Active line */
.cm-s-solarized.cm-s-dark .CodeMirror-activeline-background {
  background: rgba(255, 255, 255, 0.06);
}
.cm-s-solarized.cm-s-light .CodeMirror-activeline-background {
  background: rgba(0, 0, 0, 0.06);
}

.cm-s-the-matrix.CodeMirror { background: #000000; color: #00FF00; }
.cm-s-the-matrix div.CodeMirror-selected { background: #2D2D2D; }
.cm-s-the-matrix .CodeMirror-line::selection, .cm-s-the-matrix .CodeMirror-line > span::selection, .cm-s-the-matrix .CodeMirror-line > span > span::selection { background: rgba(45, 45, 45, 0.99); }
.cm-s-the-matrix .CodeMirror-line::-moz-selection, .cm-s-the-matrix .CodeMirror-line > span::-moz-selection, .cm-s-the-matrix .CodeMirror-line > span > span::-moz-selection { background: rgba(45, 45, 45, 0.99); }
.cm-s-the-matrix .CodeMirror-gutters { background: #060; border-right: 2px solid #00FF00; }
.cm-s-the-matrix .CodeMirror-guttermarker { color: #0f0; }
.cm-s-the-matrix .CodeMirror-guttermarker-subtle { color: white; }
.cm-s-the-matrix .CodeMirror-linenumber { color: #FFFFFF; }
.cm-s-the-matrix .CodeMirror-cursor { border-left: 1px solid #00FF00; }

.cm-s-the-matrix span.cm-keyword { color: #008803; font-weight: bold; }
.cm-s-the-matrix span.cm-atom { color: #3FF; }
.cm-s-the-matrix span.cm-number { color: #FFB94F; }
.cm-s-the-matrix span.cm-def { color: #99C; }
.cm-s-the-matrix span.cm-variable { color: #F6C; }
.cm-s-the-matrix span.cm-variable-2 { color: #C6F; }
.cm-s-the-matrix span.cm-variable-3, .cm-s-the-matrix span.cm-type { color: #96F; }
.cm-s-the-matrix span.cm-property { color: #62FFA0; }
.cm-s-the-matrix span.cm-operator { color: #999; }
.cm-s-the-matrix span.cm-comment { color: #CCCCCC; }
.cm-s-the-matrix span.cm-string { color: #39C; }
.cm-s-the-matrix span.cm-meta { color: #C9F; }
.cm-s-the-matrix span.cm-qualifier { color: #FFF700; }
.cm-s-the-matrix span.cm-builtin { color: #30a; }
.cm-s-the-matrix span.cm-bracket { color: #cc7; }
.cm-s-the-matrix span.cm-tag { color: #FFBD40; }
.cm-s-the-matrix span.cm-attribute { color: #FFF700; }
.cm-s-the-matrix span.cm-error { color: #FF0000; }

.cm-s-the-matrix .CodeMirror-activeline-background { background: #040; }

/*
Copyright (C) 2011 by MarkLogic Corporation
Author: Mike Brevoort <mike@brevoort.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
*/
.cm-s-xq-light span.cm-keyword { line-height: 1em; font-weight: bold; color: #5A5CAD; }
.cm-s-xq-light span.cm-atom { color: #6C8CD5; }
.cm-s-xq-light span.cm-number { color: #164; }
.cm-s-xq-light span.cm-def { text-decoration:underline; }
.cm-s-xq-light span.cm-variable { color: black; }
.cm-s-xq-light span.cm-variable-2 { color:black; }
.cm-s-xq-light span.cm-variable-3, .cm-s-xq-light span.cm-type { color: black; }
.cm-s-xq-light span.cm-property {}
.cm-s-xq-light span.cm-operator {}
.cm-s-xq-light span.cm-comment { color: #0080FF; font-style: italic; }
.cm-s-xq-light span.cm-string { color: red; }
.cm-s-xq-light span.cm-meta { color: yellow; }
.cm-s-xq-light span.cm-qualifier { color: grey; }
.cm-s-xq-light span.cm-builtin { color: #7EA656; }
.cm-s-xq-light span.cm-bracket { color: #cc7; }
.cm-s-xq-light span.cm-tag { color: #3F7F7F; }
.cm-s-xq-light span.cm-attribute { color: #7F007F; }
.cm-s-xq-light span.cm-error { color: #f00; }

.cm-s-xq-light .CodeMirror-activeline-background { background: #e8f2ff; }
.cm-s-xq-light .CodeMirror-matchingbracket { outline:1px solid grey;color:black !important;background:yellow; }

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.CodeMirror {
  line-height: var(--jp-code-line-height);
  font-size: var(--jp-code-font-size);
  font-family: var(--jp-code-font-family);
  border: 0;
  border-radius: 0;
  height: auto;
  /* Changed to auto to autogrow */
}

.CodeMirror pre {
  padding: 0 var(--jp-code-padding);
}

.jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-dialog {
  background-color: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

/* This causes https://github.com/jupyter/jupyterlab/issues/522 */
/* May not cause it not because we changed it! */
.CodeMirror-lines {
  padding: var(--jp-code-padding) 0;
}

.CodeMirror-linenumber {
  padding: 0 8px;
}

.jp-CodeMirrorEditor-static {
  margin: var(--jp-code-padding);
}

.jp-CodeMirrorEditor,
.jp-CodeMirrorEditor-static {
  cursor: text;
}

.jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
  border-left: var(--jp-code-cursor-width0) solid var(--jp-editor-cursor-color);
}

/* When zoomed out 67% and 33% on a screen of 1440 width x 900 height */
@media screen and (min-width: 2138px) and (max-width: 4319px) {
  .jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
    border-left: var(--jp-code-cursor-width1) solid
      var(--jp-editor-cursor-color);
  }
}

/* When zoomed out less than 33% */
@media screen and (min-width: 4320px) {
  .jp-CodeMirrorEditor[data-type='inline'] .CodeMirror-cursor {
    border-left: var(--jp-code-cursor-width2) solid
      var(--jp-editor-cursor-color);
  }
}

.CodeMirror.jp-mod-readOnly .CodeMirror-cursor {
  display: none;
}

.CodeMirror-gutters {
  border-right: 1px solid var(--jp-border-color2);
  background-color: var(--jp-layout-color0);
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

.CodeMirror-selectedtext.cm-searching {
  background-color: var(--jp-search-selected-match-background-color) !important;
  color: var(--jp-search-selected-match-color) !important;
}

.cm-searching {
  background-color: var(
    --jp-search-unselected-match-background-color
  ) !important;
  color: var(--jp-search-unselected-match-color) !important;
}

.CodeMirror-focused .CodeMirror-selected {
  background-color: var(--jp-editor-selected-focused-background);
}

.CodeMirror-selected {
  background-color: var(--jp-editor-selected-background);
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

/**
 * Here is our jupyter theme for CodeMirror syntax highlighting
 * This is used in our marked.js syntax highlighting and CodeMirror itself
 * The string "jupyter" is set in ../codemirror/widget.DEFAULT_CODEMIRROR_THEME
 * This came from the classic notebook, which came form highlight.js/GitHub
 */

/**
 * CodeMirror themes are handling the background/color in this way. This works
 * fine for CodeMirror editors outside the notebook, but the notebook styles
 * these things differently.
 */
.CodeMirror.cm-s-jupyter {
  background: var(--jp-layout-color0);
  color: var(--jp-content-font-color1);
}

/* In the notebook, we want this styling to be handled by its container */
.jp-CodeConsole .CodeMirror.cm-s-jupyter,
.jp-Notebook .CodeMirror.cm-s-jupyter {
  background: transparent;
}

.cm-s-jupyter .CodeMirror-cursor {
  border-left: var(--jp-code-cursor-width0) solid var(--jp-editor-cursor-color);
}
.cm-s-jupyter span.cm-keyword {
  color: var(--jp-mirror-editor-keyword-color);
  font-weight: bold;
}
.cm-s-jupyter span.cm-atom {
  color: var(--jp-mirror-editor-atom-color);
}
.cm-s-jupyter span.cm-number {
  color: var(--jp-mirror-editor-number-color);
}
.cm-s-jupyter span.cm-def {
  color: var(--jp-mirror-editor-def-color);
}
.cm-s-jupyter span.cm-variable {
  color: var(--jp-mirror-editor-variable-color);
}
.cm-s-jupyter span.cm-variable-2 {
  color: var(--jp-mirror-editor-variable-2-color);
}
.cm-s-jupyter span.cm-variable-3 {
  color: var(--jp-mirror-editor-variable-3-color);
}
.cm-s-jupyter span.cm-punctuation {
  color: var(--jp-mirror-editor-punctuation-color);
}
.cm-s-jupyter span.cm-property {
  color: var(--jp-mirror-editor-property-color);
}
.cm-s-jupyter span.cm-operator {
  color: var(--jp-mirror-editor-operator-color);
  font-weight: bold;
}
.cm-s-jupyter span.cm-comment {
  color: var(--jp-mirror-editor-comment-color);
  font-style: italic;
}
.cm-s-jupyter span.cm-string {
  color: var(--jp-mirror-editor-string-color);
}
.cm-s-jupyter span.cm-string-2 {
  color: var(--jp-mirror-editor-string-2-color);
}
.cm-s-jupyter span.cm-meta {
  color: var(--jp-mirror-editor-meta-color);
}
.cm-s-jupyter span.cm-qualifier {
  color: var(--jp-mirror-editor-qualifier-color);
}
.cm-s-jupyter span.cm-builtin {
  color: var(--jp-mirror-editor-builtin-color);
}
.cm-s-jupyter span.cm-bracket {
  color: var(--jp-mirror-editor-bracket-color);
}
.cm-s-jupyter span.cm-tag {
  color: var(--jp-mirror-editor-tag-color);
}
.cm-s-jupyter span.cm-attribute {
  color: var(--jp-mirror-editor-attribute-color);
}
.cm-s-jupyter span.cm-header {
  color: var(--jp-mirror-editor-header-color);
}
.cm-s-jupyter span.cm-quote {
  color: var(--jp-mirror-editor-quote-color);
}
.cm-s-jupyter span.cm-link {
  color: var(--jp-mirror-editor-link-color);
}
.cm-s-jupyter span.cm-error {
  color: var(--jp-mirror-editor-error-color);
}
.cm-s-jupyter span.cm-hr {
  color: #999;
}

.cm-s-jupyter span.cm-tab {
  background: url(data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAADAAAAAMCAYAAAAkuj5RAAAAAXNSR0IArs4c6QAAAGFJREFUSMft1LsRQFAQheHPowAKoACx3IgEKtaEHujDjORSgWTH/ZOdnZOcM/sgk/kFFWY0qV8foQwS4MKBCS3qR6ixBJvElOobYAtivseIE120FaowJPN75GMu8j/LfMwNjh4HUpwg4LUAAAAASUVORK5CYII=);
  background-position: right;
  background-repeat: no-repeat;
}

.cm-s-jupyter .CodeMirror-activeline-background,
.cm-s-jupyter .CodeMirror-gutter {
  background-color: var(--jp-layout-color2);
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| RenderedText
|----------------------------------------------------------------------------*/

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
  margin: 0px;
  padding: 0px;
  line-height: normal;
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
}
.jp-RenderedText pre .ansi-red-bg {
  background-color: #e75c58;
}
.jp-RenderedText pre .ansi-green-bg {
  background-color: #00a250;
}
.jp-RenderedText pre .ansi-yellow-bg {
  background-color: #ddb62b;
}
.jp-RenderedText pre .ansi-blue-bg {
  background-color: #208ffb;
}
.jp-RenderedText pre .ansi-magenta-bg {
  background-color: #d160c4;
}
.jp-RenderedText pre .ansi-cyan-bg {
  background-color: #60c6c8;
}
.jp-RenderedText pre .ansi-white-bg {
  background-color: #c5c1b4;
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
}
.jp-RenderedText pre .ansi-red-intense-bg {
  background-color: #b22b31;
}
.jp-RenderedText pre .ansi-green-intense-bg {
  background-color: #007427;
}
.jp-RenderedText pre .ansi-yellow-intense-bg {
  background-color: #b27d12;
}
.jp-RenderedText pre .ansi-blue-intense-bg {
  background-color: #0065ca;
}
.jp-RenderedText pre .ansi-magenta-intense-bg {
  background-color: #a03196;
}
.jp-RenderedText pre .ansi-cyan-intense-bg {
  background-color: #258f8f;
}
.jp-RenderedText pre .ansi-white-intense-bg {
  background-color: #a1a6b2;
}

.jp-RenderedText pre .ansi-default-inverse-fg {
  color: var(--jp-ui-inverse-font-color0);
}
.jp-RenderedText pre .ansi-default-inverse-bg {
  background-color: var(--jp-inverse-layout-color0);
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
  margin-bottom: 0em;
}

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
  font-size: 12px;
  table-layout: fixed;
  margin-left: auto;
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
  padding: 0.5em 0.5em;
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

.jp-RenderedHTMLCommon table {
  margin-bottom: 1em;
}

.jp-RenderedHTMLCommon p {
  text-align: left;
  margin: 0px;
}

.jp-RenderedHTMLCommon p {
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
/* ...or leave it untouched if they don't */
[data-jp-theme-light='false'] .jp-RenderedImage img.jp-needs-dark-background {
}
[data-jp-theme-light='true'] .jp-RenderedImage img.jp-needs-light-background {
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
  font-size: 0.8em;
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

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

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

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

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
  --jp-private-filebrowser-button-height: 28px;
  --jp-private-filebrowser-button-width: 48px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-FileBrowser {
  display: flex;
  flex-direction: column;
  color: var(--jp-ui-font-color1);
  background: var(--jp-layout-color1);
  /* This is needed so that all font sizing of children done in ems is
   * relative to this base size */
  font-size: var(--jp-ui-font-size1);
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  border-bottom: none;
  height: auto;
  margin: var(--jp-toolbar-header-margin);
  box-shadow: none;
}

.jp-BreadCrumbs {
  flex: 0 0 auto;
  margin: 4px 12px;
}

.jp-BreadCrumbs-item {
  margin: 0px 2px;
  padding: 0px 2px;
  border-radius: var(--jp-border-radius);
  cursor: pointer;
}

.jp-BreadCrumbs-item:hover {
  background-color: var(--jp-layout-color2);
}

.jp-BreadCrumbs-item:first-child {
  margin-left: 0px;
}

.jp-BreadCrumbs-item.jp-mod-dropTarget {
  background-color: var(--jp-brand-color2);
  opacity: 0.7;
}

/*-----------------------------------------------------------------------------
| Buttons
|----------------------------------------------------------------------------*/

.jp-FileBrowser-toolbar.jp-Toolbar {
  padding: 0px;
}

.jp-FileBrowser-toolbar.jp-Toolbar {
  justify-content: space-evenly;
}

.jp-FileBrowser-toolbar.jp-Toolbar .jp-Toolbar-item {
  flex: 1;
}

.jp-FileBrowser-toolbar.jp-Toolbar .jp-ToolbarButtonComponent {
  width: 100%;
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
  overflow: hidden;
  border-top: var(--jp-border-width) solid var(--jp-border-color2);
  border-bottom: var(--jp-border-width) solid var(--jp-border-color1);
  box-shadow: var(--jp-toolbar-box-shadow);
  z-index: 2;
}

.jp-DirListing-headerItem {
  padding: 4px 12px 2px 12px;
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

/* Style the directory listing content when a user drops a file to upload */
.jp-DirListing.jp-mod-native-drop .jp-DirListing-content {
  outline: 5px dashed rgba(128, 128, 128, 0.5);
  outline-offset: -10px;
  cursor: copy;
}

.jp-DirListing-item {
  display: flex;
  flex-direction: row;
  padding: 4px 12px;
  -webkit-user-select: none;
  -moz-user-select: none;
  -ms-user-select: none;
  user-select: none;
}

.jp-DirListing-item.jp-mod-selected {
  color: white;
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

.jp-DirListing-itemModified {
  flex: 0 0 125px;
  text-align: right;
}

.jp-DirListing-editor {
  flex: 1 0 64px;
  outline: none;
  border: none;
}

.jp-DirListing-item.jp-mod-running .jp-DirListing-itemIcon:before {
  color: limegreen;
  content: '\25CF';
  font-size: 8px;
  position: absolute;
  left: -8px;
}

.jp-DirListing-item.lm-mod-drag-image,
.jp-DirListing-item.jp-mod-selected.lm-mod-drag-image {
  font-size: var(--jp-ui-font-size1);
  padding-left: 4px;
  margin-left: 4px;
  width: 160px;
  background-color: var(--jp-ui-inverse-font-color2);
  box-shadow: var(--jp-elevation-z2);
  border-radius: 0px;
  color: var(--jp-ui-font-color1);
  transform: translateX(-40%) translateY(-58%);
}

.jp-DirListing-deadSpace {
  flex: 1 1 auto;
  margin: 0;
  padding: 0;
  list-style-type: none;
  overflow: auto;
  background-color: var(--jp-layout-color1);
}

.jp-Document {
  min-width: 120px;
  min-height: 120px;
  outline: none;
}

.jp-FileDialog.jp-mod-conflict input {
  color: red;
}

.jp-FileDialog .jp-new-name-title {
  margin-top: 12px;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
}

/*-----------------------------------------------------------------------------
| Main OutputArea
| OutputArea has a list of Outputs
|----------------------------------------------------------------------------*/

.jp-OutputArea {
  overflow-y: auto;
}

.jp-OutputArea-child {
  display: flex;
  flex-direction: row;
}

.jp-OutputPrompt {
  flex: 0 0 var(--jp-cell-prompt-width);
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

.jp-OutputArea-output {
  height: auto;
  overflow: auto;
  user-select: text;
  -moz-user-select: text;
  -webkit-user-select: text;
  -ms-user-select: text;
}

.jp-OutputArea-child .jp-OutputArea-output {
  flex-grow: 1;
  flex-shrink: 1;
}

/**
 * Isolated output.
 */
.jp-OutputArea-output.jp-mod-isolated {
  width: 100%;
  display: block;
}

/*
When drag events occur, `p-mod-override-cursor` is added to the body.
Because iframes steal all cursor events, the following two rules are necessary
to suppress pointer events while resize drags are occurring. There may be a
better solution to this problem.
*/
body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated {
  position: relative;
}

body.lm-mod-override-cursor .jp-OutputArea-output.jp-mod-isolated:before {
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
  margin: 0px;
  padding: 0px;
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

/* Hide the gutter in case of
 *  - nested output areas (e.g. in the case of output widgets)
 *  - mirrored output areas
 */
.jp-OutputArea .jp-OutputArea .jp-OutputArea-prompt {
  display: none;
}

/*-----------------------------------------------------------------------------
| executeResult is added to any Output-result for the display of the object
| returned by a cell
|----------------------------------------------------------------------------*/

.jp-OutputArea-output.jp-OutputArea-executeResult {
  margin-left: 0px;
  flex: 1 1 auto;
}

.jp-OutputArea-executeResult.jp-RenderedText {
  padding-top: var(--jp-code-padding);
}

/*-----------------------------------------------------------------------------
| The Stdin output
|----------------------------------------------------------------------------*/

.jp-OutputArea-stdin {
  line-height: var(--jp-code-line-height);
  padding-top: var(--jp-code-padding);
  display: flex;
}

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
  padding: 0em 0.25em;
  margin: 0em 0.25em;
  flex: 0 0 70%;
}

.jp-Stdin-input:focus {
  box-shadow: none;
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
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

.jp-Collapser {
  flex: 0 0 var(--jp-cell-collapser-width);
  padding: 0px;
  margin: 0px;
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
  top: 0px;
  bottom: 0px;
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
  height: 0px;
  width: 100%;
  padding: 0px;
  margin: 0px;
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
  display: flex;
  flex-direction: row;
}

.jp-InputArea-editor {
  flex: 1 1 auto;
}

.jp-InputArea-editor {
  /* This is the non-active, default styling */
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  border-radius: 0px;
  background: var(--jp-cell-editor-background);
}

.jp-InputPrompt {
  flex: 0 0 var(--jp-cell-prompt-width);
  color: var(--jp-cell-inprompt-font-color);
  font-family: var(--jp-cell-prompt-font-family);
  padding: var(--jp-code-padding);
  letter-spacing: var(--jp-cell-prompt-letter-spacing);
  opacity: var(--jp-cell-prompt-opacity);
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

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Placeholder
|----------------------------------------------------------------------------*/

.jp-Placeholder {
  display: flex;
  flex-direction: row;
  flex: 1 1 auto;
}

.jp-Placeholder-prompt {
  box-sizing: border-box;
}

.jp-Placeholder-content {
  flex: 1 1 auto;
  border: none;
  background: transparent;
  height: 20px;
  box-sizing: border-box;
}

.jp-Placeholder-content .jp-MoreHorizIcon {
  width: 32px;
  height: 16px;
  border: 1px solid transparent;
  border-radius: var(--jp-border-radius);
}

.jp-Placeholder-content .jp-MoreHorizIcon:hover {
  border: 1px solid var(--jp-border-color1);
  box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.25);
  background-color: var(--jp-layout-color0);
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
  margin: 0px;
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
  padding: 0px;
  margin: 0px;
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

/* Text output with the Out[] prompt needs a top padding to match the
 * alignment of the Out[] prompt itself.
 */
.jp-OutputArea-executeResult .jp-RenderedText.jp-OutputArea-output {
  padding-top: var(--jp-code-padding);
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-Cell-outputArea {
  overflow-y: auto;
  max-height: 200px;
  box-shadow: inset 0 0 6px 2px rgba(0, 0, 0, 0.3);
  margin-left: var(--jp-private-cell-scrolling-output-offset);
}

.jp-CodeCell.jp-mod-outputsScrolled .jp-OutputArea-prompt {
  flex: 0 0
    calc(
      var(--jp-cell-prompt-width) -
        var(--jp-private-cell-scrolling-output-offset)
    );
}

/*-----------------------------------------------------------------------------
| CodeCell
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| MarkdownCell
|----------------------------------------------------------------------------*/

.jp-MarkdownOutput {
  flex: 1 1 auto;
  margin-top: 0;
  margin-bottom: 0;
  padding-left: var(--jp-code-padding);
}

.jp-MarkdownOutput.jp-RenderedHTMLCommon {
  overflow: auto;
}

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

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

.jp-NotebookPanel-toolbar {
  padding: 2px;
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

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Private CSS variables
|----------------------------------------------------------------------------*/

:root {
  --jp-private-notebook-dragImage-width: 304px;
  --jp-private-notebook-dragImage-height: 36px;
  --jp-private-notebook-selected-color: var(--md-blue-400);
  --jp-private-notebook-active-color: var(--md-green-400);
}

/*-----------------------------------------------------------------------------
| Imports
|----------------------------------------------------------------------------*/

/*-----------------------------------------------------------------------------
| Notebook
|----------------------------------------------------------------------------*/

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
  display: flex;
  flex-direction: row;
  width: var(--jp-private-notebook-dragImage-width);
  height: var(--jp-private-notebook-dragImage-height);
  border: var(--jp-border-width) solid var(--jp-cell-editor-border-color);
  background: var(--jp-cell-editor-background);
  overflow: visible;
}

.jp-dragImage-singlePrompt {
  box-shadow: 2px 2px 4px 0px rgba(0, 0, 0, 0.12);
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
  margin: 4px 4px 4px 0px;
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
  box-shadow: 2px 2px 4px 0px rgba(0, 0, 0, 0.12);
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

.jp-NotebookTools-tool {
  padding: 0px 12px 0 12px;
}

.jp-ActiveCellTool {
  padding: 12px;
  background-color: var(--jp-layout-color1);
  border-top: none !important;
}

.jp-ActiveCellTool .jp-InputArea-prompt {
  flex: 0 0 auto;
  padding-left: 0px;
}

.jp-ActiveCellTool .jp-InputArea-editor {
  flex: 1 1 auto;
  background: var(--jp-cell-editor-background);
  border-color: var(--jp-cell-editor-border-color);
}

.jp-ActiveCellTool .jp-InputArea-editor .CodeMirror {
  background: transparent;
}

.jp-MetadataEditorTool {
  flex-direction: column;
  padding: 12px 0px 12px 0px;
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
.jp-MetadataEditorTool label {
  line-height: 1.4;
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
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

/* This file was auto-generated by ensurePackage() in @jupyterlab/buildutils */

/*-----------------------------------------------------------------------------
| Copyright (c) Jupyter Development Team.
| Distributed under the terms of the Modified BSD License.
|----------------------------------------------------------------------------*/

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
  --jp-elevation-z1: 0px 2px 1px -1px var(--jp-shadow-umbra-color),
    0px 1px 1px 0px var(--jp-shadow-penumbra-color),
    0px 1px 3px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z2: 0px 3px 1px -2px var(--jp-shadow-umbra-color),
    0px 2px 2px 0px var(--jp-shadow-penumbra-color),
    0px 1px 5px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z4: 0px 2px 4px -1px var(--jp-shadow-umbra-color),
    0px 4px 5px 0px var(--jp-shadow-penumbra-color),
    0px 1px 10px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z6: 0px 3px 5px -1px var(--jp-shadow-umbra-color),
    0px 6px 10px 0px var(--jp-shadow-penumbra-color),
    0px 1px 18px 0px var(--jp-shadow-ambient-color);
  --jp-elevation-z8: 0px 5px 5px -3px var(--jp-shadow-umbra-color),
    0px 8px 10px 1px var(--jp-shadow-penumbra-color),
    0px 3px 14px 2px var(--jp-shadow-ambient-color);
  --jp-elevation-z12: 0px 7px 8px -4px var(--jp-shadow-umbra-color),
    0px 12px 17px 2px var(--jp-shadow-penumbra-color),
    0px 5px 22px 4px var(--jp-shadow-ambient-color);
  --jp-elevation-z16: 0px 8px 10px -5px var(--jp-shadow-umbra-color),
    0px 16px 24px 2px var(--jp-shadow-penumbra-color),
    0px 6px 30px 5px var(--jp-shadow-ambient-color);
  --jp-elevation-z20: 0px 10px 13px -6px var(--jp-shadow-umbra-color),
    0px 20px 31px 3px var(--jp-shadow-penumbra-color),
    0px 8px 38px 7px var(--jp-shadow-ambient-color);
  --jp-elevation-z24: 0px 11px 15px -7px var(--jp-shadow-umbra-color),
    0px 24px 38px 3px var(--jp-shadow-penumbra-color),
    0px 9px 46px 8px var(--jp-shadow-ambient-color);

  /* Borders
   *
   * The following variables, specify the visual styling of borders in JupyterLab.
   */

  --jp-border-width: 1px;
  --jp-border-color0: var(--md-grey-400);
  --jp-border-color1: var(--md-grey-400);
  --jp-border-color2: var(--md-grey-300);
  --jp-border-color3: var(--md-grey-200);
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

  --jp-ui-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Helvetica,
    Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji', 'Segoe UI Symbol';

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

  --jp-content-link-color: var(--md-blue-700);

  --jp-content-font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI',
    Helvetica, Arial, sans-serif, 'Apple Color Emoji', 'Segoe UI Emoji',
    'Segoe UI Symbol';

  /*
   * Code Fonts
   *
   * Code font variables are used for typography of code and other monospaces content.
   */

  --jp-code-font-size: 13px;
  --jp-code-line-height: 1.3077; /* 17px for 13px base */
  --jp-code-padding: 5px; /* 5px for 13px base, codemirror highlighting needs integer px value */
  --jp-code-font-family-default: Menlo, Consolas, 'DejaVu Sans Mono', monospace;
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

  --jp-inverse-layout-color0: #111111;
  --jp-inverse-layout-color1: var(--md-grey-900);
  --jp-inverse-layout-color2: var(--md-grey-800);
  --jp-inverse-layout-color3: var(--md-grey-700);
  --jp-inverse-layout-color4: var(--md-grey-600);

  /* Brand/accent */

  --jp-brand-color0: var(--md-blue-700);
  --jp-brand-color1: var(--md-blue-500);
  --jp-brand-color2: var(--md-blue-300);
  --jp-brand-color3: var(--md-blue-100);
  --jp-brand-color4: var(--md-blue-50);

  --jp-accent-color0: var(--md-green-700);
  --jp-accent-color1: var(--md-green-500);
  --jp-accent-color2: var(--md-green-300);
  --jp-accent-color3: var(--md-green-100);

  /* State colors (warn, error, success, info) */

  --jp-warn-color0: var(--md-orange-700);
  --jp-warn-color1: var(--md-orange-500);
  --jp-warn-color2: var(--md-orange-300);
  --jp-warn-color3: var(--md-orange-100);

  --jp-error-color0: var(--md-red-700);
  --jp-error-color1: var(--md-red-500);
  --jp-error-color2: var(--md-red-300);
  --jp-error-color3: var(--md-red-100);

  --jp-success-color0: var(--md-green-700);
  --jp-success-color1: var(--md-green-500);
  --jp-success-color2: var(--md-green-300);
  --jp-success-color3: var(--md-green-100);

  --jp-info-color0: var(--md-cyan-700);
  --jp-info-color1: var(--md-cyan-500);
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
  --jp-cell-prompt-font-family: 'Source Code Pro', monospace;
  --jp-cell-prompt-letter-spacing: 0px;
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
  --jp-toolbar-box-shadow: 0px 0px 2px 0px rgba(0, 0, 0, 0.24);
  --jp-toolbar-header-margin: 4px 4px 0px 4px;
  --jp-toolbar-active-background: var(--md-grey-300);

  /* Input field styles */

  --jp-input-box-shadow: inset 0 0 2px var(--md-blue-300);
  --jp-input-active-background: var(--jp-layout-color1);
  --jp-input-hover-background: var(--jp-layout-color1);
  --jp-input-background: var(--md-grey-100);
  --jp-input-border-color: var(--jp-border-color1);
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
  --jp-mirror-editor-variable-2-color: #05a;
  --jp-mirror-editor-variable-3-color: #085;
  --jp-mirror-editor-punctuation-color: #05a;
  --jp-mirror-editor-property-color: #05a;
  --jp-mirror-editor-operator-color: #aa22ff;
  --jp-mirror-editor-comment-color: #408080;
  --jp-mirror-editor-string-color: #ba2121;
  --jp-mirror-editor-string-2-color: #708;
  --jp-mirror-editor-meta-color: #aa22ff;
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

  /* Vega extension styles */

  --jp-vega-background: white;

  /* Sidebar-related styles */

  --jp-sidebar-min-width: 180px;

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
}
</style>

<style type="text/css">
a.anchor-link {
   display: none;
}
.highlight  {
    margin: 0.4em;
}

/* Input area styling */
.jp-InputArea {
    overflow: hidden;
}

.jp-InputArea-editor {
    overflow: hidden;
}

@media print {
  body {
    margin: 0;
  }
}
</style>



<!-- Load mathjax -->
    <script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/latest.js?config=TeX-MML-AM_CHTML-full,Safe"> </script>
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
                },
                "HTML-CSS": {
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
    <!-- End of mathjax configuration --></head>
<body class="jp-Notebook" data-jp-theme-light="true" data-jp-theme-name="JupyterLab Light">

<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h1 id="Analyzing-COVID-19-Lethality-By-Patient">Analyzing COVID-19 Lethality By Patient<a class="anchor-link" href="#Analyzing-COVID-19-Lethality-By-Patient">&#182;</a></h1><p><strong>By Aaron Dixon</strong></p>
<h2 id="Introduction">Introduction<a class="anchor-link" href="#Introduction">&#182;</a></h2><p>This tutorial will walk you through the process of the data science pipeline, from collecting data to analyzing it for insights. The goal of this particular tutorial is to analyze records of individual COVID-19 cases in order to determine what data about the patients, if any, has a correlation with whether or not that patient died. We will see how well we can predict whether a patient with COVID-19 will die based on demographic data (age, sex, and race) as well as the presence of any pre-existing medical conditions.</p>
<p>This analysis is important for the purpose of responding to COVID-19 effectively - by knowing which groups are at higher risk of death if they contract COVID-19, we know which groups require more resources and effort put into both reducing their chances of contracting COVID-19 and treating them if they do contract it. Given how widespread COVID-19 has been, and how severely it has impacted and continues to impact us all, making this analysis for COVID-19 is particularly important.</p>
<h2 id="Setup">Setup<a class="anchor-link" href="#Setup">&#182;</a></h2><p>The following cell imports all of the libraries needed to import, process, visualize, and anlayze our data.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[1]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="kn">import</span> <span class="nn">pandas</span> <span class="k">as</span> <span class="nn">pd</span>
<span class="kn">import</span> <span class="nn">numpy</span> <span class="k">as</span> <span class="nn">np</span>
<span class="kn">from</span> <span class="nn">matplotlib</span> <span class="kn">import</span> <span class="n">pyplot</span> <span class="k">as</span> <span class="n">plt</span>
<span class="kn">import</span> <span class="nn">seaborn</span> <span class="k">as</span> <span class="nn">sns</span>
<span class="kn">from</span> <span class="nn">sklearn.tree</span> <span class="kn">import</span> <span class="n">DecisionTreeClassifier</span>
<span class="kn">from</span> <span class="nn">sklearn.svm</span> <span class="kn">import</span> <span class="n">SVC</span>
<span class="kn">import</span> <span class="nn">sklearn.model_selection</span> <span class="k">as</span> <span class="nn">ms</span>
<span class="kn">import</span> <span class="nn">sklearn.metrics</span> <span class="k">as</span> <span class="nn">met</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Data-Collection">Data Collection<a class="anchor-link" href="#Data-Collection">&#182;</a></h2><p>The dataset we will be using for this analysis is the <a href="https://data.cdc.gov/Case-Surveillance/COVID-19-Case-Surveillance-Public-Use-Data/vbim-akqf">COVID-19 Case Surveillance Public Use Data</a> made available by the CDC. This data set gives information on individual patients' demographics and outcomes from COVID-19, which we will need to analyze COVID-19 deaths on a patient-by-patient basis.</p>
<p>I downloaded this dataset as a CSV file from the website. However, because the dataset contains a massive amount of data - over 27 million lines - it was impractical to work with the entire dataset. Instead, I downloaded a filtered version of the dataset that only contains data on patients whose cdc_case_earliest_dt (a column containing the earliest of the date the case was reported to the CDC, the date of first symptom onset, and first positive specimen collection) was January 1st, 2021.</p>
<p>I chose this date because it was late enough in the pandemic that health care providers mostly knew how best to treat COVID-19, but early enough that any case which started on this date would have come to a conclusion, either death or recovery, by now. Also, by selecting which rows to keep purely by date, it is unlikely that I would have introduced bias regarding the relative likelihood of different demographics to die into the data. This also removes date as a factor in death rate, allowing us to only focus on what characteristics of a patient affect risk of death.</p>
<p>The following cell loads the data from the csv file into a Pandas DataFrame.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[2]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">read_csv</span><span class="p">(</span><span class="s2">&quot;COVID-19_Case_Surveillance_Public_Use_Data.csv&quot;</span><span class="p">)</span>
<span class="n">df</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[2]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
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
      <th>cdc_case_earliest_dt</th>
      <th>cdc_report_dt</th>
      <th>pos_spec_dt</th>
      <th>onset_dt</th>
      <th>current_status</th>
      <th>sex</th>
      <th>age_group</th>
      <th>race_ethnicity_combined</th>
      <th>hosp_yn</th>
      <th>icu_yn</th>
      <th>death_yn</th>
      <th>medcond_yn</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>2021/01/01</td>
      <td>2020/12/31</td>
      <td>2020/12/31</td>
      <td>2021/01/01</td>
      <td>Laboratory-confirmed case</td>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black, Non-Hispanic</td>
      <td>No</td>
      <td>Missing</td>
      <td>No</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2021/01/01</td>
      <td>2021/03/24</td>
      <td>NaN</td>
      <td>2021/01/01</td>
      <td>Laboratory-confirmed case</td>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black, Non-Hispanic</td>
      <td>No</td>
      <td>Missing</td>
      <td>No</td>
      <td>Missing</td>
    </tr>
    <tr>
      <th>2</th>
      <td>2021/01/01</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Laboratory-confirmed case</td>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black, Non-Hispanic</td>
      <td>Missing</td>
      <td>Missing</td>
      <td>No</td>
      <td>Missing</td>
    </tr>
    <tr>
      <th>3</th>
      <td>2021/01/01</td>
      <td>2021/01/16</td>
      <td>NaN</td>
      <td>2021/01/01</td>
      <td>Laboratory-confirmed case</td>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black, Non-Hispanic</td>
      <td>No</td>
      <td>Missing</td>
      <td>No</td>
      <td>Missing</td>
    </tr>
    <tr>
      <th>4</th>
      <td>2021/01/01</td>
      <td>2021/01/04</td>
      <td>NaN</td>
      <td>2021/01/01</td>
      <td>Laboratory-confirmed case</td>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black, Non-Hispanic</td>
      <td>Missing</td>
      <td>Missing</td>
      <td>Missing</td>
      <td>Missing</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<h2 id="Data-Management">Data Management<a class="anchor-link" href="#Data-Management">&#182;</a></h2><p>There are a number of steps we have to take to tidy this data before we can begin analyzing it. First, we want to drop any columns that are irrelevant to our analysis.</p>
<p>This means that the four datetime columns will be dropped, since our analysis does not care when the case began, as long as it began long enough ago that all cases will have run their course by now, which we have already ensured. We are only interested in which qualities of the patient affect their survival chances, not how survival chances of patients have changed over the course of the pandemic.</p>
<p>Additionally, we drop the columns hosp_yn and icu_yn, which describe whether or not the patient was hospitalized or placed in the icu respectively, since we are only concerned with whether patients died or not. We also do not want to use these columns as predictors of whether patients died, since our goal here is to determine which general demographic groups of people are at the most risk of death.</p>
<p>We also drop the current_status column - this column tells us whether the patient's case has actually been tested and confirmed to be COVID-19, or whether it is simply probable to be COVID-19 based on clinical criteria. Since it is likely that more severe cases would be more likely to get tested, while less severe cases may not bother, simply dropping the non-confirmed cases could exclude many less-severe cases and bias our results. Instead, we will trust that the probable cases have been diagnosed accurately and include all cases in our analysis, which means we can drop this column.</p>
<p>The following cell drops these seven columns from the DataFrame.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[3]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;cdc_case_earliest_dt &#39;</span><span class="p">,</span> <span class="s1">&#39;cdc_report_dt&#39;</span><span class="p">,</span> <span class="s1">&#39;pos_spec_dt&#39;</span><span class="p">,</span> <span class="s1">&#39;onset_dt&#39;</span><span class="p">,</span> <span class="s1">&#39;current_status&#39;</span><span class="p">,</span> <span class="s1">&#39;hosp_yn&#39;</span><span class="p">,</span> <span class="s1">&#39;icu_yn&#39;</span><span class="p">],</span> <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[3]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
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
      <th>sex</th>
      <th>age_group</th>
      <th>race_ethnicity_combined</th>
      <th>death_yn</th>
      <th>medcond_yn</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black, Non-Hispanic</td>
      <td>No</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black, Non-Hispanic</td>
      <td>No</td>
      <td>Missing</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black, Non-Hispanic</td>
      <td>No</td>
      <td>Missing</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black, Non-Hispanic</td>
      <td>No</td>
      <td>Missing</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black, Non-Hispanic</td>
      <td>Missing</td>
      <td>Missing</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>For the sake of brevity and easier to read data, we will now also change some column names to be shorter. Additionally, since there is only one value in the race column that is a hispanic identity, we will drop the "Non-Hispanic" from other values in this column, as it will be assumed that a race is non-hispanic if not specified otherwise.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[4]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;race_ethnicity_combined&#39;</span><span class="p">:</span><span class="s1">&#39;race&#39;</span><span class="p">,</span> <span class="s1">&#39;death_yn&#39;</span><span class="p">:</span><span class="s1">&#39;death&#39;</span><span class="p">,</span> <span class="s1">&#39;medcond_yn&#39;</span><span class="p">:</span><span class="s1">&#39;medcond&#39;</span><span class="p">},</span> <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="p">[</span><span class="s1">&#39;race&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">df</span><span class="p">[</span><span class="s1">&#39;race&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">apply</span><span class="p">(</span><span class="k">lambda</span> <span class="n">x</span><span class="p">:</span> <span class="n">x</span><span class="o">.</span><span class="n">replace</span><span class="p">(</span><span class="s1">&#39;, Non-Hispanic&#39;</span><span class="p">,</span><span class="s1">&#39;&#39;</span><span class="p">))</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Next, we want to consider missing values in the data. For the columns that still remain, all missing data is encoded as either "Unknown" (if the question on the data collection form was specifically marked as unknown) or "Missing" (if the question on the data collection form was left blank).</p>
<p>We must now replace these missing values with values that Pandas will actually consider as missing. For our purposes, we have no reason to treat these two missing values differently, so we will replace both of them with pd.NA. If any of these columns contained numeric data, we might instead consider replacing missing values with np.NaN.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[5]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">replace</span><span class="p">([</span><span class="s1">&#39;Missing&#39;</span><span class="p">,</span> <span class="s1">&#39;Unknown&#39;</span><span class="p">],</span> <span class="n">pd</span><span class="o">.</span><span class="n">NA</span><span class="p">,</span> <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[5]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
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
      <th>sex</th>
      <th>age_group</th>
      <th>race</th>
      <th>death</th>
      <th>medcond</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black</td>
      <td>No</td>
      <td>Yes</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black</td>
      <td>No</td>
      <td>&lt;NA&gt;</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black</td>
      <td>No</td>
      <td>&lt;NA&gt;</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black</td>
      <td>No</td>
      <td>&lt;NA&gt;</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black</td>
      <td>&lt;NA&gt;</td>
      <td>&lt;NA&gt;</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>In order to do most forms of analysis on our data, we need to convert some of the categorical variables in our current DataFrame to numerical values. This begins by converting "Yes" and "No" values in the death and medcond columns to 1 and 0 respectively, which the next cell does.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[6]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">replace</span><span class="p">([</span><span class="s1">&#39;Yes&#39;</span><span class="p">,</span><span class="s1">&#39;No&#39;</span><span class="p">],</span> <span class="p">[</span><span class="mi">1</span><span class="p">,</span> <span class="mi">0</span><span class="p">],</span> <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">df</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[6]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
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
      <th>sex</th>
      <th>age_group</th>
      <th>race</th>
      <th>death</th>
      <th>medcond</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black</td>
      <td>0</td>
      <td>&lt;NA&gt;</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black</td>
      <td>0</td>
      <td>&lt;NA&gt;</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black</td>
      <td>0</td>
      <td>&lt;NA&gt;</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Male</td>
      <td>10 - 19 Years</td>
      <td>Black</td>
      <td>&lt;NA&gt;</td>
      <td>&lt;NA&gt;</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>For some forms of analysis - mainly graphs - these modifications are enough. However, for other forms of analysis, we need to convert the remaining columns to numeric variables as well. Thus, we will make further changes on a new, separate DataFrame.</p>
<p>First, we will convert the age groups to numbers. Because the list of age groups has a natural ordering, with older age groups being "greater" in a meaningful sense than younger age groups, it is reasonable to convert these age groups to a single column with a range of possible number values, and this will still lead to sensible conclusions from our analysis. The following cell replaces the age_group values with numbers from 0-8, representing increasing age.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[7]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Get sorted list of age groups </span>
<span class="n">age_groups_list</span> <span class="o">=</span> <span class="nb">list</span><span class="p">(</span><span class="n">df</span><span class="p">[</span><span class="s1">&#39;age_group&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">unique</span><span class="p">())</span>
<span class="n">age_groups_list</span> <span class="o">=</span> <span class="p">[</span><span class="n">age</span> <span class="k">for</span> <span class="n">age</span> <span class="ow">in</span> <span class="n">age_groups_list</span> <span class="k">if</span> <span class="n">pd</span><span class="o">.</span><span class="n">notna</span><span class="p">(</span><span class="n">age</span><span class="p">)]</span>
<span class="n">age_groups_list</span><span class="o">.</span><span class="n">sort</span><span class="p">()</span>

<span class="c1"># Replace age groups with corresponding number</span>
<span class="n">all_numerical</span> <span class="o">=</span> <span class="n">df</span><span class="o">.</span><span class="n">replace</span><span class="p">(</span><span class="n">age_groups_list</span><span class="p">,</span> <span class="nb">range</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">9</span><span class="p">))</span>
<span class="n">all_numerical</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[7]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
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
      <th>sex</th>
      <th>age_group</th>
      <th>race</th>
      <th>death</th>
      <th>medcond</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Male</td>
      <td>1</td>
      <td>Black</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Male</td>
      <td>1</td>
      <td>Black</td>
      <td>0</td>
      <td>&lt;NA&gt;</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Male</td>
      <td>1</td>
      <td>Black</td>
      <td>0</td>
      <td>&lt;NA&gt;</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Male</td>
      <td>1</td>
      <td>Black</td>
      <td>0</td>
      <td>&lt;NA&gt;</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Male</td>
      <td>1</td>
      <td>Black</td>
      <td>&lt;NA&gt;</td>
      <td>&lt;NA&gt;</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>We now want to convert the categorical variables of sex and race to numerical variables. In order to do this, we will create dummy variables for these two columns. This means that each of these columns will be replaced with multiple new columns, one for each possible value of sex or race, which will each have a value of 0 or 1 depending on if the patient is that given sex or race.</p>
<p>Before we can do this, we have to decide how to deal with missing values in the sex and race columns. Because I think it is unlikely that these values would be any more or less likely to be missing based on the values of other columns in the data or based on the true values of the missing data themselves, I decided to simply drop rows with missing values for these columns, since I do not believe it will introduce bias into the data. While I'm at it, I also drop rows with missing values for the medcond and age_group columns, since I do not think the values in this column are more or less likely to be missing because of other collected values either.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[8]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">all_numerical</span><span class="o">.</span><span class="n">dropna</span><span class="p">(</span><span class="n">subset</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;sex&#39;</span><span class="p">,</span><span class="s1">&#39;race&#39;</span><span class="p">,</span><span class="s1">&#39;age_group&#39;</span><span class="p">,</span><span class="s1">&#39;medcond&#39;</span><span class="p">],</span> <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">all_numerical</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[8]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
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
      <th>sex</th>
      <th>age_group</th>
      <th>race</th>
      <th>death</th>
      <th>medcond</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Male</td>
      <td>1</td>
      <td>Black</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Male</td>
      <td>1</td>
      <td>Black</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Male</td>
      <td>1</td>
      <td>Black</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Male</td>
      <td>1</td>
      <td>Black</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>28</th>
      <td>Male</td>
      <td>1</td>
      <td>Black</td>
      <td>&lt;NA&gt;</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>In the following cell, I create dummy variables for the sex and race columns, then concatenate these together with the all_numerical DataFrame and drop the original sex and race columns, which are no longer needed.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[9]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Get dummies for each column</span>
<span class="n">sex_dummies</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">get_dummies</span><span class="p">(</span><span class="n">all_numerical</span><span class="p">[</span><span class="s1">&#39;sex&#39;</span><span class="p">],</span> <span class="n">prefix</span><span class="o">=</span><span class="s1">&#39;sex&#39;</span><span class="p">)</span>
<span class="n">race_dummies</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">get_dummies</span><span class="p">(</span><span class="n">all_numerical</span><span class="p">[</span><span class="s1">&#39;race&#39;</span><span class="p">],</span> <span class="n">prefix</span><span class="o">=</span><span class="s1">&#39;race&#39;</span><span class="p">)</span>

<span class="c1"># Concatenate into one DataFrame</span>
<span class="n">all_numerical</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">sex_dummies</span><span class="p">,</span> <span class="n">race_dummies</span><span class="p">,</span> <span class="n">all_numerical</span><span class="p">],</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">all_numerical</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;sex&#39;</span><span class="p">,</span><span class="s1">&#39;race&#39;</span><span class="p">],</span> <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>

<span class="c1"># Convert types of columns to optimal types (this prevents issues with making correlation matrices later)</span>
<span class="n">all_numerical</span> <span class="o">=</span> <span class="n">all_numerical</span><span class="o">.</span><span class="n">convert_dtypes</span><span class="p">()</span>
<span class="n">all_numerical</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[9]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
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
      <th>sex_Female</th>
      <th>sex_Male</th>
      <th>sex_Other</th>
      <th>race_American Indian/Alaska Native</th>
      <th>race_Asian</th>
      <th>race_Black</th>
      <th>race_Hispanic/Latino</th>
      <th>race_Multiple/Other</th>
      <th>race_Native Hawaiian/Other Pacific Islander</th>
      <th>race_White</th>
      <th>age_group</th>
      <th>death</th>
      <th>medcond</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16</th>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>27</th>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>28</th>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>&lt;NA&gt;</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>There is something potentially problematic with the DataFrame we just created - there is redundant information in the dummy variable columns. As an example of what I mean, if a patient has values of 0 for sex_Male and sex_Other, we already know that this patient must be female, without needing another column to tell us that. As a result of this redundant information, if we fed the DataFrame as is to a regression model or machine learning analysis, our results would be inaccurate. This is called the Dummy Variable Trap, and you can read more about it <a href="https://www.learndatasci.com/glossary/dummy-variable-trap/">here</a>.</p>
<p>For the correlation matrices that we are about to create, the dummy variable trap will not cause problems, and we want the DataFrame as it currently is. However, for some future analyses, we need to correct this problem by dropping the first column of each set of dummy variables. The following cell creates a new DataFrame with the first dummy columns dropped.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[10]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">dropped_first</span> <span class="o">=</span> <span class="n">all_numerical</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;sex_Female&#39;</span><span class="p">,</span><span class="s1">&#39;race_American Indian/Alaska Native&#39;</span><span class="p">])</span>
<span class="n">dropped_first</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[10]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
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
      <th>sex_Male</th>
      <th>sex_Other</th>
      <th>race_Asian</th>
      <th>race_Black</th>
      <th>race_Hispanic/Latino</th>
      <th>race_Multiple/Other</th>
      <th>race_Native Hawaiian/Other Pacific Islander</th>
      <th>race_White</th>
      <th>age_group</th>
      <th>death</th>
      <th>medcond</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16</th>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>27</th>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>28</th>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>&lt;NA&gt;</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Next, we want to do an analysis checking if there is any correlation between any of these columns and whether the value for the death column is missing, which will help us determine how to deal with missing values in the death column.</p>
<p>To do this, we first convert the death column in all_numerical to an "is_death_missing" column, which has a value of 1 if death is missing, and 0 otherwise.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[11]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Rename column</span>
<span class="n">missing_check</span> <span class="o">=</span> <span class="n">all_numerical</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;death&#39;</span><span class="p">:</span><span class="s1">&#39;is_death_missing&#39;</span><span class="p">})</span>

<span class="c1"># Replace values of death column</span>
<span class="n">missing_check</span><span class="p">[</span><span class="s1">&#39;is_death_missing&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">missing_check</span><span class="p">[</span><span class="s1">&#39;is_death_missing&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">replace</span><span class="p">([</span><span class="mi">0</span><span class="p">,</span> <span class="mi">1</span><span class="p">],</span> <span class="mi">0</span><span class="p">)</span><span class="o">.</span><span class="n">fillna</span><span class="p">(</span><span class="n">value</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">missing_check</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[11]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
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
      <th>sex_Female</th>
      <th>sex_Male</th>
      <th>sex_Other</th>
      <th>race_American Indian/Alaska Native</th>
      <th>race_Asian</th>
      <th>race_Black</th>
      <th>race_Hispanic/Latino</th>
      <th>race_Multiple/Other</th>
      <th>race_Native Hawaiian/Other Pacific Islander</th>
      <th>race_White</th>
      <th>age_group</th>
      <th>is_death_missing</th>
      <th>medcond</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16</th>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>27</th>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>28</th>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Now, we can simply create a correlation matrix of the different columns in missing_check. We are currently only interested in the correlation of is_death_missing with other variables, so we simply isolate and display the corresponding column.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[12]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">corr</span> <span class="o">=</span> <span class="n">missing_check</span><span class="o">.</span><span class="n">corr</span><span class="p">()</span>
<span class="n">corr</span><span class="p">[</span><span class="s1">&#39;is_death_missing&#39;</span><span class="p">]</span><span class="o">.</span><span class="n">to_frame</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[12]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
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
      <th>is_death_missing</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>sex_Female</th>
      <td>-0.042821</td>
    </tr>
    <tr>
      <th>sex_Male</th>
      <td>0.042712</td>
    </tr>
    <tr>
      <th>sex_Other</th>
      <td>0.003962</td>
    </tr>
    <tr>
      <th>race_American Indian/Alaska Native</th>
      <td>-0.005109</td>
    </tr>
    <tr>
      <th>race_Asian</th>
      <td>0.082388</td>
    </tr>
    <tr>
      <th>race_Black</th>
      <td>0.011600</td>
    </tr>
    <tr>
      <th>race_Hispanic/Latino</th>
      <td>0.142565</td>
    </tr>
    <tr>
      <th>race_Multiple/Other</th>
      <td>0.053437</td>
    </tr>
    <tr>
      <th>race_Native Hawaiian/Other Pacific Islander</th>
      <td>0.016488</td>
    </tr>
    <tr>
      <th>race_White</th>
      <td>-0.179433</td>
    </tr>
    <tr>
      <th>age_group</th>
      <td>0.130938</td>
    </tr>
    <tr>
      <th>is_death_missing</th>
      <td>1.000000</td>
    </tr>
    <tr>
      <th>medcond</th>
      <td>0.203737</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>As we can see from the table above, no variable (other than, of course, is_death_missing itself) has a correlation coefficient with an absolute value greater than about 0.205. This would not generally be considered a meaningful correlation that indicates a real relationship - usually, for a correlation to even be considered a weak correlation, it requires a correlation coefficient around 0.25-0.3. Thus, based on these results, we can conclude that we cannot accurately predict whether the death column will be missing based on the other data we have collected.</p>
<p>That does not necessarily mean that whether the death column is missing for a patient is indepndent of whether or not that patient died, however. If this column has a missing value, that generally means that the jurisdiction that initially gave the CDC the report has not updated the CDC on whether or not the patient eventually died after initial reporting of the case. We can imagine that jurisdictions could be more likely to update their case reportings if the patient actually died in the end, since they may be more likely to learn that the patient died than that the patient recovered.</p>
<p>However, I was not able to find any information on whether or not this is actually the case, and given that lack of information, the only response I can justify to this missing data is to simply drop cases with missing data for this column. It is possible that this decision will introduce bias into our data by being more likely to drop cases where patients recovered than where patients died.</p>
<p>The following cell drops the rows with missing death values from the all_numerical, dropped_first, and df DataFrames.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[13]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">all_numerical</span><span class="o">.</span><span class="n">dropna</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">subset</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;death&#39;</span><span class="p">])</span>
<span class="n">dropped_first</span><span class="o">.</span><span class="n">dropna</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">subset</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;death&#39;</span><span class="p">])</span>
<span class="n">df</span><span class="o">.</span><span class="n">dropna</span><span class="p">(</span><span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">subset</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;death&#39;</span><span class="p">])</span>
<span class="n">all_numerical</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[13]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
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
      <th>sex_Female</th>
      <th>sex_Male</th>
      <th>sex_Other</th>
      <th>race_American Indian/Alaska Native</th>
      <th>race_Asian</th>
      <th>race_Black</th>
      <th>race_Hispanic/Latino</th>
      <th>race_Multiple/Other</th>
      <th>race_Native Hawaiian/Other Pacific Islander</th>
      <th>race_White</th>
      <th>age_group</th>
      <th>death</th>
      <th>medcond</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>16</th>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
    </tr>
    <tr>
      <th>27</th>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
    <tr>
      <th>42</th>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>0</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>For further information on how to manipulate Pandas DataFrames, you can check the <a href="https://pandas.pydata.org/docs/reference/index.html">Pandas documentation</a>.</p>
<p>For further information on how to handle missing values, you can look at <a href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3668100/">this article</a>.</p>
<h2 id="Exploratory-Data-Analysis">Exploratory Data Analysis<a class="anchor-link" href="#Exploratory-Data-Analysis">&#182;</a></h2><p>The next step in the data science pipeline is to do some exploratory analysis and visualization of the data to get a picture of which variables may be correlated and what relationships may exist between the data.</p>
<p>To begin, we will create and plot a correlation matrix of the data to see which characteristics of a patient are correlated with whether or not they died.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[14]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Convert types of columns to optimal types again </span>
<span class="c1"># (needed to give death column numerical dtype now that it no longer has NA values)</span>
<span class="n">all_numerical</span> <span class="o">=</span> <span class="n">all_numerical</span><span class="o">.</span><span class="n">convert_dtypes</span><span class="p">()</span>

<span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">(</span><span class="n">figsize</span><span class="o">=</span><span class="p">(</span><span class="mi">15</span><span class="p">,</span> <span class="mi">9</span><span class="p">))</span>
<span class="n">sns</span><span class="o">.</span><span class="n">heatmap</span><span class="p">(</span><span class="n">all_numerical</span><span class="o">.</span><span class="n">corr</span><span class="p">(),</span> <span class="n">annot</span><span class="o">=</span><span class="kc">True</span><span class="p">,</span> <span class="n">ax</span><span class="o">=</span><span class="n">ax</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s2">&quot;Correlation Heatmap of Patient Characteristics&quot;</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[14]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>Text(0.5, 1.0, &#39;Correlation Heatmap of Patient Characteristics&#39;)</pre>
</div>

</div>

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>The results of this correlation heatmap tell us that the only factors with any particularly notable correlations with a patient's death are their age group and the presence of a pre-existing medical condition, with correlation coefficients of 0.3 and 0.19 respectively. Additionally, the correlation with age group is the only correlation that would generally be considered even a weak correlation.</p>
<p>To follow up on this result, we will make a plot showing death rate by age group. First, we will need to calculate the death rate of each age group. Since we will need to do a similar operation multiple times in the future, we will define a function to do this for any arbitrary feature of the dataset.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[15]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># The death_rate function groups the given DataFrame by the given grouping_feature and calculates the</span>
<span class="c1"># death rate for each value of that grouping feature.</span>
<span class="k">def</span> <span class="nf">death_rate</span><span class="p">(</span><span class="n">df</span><span class="p">,</span> <span class="n">grouping_feature</span><span class="p">):</span>
    <span class="c1"># Get DataFrames containing the number of deaths and number of total patients for each age group</span>
    <span class="n">age_death</span> <span class="o">=</span> <span class="n">df</span><span class="p">[[</span><span class="n">grouping_feature</span><span class="p">,</span> <span class="s1">&#39;death&#39;</span><span class="p">]]</span>
    <span class="n">totals</span> <span class="o">=</span> <span class="n">age_death</span><span class="o">.</span><span class="n">groupby</span><span class="p">(</span><span class="n">grouping_feature</span><span class="p">)</span><span class="o">.</span><span class="n">count</span><span class="p">()</span><span class="o">.</span><span class="n">rename</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">{</span><span class="s1">&#39;death&#39;</span><span class="p">:</span><span class="s1">&#39;patients&#39;</span><span class="p">})</span>
    <span class="n">total_deaths</span> <span class="o">=</span> <span class="n">age_death</span><span class="o">.</span><span class="n">groupby</span><span class="p">(</span><span class="n">grouping_feature</span><span class="p">)</span><span class="o">.</span><span class="n">sum</span><span class="p">()</span>

    <span class="c1"># Combine DataFrames and calculate death percentage</span>
    <span class="n">combined</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">concat</span><span class="p">([</span><span class="n">totals</span><span class="p">,</span> <span class="n">total_deaths</span><span class="p">],</span> <span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
    <span class="k">for</span> <span class="p">(</span><span class="n">i</span><span class="p">,</span> <span class="n">row</span><span class="p">)</span> <span class="ow">in</span> <span class="n">combined</span><span class="o">.</span><span class="n">iterrows</span><span class="p">():</span>
        <span class="n">combined</span><span class="o">.</span><span class="n">at</span><span class="p">[</span><span class="n">i</span><span class="p">,</span> <span class="s1">&#39;death_rate&#39;</span><span class="p">]</span> <span class="o">=</span> <span class="n">row</span><span class="p">[</span><span class="s1">&#39;death&#39;</span><span class="p">]</span><span class="o">/</span><span class="n">row</span><span class="p">[</span><span class="s1">&#39;patients&#39;</span><span class="p">]</span>

    <span class="c1"># Drop unnecessary patients and death columns</span>
    <span class="n">combined</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;patients&#39;</span><span class="p">,</span><span class="s1">&#39;death&#39;</span><span class="p">],</span> <span class="n">inplace</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
    <span class="k">return</span> <span class="n">combined</span>

<span class="c1"># Call function</span>
<span class="n">combined</span> <span class="o">=</span> <span class="n">death_rate</span><span class="p">(</span><span class="n">all_numerical</span><span class="p">,</span> <span class="s1">&#39;age_group&#39;</span><span class="p">)</span>
<span class="n">combined</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[15]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
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
      <th>death_rate</th>
    </tr>
    <tr>
      <th>age_group</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>1</th>
      <td>0.000000</td>
    </tr>
    <tr>
      <th>2</th>
      <td>0.000870</td>
    </tr>
    <tr>
      <th>3</th>
      <td>0.005144</td>
    </tr>
    <tr>
      <th>4</th>
      <td>0.008008</td>
    </tr>
    <tr>
      <th>5</th>
      <td>0.015658</td>
    </tr>
    <tr>
      <th>6</th>
      <td>0.056695</td>
    </tr>
    <tr>
      <th>7</th>
      <td>0.151292</td>
    </tr>
    <tr>
      <th>8</th>
      <td>0.342508</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Now, we can make a line plot of death rate versus age group.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[16]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">()</span>

<span class="n">ax</span><span class="o">.</span><span class="n">plot</span><span class="p">(</span><span class="n">combined</span><span class="o">.</span><span class="n">index</span><span class="p">,</span> <span class="n">combined</span><span class="p">[</span><span class="s1">&#39;death_rate&#39;</span><span class="p">])</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_xticks</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">0</span><span class="p">,</span> <span class="mi">9</span><span class="p">))</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_xticklabels</span><span class="p">(</span><span class="n">age_groups_list</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s1">&#39;Age Group&#39;</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s1">&#39;Death Rate&#39;</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s2">&quot;Death Rate of COVID-19 Patients by Age Group&quot;</span><span class="p">)</span>

<span class="n">fig</span><span class="o">.</span><span class="n">set_size_inches</span><span class="p">(</span><span class="mi">15</span><span class="p">,</span> <span class="mi">9</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>As we can see from this line plot, there is a clear relationship between age group of patients and their death rate, with older age groups having higher death rates. The increase is not especially noticable until reaching the 50-59 year old age group, but from then on, death rate increases rapidly with age.</p>
<p>Next, we will make a bar plot showing death rate by the presence or absence of a medical condition, as this was the feature with the second most correlation with a patient's survival.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[17]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Get death rate by medical condition</span>
<span class="n">combined</span> <span class="o">=</span> <span class="n">death_rate</span><span class="p">(</span><span class="n">df</span><span class="p">,</span> <span class="s1">&#39;medcond&#39;</span><span class="p">)</span>

<span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">()</span>

<span class="n">ax</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="n">combined</span><span class="o">.</span><span class="n">index</span><span class="p">,</span> <span class="n">combined</span><span class="p">[</span><span class="s1">&#39;death_rate&#39;</span><span class="p">],</span> <span class="n">tick_label</span> <span class="o">=</span> <span class="p">[</span><span class="s1">&#39;No&#39;</span><span class="p">,</span> <span class="s1">&#39;Yes&#39;</span><span class="p">])</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s1">&#39;Medical Condition?&#39;</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s1">&#39;Death Rate&#39;</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s2">&quot;Death Rate of COVID-19 Patients With and Without Prior Medical Condition&quot;</span><span class="p">)</span>

<span class="n">fig</span><span class="o">.</span><span class="n">set_size_inches</span><span class="p">(</span><span class="mi">15</span><span class="p">,</span> <span class="mi">9</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>From the above plot, it is apparent that the presence of a pre-existing medical condition greatly increases the death rate of COVID-19 patients, as the death rate increases from less than 0.01 without a medical condition to over 0.07 with a medical condition.</p>
<p>Although the sex of patients had much less correlation with death, we will still make a bar graph of death rate versus patient sex to get a better picture.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[18]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Get death rate by sex</span>
<span class="n">combined</span> <span class="o">=</span> <span class="n">death_rate</span><span class="p">(</span><span class="n">df</span><span class="p">,</span> <span class="s1">&#39;sex&#39;</span><span class="p">)</span>

<span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">()</span>

<span class="n">ax</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="n">combined</span><span class="o">.</span><span class="n">index</span><span class="p">,</span> <span class="n">combined</span><span class="p">[</span><span class="s1">&#39;death_rate&#39;</span><span class="p">])</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s1">&#39;Sex&#39;</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s1">&#39;Death Rate&#39;</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s2">&quot;Death Rate of COVID-19 Patients By Sex&quot;</span><span class="p">)</span>

<span class="n">fig</span><span class="o">.</span><span class="n">set_size_inches</span><span class="p">(</span><span class="mi">15</span><span class="p">,</span> <span class="mi">9</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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W7apqj2S/GWS3+zu7y51J939pu4+tLsPXb9+/c0eLAAAwKjmGX6XJzlgwe39k1yx0m2qatfMou/Pu/vdcxwnAADA0OYZfucl2VBVd6uq3ZI8KckZi7Y5I8mx09U9D09ydXdfWVWV5E+TXNzdr53jGAEAAIa3y7wO3N03VtWzk5yVZF2SU7r7oqo6flp/cpIzkzwyycYk1yV5+rT7A5I8Ncnnq+pz07IXdveZ8xovAADAqOYWfkkyhdqZi5advODzTvKsJfb7RJZ+/R8AAADbaK5v4A4AAMDaE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDE34AAACDm2v4VdWRVXVJVW2sqhOWWF9VdeK0/sKqOmTBulOq6htV9YV5jhEAAGB0cwu/qlqX5A1JjkpyUJJjquqgRZsdlWTD9HFckpMWrHtzkiPnNT4AAIBbi3nO+B2WZGN3X9rdNyQ5PcnRi7Y5OslpPXNukr2rat8k6e6PJ/nWHMcHAABwqzDP8NsvyVcX3L58Wrat2yyrqo6rqvOr6vxNmzbdrIECAACMbJ7h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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>The bar graph does reveal a noticeably higher death rate for males than for females - about 0.05 for males compared to 0.03 for females. The graph would appear to indicate that the death rate for people of other sexes is very low, but we cannot actually draw meaningful conclusions from this since our sample size for people of other sexes is so small. The next cell shows that we only have one patient with sex listed as 'Other' in our dataset, meaning that all this data realy indicates is that this one patient happened to not die.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[19]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">df</span><span class="o">.</span><span class="n">groupby</span><span class="p">(</span><span class="s1">&#39;sex&#39;</span><span class="p">)</span><span class="o">.</span><span class="n">count</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[19]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
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
      <th>age_group</th>
      <th>race</th>
      <th>death</th>
      <th>medcond</th>
    </tr>
    <tr>
      <th>sex</th>
      <th></th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Female</th>
      <td>32947</td>
      <td>25677</td>
      <td>32981</td>
      <td>4500</td>
    </tr>
    <tr>
      <th>Male</th>
      <td>28615</td>
      <td>21507</td>
      <td>28638</td>
      <td>3668</td>
    </tr>
    <tr>
      <th>Other</th>
      <td>1</td>
      <td>1</td>
      <td>1</td>
      <td>1</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Lastly, we will make a bar graph displaying death rate by race.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[20]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Get death rate by sex</span>
<span class="n">combined</span> <span class="o">=</span> <span class="n">death_rate</span><span class="p">(</span><span class="n">df</span><span class="p">,</span> <span class="s1">&#39;race&#39;</span><span class="p">)</span>

<span class="n">fig</span><span class="p">,</span> <span class="n">ax</span> <span class="o">=</span> <span class="n">plt</span><span class="o">.</span><span class="n">subplots</span><span class="p">()</span>

<span class="n">ax</span><span class="o">.</span><span class="n">bar</span><span class="p">(</span><span class="n">combined</span><span class="o">.</span><span class="n">index</span><span class="p">,</span> <span class="n">combined</span><span class="p">[</span><span class="s1">&#39;death_rate&#39;</span><span class="p">])</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_xlabel</span><span class="p">(</span><span class="s1">&#39;Race&#39;</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_ylabel</span><span class="p">(</span><span class="s1">&#39;Death Rate&#39;</span><span class="p">)</span>
<span class="n">ax</span><span class="o">.</span><span class="n">set_title</span><span class="p">(</span><span class="s2">&quot;Death Rate of COVID-19 Patients By Race&quot;</span><span class="p">)</span>

<span class="n">fig</span><span class="o">.</span><span class="n">set_size_inches</span><span class="p">(</span><span class="mi">15</span><span class="p">,</span> <span class="mi">9</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt"></div>




<div class="jp-RenderedImage jp-OutputArea-output ">
<img src="data:image/png;base64,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
"
>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>This bar graph does show some variation in death rate by race, with Hispanic/Latino and Multiple/Other patients having lower death rates than other races, and American Indian/Alaska Native patients having the highest death rate. The relationship between race and death rate appears relatively weak, but it is still there.</p>
<h2 id="Machine-Learning">Machine Learning<a class="anchor-link" href="#Machine-Learning">&#182;</a></h2><p>Now that we have explored the data and gotten an idea of what relationships exist, we will attempt to train a machine learning model to predict which patients will die if they contract COVID-19.</p>
<p>First, because our model needs to know that the output feature - death - is a categorical variable, we need to split it into two dummy columns. Since these columns represent an output feature, we do not need to drop the first column to avoid the dummy variable trap - that is only for input features. We assign these dummy columsn to a new variable, dep, indicating the dependent data.</p>
<p>Similarly, we make another variable, ind, by dropping the death column to isolate just the independent data.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[21]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">dep</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">get_dummies</span><span class="p">(</span><span class="n">dropped_first</span><span class="p">[</span><span class="s1">&#39;death&#39;</span><span class="p">],</span> <span class="n">prefix</span><span class="o">=</span><span class="s1">&#39;death&#39;</span><span class="p">)</span>
<span class="n">ind</span> <span class="o">=</span> <span class="n">dropped_first</span><span class="o">.</span><span class="n">drop</span><span class="p">(</span><span class="n">columns</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;death&#39;</span><span class="p">])</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Now, we are going to attempt to train a Decision Tree Classifier on our data set to predict whether a patient will die or not. This model essentially generates a tree of questions to ask about the input data, similar to a game of 20 questions, and uses the answers to predict the output.</p>
<p>Before using this model, we have to decide on the optimal value of the hyperparameter max_depth, which decides the maximum depth we allow the decision tree to be. Setting this value too high may lead to overfitting, in which the model learns the training data too closely and becomes bad at accurately predicting the output for new data, but setting the value too low may not give the model enough questions to accurately determine the result.</p>
<p>To test for the best value, we will use the GridSearchCV function from SKLearn, which tests a variety of hyper-parameters for the accuracy of the resulting model.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[22]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Perform GridSearch</span>
<span class="n">dt</span> <span class="o">=</span> <span class="n">DecisionTreeClassifier</span><span class="p">()</span>
<span class="n">param_grid</span> <span class="o">=</span> <span class="p">{</span><span class="s1">&#39;max_depth&#39;</span><span class="p">:</span> <span class="nb">list</span><span class="p">(</span><span class="nb">range</span><span class="p">(</span><span class="mi">1</span><span class="p">,</span> <span class="mi">51</span><span class="p">))}</span>
<span class="n">search</span> <span class="o">=</span> <span class="n">ms</span><span class="o">.</span><span class="n">GridSearchCV</span><span class="p">(</span><span class="n">dt</span><span class="p">,</span> <span class="n">param_grid</span><span class="p">,</span> <span class="n">cv</span><span class="o">=</span><span class="mi">10</span><span class="p">)</span>
<span class="n">search</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">ind</span><span class="p">,</span> <span class="n">dep</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[22]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>GridSearchCV(cv=10, estimator=DecisionTreeClassifier(),
             param_grid={&#39;max_depth&#39;: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12,
                                       13, 14, 15, 16, 17, 18, 19, 20, 21, 22,
                                       23, 24, 25, 26, 27, 28, 29, 30, ...]})</pre>
</div>

</div>

</div>

</div>

</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[23]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># View results of GridSearch</span>
<span class="n">results</span> <span class="o">=</span> <span class="n">pd</span><span class="o">.</span><span class="n">DataFrame</span><span class="p">(</span><span class="n">search</span><span class="o">.</span><span class="n">cv_results_</span><span class="p">)</span>
<span class="n">results</span> <span class="o">=</span> <span class="n">results</span><span class="o">.</span><span class="n">sort_values</span><span class="p">(</span><span class="n">by</span><span class="o">=</span><span class="p">[</span><span class="s1">&#39;rank_test_score&#39;</span><span class="p">])</span>
<span class="n">results</span> <span class="o">=</span> <span class="n">results</span><span class="p">[[</span><span class="s1">&#39;params&#39;</span><span class="p">,</span><span class="s1">&#39;mean_test_score&#39;</span><span class="p">]]</span>
<span class="n">results</span><span class="o">.</span><span class="n">head</span><span class="p">()</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[23]:</div>



<div class="jp-RenderedHTMLCommon jp-RenderedHTML jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/html">
<div>
<style scoped>
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
      <th>params</th>
      <th>mean_test_score</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>{'max_depth': 1}</td>
      <td>0.960471</td>
    </tr>
    <tr>
      <th>1</th>
      <td>{'max_depth': 2}</td>
      <td>0.960471</td>
    </tr>
    <tr>
      <th>2</th>
      <td>{'max_depth': 3}</td>
      <td>0.960471</td>
    </tr>
    <tr>
      <th>3</th>
      <td>{'max_depth': 4}</td>
      <td>0.959300</td>
    </tr>
    <tr>
      <th>28</th>
      <td>{'max_depth': 29}</td>
      <td>0.958568</td>
    </tr>
  </tbody>
</table>
</div>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>The results indicate that the best accuracy is obtained with a max_depth parameter of 1, which results in a mean test score of about 0.96 (though this value will change each time the code is run, since the selection of testing and training data is random.)</p>
<p>The next cell randomly divides the data into training and testing sets, then fits the data to a decision tree classifier model and generates predictions.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[24]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Split data into train and test sets</span>
<span class="n">ind_train</span><span class="p">,</span> <span class="n">ind_test</span><span class="p">,</span> <span class="n">dep_train</span><span class="p">,</span> <span class="n">dep_test</span> <span class="o">=</span> <span class="n">ms</span><span class="o">.</span><span class="n">train_test_split</span><span class="p">(</span><span class="n">ind</span><span class="p">,</span> <span class="n">dep</span><span class="p">)</span>

<span class="c1"># Fit data to decision tree model</span>
<span class="n">dt</span> <span class="o">=</span> <span class="n">DecisionTreeClassifier</span><span class="p">(</span><span class="n">max_depth</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">dt</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">ind_train</span><span class="p">,</span> <span class="n">dep_train</span><span class="p">)</span>

<span class="n">predicted</span> <span class="o">=</span> <span class="n">dt</span><span class="o">.</span><span class="n">predict</span><span class="p">(</span><span class="n">ind_test</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>Now, we need to test how accurate our predictions are by comparing them to the actual values for the testing set. We do this using the accuracy_score test provided by SKLearn, which essentially checks what percentage of predicted values for the death_column are correct.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[25]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Convert outputs back to single label classifiers from dummy variables, which is needed to use accuracy_score</span>
<span class="n">predictions</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">(</span><span class="n">predicted</span><span class="p">)</span><span class="o">.</span><span class="n">argmax</span><span class="p">(</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>
<span class="n">actual</span> <span class="o">=</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">(</span><span class="n">dep_test</span><span class="p">)</span><span class="o">.</span><span class="n">argmax</span><span class="p">(</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">)</span>

<span class="c1"># Test accuracy</span>
<span class="n">met</span><span class="o">.</span><span class="n">accuracy_score</span><span class="p">(</span><span class="n">actual</span><span class="p">,</span> <span class="n">predictions</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[25]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>0.9596018735362998</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>At first glance, this result seems quite good - this means that about 96% of our model's predictions are accurate. However, there is a problem with this analysis, which we will demonstrate in the next cell by printing the confusion matrix. This metric prints an array for which, for the value at row i and column j, this value represents the number of cases known to be in category i but predicted to be in category j.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[26]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">met</span><span class="o">.</span><span class="n">confusion_matrix</span><span class="p">(</span><span class="n">actual</span><span class="p">,</span> <span class="n">predictions</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[26]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>array([[1639,    0],
       [  69,    0]])</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>As we can see by the fact that all non-zero values are in the first column, the decision tree has only predicted that every patient will survive - not a single patient was predicted to die. This is not because this is the most accurate prediction, since there were 68 patients who did die but were predicted to survive nonetheless.</p>
<p>This result is likely because the death rate from COVID-19 is low enough that, even if you are in the highest possible risk group for death, it is still more likely that you will survive than that you will die. As a result, no matter what the characteristics of a patient are, the most likely prediction is still that they will survive.</p>
<p>The result of this is a rather useless machine learning model - we don't exactly need a fancy algorithm to tell us to always predict a patient will survive. This result indicates that typical machine learning methods are not a good fit for this task, since we cannot confidently predict whether a COVID-19 patient will live or die based purely on demographic and medical data about them.</p>
<p>Instead, what would be more valuable is if we can train a machine learning model to predict the <em>probability</em> that a patient will die of COVID-19 based on their characteristics. One classifier provided by SKLearn, SVC, has an option to predict probabilities of classes rather than just output the most likely classification. The next cell trains this model.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell jp-mod-noOutputs  ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[27]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="c1"># Create and train SVC classifier (this model requires output class to be class labels,</span>
<span class="c1"># so we convert dep_train back to class labels from dummy variables)</span>
<span class="n">svc</span> <span class="o">=</span> <span class="n">SVC</span><span class="p">(</span><span class="n">probability</span><span class="o">=</span><span class="kc">True</span><span class="p">)</span>
<span class="n">svc</span><span class="o">.</span><span class="n">fit</span><span class="p">(</span><span class="n">ind_train</span><span class="p">,</span> <span class="n">np</span><span class="o">.</span><span class="n">array</span><span class="p">(</span><span class="n">dep_train</span><span class="p">)</span><span class="o">.</span><span class="n">argmax</span><span class="p">(</span><span class="n">axis</span><span class="o">=</span><span class="mi">1</span><span class="p">))</span>

<span class="c1"># Extract probability of death</span>
<span class="n">predicted</span> <span class="o">=</span> <span class="n">svc</span><span class="o">.</span><span class="n">predict_proba</span><span class="p">(</span><span class="n">ind_test</span><span class="p">)</span>
<span class="n">death_chances</span> <span class="o">=</span> <span class="n">predicted</span><span class="p">[:,</span><span class="mi">1</span><span class="p">]</span>
</pre></div>

     </div>
</div>
</div>
</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>To test the accuracy of this model, we can use a metric called the Brier score loss, which measures the mean squared difference between the predicted probability of the output classes and the actual output class. This test is appropriate for classifications with only two possible values such as our own.</p>

</div>
</div><div class="jp-Cell jp-CodeCell jp-Notebook-cell   ">
<div class="jp-Cell-inputWrapper">
<div class="jp-InputArea jp-Cell-inputArea">
<div class="jp-InputPrompt jp-InputArea-prompt">In&nbsp;[28]:</div>
<div class="jp-CodeMirrorEditor jp-Editor jp-InputArea-editor" data-type="inline">
     <div class="CodeMirror cm-s-jupyter">
<div class=" highlight hl-ipython3"><pre><span></span><span class="n">met</span><span class="o">.</span><span class="n">brier_score_loss</span><span class="p">(</span><span class="n">actual</span><span class="p">,</span> <span class="n">death_chances</span><span class="p">)</span>
</pre></div>

     </div>
</div>
</div>
</div>

<div class="jp-Cell-outputWrapper">


<div class="jp-OutputArea jp-Cell-outputArea">

<div class="jp-OutputArea-child">

    
    <div class="jp-OutputPrompt jp-OutputArea-prompt">Out[28]:</div>




<div class="jp-RenderedText jp-OutputArea-output jp-OutputArea-executeResult" data-mime-type="text/plain">
<pre>0.038625057055698506</pre>
</div>

</div>

</div>

</div>

</div>
<div class="jp-Cell-inputWrapper"><div class="jp-InputPrompt jp-InputArea-prompt">
</div><div class="jp-RenderedHTMLCommon jp-RenderedMarkdown jp-MarkdownOutput " data-mime-type="text/markdown">
<p>For Brier score loss, a lower score is better, which means that this score of about 0.037 indicates our model does a good job at predicting the probabilities of patients dying. This model is thus much more useful than the standard non-probabilistic classifier we attempted to use earlier, as it will allow us to approximately predict the risk of a patient dying from COVID-19 based on their demographic and medical characteristics.</p>
<p>For more information on how to use the SKLearn library, check <a href="https://scikit-learn.org/stable/modules/classes.html">their documentation</a>.</p>
<p>You can read more about probabilistic classifiers <a href="https://en.wikipedia.org/wiki/Probabilistic_classification">here</a>.</p>
<p>For a general reference on machine learning, check <a href="https://www.mygreatlearning.com/blog/machine-learning-tutorial/">this page</a>.</p>
<h2 id="Conclusion-and-Insights">Conclusion and Insights<a class="anchor-link" href="#Conclusion-and-Insights">&#182;</a></h2><p>The analysis here has made it clear that a patient's risk of dying from COVID-19 is definitely related to a number of demographic factors about them, as well as whether they have any pre-existing medical conditions. The most influential feature on death rate is age of the patient, with older patients being much more likely to die, followed by the presence of a medical condition, which greatly increases the chances of a patient dying from COVID-19. Effects of sex and race on death rate are lesser, but still present.</p>
<p>While it is not possible to confidently predict whether a patient will die from COVID-19 based on these features, we can train a machine learning model to estimate the probability that a patient will die with reasonably good accuracy using this information. This is a useful result, as having such a model would allow us to determine a personal risk of death from COVID-19 for individual people, which can help in making decisions about how to allocate medical resources and what kind of treatment COVID-19 patients need to receive. Similar models could be trained for many other diseases, which would also help with managing and treating those diseases, too.</p>

</div>
</div>
</body>







</html>
