## Classes

<dl>
<dt><a href="#desktop">desktop</a></dt>
<dd></dd>
<dt><a href="#tfw">tfw</a></dt>
<dd></dd>
<dt><a href="#prvek">prvek</a></dt>
<dd></dd>
<dt><del><a href="#Dyntable">Dyntable</a></del></dt>
<dd></dd>
</dl>

## Constants

<dl>
<dt><a href="#AJAX_LOADER">AJAX_LOADER</a> : <code>string</code></dt>
<dd><p>HTML to show when some content is being loaded.</p>
</dd>
</dl>

## Functions

<dl>
<dt><a href="#cmp">cmp(a, b)</a></dt>
<dd></dd>
</dl>

<a name="desktop"></a>

## desktop
**Kind**: global class  

* [desktop](#desktop)
    * [new desktop()](#new_desktop_new)
    * [.newLayer(params)](#desktop.newLayer)

<a name="new_desktop_new"></a>

### new desktop()
Triobo. This is a singleton (a single "instance" of a "class").

<a name="desktop.newLayer"></a>

### desktop.newLayer(params)
Create a new layer.

**Kind**: static method of <code>[desktop](#desktop)</code>  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| params | <code>Object</code> |  | layer parameters |
| [params.modal] | <code>boolean</code> &#124; <code>string</code> |  | whether to add class modal (if set to "auto", copies from currently active layer) |
| [params.autoclose] | <code>boolean</code> | <code>false</code> | whether to close layer by clicking it |
| [param.overlay] | <code>boolean</code> | <code>false</code> | whether to add overlay to this layer |

<a name="tfw"></a>

## tfw
**Kind**: global class  
**Todo**

- [ ] Replace [reserved words](http://www.w3schools.com/js/js_reserved.asp) in function names


* [tfw](#tfw)
    * [new tfw()](#new_tfw_new)
    * _static_
        * [.dynamicTableClass](#tfw.dynamicTableClass)
            * [new dynamicTableClass(params)](#new_tfw.dynamicTableClass_new)
            * _instance_
                * [.tableContainer](#tfw.dynamicTableClass+tableContainer) : <code>Object</code>
                * [.data](#tfw.dynamicTableClass+data) : <code>Object</code>
                * [.setPreference(key, [value])](#tfw.dynamicTableClass+setPreference)
                * [.getPreference(key)](#tfw.dynamicTableClass+getPreference) ⇒ <code>Object</code>
                * [.getTable()](#tfw.dynamicTableClass+getTable) ⇒ <code>Object</code>
                * [.reload()](#tfw.dynamicTableClass+reload)
                * [.serverWatch()](#tfw.dynamicTableClass+serverWatch)
                * [.destroy()](#tfw.dynamicTableClass+destroy)
                * [.reorderEnabled()](#tfw.dynamicTableClass+reorderEnabled) ⇒ <code>boolean</code>
                * [.toggleReorder()](#tfw.dynamicTableClass+toggleReorder)
                * [.updateInput(input)](#tfw.dynamicTableClass+updateInput)
                * [.orderChange(element)](#tfw.dynamicTableClass+orderChange)
                * [.paint([changes])](#tfw.dynamicTableClass+paint)
                * [.prepareCalendar()](#tfw.dynamicTableClass+prepareCalendar)
                * [.filter(filterElement, dataCol)](#tfw.dynamicTableClass+filter)
                * [.sort(dataCol, asc)](#tfw.dynamicTableClass+sort)
                * [.setActiveFilterInColumn(column, on, arrowType, [arrowBase])](#tfw.dynamicTableClass+setActiveFilterInColumn)
                * [.filterAny(dataCol, value, [searchType], [dontSave])](#tfw.dynamicTableClass+filterAny)
                * [.resetFilters()](#tfw.dynamicTableClass+resetFilters)
                * [.toggleColumn(dataCol, [dontSave])](#tfw.dynamicTableClass+toggleColumn)
                    * [~hiddenColumns](#tfw.dynamicTableClass+toggleColumn..hiddenColumns) : <code>Array.&lt;boolean&gt;</code>
                * [.toggleColumnDialog(element)](#tfw.dynamicTableClass+toggleColumnDialog)
            * _static_
                * [.serverActions](#tfw.dynamicTableClass.serverActions) : <code>enum</code>
                * [.colTypes](#tfw.dynamicTableClass.colTypes) : <code>enum</code>
                * [.sortTypes](#tfw.dynamicTableClass.sortTypes) : <code>enum</code>
                * [.arrowTypes](#tfw.dynamicTableClass.arrowTypes) : <code>enum</code>
                * [.ROW_EDIT_WIDTH](#tfw.dynamicTableClass.ROW_EDIT_WIDTH) : <code>number</code>
                * [.serverAction](#tfw.dynamicTableClass.serverAction) : <code>Object</code>
            * _inner_
                * [~serverCall(params)](#tfw.dynamicTableClass..serverCall)
                * [~serverUpdateCell(params)](#tfw.dynamicTableClass..serverUpdateCell)
                * [~serverUpdateOrder(params)](#tfw.dynamicTableClass..serverUpdateOrder)
                * [~setActiveArrow(element, base)](#tfw.dynamicTableClass..setActiveArrow)
                * [~rowEdit](#tfw.dynamicTableClass..rowEdit) : <code>function</code>
                * [~goToSub](#tfw.dynamicTableClass..goToSub) : <code>function</code>
                * [~serverCallback](#tfw.dynamicTableClass..serverCallback) : <code>function</code>
                * [~dataChange](#tfw.dynamicTableClass..dataChange) : <code>Object</code>
                * [~filterValue](#tfw.dynamicTableClass..filterValue) : <code>string</code> &#124; <code>Object</code>
        * [.calendar](#tfw.calendar)
            * [new calendar(input)](#new_tfw.calendar_new)
            * _static_
                * [.months](#tfw.calendar.months) : <code>Array.&lt;String&gt;</code>
                * [.daysShort](#tfw.calendar.daysShort) : <code>Array.&lt;String&gt;</code>
                * [.placeCalendar](#tfw.calendar.placeCalendar) : <code>[placeCalendar](#tfw.calendar..placeCalendar)</code>
            * _inner_
                * [~placeCalendar](#tfw.calendar..placeCalendar) : <code>function</code>
        * [.strings](#tfw.strings) : <code>enum</code>
        * [.ajaxIncludeParams](#tfw.ajaxIncludeParams) : <code>function</code>
        * [.ajaxOnErrorCode](#tfw.ajaxOnErrorCode) : <code>function</code>
        * [.ajaxOnError](#tfw.ajaxOnError) : <code>function</code>
        * [.insertStyle(style, [tag])](#tfw.insertStyle)
        * [.init()](#tfw.init)
        * [.localize(newStrings)](#tfw.localize)
        * [.fillElemDefs(element, params)](#tfw.fillElemDefs)
        * [.select(params)](#tfw.select) ⇒ <code>Object</code>
        * [.createLayerAndWrapperAtElement(element, params, [above])](#tfw.createLayerAndWrapperAtElement) ⇒ <code>Object</code>
        * [.dropDown(params)](#tfw.dropDown) ⇒ <code>Object</code>
        * [.button(params)](#tfw.button) ⇒ <code>Object</code>
        * [.inputFieldLegend(element, params)](#tfw.inputFieldLegend) ⇒ <code>Object</code>
        * [.input(params)](#tfw.input) ⇒ <code>Object</code>
        * [.textArea(params)](#tfw.textArea) ⇒ <code>Object</code>
        * [.checkbox(params)](#tfw.checkbox) ⇒ <code>Object</code>
        * [.icon(params)](#tfw.icon) ⇒ <code>Object</code>
        * [.table(params)](#tfw.table) ⇒ <code>Object</code>
        * [.tr(params)](#tfw.tr) ⇒ <code>Object</code>
        * [.td(params)](#tfw.td) ⇒ <code>Object</code>
        * [.slider(params)](#tfw.slider) ⇒ <code>Object</code>
        * [.ajaxGet(o)](#tfw.ajaxGet) ⇒ <code>XMLHttpRequest</code>
        * [.ajaxPost(o)](#tfw.ajaxPost) ⇒ <code>XMLHttpRequest</code>
        * [.encodeFormValues(fields)](#tfw.encodeFormValues) ⇒ <code>string</code>
        * [.decodeJSON(json)](#tfw.decodeJSON) ⇒ <code>Object</code>
        * [.dynamicTable(params)](#tfw.dynamicTable) ⇒ <code>Object</code>
    * _inner_
        * [~ajaxGetCallback](#tfw..ajaxGetCallback) : <code>function</code>

<a name="new_tfw_new"></a>

### new tfw()
Triobo framework. This is a singleton (a single "instance" of a "class").

<a name="tfw.dynamicTableClass"></a>

### tfw.dynamicTableClass
**Kind**: static class of <code>[tfw](#tfw)</code>  
**See**: AJAX_LOADER  
**Todo**

- [ ] View preferences (width, order of columns)


* [.dynamicTableClass](#tfw.dynamicTableClass)
    * [new dynamicTableClass(params)](#new_tfw.dynamicTableClass_new)
    * _instance_
        * [.tableContainer](#tfw.dynamicTableClass+tableContainer) : <code>Object</code>
        * [.data](#tfw.dynamicTableClass+data) : <code>Object</code>
        * [.setPreference(key, [value])](#tfw.dynamicTableClass+setPreference)
        * [.getPreference(key)](#tfw.dynamicTableClass+getPreference) ⇒ <code>Object</code>
        * [.getTable()](#tfw.dynamicTableClass+getTable) ⇒ <code>Object</code>
        * [.reload()](#tfw.dynamicTableClass+reload)
        * [.serverWatch()](#tfw.dynamicTableClass+serverWatch)
        * [.destroy()](#tfw.dynamicTableClass+destroy)
        * [.reorderEnabled()](#tfw.dynamicTableClass+reorderEnabled) ⇒ <code>boolean</code>
        * [.toggleReorder()](#tfw.dynamicTableClass+toggleReorder)
        * [.updateInput(input)](#tfw.dynamicTableClass+updateInput)
        * [.orderChange(element)](#tfw.dynamicTableClass+orderChange)
        * [.paint([changes])](#tfw.dynamicTableClass+paint)
        * [.prepareCalendar()](#tfw.dynamicTableClass+prepareCalendar)
        * [.filter(filterElement, dataCol)](#tfw.dynamicTableClass+filter)
        * [.sort(dataCol, asc)](#tfw.dynamicTableClass+sort)
        * [.setActiveFilterInColumn(column, on, arrowType, [arrowBase])](#tfw.dynamicTableClass+setActiveFilterInColumn)
        * [.filterAny(dataCol, value, [searchType], [dontSave])](#tfw.dynamicTableClass+filterAny)
        * [.resetFilters()](#tfw.dynamicTableClass+resetFilters)
        * [.toggleColumn(dataCol, [dontSave])](#tfw.dynamicTableClass+toggleColumn)
            * [~hiddenColumns](#tfw.dynamicTableClass+toggleColumn..hiddenColumns) : <code>Array.&lt;boolean&gt;</code>
        * [.toggleColumnDialog(element)](#tfw.dynamicTableClass+toggleColumnDialog)
    * _static_
        * [.serverActions](#tfw.dynamicTableClass.serverActions) : <code>enum</code>
        * [.colTypes](#tfw.dynamicTableClass.colTypes) : <code>enum</code>
        * [.sortTypes](#tfw.dynamicTableClass.sortTypes) : <code>enum</code>
        * [.arrowTypes](#tfw.dynamicTableClass.arrowTypes) : <code>enum</code>
        * [.ROW_EDIT_WIDTH](#tfw.dynamicTableClass.ROW_EDIT_WIDTH) : <code>number</code>
        * [.serverAction](#tfw.dynamicTableClass.serverAction) : <code>Object</code>
    * _inner_
        * [~serverCall(params)](#tfw.dynamicTableClass..serverCall)
        * [~serverUpdateCell(params)](#tfw.dynamicTableClass..serverUpdateCell)
        * [~serverUpdateOrder(params)](#tfw.dynamicTableClass..serverUpdateOrder)
        * [~setActiveArrow(element, base)](#tfw.dynamicTableClass..setActiveArrow)
        * [~rowEdit](#tfw.dynamicTableClass..rowEdit) : <code>function</code>
        * [~goToSub](#tfw.dynamicTableClass..goToSub) : <code>function</code>
        * [~serverCallback](#tfw.dynamicTableClass..serverCallback) : <code>function</code>
        * [~dataChange](#tfw.dynamicTableClass..dataChange) : <code>Object</code>
        * [~filterValue](#tfw.dynamicTableClass..filterValue) : <code>string</code> &#124; <code>Object</code>

<a name="new_tfw.dynamicTableClass_new"></a>

#### new dynamicTableClass(params)
Class for creating dynamic tables.


| Param | Type | Default | Description |
| --- | --- | --- | --- |
| params | <code>Object</code> |  | table parameters |
| params.baseURL | <code>string</code> |  | URL of script (etc.) handling data, without query string |
| [params.urlParams] | <code>string</code> |  | general parameters appended to requests (e.g. a token) |
| [params.id] | <code>string</code> | <code>&quot;&#x27;dynamicTable&#x27;&quot;</code> | table ID (name) - required for field (cell) updates |
| [params.rowEdit] | <code>[rowEdit](#tfw.dynamicTableClass..rowEdit)</code> |  | Function fired when row editing/adding is triggered |
| [params.goToSub] | <code>[goToSub](#tfw.dynamicTableClass..goToSub)</code> |  | Function fired when moving to subordinate table is triggered |
| [params.rowAdd] | <code>boolean</code> | <code>false</code> | whether to allow adding new rows |
| [params.bodyHeight] | <code>string</code> |  | (CSS) height of table body including unit (to make header and footer always visible) |
| [params.watchChanges] | <code>boolean</code> | <code>false</code> | whether to allow [watching](#tfw.dynamicTableClass+serverWatch) for changes (long polling) |
| [params.onload] | <code>function</code> |  | function to call after data is loaded for the first time |

**Example**  
```js
function myRowEditFunction(id){	// ...}var table = document.body.appendChild( tfw.dynamicTable(  {   id: "table1",   baseURL: "data.php",   urlParams: "token=Nd5qPxH&timestamp=1234567890",   rowEdit: myRowEditFunction,   bodyHeight: "300px"  } ));
```
<a name="tfw.dynamicTableClass+tableContainer"></a>

#### dynamicTableClass.tableContainer : <code>Object</code>
DIV containing the table.

**Kind**: instance property of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**Read only**: true  
<a name="tfw.dynamicTableClass+data"></a>

#### dynamicTableClass.data : <code>Object</code>
Data obtained from server. [reload()](#tfw.dynamicTableClass+reload) has to be called to fill this.Any other attributes provided by server are preserved (e.g. data.meta).

**Kind**: instance property of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**Default**: <code>null</code>  
**Access:** public  
**Read only**: true  
**Properties**

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| cols | <code>Array.&lt;Object&gt;</code> |  | list of columns |
| cols[].name | <code>string</code> |  | name (HTML) |
| cols[].width | <code>number</code> | <code>200</code> | width (in pixels) |
| cols[].hidden | <code>boolean</code> | <code>false</code> | hidden |
| cols[].type | <code>[colTypes](#tfw.dynamicTableClass.colTypes)</code> | <code></code> | type of field (string) |
| cols[].sort | <code>boolean</code> | <code>false</code> | whether to allow sorting by this column's values |
| cols[].filter | <code>boolean</code> &#124; <code>number</code> | <code>false</code> | whether to allow filtering/searching (depends on type; 1=match from beginning, 2=match anywhere) |
| cols[].subtable | <code>boolean</code> | <code>false</code> | whether this column should contain a link to subtable (handled by goToSub) |
| rows | <code>Array.&lt;Object&gt;</code> |  | list of rows |
| rows[].id | <code>number</code> |  | row ID |
| rows[].cols | <code>Array.&lt;string&gt;</code> |  | contents for each column (HTML) |

<a name="tfw.dynamicTableClass+setPreference"></a>

#### dynamicTableClass.setPreference(key, [value])
Save user's preference.

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | preference key (name) |
| [value] |  | preference value (any type) - if not set, preference is deleted |

<a name="tfw.dynamicTableClass+getPreference"></a>

#### dynamicTableClass.getPreference(key) ⇒ <code>Object</code>
Read user's preference.

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**Returns**: <code>Object</code> - preference value (any type)  

| Param | Type | Description |
| --- | --- | --- |
| key | <code>string</code> | preference key (name) |

<a name="tfw.dynamicTableClass+getTable"></a>

#### dynamicTableClass.getTable() ⇒ <code>Object</code>
Get table container (for inserting into document).

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**Returns**: <code>Object</code> - Returns the table container (HTML element).  
<a name="tfw.dynamicTableClass+reload"></a>

#### dynamicTableClass.reload()
Reload (or load) data from server.Loads preferences and data, then [paint](#tfw.dynamicTableClass+paint)s the table.

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**See**

- tfw.dynamicTableClass#paint
- tfw.dynamicTableClass~serverCall

<a name="tfw.dynamicTableClass+serverWatch"></a>

#### dynamicTableClass.serverWatch()
Watch for updates from the server.

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**See**: tfw.dynamicTableClass#paint  
**Todo**

- [ ] Call again after finishing

<a name="tfw.dynamicTableClass+destroy"></a>

#### dynamicTableClass.destroy()
A "destructor" for table.Aborts all pending requests created by current table.Removes associated CSS.

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**See**: tfw.dynamicTableClass~serverCall  
<a name="tfw.dynamicTableClass+reorderEnabled"></a>

#### dynamicTableClass.reorderEnabled() ⇒ <code>boolean</code>
Test if no filters are applied and table is sorted by column of type 'order'.

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**Returns**: <code>boolean</code> - True if reordering can be done, false otherwise.  
<a name="tfw.dynamicTableClass+toggleReorder"></a>

#### dynamicTableClass.toggleReorder()
Toggle reordering of rows via drag & drop.Reflects the value of a private variable set by onclick events fired with filters.Recommended CSS: tr.draggable{cursor:grab}, tr.draggable:active{cursor:grabbing}

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
<a name="tfw.dynamicTableClass+updateInput"></a>

#### dynamicTableClass.updateInput(input)
Updates data and sends change to server.

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**See**: tfw.dynamicTableClass~serverUpdateCell  

| Param | Type | Description |
| --- | --- | --- |
| input | <code>HTMLElement</code> | input field in a cell of dynamic table |
| input.value | <code>string</code> | value that can be obtained |

<a name="tfw.dynamicTableClass+orderChange"></a>

#### dynamicTableClass.orderChange(element)
Reflect a change in order in the table.

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  

| Param | Type | Description |
| --- | --- | --- |
| element | <code>Object</code> | row that was dropped (HTML element) |

<a name="tfw.dynamicTableClass+paint"></a>

#### dynamicTableClass.paint([changes])
Refresh the content of the table using data gotten by (re)loading.Assumes that there is only 1 order column and that data is initially sorted by that column.

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**Todo**

- [ ] Change drag&dropping so that it is clear where the dragged row will end
- [ ] Add temporary class hasBeenChanged to edited cells.
- [ ] Change checkbox value so that it's not sent back to server
- [ ] Handle update of cell that is currently being edited


| Param | Type | Description |
| --- | --- | --- |
| [changes] | <code>[Array.&lt;dataChange&gt;](#tfw.dynamicTableClass..dataChange)</code> | changes made to data (loaded by [watch](#tfw.dynamicTableClass+serverWatch)) |

<a name="tfw.dynamicTableClass+prepareCalendar"></a>

#### dynamicTableClass.prepareCalendar()
Prepare calendar class for use. Sets the [placeCalendar](#tfw.calendar.placeCalendar) callback, if null.

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**Todo**

- [ ] Use as (default) placeCalendar for all calendars

<a name="tfw.dynamicTableClass+filter"></a>

#### dynamicTableClass.filter(filterElement, dataCol)
Apply filter for values of a column.Creates a [dialog](tfw.dialog) with filter.

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**Todo**

- [ ] Change rangeMin/rangeMax/dateMin/dateMax classes + [filterAny](#tfw.dynamicTableClass+filterAny)


| Param | Type | Description |
| --- | --- | --- |
| filterElement | <code>Object</code> | element to position new layer to (HTML element) |
| dataCol | <code>number</code> | order of searched column (in data) |

<a name="tfw.dynamicTableClass+sort"></a>

#### dynamicTableClass.sort(dataCol, asc)
Apply sorting by values (text without HTML) of a column.Text fields are sorted locale aware, with empty strings always last.

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  

| Param | Type | Description |
| --- | --- | --- |
| dataCol | <code>number</code> | order of column (in data) |
| asc | <code>[sortTypes](#tfw.dynamicTableClass.sortTypes)</code> | sorting type (ascending or descending) |

<a name="tfw.dynamicTableClass+setActiveFilterInColumn"></a>

#### dynamicTableClass.setActiveFilterInColumn(column, on, arrowType, [arrowBase])
Set status of filter icon in a column.

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**See**: tfw.dynamicTableClass~setActiveArrow  

| Param | Type | Description |
| --- | --- | --- |
| column | <code>number</code> | column number |
| on | <code>boolean</code> | whether to toggle active on or off |
| arrowType | <code>[arrowTypes](#tfw.dynamicTableClass.arrowTypes)</code> | type of arrow |
| [arrowBase] | <code>HTMLElement</code> | base to pass to [setActiveArrow](#tfw.dynamicTableClass..setActiveArrow) (defaults to column's heading) |

<a name="tfw.dynamicTableClass+filterAny"></a>

#### dynamicTableClass.filterAny(dataCol, value, [searchType], [dontSave])
Apply any filter.

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**Todo**

- [ ] Better behaviour when min and max are crossed (min > max)


| Param | Type | Default | Description |
| --- | --- | --- | --- |
| dataCol | <code>number</code> |  | order number of filtered column (in data) |
| value | <code>[filterValue](#tfw.dynamicTableClass..filterValue)</code> |  | value to filter by |
| [searchType] | <code>number</code> | <code>2</code> | type of search for TEXT (1 = starts with, 2 = includes) |
| [dontSave] | <code>boolean</code> | <code>false</code> | dont save into preferences (for TEXT) |

<a name="tfw.dynamicTableClass+resetFilters"></a>

#### dynamicTableClass.resetFilters()
Reset all applied filters.

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
<a name="tfw.dynamicTableClass+toggleColumn"></a>

#### dynamicTableClass.toggleColumn(dataCol, [dontSave])
Toggle visibility of a column. Only hides cells in TBODY and THEAD.Requires .hideColumn{display:none}

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| dataCol | <code>number</code> |  | number of column (in data) |
| [dontSave] | <code>boolean</code> | <code>false</code> | don't save into preferences |

<a name="tfw.dynamicTableClass+toggleColumn..hiddenColumns"></a>

##### toggleColumn~hiddenColumns : <code>Array.&lt;boolean&gt;</code>
**Kind**: inner property of <code>[toggleColumn](#tfw.dynamicTableClass+toggleColumn)</code>  
<a name="tfw.dynamicTableClass+toggleColumnDialog"></a>

#### dynamicTableClass.toggleColumnDialog(element)
Toggle visibility of a column.Creates a [dialog](tfw.dialog) with checkboxes.

**Kind**: instance method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  

| Param | Type | Description |
| --- | --- | --- |
| element | <code>HTMLElement</code> | above which element should checkboxes be positioned |

<a name="tfw.dynamicTableClass.serverActions"></a>

#### dynamicTableClass.serverActions : <code>enum</code>
Implemented server actions.

**Kind**: static enum property of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**Read only**: true  
**Properties**

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| LOAD | <code>[serverAction](#tfw.dynamicTableClass.serverAction)</code> | <code>{&quot;name&quot;:&quot;load&quot;}</code> | load all rows |
| NEW | <code>[serverAction](#tfw.dynamicTableClass.serverAction)</code> | <code>{&quot;name&quot;:&quot;new&quot;,&quot;method&quot;:&quot;POST&quot;}</code> | add new row, return ID |
| SAVE | <code>[serverAction](#tfw.dynamicTableClass.serverAction)</code> | <code>{&quot;name&quot;:&quot;savedata&quot;,&quot;method&quot;:&quot;POST&quot;}</code> | edit 1 cell (id, col) |
| CHANGE_ORDER | <code>[serverAction](#tfw.dynamicTableClass.serverAction)</code> | <code>{&quot;name&quot;:&quot;changeorder&quot;,&quot;method&quot;:&quot;POST&quot;}</code> | change order of rows - updates multiple rows |
| WATCH | <code>[serverAction](#tfw.dynamicTableClass.serverAction)</code> | <code>{&quot;name&quot;:&quot;watch&quot;}</code> | long polling |
| DELETE | <code>[serverAction](#tfw.dynamicTableClass.serverAction)</code> | <code>{&quot;name&quot;:&quot;delete&quot;,&quot;method&quot;:&quot;POST&quot;}</code> | delete row |
| PREF_GET | <code>[serverAction](#tfw.dynamicTableClass.serverAction)</code> | <code>{&quot;name&quot;:&quot;getusersettings&quot;}</code> | load user's preferences |
| PREF_SET | <code>[serverAction](#tfw.dynamicTableClass.serverAction)</code> | <code>{&quot;name&quot;:&quot;setusersettings&quot;,&quot;method&quot;:&quot;POST&quot;}</code> | save user's preferences |

<a name="tfw.dynamicTableClass.colTypes"></a>

#### dynamicTableClass.colTypes : <code>enum</code>
Types of columns (and filters).

**Kind**: static enum property of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**Read only**: true  
**Properties**

| Name | Type | Default |
| --- | --- | --- |
| TEXT | <code>string</code> | <code>&quot;text&quot;</code> | 
| NUMBER | <code>string</code> | <code>&quot;number&quot;</code> | 
| CHECKBOX | <code>string</code> | <code>&quot;checkbox&quot;</code> | 
| DATE | <code>string</code> | <code>&quot;date&quot;</code> | 
| ORDER | <code>string</code> | <code>&quot;order&quot;</code> | 

<a name="tfw.dynamicTableClass.sortTypes"></a>

#### dynamicTableClass.sortTypes : <code>enum</code>
Types of sorting.

**Kind**: static enum property of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**Read only**: true  
**Properties**

| Name | Type | Default |
| --- | --- | --- |
| ASC | <code>number</code> | <code>1</code> | 
| DESC | <code>number</code> | <code>-1</code> | 

<a name="tfw.dynamicTableClass.arrowTypes"></a>

#### dynamicTableClass.arrowTypes : <code>enum</code>
Types of "arrows".

**Kind**: static enum property of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**Read only**: true  
**Properties**

| Name | Type | Default |
| --- | --- | --- |
| FILTER | <code>string</code> | <code>&quot;filter&quot;</code> | 
| UP | <code>string</code> | <code>&quot;up&quot;</code> | 
| DOWN | <code>string</code> | <code>&quot;down&quot;</code> | 

<a name="tfw.dynamicTableClass.ROW_EDIT_WIDTH"></a>

#### dynamicTableClass.ROW_EDIT_WIDTH : <code>number</code>
Width of column with row edit icon (icon's width including padding, border, margin + cell's padding + border), in pixels

**Kind**: static property of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**Default**: <code>25</code>  
**Read only**: true  
<a name="tfw.dynamicTableClass.serverAction"></a>

#### dynamicTableClass.serverAction : <code>Object</code>
**Kind**: static typedef of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**Properties**

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| name | <code>string</code> |  | action name sent to server |
| method | <code>string</code> | <code>&quot;\&quot;GET\&quot;&quot;</code> | HTTP method to use (e.g. GET, POST) |

<a name="tfw.dynamicTableClass..serverCall"></a>

#### dynamicTableClass~serverCall(params)
Send a table-specific request to server.If table is [destroy](#tfw.dynamicTableClass+destroy)ed, pending requests are aborted.

**Kind**: inner method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
**See**

- tfw.ajaxGet
- tfw.decodeJSON


| Param | Type | Default | Description |
| --- | --- | --- | --- |
| params | <code>Object</code> |  | query parameters |
| params.action | <code>[serverActions](#tfw.dynamicTableClass.serverActions)</code> |  | server action |
| [params.callback] | <code>[serverCallback](#tfw.dynamicTableClass..serverCallback)</code> |  | callback that receives data |
| [params.parameters] | <code>string</code> | <code>null</code> | parameters to be send with the request (e.g. POST) |

<a name="tfw.dynamicTableClass..serverUpdateCell"></a>

#### dynamicTableClass~serverUpdateCell(params)
**Kind**: inner method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  

| Param | Type | Description |
| --- | --- | --- |
| params | <code>Object</code> | update parameters |
| params.id | <code>number</code> | ID of edited row |
| params.col | <code>number</code> | order number of edited column |
| params.value | <code>number</code> | new value |

<a name="tfw.dynamicTableClass..serverUpdateOrder"></a>

#### dynamicTableClass~serverUpdateOrder(params)
**Kind**: inner method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  

| Param | Type | Description |
| --- | --- | --- |
| params | <code>Object</code> | update parameters |
| params.id | <code>number</code> | ID of edited row |
| params.neworder | <code>number</code> | new order number of edited row |

<a name="tfw.dynamicTableClass..setActiveArrow"></a>

#### dynamicTableClass~setActiveArrow(element, base)
Set active arrow (and make other arrows of same group inactive).

**Kind**: inner method of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  

| Param | Type | Description |
| --- | --- | --- |
| element | <code>Object</code> | arrow to make active (HTML element) |
| base | <code>Object</code> | where to search for arrows (HTML element) |

<a name="tfw.dynamicTableClass..rowEdit"></a>

#### dynamicTableClass~rowEdit : <code>function</code>
Function that handles row editing.

**Kind**: inner typedef of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  

| Param | Type | Description |
| --- | --- | --- |
| id | <code>number</code> | ID of the row being edited or 0 if new row is being inserted |

<a name="tfw.dynamicTableClass..goToSub"></a>

#### dynamicTableClass~goToSub : <code>function</code>
Function that handles moving to subordinate table.

**Kind**: inner typedef of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  

| Param | Type | Description |
| --- | --- | --- |
| rowID | <code>number</code> | ID of the row being edited |
| column | <code>number</code> | order number of column in which the callback was triggered |

<a name="tfw.dynamicTableClass..serverCallback"></a>

#### dynamicTableClass~serverCallback : <code>function</code>
Function that handles data received from server.

**Kind**: inner typedef of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  

| Param | Type | Description |
| --- | --- | --- |
| receivedData | <code>Object</code> | JSON decoded data received from request |

<a name="tfw.dynamicTableClass..dataChange"></a>

#### dynamicTableClass~dataChange : <code>Object</code>
Object representing an update/insertion/deletion in data.Type of change is determined by present properties.

**Kind**: inner typedef of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  

| Param | Type | Description |
| --- | --- | --- |
| id | <code>number</code> | ID of row - if neither col nor cols are present, implies deletion |
| [col] | <code>number</code> | column number of updated cell (in data) - implies update |
| [value] | <code>string</code> | new value of updated cell - for change only |
| [cols] | <code>Array.&lt;string&gt;</code> | values of inserted row - implies insertion |

<a name="tfw.dynamicTableClass..filterValue"></a>

#### dynamicTableClass~filterValue : <code>string</code> &#124; <code>Object</code>
Value by which the table can be filtered.

**Kind**: inner typedef of <code>[dynamicTableClass](#tfw.dynamicTableClass)</code>  
<a name="tfw.calendar"></a>

### tfw.calendar
**Kind**: static class of <code>[tfw](#tfw)</code>  

* [.calendar](#tfw.calendar)
    * [new calendar(input)](#new_tfw.calendar_new)
    * _static_
        * [.months](#tfw.calendar.months) : <code>Array.&lt;String&gt;</code>
        * [.daysShort](#tfw.calendar.daysShort) : <code>Array.&lt;String&gt;</code>
        * [.placeCalendar](#tfw.calendar.placeCalendar) : <code>[placeCalendar](#tfw.calendar..placeCalendar)</code>
    * _inner_
        * [~placeCalendar](#tfw.calendar..placeCalendar) : <code>function</code>

<a name="new_tfw.calendar_new"></a>

#### new calendar(input)
Class for enhancing date input fields. Requires CSS styling.

**Returns**: <code>HTMLElement</code> - Returns input wrapper (for inserting into DOM in case input was not inserted yet)  

| Param | Type | Description |
| --- | --- | --- |
| input | <code>HTMLElement</code> | input field to turn into calendar field |

**Example**  
```js
tfw.calendar.placeCalendar = function(cal, input){ input.parentNode.insertBefore(cal, input);}var input = tfw.input({value:"2016-03-07"});document.body.appendChild(input);tfw.calendar(input);
```
**Example**  
```js
tfw.calendar.placeCalendar = function(cal, input){ input.parentNode.insertBefore(cal, input);}document.body.appendChild( tfw.calendar(  tfw.input({   value: "2016-03-07"  }) ));
```
<a name="tfw.calendar.months"></a>

#### calendar.months : <code>Array.&lt;String&gt;</code>
List of months' names.

**Kind**: static property of <code>[calendar](#tfw.calendar)</code>  
**Default**: <code>[&quot;January&quot;,&quot;February&quot;,&quot;March&quot;,&quot;April&quot;,&quot;May&quot;,&quot;June&quot;,&quot;July&quot;,&quot;August&quot;,&quot;September&quot;,&quot;October&quot;,&quot;November&quot;,&quot;December&quot;]</code>  
<a name="tfw.calendar.daysShort"></a>

#### calendar.daysShort : <code>Array.&lt;String&gt;</code>
List of days' names' first two letters (beginning with Monday)

**Kind**: static property of <code>[calendar](#tfw.calendar)</code>  
**Default**: <code>[&quot;Mo&quot;,&quot;Tu&quot;,&quot;We&quot;,&quot;Th&quot;,&quot;Fr&quot;,&quot;Sa&quot;,&quot;Su&quot;]</code>  
<a name="tfw.calendar.placeCalendar"></a>

#### calendar.placeCalendar : <code>[placeCalendar](#tfw.calendar..placeCalendar)</code>
Function called when a calendar widget is created.

**Kind**: static property of <code>[calendar](#tfw.calendar)</code>  
**Default**: <code></code>  
<a name="tfw.calendar..placeCalendar"></a>

#### calendar~placeCalendar : <code>function</code>
Callback function that puts calendar widget for an input field into page.Most likely create an overlay that closes calendar when user clicks somewhere else.

**Kind**: inner typedef of <code>[calendar](#tfw.calendar)</code>  

| Param | Type | Description |
| --- | --- | --- |
| calendar | <code>Object</code> | calendar widget (HTML element) |
| input | <code>Object</code> | related input field (HTML element) |

<a name="tfw.strings"></a>

### tfw.strings : <code>enum</code>
Strings that are output by tfw functions. Change them for localization.

**Kind**: static enum property of <code>[tfw](#tfw)</code>  
**Default**: <code>&quot;{\&quot;NO\&quot;:\&quot;No\&quot;,\&quot;YES\&quot;:\&quot;Yes\&quot;,\&quot;ALL\&quot;:\&quot;All\&quot;,\&quot;FROM\&quot;:\&quot;From:\&quot;,\&quot;TO\&quot;:\&quot;To:\&quot;,\&quot;FILTER\&quot;:\&quot;Filter…\&quot;}&quot;</code>  
**Properties**

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| NO | <code>string</code> | <code>&quot;No&quot;</code> | Label for checkbox with false value. |
| YES | <code>string</code> | <code>&quot;Yes&quot;</code> | Label for checkbox with true value. |
| ALL | <code>string</code> | <code>&quot;All&quot;</code> | Word for 'all' (e.g. both true and false) |
| FROM | <code>string</code> | <code>&quot;From:&quot;</code> | Minimum input label |
| TO | <code>string</code> | <code>&quot;To:&quot;</code> | Maximum input label |
| FILTER | <code>string</code> | <code>&quot;Filter…&quot;</code> | Placeholder when searching anywhere in a string |

<a name="tfw.ajaxIncludeParams"></a>

### tfw.ajaxIncludeParams : <code>function</code>
Generates permanent AJAX queries parameters (e.g. tokens, anti-cache)

**Kind**: static property of <code>[tfw](#tfw)</code>  
**Default**: <code>null</code>  
<a name="tfw.ajaxOnErrorCode"></a>

### tfw.ajaxOnErrorCode : <code>function</code>
Handles error generated by server (receives error code returned by server).

**Kind**: static property of <code>[tfw](#tfw)</code>  
**Default**: <code>null</code>  
<a name="tfw.ajaxOnError"></a>

### tfw.ajaxOnError : <code>function</code>
Handles HTTP errors (HTTP codes other than 200).

**Kind**: static property of <code>[tfw](#tfw)</code>  
**Default**: <code>null</code>  
**Todo**

- [ ] Implement

<a name="tfw.insertStyle"></a>

### tfw.insertStyle(style, [tag])
Add Javascript-generated CSS to the document.

**Kind**: static method of <code>[tfw](#tfw)</code>  

| Param | Type | Description |
| --- | --- | --- |
| style | <code>string</code> | CSS to be added |
| [tag] | <code>string</code> | identify (tag) CSS for overriding |

<a name="tfw.init"></a>

### tfw.init()
Initialization needed to run tfw functions (e.g. adds required CSS styling).Can be run multiple times (after adding localized strings).

**Kind**: static method of <code>[tfw](#tfw)</code>  
<a name="tfw.localize"></a>

### tfw.localize(newStrings)
Add new translations and re-[init](#tfw.init) tfw.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**See**: tfw.init  

| Param | Type | Description |
| --- | --- | --- |
| newStrings | <code>[strings](#tfw.strings)</code> | translated strings to be used (keys same as in [strings](#tfw.strings)) |

<a name="tfw.fillElemDefs"></a>

### tfw.fillElemDefs(element, params)
Set parameters of a HTML element.

**Kind**: static method of <code>[tfw](#tfw)</code>  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| element | <code>Object</code> |  | HTML element |
| params | <code>Object</code> |  | parameters object |
| [params.id] | <code>string</code> |  | ID |
| [params.className] | <code>string</code> |  | class |
| [params.innerHTML] | <code>string</code> |  | content (HTML) |
| [params.text] | <code>string</code> |  | content (text), works same as innerHTML |
| [params.style] | <code>string</code> |  | CSS styling |
| [params.title] | <code>string</code> |  | title (shows on hover) |
| [params.children] | <code>Array.&lt;Object&gt;</code> |  | descendant element(s) |
| [params.disabled] | <code>boolean</code> | <code>false</code> | disabled input field |
| [params.maxLength] | <code>number</code> |  | maximum input length |
| [params.evaluate] | <code>boolean</code> | <code>false</code> | evaluate (eval) field value after change (onchange), set to 1 or true |
| [params.onchange] | <code>function</code> |  | function to call when field changes value (onchange fires) |
| [params.onClick] | <code>function</code> |  | function to call when user clicks on the field (onclick fires) |
| [params.value] | <code>string</code> |  | default field value (or button text) |
| [params.placeholder] | <code>string</code> |  | text field placeholder |

<a name="tfw.select"></a>

### tfw.select(params) ⇒ <code>Object</code>
Create a select field with specified parameters.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**Returns**: <code>Object</code> - Created select field (HTML element).  
**See**: tfw.fillElemDefs  

| Param | Type | Description |
| --- | --- | --- |
| params | <code>Object</code> | select parameters (for more see [fillElemDefs](#tfw.fillElemDefs)) |
| [params.multiple] | <code>boolean</code> | can multiple values be selected |
| params.list | <code>string</code> &#124; <code>Array.&lt;string&gt;</code> &#124; <code>Array.&lt;Object&gt;</code> | list of options as string "label1;label2" or "label1|value1;label2|value2", as array of string labels or as object (nonspecified value defaults to numeric index, NOT label text) |
| [params.list[].id] | <code>string</code> | value (defaults to numeric index of option) |
| params.list[].t | <code>string</code> | label |

<a name="tfw.createLayerAndWrapperAtElement"></a>

### tfw.createLayerAndWrapperAtElement(element, params, [above]) ⇒ <code>Object</code>
Create a new layer and a wrapper that starts at a given element.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**Returns**: <code>Object</code> - Created wrapper (HTML element)  
**See**: desktop.newLayer  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| element | <code>Object</code> |  | HTML element |
| params | <code>Object</code> |  | parameters for [newLayer](#desktop.newLayer) |
| [above] | <code>boolean</code> | <code>false</code> | whether to position above element instead of below |

<a name="tfw.dropDown"></a>

### tfw.dropDown(params) ⇒ <code>Object</code>
Create a dropdown menu.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**Returns**: <code>Object</code> - Created dropdown menu (HTML element).  
**See**: tfw.select  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| params | <code>Object</code> |  | dropdown parameters |
| [params.legend] | <code>string</code> |  | label |
| [params.legendWidth] | <code>string</code> |  | label CSS width (including unit) |
| [params.legendStyle] | <code>string</code> |  | label CSS styling |
| [params.containerId] | <code>string</code> |  | ID of containing paragraph |
| [params.containerStyle] | <code>string</code> |  | CSS styling of containing paragraph |
| [params.id] | <code>string</code> |  | dropdown ID |
| [params.className] | <code>string</code> |  | dropdown classes (separated by spaces) |
| [params.style] | <code>string</code> |  | dropdown CSS styling |
| [params.itemWidth] | <code>number</code> | <code>0</code> | width of an item |
| [params.itemHeight] | <code>number</code> | <code>20</code> | height of an item |
| [params.onchange] | <code>function</code> |  | function to call when value changes (onchange) |
| params.list | <code>Array.&lt;string&gt;</code> &#124; <code>Array.&lt;Object&gt;</code> |  | list of options passed to [select](#tfw.select) |
| [params.value] | <code>string</code> |  | default (selected) value |

<a name="tfw.button"></a>

### tfw.button(params) ⇒ <code>Object</code>
Create a button with specified parameters.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**Returns**: <code>Object</code> - Created button (HTML element)  
**See**: tfw.fillElemDefs  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| params | <code>Object</code> |  | button parameters (for more see [fillElemDefs](#tfw.fillElemDefs)) |
| [params.step] | <code>number</code> |  | step between allowed numeric values |
| [params.default] | <code>boolean</code> | <code>false</code> | if true, type=submit, otherwise type=button |
| [params.action] | <code>function</code> |  | Function to fire when button is clicked (event propagation is stopped) |

<a name="tfw.inputFieldLegend"></a>

### tfw.inputFieldLegend(element, params) ⇒ <code>Object</code>
Wrap an input field with a legend and a container.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**Returns**: <code>Object</code> - container with legend and input field (HTML element)  

| Param | Type | Description |
| --- | --- | --- |
| element | <code>Object</code> | input field HTML element |
| params | <code>Object</code> | legend parameters |
| params.legend | <code>string</code> | legend text |
| [params.legendStyle] | <code>string</code> | legend CSS styling |
| [params.containerId] | <code>string</code> | legend container ID |
| [params.containerStyle] | <code>string</code> | legend container CSS styling |
| [params.postText] | <code>string</code> | text after input field |

<a name="tfw.input"></a>

### tfw.input(params) ⇒ <code>Object</code>
Create an input field with specified parameters.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**Returns**: <code>Object</code> - Created input field (HTML element)  
**See**

- tfw.fillElemDefs
- tfw.inputFieldLegend


| Param | Type | Default | Description |
| --- | --- | --- | --- |
| params | <code>Object</code> |  | input fields parameters (for more see [fillElemDefs](#tfw.fillElemDefs) and [inputFieldLegend](#tfw.inputFieldLegend)) |
| [params.type] | <code>string</code> | <code>&quot;\&quot;text\&quot;&quot;</code> | input field type |
| [params.value] | <code>string</code> |  | prefilled value |
| [params.min] | <code>number</code> |  | minimum allowed value |
| [params.max] | <code>number</code> |  | maximum allowed value |
| [params.step] | <code>number</code> |  | step between allowed numeric values |

<a name="tfw.textArea"></a>

### tfw.textArea(params) ⇒ <code>Object</code>
Create a text area with specified parameters.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**Returns**: <code>Object</code> - Created text area (HTML element)  
**See**

- tfw.fillElemDefs
- tfw.inputFieldLegend


| Param | Type | Description |
| --- | --- | --- |
| params | <code>Object</code> | text area parameters (for more see [fillElemDefs](#tfw.fillElemDefs) and [inputFieldLegend](#tfw.inputFieldLegend)) |
| [params.value] | <code>string</code> | prefilled value |

<a name="tfw.checkbox"></a>

### tfw.checkbox(params) ⇒ <code>Object</code>
Create a checkbox with specified parameters.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**Returns**: <code>Object</code> - Created checkbox (HTML element)  
**See**

- tfw.fillElemDefs
- tfw.inputFieldLegend

**Todo**

- [ ] Use "value" for real value, instead of using it for "checked"


| Param | Type | Default | Description |
| --- | --- | --- | --- |
| params | <code>Object</code> |  | checkbox parameters (for more see [fillElemDefs](#tfw.fillElemDefs) and [inputFieldLegend](#tfw.inputFieldLegend)) |
| [params.onchange] | <code>function</code> |  | function to call when field changes value (onchange fires) |
| [params.text] | <code>string</code> |  | checkbox label text |
| [params.value] | <code>string</code> | <code>0</code> | initial value (0=unchecked,1=checked) |

<a name="tfw.icon"></a>

### tfw.icon(params) ⇒ <code>Object</code>
Create an icon with specified parameters.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**Returns**: <code>Object</code> - Created icon (HTML element)  
**See**: tfw.fillElemDefs  

| Param | Type | Description |
| --- | --- | --- |
| params | <code>Object</code> | icon parameters (for more see [fillElemDefs](#tfw.fillElemDefs)) |
| [params.action] | <code>function</code> | function triggered when icon is clicked (basically onclick) |
| [params.index] | <code>number</code> | move background image up by this number of pixels (background-position-x) |

<a name="tfw.table"></a>

### tfw.table(params) ⇒ <code>Object</code>
Create a table with specified parameters.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**Returns**: <code>Object</code> - Created table (HTML element)  
**See**: tfw.fillElemDefs  

| Param | Type | Description |
| --- | --- | --- |
| params | <code>Object</code> | table parameters (for more see [fillElemDefs](#tfw.fillElemDefs), use params.children for rows) |

<a name="tfw.tr"></a>

### tfw.tr(params) ⇒ <code>Object</code>
Create a table row with specified parameters.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**Returns**: <code>Object</code> - Created table row (HTML element)  
**See**: tfw.fillElemDefs  

| Param | Type | Description |
| --- | --- | --- |
| params | <code>Object</code> | table row parameters (for more see [fillElemDefs](#tfw.fillElemDefs), use params.children for columns/cells) |
| [params.columns] | <code>Array</code> | list of objects, that will be passed to tfw.td and added as children |

<a name="tfw.td"></a>

### tfw.td(params) ⇒ <code>Object</code>
Create a table cell with specified parameters.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**Returns**: <code>Object</code> - Created table cell (HTML element)  
**See**: tfw.fillElemDefs  

| Param | Type | Description |
| --- | --- | --- |
| params | <code>Object</code> | table cell parameters (for more see [fillElemDefs](#tfw.fillElemDefs)) |
| [params.colspan] | <code>number</code> | number of columns that this cell will merge |

<a name="tfw.slider"></a>

### tfw.slider(params) ⇒ <code>Object</code>
Create a slider with specified parameters.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**Returns**: <code>Object</code> - Created slider (HTML element)  
**See**: tfw.fillElemDefs  

| Param | Type | Default | Description |
| --- | --- | --- | --- |
| params | <code>Object</code> |  | slider parameters (for more see [fillElemDefs](#tfw.fillElemDefs)) |
| params.id | <code>string</code> |  | ID, has to be present! |
| [params.legend] | <code>string</code> |  | legend text |
| [params.legendStyle] | <code>string</code> |  | legend CSS styling |
| [params.min] | <code>number</code> | <code>0</code> | minimum (smallest) value |
| [params.max] | <code>number</code> | <code>100</code> | maximum (largest) value |
| [params.step] | <code>number</code> |  | step between allowed values |
| [params.width] | <code>string</code> |  | width of slider (CSS, including unit) |
| [params.valueStyle] | <code>string</code> |  | value box CSS styling |
| [params.postText] | <code>string</code> |  | text after slider |

<a name="tfw.ajaxGet"></a>

### tfw.ajaxGet(o) ⇒ <code>XMLHttpRequest</code>
Get data from server via AJAX.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**Returns**: <code>XMLHttpRequest</code> - - Returns XMLHttpRequest object  
**See**

- tfw.ajaxIncludeParams
- tfw.ajaxOnErrorCode
- tfw.ajaxOnError


| Param | Type | Default | Description |
| --- | --- | --- | --- |
| o | <code>Object</code> |  | parameters object |
| o.url | <code>string</code> |  | URL of server script with data |
| o.onload | <code>[ajaxGetCallback](#tfw..ajaxGetCallback)</code> |  | function to call when request has successfully completed |
| [o.autohide] | <code>number</code> | <code>0</code> | whether to show overlay after finishing (1 = yes after 500ms, 2 = yes immediately) |
| [o.method] | <code>string</code> | <code>&quot;\&quot;GET\&quot;&quot;</code> | HTTP method to be used (GET or POST) |
| [o.parameters] | <code>string</code> | <code>null</code> | parameters to be send with the request (e.g. POST) |

<a name="tfw.ajaxPost"></a>

### tfw.ajaxPost(o) ⇒ <code>XMLHttpRequest</code>
Post data to server via AJAX.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**Returns**: <code>XMLHttpRequest</code> - - Returns XMLHttpRequest object  
**See**: tfw.ajaxGet  

| Param | Type | Description |
| --- | --- | --- |
| o | <code>Object</code> | parameters object (see [ajaxGet](#tfw.ajaxGet)) |

<a name="tfw.encodeFormValues"></a>

### tfw.encodeFormValues(fields) ⇒ <code>string</code>
Encode all items as URL.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**Returns**: <code>string</code> - String, that can be used to call server via ajax  

| Param | Type | Description |
| --- | --- | --- |
| fields | <code>Object</code> | items to be encoded {key1:id1,key2:id2,...} |

<a name="tfw.decodeJSON"></a>

### tfw.decodeJSON(json) ⇒ <code>Object</code>
Decode JSON data, show error in case they are invalid.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**Returns**: <code>Object</code> - Object that was encoded in given JSON string.  

| Param | Type | Description |
| --- | --- | --- |
| json | <code>string</code> | JSON encoded data |

<a name="tfw.dynamicTable"></a>

### tfw.dynamicTable(params) ⇒ <code>Object</code>
Wrapper that creates a dynamic table and returns it's HTML node for inserting into DOM.Class instance's properties are mirrored into the HTML element.

**Kind**: static method of <code>[tfw](#tfw)</code>  
**Returns**: <code>Object</code> - table (HTML element)  
**See**: tfw.dynamicTableClass  

| Param | Type | Description |
| --- | --- | --- |
| params | <code>Object</code> | table parameters (see [dynamicTableClass](#tfw.dynamicTableClass)) |

<a name="tfw..ajaxGetCallback"></a>

### tfw~ajaxGetCallback : <code>function</code>
Callback after successfull HTTP request.

**Kind**: inner typedef of <code>[tfw](#tfw)</code>  

| Param | Type | Description |
| --- | --- | --- |
| httpRequest | <code>XMLHttpRequest</code> | associated XMLHttpRequest object |
| httpRequest.responseText | <code>string</code> | server response |

<a name="prvek"></a>

## prvek
**Kind**: global class  

* [prvek](#prvek)
    * [new prvek()](#new_prvek_new)
    * [.seznamZatrzitek()](#prvek.seznamZatrzitek)
    * ~~[.tabulka()](#prvek.tabulka)~~
    * ~~[.radek()](#prvek.radek)~~
    * ~~[.sloupec()](#prvek.sloupec)~~
    * [.soubory()](#prvek.soubory)
    * [.barva()](#prvek.barva)
    * [.barvaSLegendou()](#prvek.barvaSLegendou)

<a name="new_prvek_new"></a>

### new prvek()
Function package for preparing HTML elements.

<a name="prvek.seznamZatrzitek"></a>

### prvek.seznamZatrzitek()
**Kind**: static method of <code>[prvek](#prvek)</code>  
**Todo**

- [ ] Move to [tfw](#tfw)

<a name="prvek.tabulka"></a>

### ~~prvek.tabulka()~~
***Deprecated***

**Kind**: static method of <code>[prvek](#prvek)</code>  
**See**: tfw.table  
<a name="prvek.radek"></a>

### ~~prvek.radek()~~
***Deprecated***

**Kind**: static method of <code>[prvek](#prvek)</code>  
**See**: tfw.tr  
<a name="prvek.sloupec"></a>

### ~~prvek.sloupec()~~
***Deprecated***

**Kind**: static method of <code>[prvek](#prvek)</code>  
**See**: tfw.td  
<a name="prvek.soubory"></a>

### prvek.soubory()
**Kind**: static method of <code>[prvek](#prvek)</code>  
**Todo**

- [ ] Remove dependencies on Triobo
- [ ] Move to [tfw](#tfw)

<a name="prvek.barva"></a>

### prvek.barva()
**Kind**: static method of <code>[prvek](#prvek)</code>  
**Todo**

- [ ] Remove dependencies on Triobo
- [ ] Move to [tfw](#tfw)

<a name="prvek.barvaSLegendou"></a>

### prvek.barvaSLegendou()
**Kind**: static method of <code>[prvek](#prvek)</code>  
**Todo**

- [ ] Remove dependencies on Triobo
- [ ] Move to [tfw](#tfw)

<a name="Dyntable"></a>

## ~~Dyntable~~
***Deprecated***

**Kind**: global class  
**See**: tfw.dynamicTable  
<a name="AJAX_LOADER"></a>

## AJAX_LOADER : <code>string</code>
HTML to show when some content is being loaded.

**Kind**: global constant  
<a name="cmp"></a>

## cmp(a, b)
**Kind**: global function  

| Param | Type |
| --- | --- |
| a | <code>number</code> | 
| b | <code>number</code> | 

