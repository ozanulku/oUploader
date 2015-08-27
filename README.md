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
**url** *(required)*

>**_String_**
>
>>Default: undefined

The path passed as the url of the ajax post request.


**trigger**

>**_jQuery, CSS Selector or DOM Element_**
>
>>Default: undefined

If you want to bind the upload to a trigger, set an element as the trigger. If you do not set a valid element as the trigger ajax request is triggered as soon as any files are selected by the file input.


**allowMultiple**

>**_Boolean_**
>
>>Default: false

Set to true in order to allow multiple file selection.
