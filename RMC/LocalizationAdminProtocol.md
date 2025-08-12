# LocalizationAdminProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [CreateLocalization](#1-createlocalization) |
| 2 | [UpdateLocalization](#2-updatelocalization) |
| 3 | [DeleteLocalization](#3-deletelocalization) |
| 4 | [GetNumberOfLocalizationContext](#4-getnumberoflocalizationcontext) |
| 5 | [GetLocalizationContexts](#5-getlocalizationcontexts) |
| 6 | [GetTranslatedStrings](#6-gettranslatedstrings) |
| 7 | [GetTranslatedString](#7-gettranslatedstring) |
| 8 | [LoadLocalizationFile](#8-loadlocalizationfile) |
| 9 | [GetLocalizationFileContent](#9-getlocalizationfilecontent) |
| 10 | [DeleteAllLocalizationsInContext](#10-deletealllocalizationsincontext) |
| 11 | [DeleteLocaleCodeForPID](#11-deletelocalecodeforpid) |

# (1) CreateLocalization

## Request

| Type | Name |
|------|------|
| string | localizationContext |
| string | localizationName |
| qlist<TranslatedString> | translatedStrings |

## Response

| Type | Name |
|------|------|
| uint32 | localizedStringID |

# (2) UpdateLocalization

## Request

| Type | Name |
|------|------|
| uint32 | localizedStringID |
| qlist<TranslatedString> | translatedStrings |

## Response
This method does not return anything.

# (3) DeleteLocalization

## Request

| Type | Name |
|------|------|
| uint32 | localizedStringID |

## Response
This method does not return anything.

# (4) GetNumberOfLocalizationContext

## Request
This method does not take any parameters.

## Response

| Type | Name |
|------|------|
| uint32 | numberOfLocalizationContext |

# (5) GetLocalizationContexts

## Request

| Type | Name |
|------|------|
| ResultRange | range |

## Response

| Type | Name |
|------|------|
| qlist<string> | localizationContexts |

# (6) GetTranslatedStrings

## Request

| Type | Name |
|------|------|
| uint32 | localizedStringID |

## Response

| Type | Name |
|------|------|
| qlist<TranslatedString> | translatedStrings |

# (7) GetTranslatedString

## Request

| Type | Name |
|------|------|
| LocalizationArgList | localizationArgList |
| string | localeCode |

## Response

| Type | Name |
|------|------|
| TranslatedString | translatedString |

# (8) LoadLocalizationFile

## Request

| Type | Name |
|------|------|
| string | localizationFileContent |
| bool | onDuplicateKeyUpdate |

## Response
This method does not return anything.

# (9) GetLocalizationFileContent

## Request

| Type | Name |
|------|------|
| qlist<string> | localizationContexts |
| char | delimiter |

## Response

| Type | Name |
|------|------|
| string | localizationFileContent |

# (10) DeleteAllLocalizationsInContext

## Request

| Type | Name |
|------|------|
| string | localizationContext |

## Response
This method does not return anything.

# (11) DeleteLocaleCodeForPID

## Request

| Type | Name |
|------|------|
| uint32 | pid |

## Response
This method does not return anything.

# Types

## TranslatedString ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_localeCode |
| string | m_translation |

## LocalizedString ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_localizationContext |
| string | m_localizedStringName |
| qlist<TranslatedString> | m_translatedStrings |

## LocalizationArg ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_key |
| string | m_value |

## LocalizationArgList ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| string | m_localizationContext |
| string | m_localizedStringName |
| qlist<LocalizationArg> | m_arguments |
