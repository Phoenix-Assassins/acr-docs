# ClientLoginProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [Authenticate](#1-authenticate) |
| 2 | [GetServerTime](#2-getservertime) |
| 3 | [GetCXBVersion](#3-getcxbversion) |
| 4 | [OnCXBChanged](#4-oncxbchanged) |

# (1) Authenticate
## Request
| Type | Name |
|------|------|
| string | unkString1 |
| string | unkString2 |

## Response
| Type | Name |
|------|------|
| bool | unkBool |
| uint32 | unkUint1 |
| uint32 | unkUint2 |
| uint32 | unkUint3 |
| string | unkString1 |
| string | unkString2 |

# (2) GetServerTime
## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| datetime | serverTime |

# (3) GetCXBVersion
## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| uint32 | cxbVersion |

# (4) OnCXBChanged
## Request
This method does not take any parameters.

## Response
This method does not return anything.
