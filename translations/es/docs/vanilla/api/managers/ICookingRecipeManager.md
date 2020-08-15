# ICookingRecipeManager

Default interface for Registry based handlers as they can all remove recipes by ResourceLocation.

Esta clase fue añadida por un mod con la ID  `crafttweaker`. Necesitas tener este mod instalado si quieres usar esta caracteristica.

## Importar la clase
Puede ser requerido que importes el paquete si encuentras algun problema (como crear un Array).
```zenscript
crafttweaker.api.registries.ICookingRecipeManager
```

## Implemented Interfaces
ICookingRecipeManager implements the following interfaces. That means any method available to them can also be used on this class.
- [crafttweaker.api.registries.IRecipeManager](/vanilla/api/managers/IRecipeManager)

## Métodos
### addJSONRecipe

Adds a recipe based on a provided IData. The provided IData should represent a DataPack JSON, this effectively allows you to register recipes for any DataPack supporting IRecipeType systems.

```zenscript
furnace.addJSONRecipe(name as String, data as crafttweaker.api.data.IData);
furnace.addJSONRecipe("recipe_name", {ingredient:{item:<item:minecraft:gold_ore>.registryName},result:<item:minecraft:cooked_porkchop>.registryName,experience:0.35 as float, cookingtime:100});
```

| Parámetro | Tipo                                                   | Descripción                     |
| --------- | ------------------------------------------------------ | ------------------------------- |
| nombre    | Cadena                                                 | name of the recipe              |
| datos     | [crafttweaker.api.data.IData](/vanilla/api/data/IData) | data representing the json file |


### addReceta

Adds a recipe based on given params.

```zenscript
furnace.addRecipe(name as String, output as crafttweaker.api.item.IItemStack, input as crafttweaker.api.item.IIngredient, xp as float, cookTime as int);
furnace.addRecipe("wool2diamond", <item:diamond>, <tag:minecraft:wool>, 1.0, 0);
```

| Parámetro | Tipo                                                                | Descripción                     |
| --------- | ------------------------------------------------------------------- | ------------------------------- |
| nombre    | Cadena                                                              | Name of the new recipe          |
| salida    | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)   | IItemStack output of the recipe |
| input     | [crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient) | IIngredient input of the recipe |
| xp        | flotante                                                            | how much xp the player gets     |
| cookTime  | int                                                                 | how long it takes to cook       |


### eliminar todo

Remove all recipes in this registry

```zenscript
furnace.removeAll();
```

### removeByModid

Remove recipe based on Registry name modid

```zenscript
furnace.removeByModid(modid as String);
furnace.removeByModid("minecraft");
```

| Parámetro | Tipo   | Descripción                    |
| --------- | ------ | ------------------------------ |
| modificar | Cadena | modid of the recipes to remove |


### removeByName

Remove recipe based on Registry name

```zenscript
furnace.removeByName(name as String);
furnace.removeByName("minecraft:furnace");
```

| Parámetro | Tipo   | Descripción                       |
| --------- | ------ | --------------------------------- |
| nombre    | Cadena | registry name of recipe to remove |


### removeByRegex

Remove recipe based on regex

```zenscript
furnace.removeByRegex(regex as String);
furnace.removeByRegex("\\d_\\d");
```

| Parámetro | Tipo   | Descripción            |
| --------- | ------ | ---------------------- |
| regex     | Cadena | regex to match against |


### removeRecipe

Remove a recipe based on it's output.

```zenscript
furnace.removeRecipe(output as crafttweaker.api.item.IItemStack);
furnace.removeRecipe(<item:minecraft:glass>);
```

| Parámetro | Tipo                                                              | Descripción          |
| --------- | ----------------------------------------------------------------- | -------------------- |
| salida    | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack) | output of the recipe |



Removes a recipe based on it's output and input.

```zenscript
furnace.removeRecipe(output as crafttweaker.api.item.IItemStack, input as crafttweaker.api.item.IIngredient);
furnace.removeRecipe(<item:minecraft:diamond>, <tag:minecraft:wool>);
```

| Parámetro | Tipo                                                                | Descripción                          |
| --------- | ------------------------------------------------------------------- | ------------------------------------ |
| salida    | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)   | IItemStack output of the recipe.     |
| input     | [crafttweaker.api.item.IIngredient](/vanilla/api/items/IIngredient) | IIngredient of the recipe to remove. |


