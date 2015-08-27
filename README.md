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


**triggerEvent**

>**_String_**
>
>>Default: "click"

The name of the event that will trigger the upload when fired on the **trigger**. This option only makes sense when set along with the **trigger** option.


**serverParameters**

>**_Object_**
>
>>Default: {}

Key-Value pair you put in this option will be passed as Data to ajax post requests.


**text**

>**_String_**
>
>>Default: "Select File..."

The text of the select file button.


**buttonClass**

>**_String_** (*seperate multiple classes spaces*)
>
>>Default: ""

Class(es) to be added to the select file button.

**buttonStyle**

>**_Object_**
>
>>Default: {}

An object containing style rules to be added to the select file button.


**allowMultiple**

>**_Boolean_**
>
>>Default: false

Set to true in order to allow multiple file selection.

**maxSize**

>**_Number_** (*KiB*)
>
>>Default: undefined

Maximum allowed file size in KiB.


**customFileTypes**

>**_String_**
>
>>Default: undefined

String passed into file input's [accept attribute](http://www.w3schools.com/tags/att_input_accept.asp).


**feedback**

>**_Object_**

**feedback.enabled**

>**_Boolean_**
>
>>Default: true

Set to false if yo do not want the feedback texts to be shown.

**feedback.element**

>**_jQuery, CSS Selector or DOM Element_**
>
>>Default: internal info element of oUploader

The element that feedback text will be written into.


**texts_**

>**_Object_**

Texts used in the plugin.

**texts.success**

>**_String_**
>
>>Default: "Files were successfully uploaded."

success text.

**texts.sizeFail**

>**_String_**
>
>>Default: "Cannot be uploaded because file size exceeds the limit."

Exceeds maximum size failure text.


**onChange**

>**_Function(e, input)_**
>
>>e => change event object
>>input => file input element

Assign a callback to **change** event of the **file input**. If the function *return*s *false*, the selection will be canceled and the input be cleared.


**beforeSend**

>**_Function(jqxhr, ajaxSettings)_**
>
>>jqxhr => [jQuery xhr object](http://api.jquery.com/Types/#jqXHR)
>>ajaxSettings => options of the ajax post

Assign a function to be called on [ajax post before it is send](http://api.jquery.com/jquery.ajax/#jQuery-ajax-settings).

" *A pre-request callback function that can be used to modify the jqXHR object before it is sent. Use this to set custom headers, etc. The jqXHR and settings objects are passed as arguments. This is an Ajax Event. Returning false in the beforeSend function will cancel the request.* "
