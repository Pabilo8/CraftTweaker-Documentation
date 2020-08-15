# BlockPos

Represents a position of a block in the world

这个类由mod-id为`crafttweaker`的模组添加. 因此，如果要使用此功能，则需要安装此mod。

## 导入类
如果遇到任何问题（例如强制转换数组），则可能需要导入软件包，因此，最好的方式就是导入包支持。
```zenscript
crafttweaker.api.util.BlockPos
```

## Constructor #构造函数
```zenscript
new crafttweaker.api.util.BlockPos(x as int, y as int, z as int);
```
| 参数 | 类型  | 描述                      |
| -- | --- | ----------------------- |
| x  | int | No description provided |
| y  | int | No description provided |
| z  | 整数  | No description provided |



## 方法
### 添加

Adds two positions together and returns the result.

Returns [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos)

```zenscript
new BlockPos(0, 1, 2).add(pos as crafttweaker.api.util.BlockPos);
new BlockPos(0, 1, 2).add(new BlockPos(3, 2, 1));
```

| 参数 | 类型                                                           | 说明                    |
| -- | ------------------------------------------------------------ | --------------------- |
| 点  | [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) | other position to add |



Adds the given values to this position, and returns a new position with the new values.

Returns [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos)

```zenscript
new BlockPos(0, 1, 2).add(x as double, y as double, z as double);
new BlockPos(0, 1, 2).add(50.21, -20.8, -25.2);
```

| 参数 | 类型  | 描述             |
| -- | --- | -------------- |
| x  | 双精度 | x value to add |
| 年  | 双精度 | y value to add |
| z  | 双精度 | z value to add |


### crossProduct

Creates a new BlockPos based on the cross product of this position, and the given position

Returns [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos)

```zenscript
new BlockPos(0, 1, 2).crossProduct(pos as crafttweaker.api.util.BlockPos);
new BlockPos(0, 1, 2).crossProduct(new BlockPos(5, 8, 2););
```

| 参数 | 类型                                                           | 描述                        |
| -- | ------------------------------------------------------------ | ------------------------- |
| 点  | [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) | BlockPos to cross product |


### distanceSq

Gets the squared distance of this position to the specified BlockPos, using the center of the BlockPos

Returns double

```zenscript
new BlockPos(0, 1, 2).distanceSq(to as crafttweaker.api.util.BlockPos);
new BlockPos(0, 1, 2).distanceSq(new BlockPos(256, 128, 10););
```

| 参数 | 类型                                                           | 描述                        |
| -- | ------------------------------------------------------------ | ------------------------- |
| 到  | [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) | BlockPos to check against |



Gets the squared distance of this position to the specified BlockPos

Returns double

```zenscript
new BlockPos(0, 1, 2).distanceSq(to as crafttweaker.api.util.BlockPos, useCenter as boolean);
new BlockPos(0, 1, 2).distanceSq(new BlockPos(256, 128, 10);, true);
```

| 参数        | 类型                                                           | 描述                                                                    |
| --------- | ------------------------------------------------------------ | --------------------------------------------------------------------- |
| 到         | [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) | BlockPos to check against                                             |
| useCenter | boolean                                                      | should the center of the coordinate be used? (adds 0.5 to each value) |



Gets the squared distance of this position to the specified coordinates

Returns double

```zenscript
new BlockPos(0, 1, 2).distanceSq(x as double, y as double, z as double, useCenter as boolean);
new BlockPos(0, 1, 2).distanceSq(500.25, 250.75, 100.20, false);
```

| 参数        | 类型      | 描述                                                                    |
| --------- | ------- | --------------------------------------------------------------------- |
| x         | 双精度     | x position to check against                                           |
| 年         | 双精度     | y position to check against                                           |
| z         | 双精度     | z position to check against                                           |
| useCenter | boolean | should the center of the coordinate be used? (adds 0.5 to each value) |


### 向下

Creates a new BlockPos based on this BlockPos that is one block lower than this BlockPos

 Returns: `a new BlockPos that is one block lower than this BlockPos`

Returns net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).down();
```

### 东部地区

Creates a new BlockPos based on this BlockPos that is one block east of this BlockPos

 Returns: `a new BlockPos that is one block east of this BlockPos`

Returns net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).east();
```


Creates a new BlockPos based on this BlockPos that is n block(s) east of this BlockPos

 Returns: `a new BlockPos that is n block(s) east of this BlockPos`

Returns net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).east(n as int);
new BlockPos(0, 1, 2).east(2);
```

| 参数 | 类型 | 描述                      |
| -- | -- | ----------------------- |
| n  | 整数 | No description provided |


### manhattanDistance

Gets the Manhattan Distance of this pos compared to a different position

返回为int值

```zenscript
new BlockPos(0, 1, 2).manhattanDistance(other as crafttweaker.api.util.BlockPos);
new BlockPos(0, 1, 2).manhattanDistance(new BlockPos(4, 5, 6));
```

| 参数    | 类型                                                           | 描述                                    |
| ----- | ------------------------------------------------------------ | ------------------------------------- |
| other | [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) | other position to get the distance to |


### 北区

Creates a new BlockPos based on this BlockPos that is one block north of this BlockPos

 Returns: `a new BlockPos that is one block north of this BlockPos`

Returns net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).north();
```


Creates a new BlockPos based on this BlockPos that is n block(s) north of this BlockPos

 Returns: `a new BlockPos that is n block(s) north of this BlockPos`

