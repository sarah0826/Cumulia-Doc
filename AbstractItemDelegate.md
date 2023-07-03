[wui.basic](../README.md) / [Exports](../modules.md) / AbstractItemDelegate

# Class: AbstractItemDelegate

The AbstractItemDelegate class is used to edit view items.

## Hierarchy

- [`EventWatcher`](EventWatcher.md)

  ↳ **`AbstractItemDelegate`**

  ↳↳ [`ItemDelegate`](ItemDelegate.md)

## Table of contents

### Constructors

- [constructor](AbstractItemDelegate.md#constructor)

### Properties

- [m\_editOnClose](AbstractItemDelegate.md#m_editonclose)
- [m\_editor](AbstractItemDelegate.md#m_editor)
- [m\_item](AbstractItemDelegate.md#m_item)

### Accessors

- [blocked](AbstractItemDelegate.md#blocked)
- [sender](AbstractItemDelegate.md#sender)

### Methods

- [bind](AbstractItemDelegate.md#bind)
- [closeEditor](AbstractItemDelegate.md#closeeditor)
- [createEditor](AbstractItemDelegate.md#createeditor)
- [delegate](AbstractItemDelegate.md#delegate)
- [edit](AbstractItemDelegate.md#edit)
- [emit](AbstractItemDelegate.md#emit)
- [setItemData](AbstractItemDelegate.md#setitemdata)
- [unbind](AbstractItemDelegate.md#unbind)

## Constructors

### constructor

• **new AbstractItemDelegate**()

Creates a new abstract item delegate.

#### Overrides

[EventWatcher](EventWatcher.md).[constructor](EventWatcher.md#constructor)

#### Defined in

view/itemdelegate.ts:14

## Properties

### m\_editOnClose

• `Protected` **m\_editOnClose**: `boolean` = `true`

#### Defined in

view/itemdelegate.ts:9

___

### m\_editor

• `Private` **m\_editor**: [`Widget`](Widget.md)

#### Defined in

view/itemdelegate.ts:8

___

### m\_item

• `Private` **m\_item**: [`ViewItem`](ViewItem.md)

#### Defined in

view/itemdelegate.ts:7

## Accessors

### blocked

• `get` **blocked**(): `boolean`

Returns true if events are blocked; otherwise returns false.

#### Returns

`boolean`

#### Inherited from

EventWatcher.blocked

#### Defined in

abstract/eventwatcher.ts:78

• `set` **blocked**(`blocked`): `void`

If blocked is true, events emitted by this event watcher are blocked (i.e., emitting an event will not call any callback functions binded to it).

#### Parameters

| Name | Type |
| :------ | :------ |
| `blocked` | `boolean` |

#### Returns

`void`

#### Inherited from

EventWatcher.blocked

#### Defined in

abstract/eventwatcher.ts:85

___

### sender

• `Static` `get` **sender**(): [`EventWatcher`](EventWatcher.md)

Returns the object that sent the event.

#### Returns

[`EventWatcher`](EventWatcher.md)

#### Inherited from

EventWatcher.sender

#### Defined in

abstract/eventwatcher.ts:21

## Methods

### bind

▸ **bind**<`K`\>(`name`, `callback`): `void`

Adds a callback function that's going to be called when the event is emitted.

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof [`EventMap`](../interfaces/EventMap.md) |

#### Parameters

| Name | Type |
| :------ | :------ |
| `name` | `K` |
| `callback` | (...`data`: [`EventMap`](../interfaces/EventMap.md)[`K`]) => `void` |

#### Returns

`void`

#### Inherited from

[EventWatcher](EventWatcher.md).[bind](EventWatcher.md#bind)

#### Defined in

abstract/eventwatcher.ts:28

▸ **bind**(`name`, `callback`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `name` | `string` |
| `callback` | (...`data`: `any`[]) => `void` |

#### Returns

`void`

#### Inherited from

[EventWatcher](EventWatcher.md).[bind](EventWatcher.md#bind)

#### Defined in

abstract/eventwatcher.ts:29

___

### closeEditor

▸ `Protected` **closeEditor**(): `void`

Closes the editor.

#### Returns

`void`

#### Defined in

view/itemdelegate.ts:50

___

### createEditor

▸ `Protected` `Abstract` **createEditor**(`item`): [`Widget`](Widget.md)

Returns the editor to be used for editing the given item.

#### Parameters

| Name | Type |
| :------ | :------ |
| `item` | [`ViewItem`](ViewItem.md) |

#### Returns

[`Widget`](Widget.md)

#### Defined in

view/itemdelegate.ts:40

___

### delegate

▸ **delegate**<`K`\>(`watcher`, `name`): `void`

Delegates this event watcher to handle the given watcher's event named name.

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof [`EventMap`](../interfaces/EventMap.md) |

#### Parameters

| Name | Type |
| :------ | :------ |
| `watcher` | [`EventWatcher`](EventWatcher.md) |
| `name` | `K` |

#### Returns

`void`

#### Inherited from

[EventWatcher](EventWatcher.md).[delegate](EventWatcher.md#delegate)

#### Defined in

abstract/eventwatcher.ts:67

▸ **delegate**(`watcher`, `name`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `watcher` | [`EventWatcher`](EventWatcher.md) |
| `name` | `string` |

#### Returns

`void`

#### Inherited from

[EventWatcher](EventWatcher.md).[delegate](EventWatcher.md#delegate)

#### Defined in

abstract/eventwatcher.ts:68

___

### edit

▸ **edit**(`item`): `void`

Starts to edit the given item.

#### Parameters

| Name | Type |
| :------ | :------ |
| `item` | [`ViewItem`](ViewItem.md) |

#### Returns

`void`

#### Defined in

view/itemdelegate.ts:21

___

### emit

▸ **emit**<`K`\>(`name`, `...data`): `boolean`

Emits an arbitrary set of arguments to the callback function which is binded to the event named name.

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof [`EventMap`](../interfaces/EventMap.md) |

#### Parameters

| Name | Type |
| :------ | :------ |
| `name` | `K` |
| `...data` | [`EventMap`](../interfaces/EventMap.md)[`K`] |

#### Returns

`boolean`

#### Inherited from

[EventWatcher](EventWatcher.md).[emit](EventWatcher.md#emit)

#### Defined in

abstract/eventwatcher.ts:48

▸ **emit**(`name`, `...data`): `boolean`

#### Parameters

| Name | Type |
| :------ | :------ |
| `name` | `string` |
| `...data` | `any`[] |

#### Returns

`boolean`

#### Inherited from

[EventWatcher](EventWatcher.md).[emit](EventWatcher.md#emit)

#### Defined in

abstract/eventwatcher.ts:49

___

### setItemData

▸ `Protected` `Abstract` **setItemData**(`editor`, `item`): `void`

Sets the contents of the given editor to the data for the given item.

#### Parameters

| Name | Type |
| :------ | :------ |
| `editor` | [`Widget`](Widget.md) |
| `item` | [`ViewItem`](ViewItem.md) |

#### Returns

`void`

#### Defined in

view/itemdelegate.ts:45

___

### unbind

▸ **unbind**<`K`\>(`name`): `void`

Removes the specified watcher for the event named name.

#### Type parameters

| Name | Type |
| :------ | :------ |
| `K` | extends keyof [`EventMap`](../interfaces/EventMap.md) |

#### Parameters

| Name | Type |
| :------ | :------ |
| `name` | `K` |

#### Returns

`void`

#### Inherited from

[EventWatcher](EventWatcher.md).[unbind](EventWatcher.md#unbind)

#### Defined in

abstract/eventwatcher.ts:37

▸ **unbind**(`name`): `void`

#### Parameters

| Name | Type |
| :------ | :------ |
| `name` | `string` |

#### Returns

`void`

#### Inherited from

[EventWatcher](EventWatcher.md).[unbind](EventWatcher.md#unbind)

#### Defined in

abstract/eventwatcher.ts:38
