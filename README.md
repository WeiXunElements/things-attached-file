# things-attached-file

### 첨부파일 목록을 서버로 부터 받아와 출력하고 파일을 다운로드 및 업로드 할 수 있는 컴퍼넌트

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
Ex)
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
Ex)
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

## 2. 개발
### 2.1 Polymer-CLI 설치

First, make sure you have the [Polymer CLI](https://www.npmjs.com/package/polymer-cli) installed. Then run `polymer serve` to serve your application locally.

### 2.2 Application 수행

```
$ polymer serve
```

### 2.3 Application 빌드

```
$ polymer build
```

아래 명령어로 ` build/bundled`나 ` build/unbundled`에서 서버를 띄울수 있다.

```
$ polymer serve build/bundled
```

### 2.3 Running Tests

```
$ polymer test
```

테스트는 [web-component-tester](https://github.com/Polymer/web-component-tester)에서 설명한데로 설정완료됨.
아래 명령어로 테스트를 수행할 수 있다.
```
$ polymer test
```
