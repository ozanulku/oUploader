# oUploader
A simple jQuery Ajax File Uploader Plugin


Options
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
```javascript
var instance = $("#ou-wrap").oUploader("instance");
```

**destroy**
Destroy the everything related to a oUploader instance
```javascript
instance.destroy();
```
