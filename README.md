# things-attached-file

### things-attached-file. 첨부파일 목록을 서버로 부터 받아와 출력하고 파일을 다운로드 및 업로드 할 수 있는 컴퍼넌트

  Example:
```html
    <things-attached-file
      target-url="upload/attach"
      method="POST"
      resource-id="1"
      resource-type="Alarm">
    </things-attached-file>
```

## Dependencies

Element dependencies are managed via [Bower](http://bower.io/). You can
install that via:

    npm install -g bower

Then, go ahead and download the element's dependencies:

    bower install


## Playing With Your Element

If you wish to work on your element in isolation, we recommend that you use
[Polyserve](https://github.com/PolymerLabs/polyserve) to keep your element's
bower dependencies in line. You can install it via:

    npm install -g polyserve

And you can run it via:

    polyserve

Once running, you can preview your element at
`http://localhost:8080/components/things-attached-file/`, where `things-attached-file` is the name of the directory containing it.


## Example 1. Things Attached File
`<things-attached-file>` Things Attached File
