# Unity-Utils
Unity向けの便利な何かしら達

## Extensions

拡張クラスたち

### ButtonExtension

- `void SetTitle()`: Buttonのタイトルをセットするやつ（HierarchからButton作ったものを想定している）

### DateTimeExtension

- `long Timestamp()`: DateTimeをUNIXタイムスタンプに変換する

### GameObjectExtension

- `void AddComponentIfNeeded<T>()`: 指定されたComponentがなければ追加するやつ  
- `void AddClickEventTrigger(UnityAction<BaseEventData>)`: EventTrigger.PointerClickを設定してくれるやつ  
- `void AddEventTrigger(EventTriggerType, UnityAction<BaseEventData>)`: 指定されたEventTriggerを設定してくれるやつ

### IEnumerableExtension

- `IEnumerable<T> Shuffle<T>()`: シャッフルして返すやつ

### ListExtension

- `T At(T)`: Listの指定された位置を返すやつ引数でなかった場合のデフォルト値を指定する  
- `T Pop()`: Listの最後尾を取り出すやつ（破壊的）  
- `T RandomOne()`: Listからランダムで1つ抜き出すやつ

### ObjectExtension

- `int ToInt(int)`: intにparseしてくれるやつ（引数でparse失敗した場合のデフォルト値を設定）  

### StringExtension

- `Color ToColor()`: カラーコードからColorを生成するやつ

### TransformExtension

- `void ChangeLayersRecursively(string)`: 再帰的に指定されたレイヤーに変えるやつ

## Network

### NTP

公開されているNTPサービスをつかって正しい現在時刻を取得するやつ
CREDIT: [NICT様](http://jjy.nict.go.jp/ntp/)

- `void GetTimestamp(System.Action<long?>)`: UNIXタイムスタンプを取得
- `void GetTimestamp(System.Action<DateTime?>)`: UNIXタイムスタンプをDateTimeに変換して取得  
  DateTimeはLocalDateTimeに変換
