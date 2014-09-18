cf-ckeditor-imagebrowser
========================

A barebones setup example for using CKEditor's Image Browser plugin with ColdFusion 10+

This bundle includes a the ImageBrowser CFC for processing the JSON needed for the plugin; along with files for a example setup including a extremely stripped down version of CKEditor.

Here's an example:

```
<html lang="en">

  <head>
  	<script type="text/javascript" src="path/to/ckeditor/ckeditor.js"></script>
  </head>
  
  <body>
    <form style="width: 400px; margin: 20px auto;">
    	<textarea id="pagecontent" name="pagecontent"></textarea>
    </form>
    <script type="text/javascript">
    	CKEDITOR.replace( 'pagecontent', {
    		extraPlugins: "imagebrowser",
    		imageBrowser_listUrl: "path/to/cfc/ImageBrowser.cfc?method=list&dir=path/to/images",
    		toolbar : [ { name: 'insert', items : [ 'Image' ] } ]
    	});
    </script>
  </body>
  
</html>
```
