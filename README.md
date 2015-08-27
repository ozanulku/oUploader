# oUploader
A simple jQuery Ajax File Uploader Plugin


Methods
------
**setDefaults**

Let's you globally change the default options of oUploader.
```javascript
defaults: {
  url: "myUploadHandler.php"
}
$.oUploader("setDefaults", defaults);
//make the myUploaderHandler.php the default url for ajax post
```

**instance**

Get the instance of oUploader.

*returns oUploader Object*
```javascript
var instance = $("#ou-wrap").oUploader("instance");
```

**destroy**

Destroy the everything related to a oUploader instance

*returns jQuery of the oUploader container*
```javascript
instance.destroy();
```

**isEmpty**

Check if there is any files selected.

*returns true if there is any files selected, false otherwise*
```javascript
instance.isEmpty();
```
