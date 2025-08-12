# MatchMakingProtocolExt

| Method ID | Method Name |
|-----------|-------------|
| 1 | [EndParticipation](#1-endparticipation) |
| 2 | [GetParticipants](#2-getparticipants) |
| 3 | [GetDetailedParticipants](#3-getdetailedparticipants) |
| 4 | [GetParticipantsURLs](#4-getparticipantsurls) |
| 5 | [GetGatheringRelations](#5-getgatheringrelations) |
| 6 | [DeleteFromDeletions](#6-deletefromdeletions) |

# (1) EndParticipation

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |
| string | strMessage |

## Response

| Type | Name |
|------|------|
| bool | %retval% |

# (2) GetParticipants

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |
| bool | bOnlyActive |

## Response

| Type | Name |
|------|------|
| std_list<uint32> | lstParticipants |

# (3) GetDetailedParticipants

## Request

| Type | Name |
|------|------|
| uint32 | idGathering |
| bool | bOnlyActive |

## Response

| Type | Name |
|------|------|
| std_list<ParticipantDetails> | lstParticipants |

# (4) GetParticipantsURLs

## Request

| Type | Name |
|------|------|
| std_list<uint32> | lstGatherings |

## Response

| Type | Name |
|------|------|
| std_list<GatheringURLs> | lstGatheringURLs |

# (5) GetGatheringRelations

## Request

| Type | Name |
|------|------|
| uint32 | id |
| string | descr |

## Response

| Type | Name |
|------|------|
| string | %retval% |

# (6) DeleteFromDeletions

## Request

| Type | Name |
|------|------|
| std_list<uint32> | lstDeletions |
| uint32 | pid |

## Response
This method does not return anything.

# Types

## ParticipantDetails ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_idParticipant |
| string | m_strName |
| string | m_strMessage |

## Gathering ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_idMyself |
| uint32 | m_pidOwner |
| uint32 | m_pidHost |
| uint16 | m_uiMinParticipants |
| uint16 | m_uiMaxParticipants |
| uint32 | m_uiParticipationPolicy |
| uint32 | m_uiPolicyArgument |
| uint32 | m_uiFlags |
| uint32 | m_uiState |
| string | m_strDescription |

## DynamicGathering ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends `Gathering`.

| Type | Name |
|------|------|
| buffertail | m_bufTail |

## Invitation ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_idGathering |
| uint32 | m_idGuest |
| string | m_strMessage |

## GatheringStats ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_pidParticipant |
| uint32 | m_uiFlags |
| std_list<float> | m_lstValues |

## DeletionEntry ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_idGathering |
| uint32 | m_pid |
| uint32 | m_uiReason |

## GatheringURLs ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_gid |
| std_list<stationurl> | m_lstStationURLs |
