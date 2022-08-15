# モック
## テストダブル
`double メソッド`を使用して、代替えオブジェクトを作成する
   
(例)
```rb
item = double('item')
```
  
### 検証機能付きテストダブル
モデルのインスタンスと同じように振る舞う
  
`instance_double`とすることでスタブ化するメソッドが存在するか検証する
(例)`Item`モデルのインスタンスのように振る舞う
```rb
item = instance_double('Item', name: 'アイテム名')
```

<br>

## スタブ
ダミーメソッドを作成。  
`item.name`を呼ぶと`"アイテム名"`と返す
```rb
item.stub(:name) { "アイテム名" }
```