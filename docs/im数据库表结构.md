
# Database: openfire

## ofextcomponentconf
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | subdomain | varchar(255) | No |  |
|  | wildcard | tinyint(4) | No |  |
|  | secret | varchar(255) | Yes |  |
|  | permission | varchar(10) | No |  |


## ofgroup
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | groupName | varchar(50) | No |  |
|  | description | varchar(255) | Yes |  |


## ofgroupprop
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | groupName | varchar(50) | No |  |
| P | name | varchar(100) | No |  |
|  | propValue | text | No |  |


## ofgroupuser
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | groupName | varchar(50) | No |  |
| P | username | varchar(100) | No |  |
| P | administrator | tinyint(4) | No |  |


## ofid
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | idType | int(11) | No |  |
|  | id | bigint(20) | No |  |


## ofmucaffiliation
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | roomID | bigint(20) | No |  |
| P | jid | text | No |  |
|  | affiliation | tinyint(4) | No |  |


## ofmucconversationlog
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
|  | roomID | bigint(20) | No |  |
|  | messageID | bigint(20) | No |  |
|  | sender | text | No |  |
|  | nickname | varchar(255) | Yes |  |
|  | logTime | char(15) | No |  |
|  | subject | varchar(255) | Yes |  |
|  | body | text | Yes |  |
|  | stanza | text | Yes |  |


## ofmucmember
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | roomID | bigint(20) | No |  |
| P | jid | text | No |  |
|  | nickname | varchar(255) | Yes |  |
|  | firstName | varchar(100) | Yes |  |
|  | lastName | varchar(100) | Yes |  |
|  | url | varchar(100) | Yes |  |
|  | email | varchar(100) | Yes |  |
|  | faqentry | varchar(100) | Yes |  |


## ofmucroom
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | serviceID | bigint(20) | No |  |
|  | roomID | bigint(20) | No |  |
|  | creationDate | char(15) | No |  |
|  | modificationDate | char(15) | No |  |
| P | name | varchar(50) | No |  |
|  | naturalName | varchar(255) | No |  |
|  | description | varchar(255) | Yes |  |
|  | lockedDate | char(15) | No |  |
|  | emptyDate | char(15) | Yes |  |
|  | canChangeSubject | tinyint(4) | No |  |
|  | maxUsers | int(11) | No |  |
|  | publicRoom | tinyint(4) | No |  |
|  | moderated | tinyint(4) | No |  |
|  | membersOnly | tinyint(4) | No |  |
|  | canInvite | tinyint(4) | No |  |
|  | roomPassword | varchar(50) | Yes |  |
|  | canDiscoverJID | tinyint(4) | No |  |
|  | logEnabled | tinyint(4) | No |  |
|  | subject | varchar(100) | Yes |  |
|  | rolesToBroadcast | tinyint(4) | No |  |
|  | useReservedNick | tinyint(4) | No |  |
|  | canChangeNick | tinyint(4) | No |  |
|  | canRegister | tinyint(4) | No |  |
|  | allowpm | tinyint(4) | Yes |  |


## ofmucroomprop
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | roomID | bigint(20) | No |  |
| P | name | varchar(100) | No |  |
|  | propValue | text | No |  |


## ofmucservice
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
|  | serviceID | bigint(20) | No |  |
| P | subdomain | varchar(255) | No |  |
|  | description | varchar(255) | Yes |  |
|  | isHidden | tinyint(4) | No |  |


## ofmucserviceprop
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | serviceID | bigint(20) | No |  |
| P | name | varchar(100) | No |  |
|  | propValue | text | No |  |


## ofoffline
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | username | varchar(64) | No |  |
| P | messageID | bigint(20) | No |  |
|  | creationDate | char(15) | No |  |
|  | messageSize | int(11) | No |  |
|  | stanza | text | No |  |


## ofpresence
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | username | varchar(64) | No |  |
|  | offlinePresence | text | Yes |  |
|  | offlineDate | char(15) | No |  |


## ofprivacylist
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | username | varchar(64) | No |  |
| P | name | varchar(100) | No |  |
|  | isDefault | tinyint(4) | No |  |
|  | list | text | No |  |


## ofprivate
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | username | varchar(64) | No |  |
| P | name | varchar(100) | No |  |
| P | namespace | varchar(200) | No |  |
|  | privateData | text | No |  |


## ofproperty
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | name | varchar(100) | No |  |
|  | propValue | text | No |  |


## ofpubsubaffiliation
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | serviceID | varchar(100) | No |  |
| P | nodeID | varchar(100) | No |  |
| P | jid | varchar(255) | No |  |
|  | affiliation | varchar(10) | No |  |


## ofpubsubdefaultconf
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | serviceID | varchar(100) | No |  |
| P | leaf | tinyint(4) | No |  |
|  | deliverPayloads | tinyint(4) | No |  |
|  | maxPayloadSize | int(11) | No |  |
|  | persistItems | tinyint(4) | No |  |
|  | maxItems | int(11) | No |  |
|  | notifyConfigChanges | tinyint(4) | No |  |
|  | notifyDelete | tinyint(4) | No |  |
|  | notifyRetract | tinyint(4) | No |  |
|  | presenceBased | tinyint(4) | No |  |
|  | sendItemSubscribe | tinyint(4) | No |  |
|  | publisherModel | varchar(15) | No |  |
|  | subscriptionEnabled | tinyint(4) | No |  |
|  | accessModel | varchar(10) | No |  |
|  | language | varchar(255) | Yes |  |
|  | replyPolicy | varchar(15) | Yes |  |
|  | associationPolicy | varchar(15) | No |  |
|  | maxLeafNodes | int(11) | No |  |


