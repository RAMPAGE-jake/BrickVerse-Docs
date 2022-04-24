---
description: >-
  This API Reference Manual documents all of classes, enumerations, data types,
  services, event, callbacks, and properties developers use while creating there
  game universes.
---

# BrickVerse Game API Reference Manual

## BrickVerse Globals

bool , Variant **pcall** ( function func, Tuple args )

Calls the function _func_ with the given arguments in protected mode. This means that any error inside _func_ is not propagated; instead, pcall catches the error and returns a status code. Its first result is the status code (a boolean), which is true if the call succeeds without errors. In such case, pcall also returns all results from the call, after this first result. In case of any error, pcall returns false plus the error message.

| [function](brickverse-game-api-reference-manual.md) , [table](brickverse-game-api-reference-manual.md) **pairs** ( [table](brickverse-game-api-reference-manual.md) t )                                                                                                                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Returns an iterator function, the passed table <em>t</em> and nil, so that the construction will iterate over all key/value pairs of that table when used in a generic for-loop:</p><p></p><pre class="language-lua"><code class="lang-lua">local scores = { ["John"] = 5, ["Sally"] = 10 }

for name, score in pairs(scores) do   
   print(name .. " has score: " .. score) -- "John has score: 5" etc
end</code></pre> |

| [Variant](brickverse-game-api-reference-manual.md) **loadstring** ( [string](brickverse-game-api-reference-manual.md) contents ) |
| -------------------------------------------------------------------------------------------------------------------------------- |
| Loads Lua code from a string, and returns it as a function. This cannot load the binary version of Lua using loadstring.         |

## Lua Globals

* [corountine](globals/coroutine.md)
* [debug](globals/debug.md)
