# flutter_webview

Example showing how to serve files from asset to Webview.

Uses [`jaguar_flutter_asset`](https://pub.dartlang.org/packages/jaguar_flutter_asset)
package to serve files from asset.

# Explanation

This example serves flutter assets from asset directory using `FlutterAssetServer`
on port 8080.

```dart
  final server = new Jaguar();
  server.addApi(new FlutterAssetServer());
  await server.serve();
```

It launches a webview on click of a button and point it to `http://localhost:8080/`.

```dart
  flutterWebviewPlugin.launch('http://localhost:8080/',
      fullScreen: true);
```