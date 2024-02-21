# About People

 The people endpoints can be used to fetch data by and about a specific Miiverse user or users. This, for example, can be used to fetch a list of users that the client follows.

# Query Table

| Name         | Type      | Options                                                                     | Description                                                              |
| ------------ | --------- | --------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| language_id  | int       |                                                                             |                                                                          |
| limit        | int       |                                                                             |                                                                          |
| distinct_pid |           |                                                                             |                                                                          |
| with_mii     | bool      |                                                                             |                                                                          |
| relation     | string    | following: Users the user is following.<br>friend: The user's friends.<br/> | Sets a filter on which users are returned by their relation to the user. |
| pid          | int array | Range: 1-11                                                                 | One or more PIDs of users you would like data from.                      |

# v1/people/

## GET

Friends that appear on your Wii U Menu with orange pants.

## POST

Create a new user
