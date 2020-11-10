# Post request

```javascript
function POST() {
  //var data = arguments.length > 1 && arguments[1] !== undefined ? arguments[1] : {};
  //var successCallback = arguments[2];
  //var failureCallback = arguments[3];

  var request = window.XMLHttpRequest ? new XMLHttpRequest() : new ActiveXObject('Microsoft.XMLHTTP');

  request.onreadystatechange = function () {
    if (request.readyState === 4 && request.status === 201) {
	//successCallback(JSON.parse(request.responseText), request.status);
    } else if (request.readyState === 4 && request.status === 204) {
      //successCallback({}, request.status);
    } else if (request.readyState === 4 && request.status >= 400) {
      //failureCallback(request.responseText, request.status);
    }
  };

  request.open('POST', config.url, config.async);
  Object.keys(config.headers).forEach(function (key) {
    request.setRequestHeader(key, config.headers[key]);
  });

  request.send(encodeURI(buildParametersString(data)));
}




```

# Get request

```javascript
function GET(config) {
  //var data = arguments.length > 1 && arguments[1] !== undefined ? arguments[1] : {};
  //var successCallback = arguments[2];
  //var failureCallback = arguments[3];

  var request = window.XMLHttpRequest ? new XMLHttpRequest() : new ActiveXObject('Microsoft.XMLHTTP');

  request.onreadystatechange = function () {
    if (request.readyState === 4 && request.status === 200) {
    //  successCallback(JSON.parse(request.responseText), request.status);
    } else if (request.readyState === 4 && request.status >= 400) {
    //  failureCallback(request.responseText, request.status);
    }
  };

  if (Object.keys(data).length < 1) {
    request.open('GET', config.url, config.async);
  } else {
    request.open('GET', config.url + ('?' + encodeURI(buildParametersString(data))), config.async);
  }

  Object.keys(config.headers).forEach(function (key) {
    request.setRequestHeader(key, config.headers[key]);
  });

  request.send();
}
```

