# ICookingRecipeManager

Default interface for Registry based handlers as they can all remove recipes by ResourceLocation.

This class was added by a mod with mod-id `crafttweaker`. So you need to have this mod installed if you want to use this feature.

## Importowanie klasy
It might be required for you to import the package if you encounter any issues (like casting an Array), so better be safe than sorry and add the import.
```zenscript
crafttweaker.api.registries.ICookingRecipeManager
```

## Implemented Interfaces
ICookingRecipeManager implements the following interfaces. That means any method available to them can also be used on this class.
- [crafttweaker.api.registries.IRecipeManager](/vanilla/api/managers/IRecipeManager)

## Metody
### addJSONRecipe

Adds a recipe based on a provided IData. The provided IData should represent a DataPack JSON, this effectively allows you to register recipes for any DataPack supporting IRecipeType systems.

```zenscript
furnace.addJSONRecipe(name as String, data as crafttweaker.api.data.IData);
furnace.addJSONRecipe("recipe_name", {ingredient:{item:<item:minecraft:gold_ore>.registryName},result:<item:minecraft:cooked_porkchop>.registryName,experience:0.35 as float, cookingtime:100});
```

| Parametr | Typ                                                    | Opis                            |
| -------- | ------------------------------------------------------ | ------------------------------- |
| Nazwa    | Ciąg znaków                                            | name of the recipe              |
| dane     | [crafttweaker.api.data.IData](/vanilla/api/data/IData) | data representing the json file |


### napis

Adds a recipe based on given params.

```zenscript
furnace.addRecipe(name as String, output as crafttweaker.api.item.IItemStack, input as crafttweaker.api.item.IIngredient, xp as float, cookTime as int);
furnace.addRecipe("wool2diamond", <item:diamond>, <tag:minecraft:wool>, 1.0, 0);
```

| Parametr | Typ                                                                 | Opis                            |
| -------- | ------------------------------------------------------------------- | ------------------------------- |
| Nazwa    | Ciąg znaków                                                         | Name of the new recipe          |
| wyjście  | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)   | IItemStack output of the recipe |
| input    | [crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient) | IIngredient input of the recipe |
| xp       | zmiennoprzecinkowe                                                  | how much xp the player gets     |
| cookTime | odcień                                                              | how long it takes to cook       |


### usuń wszystko

Remove all recipes in this registry

```zenscript
piec.removeAll();
```

### removeByModid

Remove recipe based on Registry name modid

```zenscript
furnace.removeByModid(modid as String);
furnace.removeByModid("minecraft");
```

| Parametr | Typ         | Opis                           |
| -------- | ----------- | ------------------------------ |
| modid    | Ciąg znaków | modid of the recipes to remove |


### removeByName

Remove recipe based on Registry name

```zenscript
furnace.removeByName(name as String);
furnace.removeByName("minecraft:furnace");
```

| Parametr | Typ         | Opis                              |
| -------- | ----------- | --------------------------------- |
| Nazwa    | Ciąg znaków | registry name of recipe to remove |


### removeByRegex

Remove recipe based on regex

```zenscript
furnace.removeByRegex(regex as String);
furnace.removeByRegex("\\d_\\d");
```

| Parametr | Typ         | Opis                   |
| -------- | ----------- | ---------------------- |
| regex    | Ciąg znaków | regex to match against |


### removeRecipe

Remove a recipe based on it's output.

```zenscript
furnace.removeRecipe(output as crafttweaker.api.item.IItemStack);
furnace.removeRecipe(<item:minecraft:glass>);
```

| Parametr | Typ                                                               | Opis                 |
| -------- | ----------------------------------------------------------------- | -------------------- |
| wyjście  | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack) | output of the recipe |



Removes a recipe based on it's output and input.

```zenscript
furnace.removeRecipe(output as crafttweaker.api.item.IItemStack, input as crafttweaker.api.item.IIngredient);
furnace.removeRecipe(<item:minecraft:diamond>, <tag:minecraft:wool>);
```

| Parametr | Typ                                                                 | Opis                                 |
| -------- | ------------------------------------------------------------------- | ------------------------------------ |
| wyjście  | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)   | IItemStack output of the recipe.     |
| input    | [crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient) | IIngredient of the recipe to remove. |


