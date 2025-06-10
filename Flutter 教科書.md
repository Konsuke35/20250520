できたこと（過去形）
ドラッグ＆ドロップでFlutterのUIを構築
コードを自動生成（Dart）
簡単なUIプロトタイピング


chaputer4

# chaputer4FlutterのAppBarまとめ

## AppBarとは

- Flutterにおける **Material Design** の構成要素の一つ。
- スマートフォンアプリの **画面上部** に表示される領域。
- 主な目的は **画面タイトルや操作アイコンの表示**。
- 各プラットフォームにおける対応名称:
  - Android → `Action Bar`
  - iOS → `Navigation Bar`
- 主な役割:
  - タイトル表示
  - 戻るボタンの提供
  - 検索・メニューアイコンの表示
- Material Designガイドラインに沿った統一感あるUI設計が可能。
- Flutterのウィジェットの一つで、`AppBar`クラスを使用して構築。

## AppBarの主要プロパティ

| プロパティ名 | 説明 |
|--------------|------|
| `title` | AppBarの中央に表示されるタイトル（通常は`Text`ウィジェット） |
| `actions` | 右側に並ぶアイコンやボタンのリスト（例：`IconButton`） |
| `leading` | 左側に表示されるウィジェット（例：戻るボタン、ハンバーガーメニュー） |
| `bottom` | AppBar下部に表示されるウィジェット（例：タブバー） |

## AppBarの実装例（コードスニペット）

```dart
AppBar(
  title: Text('タイトル'),
  leading: IconButton(
    icon: Icon(Icons.menu),
    onPressed: () {
      // メニューを開く処理
    },
  ),
  actions: [
    IconButton(
      icon: Icon(Icons.search),
      onPressed: () {
        // 検索処理
      },
    ),
    IconButton(
      icon: Icon(Icons.more_vert),
      onPressed: () {
        // その他のメニュー
      },
    ),
  ],
  bottom: TabBar(
    tabs: [
      Tab(icon: Icon(Icons.home)),
      Tab(icon: Icon(Icons.settings)),
    ],
  ),
)
