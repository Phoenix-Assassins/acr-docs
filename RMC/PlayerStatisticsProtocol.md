# PlayerStatisticsProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [SendArbitratedPlayerStats](#1-sendarbitratedplayerstats) |
| 2 | [SendPlayerStats](#2-sendplayerstats) |
| 3 | [ReadPlayerStats](#3-readplayerstats) |
| 4 | [ReadStatsLeaderboardByRange](#4-readstatsleaderboardbyrange) |
| 5 | [ReadStatsLeaderboardByRangeForPlayer](#5-readstatsleaderboardbyrangeforplayer) |
| 6 | [ReadStatsLeaderboardForPlayers](#6-readstatsleaderboardforplayers) |
| 7 | [ReadStatsLeaderboardFromSlidingTable](#7-readstatsleaderboardfromslidingtable) |
| 8 | [GetFilter](#8-getfilter) |
| 9 | [ActivateFilter](#9-activatefilter) |
| 10 | [DeactivateFilter](#10-deactivatefilter) |
| 11 | [ReadScoreByIds](#11-readscorebyids) |
| 12 | [ReadScoreByRank](#12-readscorebyrank) |

# (1) SendArbitratedPlayerStats

## Request

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[PlayerStatistic](#playerstatistic-structure)> | playerStats |

## Response

This method does not return anything.

# (2) SendPlayerStats

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[PlayerStatistic](#playerstatistic-structure)> | playerStats |

## Response

This method does not return anything.

# (3) ReadPlayerStats

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[StatQuery](#statquery-structure)> | statQueries |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)> | playerNames |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[PlayerStatContainer](#playerstatcontainer-structure)> | statContainers |

# (4) ReadStatsLeaderboardByRange

## Request

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |
| Uint32 | unkUint3 |
| Uint32 | unkUint4 |
| Uint32 | unkUint5 |
| Uint32 | unkUint6 |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[PlayerStatContainer](#playerstatcontainer-structure)> | statContainers |
| Uint32 | unkUint |

# (5) ReadStatsLeaderboardByRangeForPlayer

## Request

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | playerName |
| Uint32 | unkUint3 |
| Uint32 | unkUint4 |
| Uint32 | unkUint5 |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[PlayerStatContainer](#playerstatcontainer-structure)> | statContainers |
| Uint32 | unkUint |

# (6) ReadStatsLeaderboardForPlayers

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[PlayerQuery](#playerquery-structure)> | playerQueries |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)> | playerNames |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[PlayerStatContainer](#playerstatcontainer-structure)> | statContainers |
| Uint32 | unkUint |

# (7) ReadStatsLeaderboardFromSlidingTable

## Request

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[PlayerQuery](#playerquery-structure)> | playerQueries |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string)> | playerNames |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[PlayerStatContainer](#playerstatcontainer-structure)> | statContainers |

# (8) GetFilter

## Request

This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[Filter](#filter-structure)> | filters |

# (9) ActivateFilter

## Request

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |
| Uint32 | unkUint3 |

## Response

This method does not return anything.

# (10) DeactivateFilter

## Request

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |

## Response

This method does not return anything.

# (11) ReadScoreByIds

## Request

| Type | Name |
|------|------|
| Uint32 | unkUint |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[ScoreListOut](#scorelistout-structure)> | scoreLists |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[ScoreListOut](#scorelistout-structure)> | scoreLists |
| Uint32 | unkUint |

# (12) ReadScoreByRank

## Request

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |
| Uint32 | unkUint3 |

## Response

| Type | Name |
|------|------|
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[ScoreListOut](#scorelistout-structure)> | scoreLists |
| Uint32 | unkUint |

# Types

## PlayerStatContainer ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | playerName |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[PlayerStatisticExt](#playerstatisticext-structure)> | statsExt |

## PlayerStatistic ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[PlayerStatisticInfo](#playerstatisticinfo-structure)> | statInfos |


## PlayerStatisticExt ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | id |
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)<[PlayerStatisticInfoExt](#playerstatisticinfoext-structure)> | statInfosExt |
| [DateTime](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#datetime) | dateTime |

## PlayerStatisticInfo ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint8 | id |
| [PlayerStatisticValues](#playerstatisticvalues-structure) | statValues |
| Uint8 | unkByte |

## PlayerStatisticInfoExt ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint8 | id |
| [PlayerStatisticValues](#playerstatisticvalues-structure) | statValues1 |
| Uint8 | unkByte |
| [PlayerStatisticValues](#playerstatisticvalues-structure) | statValues2 |
| [PlayerStatisticValues](#playerstatisticvalues-structure) | statValues3 |

## PlayerStatisticValues ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint |
| Uint64 | unkUlong1 |
| Uint64 | unkUlong2 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkStr |
| Uint8 | unkByte |

## StatQuery ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | statID |
| [List](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#list)\<Uint32\> | infoIDs |

## PlayerQuery ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Uint32 | unkUint2 |

## Filter ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| Bool | unkBool |
| Uint32 | unkUint2 |
| Uint32 | unkUint3 |

## ScoreListOut ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| Uint32 | unkUint1 |
| [String](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#string) | unkStr |
| Uint32 | unkUint2 |
| Uint32 | unkUint3 |
