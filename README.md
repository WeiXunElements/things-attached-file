# things-attached-file

### It is a component that can receive the attachment list from the server, print it, and download and upload the file.

  Example:
```html
    <things-attached-file
      target-url="upload/attach"
      method="POST"
      resource-id="1"
      resource-type="Alarm">
    </things-attached-file>
```
buttons Ex)
```js
[{
  id: 'delete-btn',
  text: 'delete',
  icon: 'icons:delete'
}, {
  id: 'save-btn',
  text: 'save',
  icon: 'icons:save'
}]
```
gridModel Ex)
```js
[{
 fieldName: 'id'
},
{
 fieldName: 'name'
},
{
 fieldName: 'storage_info',
 dataType: 'object'
},
{
 fieldName: 'tag'
},
{
 fieldName: 'path'
},
{
 fieldName: 'file_size',
 dataType: 'number'
},
{
 fieldName: 'creator',
 dataType: 'object'
},
{
 fieldName: 'created_at'
}]
```
gridColumns Ex)
```js
{
  fieldName: 'id',
  width: 0
}, {
  fieldName: 'name',
  header: {
    text: Things.DataGlobal.t('label.name')
  },
  width: 150
}, {
  name: 'storage_info',
  fieldName: 'storage_info',
  width: 120,
  valueType: 'text',
  type: 'calced',
  header: {
    text: Things.DataGlobal.t('label.storage_info')
  },
  valueCallback : function(column, row) {
    var obj = row.getValue('storage_info');
    return obj ? obj.name : '';
  }
}, {
  fieldName: 'tag',
  header: {
    text: Things.DataGlobal.t('label.tag')
  },
  width: 100
}, {
  fieldName: 'path',
  header: {
    text: Things.DataGlobal.t('label.path')
  },
  width: 400
}, {
  fieldName: 'file_size',
  header: {
    text: Things.DataGlobal.t('label.file_size')
  },
  styles: {
    numberFormat: "#,###",
    textAlignment: 'far'
  },
  width: 80
}, {
  name: 'creator',
  fieldName: 'creator',
  header: {
    text: Things.DataGlobal.t('label.creator')
  },
  width: 100,
  valueType: 'text',
  type: 'calced',
  valueCallback : function(column, row) {
    var obj = row.getValue('creator');
    return obj ? obj.name : '';
  }
}, {
  fieldName: 'created_at',
  header: {
    text: Things.DataGlobal.t('label.created_at')
  },
  width: 130
}
```

## 2. Development
### 2.1 Install Polymer-CLI

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your application locally.

### 2.2 Run Application

```
$ polymer serve
```

### 2.3 Build Application

```
$ polymer build
```

You can launch the server from `build/bundled` or `build/unbundled` with the following command:

```
$ polymer serve build/bundled
```

### 2.4 Run Tests

```
$ polymer test
```

The test has been set up as described in [web-component-tester](https://github.com/Polymer/web-component-tester).
You can run the test with the following command.
```
$ polymer test
```
