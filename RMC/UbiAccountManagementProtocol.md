# UbiAccountManagementProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [CreateAccount](#1-createaccount) |
| 2 | [UpdateAccount](#2-updateaccount) |
| 3 | [GetAccount](#3-getaccount) |
| 4 | [LinkAccount](#4-linkaccount) |
| 5 | [GetTOS](#5-gettos) |
| 6 | [ValidateUsername](#6-validateusername) |
| 7 | [ValidatePassword](#7-validatepassword) |
| 8 | [ValidateEmail](#8-validateemail) |
| 9 | [GetCountryList](#9-getcountrylist) |
| 10 | [ForgetPassword](#10-forgetpassword) |
| 11 | [LookupPrincipalIds](#11-lookupprincipalids) |
| 12 | [LookupUbiAccountIDsByPids](#12-lookupubiaccountidsbypids) |
| 13 | [LookupUbiAccountIDsByUsernames](#13-lookupubiaccountidsbyusernames) |
| 14 | [LookupUsernamesByUbiAccountIDs](#14-lookupusernamesbyubiaccountids) |

# (1) CreateAccount

## Request

| Type | Name |
|------|------|
| UbiAccount | ubiAccount |

## Response

| Type | Name |
|------|------|
| UbiAccount | ubiAccount |
| qvector<ValidationFailureReason> | failedReasons |

# (2) UpdateAccount

## Request

| Type | Name |
|------|------|
| UbiAccount | ubiAccount |

## Response

| Type | Name |
|------|------|
| UbiAccount | ubiAccount |
| qvector<ValidationFailureReason> | failedReasons |

# (3) GetAccount

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| UbiAccount | ubiAccount |
| bool | exists |

# (4) LinkAccount

## Request

| Type | Name |
|------|------|
| string | ubiAccountUsername |
| string | ubiAccountPassword |

## Response
This method does not return anything.

# (5) GetTOS

## Request

| Type | Name |
|------|------|
| string | countryCode |
| string | languageCode |
| bool | htmlVersion |

## Response

| Type | Name |
|------|------|
| TOS | tos |

# (6) ValidateUsername

## Request

| Type | Name |
|------|------|
| string | username |

## Response

| Type | Name |
|------|------|
| UsernameValidation | usernameValidation |

# (7) ValidatePassword

## Request

| Type | Name |
|------|------|
| string | password |
| string | username |

## Response

| Type | Name |
|------|------|
| qvector<ValidationFailureReason> | failedReasons |

# (8) ValidateEmail

## Request

| Type | Name |
|------|------|
| string | email |

## Response

| Type | Name |
|------|------|
| qvector<ValidationFailureReason> | failedReasons |

# (9) GetCountryList

## Request

| Type | Name |
|------|------|
| string | languageCode |

## Response

| Type | Name |
|------|------|
| qvector<Country> | countries |

# (10) ForgetPassword

## Request

| Type | Name |
|------|------|
| string | usernameOrEmail |

## Response
This method does not return anything.

# (11) LookupPrincipalIds

## Request

| Type | Name |
|------|------|
| std_list<string> | ubiAccountIds |

## Response

| Type | Name |
|------|------|
| std_map<string,uint32> | pids |

# (12) LookupUbiAccountIDsByPids

## Request

| Type | Name |
|------|------|
| std_list<uint32> | pids |

## Response

| Type | Name |
|------|------|
| std_map<uint32,string> | ubiaccountIDs |

# (13) LookupUbiAccountIDsByUsernames

## Request

| Type | Name |
|------|------|
| std_list<string> | Usernames |

## Response

| Type | Name |
|------|------|
| std_map<string,string> | UbiAccountIDs |

# (14) LookupUsernamesByUbiAccountIDs

## Request

| Type | Name |
|------|------|
| std_list<string> | UbiAccountIds |

## Response

| Type | Name |
|------|------|
| std_map<string,string> | Usernames |

# Types

## ExternalAccount ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_accountType |
| string | m_id |
| string | m_username |

## UbiAccountStatus ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_basicStatus |
| bool | m_missingRequiredInformations |
| bool | m_recoveringPassword |
| bool | m_pendingDeactivation |

## UbiAccount ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_ubiAccountId |
| string | m_username |
| string | m_password |
| UbiAccountStatus | m_status |
| string | m_email |
| datetime | m_dateOfBirth |
| uint32 | m_gender |
| string | m_countryCode |
| bool | m_optIn |
| bool | m_thirdPartyOptIn |
| string | m_firstName |
| string | m_lastName |
| string | m_preferredLanguage |
| qvector<ExternalAccount> | m_externalAccounts |

## TOS ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_localeCode |
| string | m_content |
| string | m_storingInfoQuestion |

## ValidationFailureReason ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | m_validationId |
| string | m_description |

## UsernameValidation ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| qvector<string> | m_suggestions |
| qvector<ValidationFailureReason> | m_reasons |

## Country ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_code |
| string | m_name |
