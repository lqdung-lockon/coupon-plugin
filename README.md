# coupon-plugin (クーポン管理)

商品・カテゴリーに対して、一定額・一定率での割引を適用するクーポンを発行できます。


## 管理画面

* クーポン管理機能を追加
* 受注管理 : 受注詳細について、利用されたクーポンコードの表記を追加

## フロント
* 注文確認 : クーポンコードの入力
  入力されたクーポンコードに対応する商品がカゴ中にあれば、割引適用
    割引 = 小計 + 手数料 + 送料 - (クーポン設定額 or 割引率から求めた値）
    ※尚、率で算定した場合の端数処理は「共通税率設定>課税規則」に準じるようにしています。

# PHPUnit Code Coverage
1. In eccube 3 root folder, run:
    - vendor\bin\phpunit --configuration app\Plugin\Coupon
2. Or in plugin folder:
    - ..\..\..\vendor\bin\phpunit
