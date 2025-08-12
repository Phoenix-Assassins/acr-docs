# NewsProtocolAdmin

| Method ID | Method Name |
|-----------|-------------|
| 1 | [CreateChannel](#1-createchannel) |
| 2 | [DeleteChannel](#2-deletechannel) |
| 3 | [DeleteChannels](#3-deletechannels) |
| 4 | [GetChannels](#4-getchannels) |
| 5 | [GetChannelsByTypes](#5-getchannelsbytypes) |
| 6 | [GetChannelsByIDs](#6-getchannelsbyids) |
| 7 | [UpdateChannel](#7-updatechannel) |
| 8 | [GetNewsFeedLinks](#8-getnewsfeedlinks) |
| 9 | [GetNumberOfNewsFeedLinks](#9-getnumberofnewsfeedlinks) |
| 10 | [LinkNewsFeed](#10-linknewsfeed) |
| 11 | [UnlinkNewsFeeds](#11-unlinknewsfeeds) |
| 12 | [DeleteNewsMessages](#12-deletenewsmessages) |
| 13 | [DeleteNewsMessagesByRecipient](#13-deletenewsmessagesbyrecipient) |
| 14 | [GetNewsHeaders](#14-getnewsheaders) |
| 15 | [GetNewsMessages](#15-getnewsmessages) |
| 16 | [GetNumberOfNews](#16-getnumberofnews) |
| 17 | [PublishNews](#17-publishnews) |
| 18 | [UpdateNewsFeedLink](#18-updatenewsfeedlink) |
| 19 | [SingleNewsFeedParsingJob](#19-singlenewsfeedparsingjob) |
| 20 | [MultipleNewsFeedParsingJob](#20-multiplenewsfeedparsingjob) |
| 21 | [NewsMessageCleaningJob](#21-newsmessagecleaningjob) |
| 22 | [NewsChannelCleaningJob](#22-newschannelcleaningjob) |
| 23 | [CreateRSSFeed](#23-createrssfeed) |
| 24 | [GetDateTimeDelta](#24-getdatetimedelta) |
| 25 | [AddDateTime](#25-adddatetime) |
| 26 | [GetLocalDateTime](#26-getlocaldatetime) |
| 27 | [GetSystemDateTime](#27-getsystemdatetime) |

# (1) CreateChannel

## Request

| Type | Name |
|------|------|
| NewsChannel | channel |

## Response

| Type | Name |
|------|------|
| uint32 | newsChannelID |

# (2) DeleteChannel

## Request

| Type | Name |
|------|------|
| uint32 | newsChannelID |

## Response
This method does not return anything.

# (3) DeleteChannels

## Request

| Type | Name |
|------|------|
| qlist<uint32> | newsChannelIDs |

## Response
This method does not return anything.

# (4) GetChannels

## Request

| Type | Name |
|------|------|
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| qlist<NewsChannel> | channels |

# (5) GetChannelsByTypes

## Request

| Type | Name |
|------|------|
| qlist<string> | newsChannelTypes |
| ResultRange | resultRange |

## Response

| Type | Name |
|------|------|
| qlist<NewsChannel> | channels |

# (6) GetChannelsByIDs

## Request

| Type | Name |
|------|------|
| qlist<uint32> | newsChannelIDs |

## Response

| Type | Name |
|------|------|
| qlist<NewsChannel> | channels |

# (7) UpdateChannel

## Request

| Type | Name |
|------|------|
| NewsChannel | channel |

## Response
This method does not return anything.

# (8) GetNewsFeedLinks

## Request

| Type | Name |
|------|------|
| qlist<uint32> | newsChannelIDs |

## Response

| Type | Name |
|------|------|
| qlist<NewsFeedLink> | newsFeedLinks |

# (9) GetNumberOfNewsFeedLinks

## Request

| Type | Name |
|------|------|
| qlist<uint32> | newsChannelIDs |

## Response

| Type | Name |
|------|------|
| uint32 | numberOfNewsFeedLinks |

# (10) LinkNewsFeed

## Request

| Type | Name |
|------|------|
| NewsFeedLink | newsFeedLink |

## Response

| Type | Name |
|------|------|
| uint32 | newsFeedLinkID |

# (11) UnlinkNewsFeeds

## Request

| Type | Name |
|------|------|
| qlist<uint32> | newsFeedLinkIDs |

## Response
This method does not return anything.

# (12) DeleteNewsMessages

## Request

| Type | Name |
|------|------|
| qlist<uint32> | newsMessageIDs |

## Response
This method does not return anything.

# (13) DeleteNewsMessagesByRecipient

## Request

| Type | Name |
|------|------|
| NewsRecipient | recipient |

## Response
This method does not return anything.

# (14) GetNewsHeaders

## Request

| Type | Name |
|------|------|
| NewsRecipient | recipient |
| ResultRange | range |

## Response

| Type | Name |
|------|------|
| qlist<NewsHeader> | newsHeaders |

# (15) GetNewsMessages

## Request

| Type | Name |
|------|------|
| qlist<uint32> | newsMessageIDs |

## Response

| Type | Name |
|------|------|
| qlist<NewsMessage> | newsMessages |

# (16) GetNumberOfNews

## Request

| Type | Name |
|------|------|
| NewsRecipient | recipient |

## Response

| Type | Name |
|------|------|
| uint32 | numberOfNews |

# (17) PublishNews

## Request

| Type | Name |
|------|------|
| NewsMessage | newsMessage |

## Response

| Type | Name |
|------|------|
| NewsMessage | modifiedNewsMessage |

# (18) UpdateNewsFeedLink

## Request

| Type | Name |
|------|------|
| NewsFeedLink | newsFeedLink |

## Response
This method does not return anything.

# (19) SingleNewsFeedParsingJob

## Request
This method does not take any parameters.

## Response
This method does not return anything.

# (20) MultipleNewsFeedParsingJob

## Request
This method does not take any parameters.

## Response
This method does not return anything.

# (21) NewsMessageCleaningJob

## Request
This method does not take any parameters.

## Response
This method does not return anything.

# (22) NewsChannelCleaningJob

## Request
This method does not take any parameters.

## Response
This method does not return anything.

# (23) CreateRSSFeed

## Request

| Type | Name |
|------|------|
| string | name |
| uint32 | feedTemplateID |

## Response
This method does not return anything.

# (24) GetDateTimeDelta

## Request

| Type | Name |
|------|------|
| datetime | dt1 |
| datetime | dt2 |

## Response

| Type | Name |
|------|------|
| int64 | delta |

# (25) AddDateTime

## Request

| Type | Name |
|------|------|
| datetime | dt1 |
| int32 | years |
| int32 | months |
| int32 | days |
| int32 | hours |
| int32 | minutes |
| int32 | seconds |

## Response

| Type | Name |
|------|------|
| datetime | dt2 |

# (26) GetLocalDateTime

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| datetime | dt |

# (27) GetSystemDateTime

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| datetime | dt |

# Types

## NewsChannel ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_ID |
| uint32 | m_ownerPID |
| string | m_name |
| string | m_description |
| datetime | m_creationTime |
| datetime | m_expirationTime |
| string | m_type |
| string | m_locale |
| bool | m_subscribable |

## NewsHeader ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_ID |
| uint32 | m_recipientID |
| uint32 | m_recipientType |
| uint32 | m_publisherPID |
| string | m_publisherName |
| datetime | m_publicationTime |
| datetime | m_displayTime |
| datetime | m_expirationTime |
| string | m_title |
| string | m_link |

## NewsMessage ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))
Extends `NewsHeader`.

| Type | Name |
|------|------|
| string | m_body |

## NewsRecipient ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_recipientID |
| uint32 | m_recipientType |

## NewsFeedLink ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_ID |
| uint32 | m_newsChannelID |
| string | m_URL |
| string | m_description |
| datetime | m_feedUpdatedParseTime |
| datetime | m_lastUpdatedTime |
| datetime | m_nextRefreshTime |
| uint32 | m_refreshElapsedTimeMilliseconds |
| uint32 | m_refreshPeriodSeconds |
| bool | m_refreshEnabled |
| uint32 | m_refreshMethod |
| datetime | m_newestMessageTime |
| uint32 | m_messageAdded |
