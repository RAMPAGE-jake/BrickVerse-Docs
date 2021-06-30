---
description: This is useful for managing players in your universe
---

# Players

## Properties

| Name | Type | Description |
| :--- | :--- | :--- |
| LocalPlayer | Player | When called from a client script, returns the local player. Will not work for Server Scripts. |

Inherited from [Dynamic](https://docs.brickverse.co/bricklua-lua-references-manual/dymanic) Set

## Functions

| Name | Type | Description |
| :--- | :--- | :--- |
| GetPlayerByUsername | Player | Returns player with the username |
| GetPlayerByUserId | Player | Returns player with the userid |
| GetPlayers | Table | Returns all connected players in a table |
| Disconnect | Void | Disconnect a player from the universe |
| GetPlayerCharacterByUserId | Player | Returns character with the userid |
| RenderPlayer | String | Returns render of the player |

## Events

| Name | Description |
| :--- | :--- |
| PlayerConnected | Invoked when a player connected successfully to the universe |
| PlayerRemoved | Invoked when a player disconnected successfully to the universe |
| OnShutDown | Invoked when server is shutdown by BrickVerse staff or Universe creator. |



