# RecipeFunctionSingle

crafttweakerのmod-idを持つmodによって追加されているクラスです。 従って、この機能を利用する場合はこのmodをインストールする必要があります。

## クラスのインポート
問題が発生した場合には、インポートが必要になります。とはいえ、お手数ですが予めインポートしておくほうが安全です。
```zenscript
crafttweaker.api.recipe.RecipeFunctionSingle
```

## Functional Interface

This class is a functional interface. This means that you can use the lambda notation to create an instance of it. The lambda notation looks like:
```zenscript
(usualOut, inputs) => <item:minecraft:dirt>
```
## メソッド
### process

Return type: [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)

```zenscript
myRecipeFunctionSingle.process(usualOut as crafttweaker.api.item.IItemStack, inputs as crafttweaker.api.item.IItemStack);
```

| パラメータ    | タイプ                                                               | 説明                      |
| -------- | ----------------------------------------------------------------- | ----------------------- |
| usualOut | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack) | No description provided |
| inputs   | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack) | No description provided |


