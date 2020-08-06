# Tic-Tac-Toe
A Node.Js UI-less multiplayer Tic-Tac-Toe page

## URL

You can play the game here:

`https://pettas.herokuapp.com/`

## API

``` javascript
io.on ('connection', function (socket)
```

The central trigger that registers the player in a match or in the list of available, gives a symbol to each player and includes all other events.

`socket.on ('setName', function (msg)`
Announces the names of the players and the points each. If someone is playing for the first time he is registered in the database.

`socket.on ('move', function (msg)`
Transfers the player's movement to the opponent.

`socket.on ('victory', function (msg)`
The loser sends a message to the winner and updates the base with another victory.

`socket.on ('clean', function ())`
Restores the board in case a player abandons the game.

The database consists of the `scores` table that records the` playerName` of each player and his `score`.
