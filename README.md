# Flutter 入門：基本アプリの構造

このドキュメントでは、Flutterを使ったシンプルなアプリのコード例とその解説をまとめます。Flutterの学習の第一歩として、アプリの構造や各要素の役割を理解するのに役立つ。

## 基本コード例

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      title: 'Flutter Demo',
      home: Text(
        'Hello, Flutter World!!',
        style: TextStyle(fontSize: 32.0),
      ),
    );
  }
}


