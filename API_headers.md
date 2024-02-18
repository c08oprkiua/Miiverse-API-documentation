# Headers

The Miiverse API uses HTTP GET and HTTP POST, and always sends two headers: a service token, and a param pack.

## `x-nintendo-parampack`

The param pack is a base64 encoded structure of data that is sent with every request, containing various bits of information that the server can use, such as the title id being requested from (ie. the currently running game), the language the user expects, etc.

The following table covers all the params of the parampack, in order:

| Name                | Type   | Options            | Description                             |
| ------------------- | ------ | ------------------ | --------------------------------------- |
| title_id            |        |                    |                                         |
| access_key          |        |                    |                                         |
| platform_id         | int    | 0: 3DS<br>1: Wii U | Tells Miiverse which platform you're on |
| region_id           |        |                    |                                         |
| language_id         |        |                    |                                         |
| country_id          |        |                    |                                         |
| area_id             |        |                    |                                         |
| network_restriction |        |                    |                                         |
| friend_restriction  |        |                    |                                         |
| rating_restriction  |        |                    |                                         |
| rating_organization |        |                    |                                         |
| transferable_id     |        |                    |                                         |
| tz_name             | string |                    |                                         |
| utc_offset          |        |                    |                                         |

Each entry is put into one long string, in a `\name\value\name_2\value_2\...` format, where `name` is the name in the above table (remember the order of the entries!), and `value` is what it is set to. This string then is base64 encoded, and set as the value of the header.

## `x-nintendo-servicetoken`

The service token is obtained through an endpoint in the account server.
