# Hydna URI

## Syntax

<host> [ : <port> ] [ / <addr> ] [ ? <token> ]

## Host

Fully qualified domain name of remote entity serving intended zone.

## Port

Port on which remote server is accepting connections.

Default: 80

## Address

Address of stream specified in base-10 (must be < 4294967295). If the address
is prefixed with an `x`, the address should be interpreted as base-16 (must be
< FFFFFFFF).

Default: 1

## Token

Token that should be sent to the server along with an open-request.

Default: ''

## Examples

livetorget.hydna.net/13145
\__________________/ \___/
       |               |
      host            addr

sweet.hydna.net/13145?password
\_____________/ \___/ \______/
       |          |      |
      host       addr  token

beans.hydna.net:8080/13145?password
\_____________/ \__/ \___/ \_____/
       |         |     |      |
      host      port  addr  token
