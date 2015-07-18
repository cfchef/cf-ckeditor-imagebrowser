cf-ckeditor-imagebrowser
========================

A barebones setup example for using CKEditor's Image Browser plugin with ColdFusion 10+

This bundle includes a the ImageBrowser CFC for processing the JSON needed for the plugin; along with files for a example setup including a extremely stripped down version of CKEditor.

Here's an example:

```html
<!DOCTYPE html>

<html lang="en">
  
  <head>
    <title>ImageBrowser.cfc For CKEditor Image Browser Addon</title>
    <script src="//cdn.ckeditor.com/4.4.6/standard/ckeditor.js"></script>
  </head>

  <body>
    <h2>CKEditor Image Browser Plugin With ColdFusion 10</h2>
    <form style="width: 600px; margin: 20px auto;">
      <textarea id="pagecontent" name="pagecontent"></textarea>
    </form>
    <script type="text/javascript">
      CKEDITOR.plugins.addExternal( 'imagebrowser', '/path/to/assets/js/ckeditor/plugins/imagebrowser/', 'plugin.js' );
      CKEDITOR.replace( 'pagecontent', {
            extraPlugins: "imagebrowser",
            imageBrowser_listUrl: "path/to/ImageBrowser.cfc?method=list&dir=assets/images"
      });
    </script>
  </body>

</html>
```
