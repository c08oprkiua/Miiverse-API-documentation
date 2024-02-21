## query table

These are the queries usable in the community endpoints.

| Name         | Type       | Options             | Description                                                          |
| ------------ | ---------- | ------------------- | -------------------------------------------------------------------- |
| limit        | int        | Range: 1-100(?)     | Defines how many communities are returned in the API reponse.        |
| community_id | `id` array | Array size: 20      | Limit the response to the community ID or IDs put in.                |
| language_id  | int        | Range:1-254(?)      | The ID of the language the API will filter for to return values for. |
| search_key   | string     | (Any)               | Search keys are community dependent.                                 |
| with_icon    | bool       | 1: true<br/>0:false | Whether or not icon data will be returned in the response.           |

Example usage: `https://amiiverserevival.com/v1/communities?limit=50&with_icon=0&type=official` would return 50 communities, *without* icon data, and all the communities returned will be official ones.

# v1/communities

## Unique Queries

|      |        |                                                                                                                                               |                                                                                                               |
| ---- | ------ | --------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| type | string | favorite: get the user's favorite communities<br/>official: get official communities<br/>my:Retrieve the user's community, if applicable<br/> | Defines a filter of what kind of community or post will be returned. See the option descriptions for details. |

## GET

Used to fetch a community or communities.

# v1/communities/`id`

## GET

Returns a community, where `id` is the community ID of a community. If `id` is 0, the server will infer the community based on the titleid in the param-pack header.

# v1/communities/`id`/favorite

## GET

# v1/communities/`id`/settings

## GET
