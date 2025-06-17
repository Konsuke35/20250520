できたこと（過去形）
ドラッグ＆ドロップでFlutterのUIを構築
コードを自動生成（Dart）
簡単なUIプロトタイピング



 
# chaputer4　FlutterのAppBarまとめ（未）P140～

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
```

## Flutter ウィジェット構成: AppBarのLeadingとActions

Flutterの`AppBar`ウィジェットの主要なプロパティである`leading`と`actions`について。

### 1. `leading` (左側のアイコン)

* `AppBar`の左端に配置されるウィジェット。
* ここでは、例として**`BackButton`**ウィジェットが紹介されている。
    * `BackButton`は「前に戻る」ための専用ボタン。
    * `color`プロパティでアイコンの色を指定できる。
    * その他のプロパティは特ない。
* ユーザーが`leading`のアイコンをクリックすると、`bottom`に表示される星の数が減少するデモンストレーションが示唆される。

### 2. `actions` (右側のアイコン群)

* `AppBar`の右側に配置されるウィジェットのリスト。
* 例として**`IconButton`**ウィジェットが使用されており、以下の要素で構成される。
    * `icon`: アイコンの種類 (`Icons.android`など) を指定する。
    * `tooltip`: 長押しした際に表示されるヒントテキスト (`add star...`など) を設定する。
    * `onPressed`: アイコンがクリックされたときに実行される処理を定義する。
* `IconButton`は、アイコンや小さいスペースで内容を表現するのに適しており、クリック時の処理を設定することで様々な機能を持たせることが可能。
