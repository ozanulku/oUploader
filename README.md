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

>*returns oUploader Object*

Get the instance of oUploader.
```javascript
var instance = $("#ou-wrap").oUploader("instance");
```

**destroy**

>*returns jQuery of the oUploader container*

Destroy the everything related to a oUploader instance
```javascript
instance.destroy();
```

**isEmpty**

>*returns true if there is any files selected, false otherwise*

Check if there is any files selected.
```javascript
instance.isEmpty();
```

**option**

>*return oUploader Object*

Change/set options.
```javascript
instance.option(newOptions);
```

Options
------
