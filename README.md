# Tic-Tac-Toe
A Node.Js UI-less multiplayer Tic-Tac-Toe game

## URL

You can play the game here:

`https://pettas.herokuapp.com/`

## API

The central trigger that registers the player in a match or in the list of available, gives a symbol to each player and includes all other events.
``` javascript
io.on ('connection', function (socket)
```

Announces the names of the players and the points each. If someone is playing for the first time he is registered in the database.
``` javascript
socket.on ('setName', function (msg)
```

Transfers the player's movement to the opponent.
``` javascript 
socket.on ('move', function (msg)
```

The loser sends a message to the winner and updates the base with another victory.
``` javascript 
socket.on ('victory', function (msg)
```

Restores the board in case a player abandons the game.
``` javascript
socket.on ('clean', function ())
```

The database consists of the `scores` table that records the` playerName` of each player and his `score`.
