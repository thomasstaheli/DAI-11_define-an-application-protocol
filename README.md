# DAI-11_define-an-application-protocol

## Guess the number

### 1 - Overview

You are working for a game company that wants to create a new game called "Guess the number".

The game is simple: the server generates a random number between 1 and 100 (inclusive).

The client has to guess the number. The server will respond with with a message to indicate if the number is higher, lower or correct than the number guessed by the client.

Once the client has guessed the number, the client can ask the server to restart the game or to quit the game.

### 2 - Transport protocol

The "Guess the number" protocol is a text protocol (encoded in UTF-8). This protocol use TCP and use the port 8080.

At first, the client have to etablish the connection.

When the client connect him-self, the server generate a random number between 1 and 100 (include).

When the server has the random number, he will send a START request to the client.

When the client received the START message, he can send a number between 1 and 100.

After the client sended the number, the server has 3 differents answers : CORRECT, LOWER, UPPER. It will help the client to know which number he will send next.

Until the server send CORRECT, the client has the chance to say RESTART, if he want to play one more game or QUIT to quit the game.

If the client do not send a number between 1 and 100, the server will send an error message.

### 3 - Messages

#### Client message

GUESS "number"

QUIT

RESTART

#### Server message

START

CORRECT

LOWER

UPPER

### 4 - Examples

UML Diagram

## Temperature monitoring

### 1 - Overview

### 2 - Transport protocol

### 3 - Messages

### 4 - Examples