Returns net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).north(n as int);
new BlockPos(0, 1, 2).north(10);
```

| 参数 | 类型 | 描述                      |
| -- | -- | ----------------------- |
| n  | 整数 | No description provided |


### offset

Creates a new BlockPos based on this BlockPos that is one block offset of this BlockPos based on the given [crafttweaker.api.util.Direction](/vanilla/api/util/Direction)

 Returns: `a new BlockPos that is 1 block offset of this BlockPos`

Returns [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos)

```zenscript
new BlockPos(0, 1, 2).offset(direction as crafttweaker.api.util.Direction);
new BlockPos(0, 1, 2).offset(<direction:east>);
```

| 参数        | 类型                                                             | 描述                      |
| --------- | -------------------------------------------------------------- | ----------------------- |
| direction | [crafttweaker.api.util.Direction](/vanilla/api/util/Direction) | No description provided |



Creates a new BlockPos based on this BlockPos that is n block(s) offset of this BlockPos based on the given [crafttweaker.api.util.Direction](/vanilla/api/util/Direction)

 Returns: `a new BlockPos that is n block(s) offset of this BlockPos`

Returns [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos)

```zenscript
new BlockPos(0, 1, 2).offset(direction as crafttweaker.api.util.Direction, n as int);
new BlockPos(0, 1, 2).offset(<direction:south>, 3);
```

| 参数        | 类型                                                             | 描述                      |
| --------- | -------------------------------------------------------------- | ----------------------- |
| direction | [crafttweaker.api.util.Direction](/vanilla/api/util/Direction) | No description provided |
| n         | 整数                                                             | No description provided |


### 南方

Creates a new BlockPos based on this BlockPos that is one block south of this BlockPos

 Returns: `a new BlockPos that is one block south of this BlockPos`

Returns net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).south();
```


Creates a new BlockPos based on this BlockPos that is n block(s) south of this BlockPos

 Returns: `a new BlockPos that is n block(s) south of this BlockPos`

Returns net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).south(n as int);
new BlockPos(0, 1, 2).south(12);
```

| 参数 | 类型 | 描述                      |
| -- | -- | ----------------------- |
| n  | 整数 | No description provided |


### subtract

Subtracts two positions together and returns the result.

Returns [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos)

```zenscript
new BlockPos(0, 1, 2).subtract(pos as crafttweaker.api.util.BlockPos);
new BlockPos(0, 1, 2).subtract(new BlockPos(2, 1, 3));
```

| 参数 | 类型                                                           | 描述                       |
| -- | ------------------------------------------------------------ | ------------------------ |
| 点  | [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) | other position to remove |


### 上

Creates a new BlockPos based on this BlockPos that is one block higher than this BlockPos

 Returns: `a new BlockPos that is one block higher than this BlockPos`

Returns net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).up();
```


Creates a new BlockPos based on this BlockPos that is n block(s) higher than this BlockPos

 Returns: `a new BlockPos that is n block(s) higher than this BlockPos`

Returns net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).up(n as int);
new BlockPos(0, 1, 2).up(45);
```

| 参数 | 类型 | 描述                      |
| -- | -- | ----------------------- |
| n  | 整数 | No description provided |


### 西部地区

Creates a new BlockPos based on this BlockPos that is one block west of this BlockPos

 Returns: `a new BlockPos that is one block west of this BlockPos`

Returns net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).west();
```


Creates a new BlockPos based on this BlockPos that is n block(s) west of this BlockPos

 Returns: `a new BlockPos that is n block(s) west of this BlockPos`

Returns net.minecraft.util.math.BlockPos

```zenscript
new BlockPos(0, 1, 2).west(n as int);
new BlockPos(0, 1, 2).west(120);
```

| 参数 | 类型 | 描述                      |
| -- | -- | ----------------------- |
| n  | 整数 | No description provided |


### withinDistance

Checks if the given BlockPos is within the specified distance of this BlockPos (this uses the middle of the BlockPos)

返回为布尔值

```zenscript
new BlockPos(0, 1, 2).withinDistance(pos as crafttweaker.api.util.BlockPos, distance as double);
new BlockPos(0, 1, 2).withinDistance(new BlockPos(80, 75, 54);, 10);
```

| 参数       | 类型                                                           | 描述                                             |
| -------- | ------------------------------------------------------------ | ---------------------------------------------- |
| 点        | [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) | BlockPos to check if it is within the distance |
| distance | 双精度                                                          | distance to check within                       |



## 参数

| 名称 | 类型 | 可获得  | 可设置   |
| -- | -- | ---- | ----- |
| x  | 整数 | true | false |
| 年  | 整数 | true | false |
| z  | 整数 | true | false |

## 运算符
### ADD

Adds two positions together and returns the result.

```zenscript
new BlockPos(0, 1, 2) + pos as crafttweaker.api.util.BlockPos
new BlockPos(0, 1, 2) + new BlockPos(3, 2, 1)
```

| 参数 | 类型                                                           | 描述                    |
| -- | ------------------------------------------------------------ | --------------------- |
| 点  | [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) | other position to add |
### SUB

Subtracts two positions together and returns the result.

```zenscript
new BlockPos(0, 1, 2) - pos as crafttweaker.api.util.BlockPos
new BlockPos(0, 1, 2) - new BlockPos(2, 1, 3)
```

| 参数 | 类型                                                           | 描述                       |
| -- | ------------------------------------------------------------ | ------------------------ |
| 点  | [crafttweaker.api.util.BlockPos](/vanilla/api/util/BlockPos) | other position to remove |

## Casters

| 结果类型 | 是否隐藏  |
| ---- | ----- |
| 长    | false |
