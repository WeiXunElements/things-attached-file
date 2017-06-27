# things-attached-file

### 이는 서버로부터 첨부파일 목록을 받아와서 출력하고 파일을 다운로드 및 업로드할 수 있는 컴포넌트이다.

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

## 2. 개발
### 2.1 Polymer-CLI 설치

먼저 [Polymer CLI](https://www.npmjs.com/package/polymer-cli)가 설치되어 있는지 확인한다. 다음, `polymer serve`를 실행하여 로컬에서 응용 프로그램을 제공한다.

### 2.2 Application 실행

```
$ polymer serve
```

### 2.3 Application 빌드

```
$ polymer build
```

아래 명령어로 `build/bundled`나 `build/unbundled`에서 서버를 띄울 수 있다.

```
$ polymer serve build/bundled
```

### 2.4 Test 실행

```
$ polymer test
```

[web-component-tester](https://github.com/Polymer/web-component-tester)에서 설명한 대로, 테스트 설정은 이미 완료되어 있다.
아래 명령어로 테스트를 실행할 수 있다.
```
$ polymer test
```
