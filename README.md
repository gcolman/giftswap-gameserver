# giftswap-gameserver
Gameserver for giftswap game.


This he gameserver holds all server state and manages the connections from clients. When clients connect via the webservice, the server sends config information. 
From thereon the server responds to client side events. 

The client reads the game config from config.json

TODO: Send full state back to clients on certain events. If a client disconnets for some reason (e.g. browser refresh) while in the middle of playing, then the 
client might lose the state of the game in play, e.g. if the ItsMyTurn flag has been set in the client and then refreshed during a turn, then the player can't play 
as some of the state is inconsistent. So, recreate all of the state and send back to the client.
