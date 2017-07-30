## DataTables Export Plugin


Export your grid data to many document. 
Support doc, xls, pdf, csv, xml, html, and print

## Example

```javascript
var dt = $('#example-table').DataTable();

// Export to Word Document
// On element with id="btn-export" clicked
$('body').on('click', '#btn-export', function(e) {
    $.fn.DataTable.Export.word(dt, {
        filename: 'customer-lists',
        title: 'Report',
        message: 'Customer lists',
        header: [
        	'ID',
        	'Name',
        	'Position',
        	'Join Date',
        	'Salary'
        ],
        fields: [
        	0,
        	1,
        	4,
        	5,
        	8
        ]
    });
});

```

## Export to other document types


To Word (.doc) `$.fn.DataTable.Export.word(dataTable, config)`

To Excel (.xls) `$.fn.DataTable.Export.excel(dataTable, config)`

To CSV (.csv) `$.fn.DataTable.Export.csv(dataTable, config)`

To PDF (.pdf) `$.fn.DataTable.Export.pdf(dataTable, config)`

To XML (.xml) `$.fn.DataTable.Export.xml(dataTable, config)`

To HTML `$.fn.DataTable.Export.html(dataTable, config)`

To Print `$.fn.DataTable.Export.print(dataTable, config)`

*) for pdf you must integrate [pdfmake](http://pdfmake.org) plugin (pdfmake.js and vfs_fonts.js)

## Config

```javascript
{
    filename: '...',
    
    // document title
    title: '...',
    
    // document description
    message: '...',
    
    // header title
    header: [
        'ID',
        'Name',
        '...'
    ],
    
    // fields
    fields: [
    	0,
    	1,
    	4,
    	5,
    	'...'
    ],
    // or
    fields: [
    	'employe_id',
    	'name',
    	'....'    	
    ],
    
    // orientation (pdf and word only)
    'orientation' => 'landscape',
    
    // separator (csv only)
    'separator' => ','
    
    // for pdf only
    'download' => 'download' // or 'open' for preview
    'pageSize' => 'A4',
}

```
