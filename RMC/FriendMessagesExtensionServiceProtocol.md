# FriendMessagesExtensionServiceProtocol

| Method ID | Method Name |
|-----------|-------------|
| 1 | [SendFriendInvitationMessage](#1-sendfriendinvitationmessage) |
| 2 | [ReceiveFriendInvitationMessages](#2-receivefriendinvitationmessages) |
| 3 | [RemoveFriendInvitationMessage](#3-removefriendinvitationmessage) |

# (1) SendFriendInvitationMessage
## Request
| Type | Name |
|------|------|
| [FriendInvitationMessage](#friendinvitationmessage-structure) | invite |

## Response
This method does not return anything.

# (2) ReceiveFriendInvitationMessages
## Request
This method does not take any parameters.

## Response
| Type | Name |
|------|------|
| List<[FriendInvitationMessage](#friendinvitationmessage-structure)> | invites |

# (3) RemoveFriendInvitationMessage
## Request
| Type | Name |
|------|------|
| uint32 | unkUint |

## Response
This method does not return anything.

# Types

## FriendInvitationMessage ([Structure](https://github.com/kinnay/NintendoClients/wiki/NEX-Common-Types#structure))

| Type | Name |
|------|------|
| uint32 | unkUint |
| string | unkString |
