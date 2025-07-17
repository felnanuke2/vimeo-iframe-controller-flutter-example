# test_iframe_vimeo

This repository demonstrates how to communicate between a Flutter app and a web page using message passing via the `window` object. The example uses a Vimeo video embedded in an iframe and shows how Flutter can interact with the web player to perform actions such as play, pause, mute, unmute, and listen for player events.

## How It Works

- The web page loads the Vimeo Player API and creates an iframe for the video.
- JavaScript functions are exposed to control the video (play, pause, mute, etc.).
- The web page listens for Vimeo player events and sends messages to Flutter using `window.flutter_inappwebview.callHandler`.
- Flutter can trigger these JavaScript functions and receive event callbacks to update its UI or perform actions (e.g., show/hide controllers, seek, etc.).

## Usage

1. Open `index.html` in a webview within your Flutter app using [flutter_inappwebview](https://pub.dev/packages/flutter_inappwebview).
2. Use `callHandler` in Flutter to send commands to the web page and listen for events.
3. The web page will respond to these commands and send event notifications back to Flutter.

## Example Actions
- Display or hide video controllers
- Play, pause, mute, or unmute the video
- Seek to a specific time
- Listen for player events (play, pause, error, volume change, loaded)

## License
MIT
