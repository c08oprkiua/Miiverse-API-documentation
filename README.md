# The Miiverse API

**Disclaimer: I am not responsible for possible abuses of the API caused by this information being readily available. It is the responsiblity of API users to responsibly implement their use of the API in their app or game, and it is on API developers to implement proper checks and balances to prevent API misuse/abuse.**

I guess I am the only person out there who is gonna actually go through and document these, so hi there! The Miiverse API was Nintendo's HTTP based solution for developers to be able to talk to Miiverse within their games. On Wii U, it is mainly interacted with using the system library `nn_olv`, which does most of the background logistical work so that devs don't have to. `gd_olv` aims to do the same but in Godot 4, though neither will help someone trying to use it anywhere else, so I wrote this for anyone looking to use the Miiverse API anywhere else. Nowadays, various Miiverse revivals have recreated it, such as Pretendo Network's Juxtaposition.

# About the docs

All revivals will have to implement the same general endpoint structure, because they need to be implemented faithful to the original for full compatibility with existing Miiverse enabled games and infrastucture. To that extent, this documentation will only cover those mutual endpoints; revival specific endpoints will not be covered. 

When referring to endpoints, this documentation will not include the host name. In practice, for example, you would go to `https://your.api.site.com/v1/communities`, or connect to the domain `https://your.api.site.com`, and then request `v1/communities`, but the documentation will simply refer to the endpoint as `v1/communities`.

# Credits and Thank Yous

* NoNameGiven, for providing me useful API request logs from Aquamarine, allowing me to derive endpoints and query information. (No user information was shared in said logs.)

* Trace (TraceEntertains), for providing me with information derived from his work with decompiling `nn_olv`
