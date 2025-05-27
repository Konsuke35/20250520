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
        style: TextStyle(fontSize:32.0),
      ),
    );
  }
}

main()関数でアプリを起動：runApp(MyApp());

MyAppはStatelessWidgetを継承したウィジェット

buildメソッドでUIを構築

MaterialAppウィジェットを返す（アプリの基本構造）

homeプロパティにTextウィジェットを配置し、「Hello, Flutter World!!」を表示

テキストのサイズはTextStyle(fontSize: 32.0)で指定
