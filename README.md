It's built using:

- [Electron](https://github.com/atom/electron) - Wraps app for desktop.
- [React](https://github.com/facebook/react) - UI & view components.
- [Redux](https://github.com/rackt/redux) - State management.
- [Redux Sagas](https://github.com/redux-saga/redux-saga) - Handles side effects.
- [Ramda](https://github.com/ramda/ramda) - For functional Javascript.
- [HowlerJs](https://github.com/goldfire/howler.js) - Handles audio objects.
- [ReactIntl](https://github.com/yahoo/react-intl) - Internationalisation.
- [PostCSS](https://github.com/postcss/postcss) - Transform JS styles.
- [Webpack](https://github.com/webpack/webpack) - Bundling JS and hot module replacement.

Tests using [Jest](https://github.com/facebook/jest) and a bit of [Enzyme](https://github.com/airbnb/enzyme).

Code coverage reporting provided by [Coveralls](https://coveralls.io/).

<img src="https://raw.githubusercontent.com/alanhong902/Kakapo-assets/master/images/screenshots/web_app.jpg" />

## Install and run

``` bash
# Clone
$ git clone https://github.com/alanhong902/Kakapo-app.git

# Install
$ cd Kakapo-app && npm install

# Convert .mp3 files to .ogg with ffmpeg
$ brew install ffmpeg --with-libvpx --with-libvorbis
$ cd node_modules/kakapo-assets
$ sh mp3-to-ogg.sh

# Run desktop
$ npm start -- --platform=desktop

# Run website
$ npm start -- --platform=web
```

Both the website and desktop app should automatically open and have hot module enabled for live changes.

## Build for production

``` bash
# Build website
$ npm run build -- --platform=web --production

# Build desktop
$ npm run build -- --platform=desktop --production

# Sign apps and zip after desktop build
$ npm run installer-mac && npm run installer-win
```

## Testing

``` bash
# Test with watch
$ npm test -- --watch

# Test
$ npm test
```

## Bugs and Feature Requests

Have a bug or a feature request? [Please open a new issue here](https://github.com/alanhong902/Kakapo-app/issues/new).
