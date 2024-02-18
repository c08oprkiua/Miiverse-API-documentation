## query table

These are the queries usable in the community endpoints.

| Name               | Type      | Options                                                                                                                                  | Description                                                                                           |
| ------------------ | --------- | ---------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| limit              | int       | Range: 1-100(?)                                                                                                                          | Defines how many communities are returned in the API reponse.                                         |
| community_id       | int array | Array size: 20                                                                                                                           | Limit the response to the community ID or IDs put in                                                  |
| language_id        | int       |                                                                                                                                          | The ID of the language the API will filter for to return values for.                                  |
| search_key         | string    | step: <br/>                                                                                                                              |                                                                                                       |
| distinct_pid       | bool      |                                                                                                                                          |                                                                                                       |
| with_mii           | bool      | 1:true<br/>0:false                                                                                                                       | Whether or not mii data will be returned in the response.                                             |
| with_icon          | bool      | 1: true<br/>0:false                                                                                                                      | Whether or not icon data will be returned in the response                                             |
| with_empathy_added | bool      |                                                                                                                                          |                                                                                                       |
| allow_spoiler      | bool      |                                                                                                                                          |                                                                                                       |
| by                 | string    | friends:<br/>                                                                                                                            |                                                                                                       |
| type               | string    | favorite: get the user's favorite communities<br/>official: get official communities<br/>my:Retrieve the user's community, if applicable | Defines a filter of what kind of community will be returned. See the option descriptions for details. |

Example usage: `https://amiiverserevival.com/v1/communities?limit=50&with_icon=0&type=official` would return 50 communities, *without* icon data, and all the communities returned will be official ones.

# v1/communities

## GET

Used to fetch a community or communities.

# v1/communities/`id`

## GET

Returns a community, where `id` is the community ID of a community

- If `id` is 0, the server will infer the community based on the titleid in the param-pack

# v1/communities/`id`/posts

## GET

Returns the posts in a community, where `id` is the community ID of a community.

# v1/communities/favorite

## GET
