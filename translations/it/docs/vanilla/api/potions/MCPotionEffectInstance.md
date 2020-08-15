# MCPotionEffectInstance

Questa classe è stata aggiunta da una mod con ID `crafttweaker`. Perciò, è necessario avere questa mod installata per poter utilizzare questa funzione.

## Importare la classe
Potrebbe essere necessario importare il pacchetto, se si incontrano dei problemi (come castare un vettore), quindi meglio essere sicuri e aggiungere la direttiva di importazione.
```zenscript
crafttweaker.api.potion.MCPotionEffectInstance
```

## Metodi
### addCurativeItem

```zenscript
myMCPotionEffectInstance.addCurativeItem(stack as crafttweaker.api.item.IItemStack);
```

| Parametro | Tipo                                                              | Descrizione                 |
| --------- | ----------------------------------------------------------------- | --------------------------- |
| pila      | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack) | Nessuna descrizione fornita |


### combine

Restituisce un booleano

```zenscript
myMCPotionEffectInstance.combine(effect as crafttweaker.api.potion.MCPotionEffectInstance);
```

| Parametro | Tipo                                                                                          | Descrizione                 |
| --------- | --------------------------------------------------------------------------------------------- | --------------------------- |
| effect    | [crafttweaker.api.potion.MCPotionEffectInstance](/vanilla/api/potions/MCPotionEffectInstance) | Nessuna descrizione fornita |


### getCurativeItems

Returns List<[crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)>

```zenscript
myMCPotionEffectInstance.getCurativeItems();
```

### isCurativeItem

Restituisce un booleano

```zenscript
myMCPotionEffectInstance.isCurativeItem(stack as crafttweaker.api.item.IItemStack);
```

| Parametro | Tipo                                                              | Descrizione                 |
| --------- | ----------------------------------------------------------------- | --------------------------- |
| pila      | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack) | Nessuna descrizione fornita |


### setCurativeItems

```zenscript
myMCPotionEffectInstance.setCurativeItems(items as crafttweaker.api.item.IItemStack[]);
```

| Parametro | Tipo                                                                | Descrizione                 |
| --------- | ------------------------------------------------------------------- | --------------------------- |
| elementi  | [crafttweaker.api.item.IItemStack](/vanilla/api/items/IItemStack)[] | Nessuna descrizione fornita |



## Proprietà

| Nome          | Tipo                                                                          | Ha Getter | Ha Setter |
| ------------- | ----------------------------------------------------------------------------- | --------- | --------- |
| ambient       | boolean                                                                       | vero      | falso     |
| amplificatore | int                                                                           | vero      | falso     |
| durata        | int                                                                           | vero      | falso     |
| effectName    | Stringa                                                                       | vero      | falso     |
| pozione       | [crafttweaker.api.potion.MCPotionEffect](/vanilla/api/potions/MCPotionEffect) | vero      | falso     |
| showIcon      | boolean                                                                       | vero      | falso     |
| showParticles | boolean                                                                       | vero      | falso     |
