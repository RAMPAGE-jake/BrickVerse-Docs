---
description: >-
  This API Reference Manual documents all of classes, enumerations, data types,
  services, event, callbacks, and properties developers use while creating there
  game universes.
---

# BrickVerse Game API Reference Manual

## BrickVerse Globals

### Functions

| [function](brickverse-game-api-reference-manual.md) , [table](brickverse-game-api-reference-manual.md) **pairs** ( [table](brickverse-game-api-reference-manual.md) t )                                                                                                                                                                                                                                                      |
| ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Returns an iterator function, the passed table <em>t</em> and nil, so that the construction will iterate over all key/value pairs of that table when used in a generic for-loop:</p><p></p><pre class="language-lua"><code class="lang-lua">local scores = { ["John"] = 5, ["Sally"] = 10 }

for name, score in pairs(scores) do   
   print(name .. " has score: " .. score) -- "John has score: 5" etc
end</code></pre> |

| [bool](brickverse-game-api-reference-manual.md) , [Variant](brickverse-game-api-reference-manual.md) **pcall** ( [function](brickverse-game-api-reference-manual.md) func, [Tuple](brickverse-game-api-reference-manual.md) args )                                                                                                                                                                                                                      |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Calls the function _func_ with the given arguments in protected mode. This means that any error inside _func_ is not propagated; instead, pcall catches the error and returns a status code. Its first result is the status code (a boolean), which is true if the call succeeds without errors. In such case, pcall also returns all results from the call, after this first result. In case of any error, pcall returns false plus the error message. |

|                                                                                                                                                                                                                                                                                                                                             |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [void](brickverse-game-api-reference-manual.md) **print** ( [Tuple](brickverse-game-api-reference-manual.md) params )                                                                                                                                                                                                                       |
| Receives any number of arguments, and prints their values to the output. `print` is not intended for formatted output, but only as a quick way to show a value, typically for debugging. For a formatted output, use string.format. On BrickVerse, print does not call `tostring`, but will metatables for the the `__tostring` metamethod. |

| [Variant](brickverse-game-api-reference-manual.md) **loadstring** ( [string](brickverse-game-api-reference-manual.md) contents ) |
| -------------------------------------------------------------------------------------------------------------------------------- |
| Loads Lua code from a string, and returns it as a function. This cannot load the binary version of Lua using loadstring.         |

| [Variant](brickverse-game-api-reference-manual.md) **require** ( [ModuleScript](brickverse-game-api-reference-manual.md) module )                                                                                                                                                                                                                                                                                                                  |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Runs the supplied <a href="brickverse-game-api-reference-manual.md"><code>ModuleScript</code></a> if it has not been run already, and returns what the ModuleScript returned (in both cases).</p><p>If the ModuleScript the user wants to use has been uploaded to BrickVerse (with the instance’s name being ‘MainModule’), it can be loaded by using the require function on the asset ID of the ModuleScript, though only on the server.</p> |

| [string](brickverse-game-api-reference-manual.md) **typeof** ( [Variant](brickverse-game-api-reference-manual.md) object )                                                                                      |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Returns the type of the object specified, as a string.<br>This function is more accurate than Lua’s native <em>type</em> function, as it does not denote BrickVerse-specific types as <em>userdata</em>.</p> |

### Variables

| [string](brickverse-game-api-reference-manual.md) **\_VERSION**                                    |
| -------------------------------------------------------------------------------------------------- |
| A global variable (not a function) that holds a string containing the current interpreter version. |

| [DataModel](brickverse-game-api-reference-manual.md) **Universe**                                                                           |
| ------------------------------------------------------------------------------------------------------------------------------------------- |
| A reference to the [`DataModel`](brickverse-game-api-reference-manual.md), which is the root Instance of BrickVerse parent/child hierarchy. |

| [LuaSourceContainer](brickverse-game-api-reference-manual.md) **script**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>A reference to the script object that is executing the code you are writing.<br>It can be either a <a href="classes/programming/untitled.md"><code>ServerScript</code></a>, a <a href="classes/programming/localscript.md"><code>ClientScript</code></a>, or a <a href="https://developer.roblox.com/en-us/api-reference/class/ModuleScript"><code>ModuleScript</code></a> (and sometimes a <a href="https://developer.roblox.com/en-us/api-reference/class/CoreScript"><code>CoreScript</code></a>)<br>This variable is not available when executing code from BrickVerse Studio’s command bar.</p> |

|                                                                                                                                                                                                                             |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [array](brickverse-game-api-reference-manual.md) **shared**                                                                                                                                                                 |
|  table that is shared between all scripts of the same context level. Only shared across same authority level, for example it can't go across client -> server / server -> client. Only server -> server / client -> client. |

| [array](brickverse-game-api-reference-manual.md) **\_G**                                |
| --------------------------------------------------------------------------------------- |
| A table that is shared between all scripts of the same context level. Same as \_shared. |

## Lua Globals

* [corountine](globals/coroutine.md)
* [debug](globals/debug.md)
