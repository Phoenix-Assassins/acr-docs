# ShopProtocol
| Method ID | Method Name |
|-----------|-------------|
| 1 | [AddItem](#1-additem) |
| 2 | [RemoveItem](#2-removeitem) |
| 3 | [RequestItems](#3-requestitems) |
| 4 | [AddCurrency](#4-addcurrency) |
| 5 | [RemoveCurrency](#5-removecurrency) |
| 6 | [GetCurrency](#6-getcurrency) |
| 7 | [BuyItem](#7-buyitem) |
| 8 | [BuyItemNoChecks](#8-buyitemnochecks) |
| 9 | [BuyItems](#9-buyitems) |
| 10 | [BuyItemsNoChecks](#10-buyitemsnochecks) |
| 11 | [RequestBoughtItems](#11-requestboughtitems) |

# (1) AddItem
## Request
| Type | Name |
|------|------|
| [ShopItem](#shopitem-structure) | item |

## Response
This method does not return anything.

# (2) RemoveItem
## Request
| Type | Name |
|------|------|
| uint32 | itemId |

## Response
This method does not return anything.

# (3) RequestItems
## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| List<[ShopItem](#shopitem-structure)> | items |

# (4) AddCurrency
## Request
| Type | Name |
|------|------|
| uint32 | amount |

## Response
| Type | Name |
|------|------|
| uint32 | unkUint |

# (5) RemoveCurrency
## Request
| Type | Name |
|------|------|
| uint32 | amount |

## Response
| Type | Name |
|------|------|
| uint32 | unkUint |

# (6) GetCurrency
## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| uint32 | currency |

# (7) BuyItem
## Request
| Type | Name |
|------|------|
| uint32 | itemId |

## Response
| Type | Name |
|------|------|
| bool | unkBool |
| uint32 | unkUint |
| [PlayerBoughtShopItem](#playerboughtshopitem-structure) | boughtItem |

# (8) BuyItemNoChecks
## Request
| Type | Name |
|------|------|
| uint32 | unkUint1 |
| uint32 | unkUint2 |

## Response
| Type | Name |
|------|------|
| bool | unkBool |
| uint32 | unkUint |

# (9) BuyItems
## Request

| Type | Name |
|------|------|
| List\<uint32> | itemIds |

## Response
| Type | Name |
|------|------|
| uint32 | unkUint |
| List<[PlayerBoughtShopItem](#playerboughtshopitem-structure)> | items |

# (10) BuyItemsNoChecks
## Request
| Type | Name |
|------|------|
| List\<uint32> | itemIds |

## Response
| Type | Name |
|------|------|
| bool | unkBool |
| uint32 | unkUint |

# (11) RequestBoughtItems
## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| List<[PlayerBoughtShopItem](#playerboughtshopitem-structure)> | items |

# Types

## ShopItem ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint1 |
| string | unkString |
| uint32 | unkUint2 |
| uint32 | unkUint3 |

## PlayerBoughtShopItem ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint |
| uint64 | unkLong |
