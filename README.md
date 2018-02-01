# deep-link.js

[![NPM Version][npm-image]][npm-url]
[![NPM Downloads][downloads-image]][downloads-url]
[![Build Status][travis-image]][travis-url]
[![Test Coverage][coveralls-image]][coveralls-url]

🌈 Redirecting native iOS/Android App from your Website using app scheme.

## Usage
### 1. Include deep-link.js on your site.

#### Using Bower
> bower install --save deep-link
```
<script src="./bower_components/deep-link/dist/deep-link.min.js" type="text/javascript"></script>
```

#### Using NPM
> npm install --save flosdor@deep-link
```
import DeepLink from 'deep-link.js';
```

### 2. Initialize deep-link.js related by your app infomation.
```javascript
var deepLink = new DeepLink({
  appStore: 'https://itunes.apple.com/kr/app/id123456789',
  playStore: 'https://play.google.com/store/apps/details?id=com.example.myApp',
});
```

#### 2-1. Register click event
```javascript
deepLink.register(document.getElementById('test'), {
  appScheme: 'myApp://example/51', // Required
  webUrl: 'http://www.naver.com', // Optional
});
```

#### 2-2. Manual
```javascript
deepLink.openApp({
  appScheme: 'myApp://example/51', // Required
  webUrl: 'http://www.naver.com', // Optional
});
```

## Issues
Feel free to submit issues and enhancement requests.

## Contributing
Bug reports and pull requests are welcome on GitHub at https://github.com/flosdor/deep-link

 1. **Fork** the repo on GitHub
 2. **Clone** the project to your own machine
 3. **Commit** changes to your own branch
 4. **Push** your work back up to your fork
 5. Submit a **Pull request** so that we can review your changes

NOTE: Be sure to merge the latest from "upstream" before making a pull request!

## License

[MIT LICENSE](LICENSE)

[npm-image]: https://img.shields.io/npm/v/deep-link.js.svg
[npm-url]: https://npmjs.org/package/deep-link.js
[travis-image]: https://img.shields.io/travis/flosdor/deep-link/master.svg
[travis-url]: https://travis-ci.org/flosdor/deep-link
[coveralls-image]: https://coveralls.io/repos/github/flosdor/deep-link/badge.svg
[coveralls-url]: https://coveralls.io/github/flosdor/deep-link
[downloads-image]: https://img.shields.io/npm/dm/deep-link.js.svg
[downloads-url]: https://npmjs.org/package/deep-link.js