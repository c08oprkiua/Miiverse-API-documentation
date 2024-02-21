# Query Table

|                    |              |                                                 |                                                                                                  |
| ------------------ | ------------ | ----------------------------------------------- | ------------------------------------------------------------------------------------------------ |
| type               | string       | text: Fetch post texts?<br/>memo: Post related? | Defines a filter of what kind of post will be returned. See the option descriptions for details. |
| by                 | string array | friends:<br/>following:                         |                                                                                                  |
| distinct_pid       | bool         | 1:true<br/>0:false                              | Returns one post per user, so that every PID is distinct.                                        |
| with_empathy_added | bool         | 1: true<br/>0:false                             |                                                                                                  |
| allow_spoiler      | bool         | 1: true<br/>0:false                             | If this is false, spoilers will not be shown.                                                    |
| with_mii           | bool         | 1:true<br/>0:false                              | Whether or not mii data will be returned in the response.                                        |

# v1/posts/

## GET

# v1/posts/`id`/empathies

## GET

# v1/communities/`id`/posts

## GET

Returns the posts from a given community, `id`. If `id` is 0, the API will infer the community being fetched based on the title ID in the param-pack header.