## ofpubsubitem
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | serviceID | varchar(100) | No |  |
| P | nodeID | varchar(100) | No |  |
| P | id | varchar(100) | No |  |
|  | jid | varchar(255) | No |  |
|  | creationDate | char(15) | No |  |
|  | payload | mediumtext | Yes |  |


## ofpubsubnode
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | serviceID | varchar(100) | No |  |
| P | nodeID | varchar(100) | No |  |
|  | leaf | tinyint(4) | No |  |
|  | creationDate | char(15) | No |  |
|  | modificationDate | char(15) | No |  |
|  | parent | varchar(100) | Yes |  |
|  | deliverPayloads | tinyint(4) | No |  |
|  | maxPayloadSize | int(11) | Yes |  |
|  | persistItems | tinyint(4) | Yes |  |
|  | maxItems | int(11) | Yes |  |
|  | notifyConfigChanges | tinyint(4) | No |  |
|  | notifyDelete | tinyint(4) | No |  |
|  | notifyRetract | tinyint(4) | No |  |
|  | presenceBased | tinyint(4) | No |  |
|  | sendItemSubscribe | tinyint(4) | No |  |
|  | publisherModel | varchar(15) | No |  |
|  | subscriptionEnabled | tinyint(4) | No |  |
|  | configSubscription | tinyint(4) | No |  |
|  | accessModel | varchar(10) | No |  |
|  | payloadType | varchar(100) | Yes |  |
|  | bodyXSLT | varchar(100) | Yes |  |
|  | dataformXSLT | varchar(100) | Yes |  |
|  | creator | varchar(255) | No |  |
|  | description | varchar(255) | Yes |  |
|  | language | varchar(255) | Yes |  |
|  | name | varchar(50) | Yes |  |
|  | replyPolicy | varchar(15) | Yes |  |
|  | associationPolicy | varchar(15) | Yes |  |
|  | maxLeafNodes | int(11) | Yes |  |


## ofpubsubnodegroups
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
|  | serviceID | varchar(100) | No |  |
|  | nodeID | varchar(100) | No |  |
|  | rosterGroup | varchar(100) | No |  |


## ofpubsubnodejids
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | serviceID | varchar(100) | No |  |
| P | nodeID | varchar(100) | No |  |
| P | jid | varchar(255) | No |  |
|  | associationType | varchar(20) | No |  |


## ofpubsubsubscription
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | serviceID | varchar(100) | No |  |
| P | nodeID | varchar(100) | No |  |
| P | id | varchar(100) | No |  |
|  | jid | varchar(255) | No |  |
|  | owner | varchar(255) | No |  |
|  | state | varchar(15) | No |  |
|  | deliver | tinyint(4) | No |  |
|  | digest | tinyint(4) | No |  |
|  | digest_frequency | int(11) | No |  |
|  | expire | char(15) | Yes |  |
|  | includeBody | tinyint(4) | No |  |
|  | showValues | varchar(30) | Yes |  |
|  | subscriptionType | varchar(10) | No |  |
|  | subscriptionDepth | tinyint(4) | No |  |
|  | keyword | varchar(200) | Yes |  |


## ofremoteserverconf
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | xmppDomain | varchar(255) | No |  |
|  | remotePort | int(11) | Yes |  |
|  | permission | varchar(10) | No |  |


## ofroster
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | rosterID | bigint(20) | No |  |
|  | username | varchar(64) | No |  |
|  | jid | varchar(1024) | No |  |
|  | sub | tinyint(4) | No |  |
|  | ask | tinyint(4) | No |  |
|  | recv | tinyint(4) | No |  |
|  | nick | varchar(255) | Yes |  |


## ofrostergroups
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | rosterID | bigint(20) | No |  |
| P | rank | tinyint(4) | No |  |
|  | groupName | varchar(255) | No |  |


## ofsaslauthorized
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | username | varchar(64) | No |  |
| P | principal | text | No |  |


## ofsecurityauditlog
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | msgID | bigint(20) | No |  |
|  | username | varchar(64) | No |  |
|  | entryStamp | bigint(20) | No |  |
|  | summary | varchar(255) | No |  |
|  | node | varchar(255) | No |  |
|  | details | text | Yes |  |


## ofuser
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | username | varchar(64) | No |  |
|  | storedKey | varchar(32) | Yes |  |
|  | serverKey | varchar(32) | Yes |  |
|  | salt | varchar(32) | Yes |  |
|  | iterations | int(11) | Yes |  |
|  | plainPassword | varchar(32) | Yes |  |
|  | encryptedPassword | varchar(255) | Yes |  |
|  | name | varchar(100) | Yes |  |
|  | email | varchar(100) | Yes |  |
|  | creationDate | char(15) | No |  |
|  | modificationDate | char(15) | No |  |


## ofuserflag
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | username | varchar(64) | No |  |
| P | name | varchar(100) | No |  |
|  | startTime | char(15) | Yes |  |
|  | endTime | char(15) | Yes |  |


## ofuserprop
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | username | varchar(64) | No |  |
| P | name | varchar(100) | No |  |
|  | propValue | text | No |  |


## ofvcard
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | username | varchar(64) | No |  |
|  | vcard | mediumtext | No |  |


## ofversion
|  | Field | Type | Allow Null | Default Value |
|--|-------|------|------------|---------------|
| P | name | varchar(50) | No |  |
|  | version | int(11) | No |  |
</div>
</div>