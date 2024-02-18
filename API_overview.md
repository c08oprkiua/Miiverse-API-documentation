# API endpoints

I guess I am the only person out there who is gonna actually go through and document these, so hi there! The Miiverse API is Nintendo's HTTP based solution for developers to be able to talk to Miiverse within their games. On Wii U, it is mainly interacted with using the system library `nn_olv`, which does most of the background logistical work so that devs don't have to. `gd_olv` aims to do the same but in Godot 4, though neither will help someone trying to use it anywhere else, so I wrote this for anyone looking to use the Miiverse API anywhere else.



Since there is no garuntee that you are trying to access a specific revival, this document will cover endpoints that are shared by all revivals, because they need to be implemented for full compatibility with existing Miiverse infrastructure. In practice, for example, you would go to `https://your.api.site.com/v1/communities`, or connect to the domain `https://your.api.site.com`, and then request `v1/communities`.



**Disclaimer: I am not responsible for possible abuses of the API caused by this information being readily available. It is the responsiblity of API users to responsibly implement their use of the API in their app or game, and it is on API developers to implement proper checks and balances to prevent API misuse/abuse.**


