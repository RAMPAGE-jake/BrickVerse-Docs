---
description: Creates a new color, used for UI & Bricks. This is a function.
---

# Color

## Example

```
local MyPart = World.Brick
MyPart.Color = Color.fromRGB(255, 255, 255)
```

Inherited from [Dynamic](https://docs.brickverse.co/bricklua-lua-references-manual/dymanic) Set

### Constructors <a href="#constructors" id="constructors"></a>

| **Color3.new** ( number red = 0, number green = 0, number blue = 0 )                                        |
| ----------------------------------------------------------------------------------------------------------- |
| Returns a Color3 with the given red, green, and blue values. The parameters should be on the range \[0, 1]. |

| **Color3.fromRGB** ( number red = 0, number green = 0, number blue = 0 )                                                                                                |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Creates a Color3 with the given red, green, and blue components. Unlike most other Color3 functions, the parameters for this function should be on the range \[0, 255]. |

| **Color3.fromHSV** ( number hue, number saturation, number value )                                                                                                                                                                                  |
| --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Creates a Color3 with the given [hue](https://en.wikipedia.org/wiki/Hue), [saturation](https://en.wikipedia.org/wiki/Colorfulness#Saturation), and [value](https://en.wikipedia.org/wiki/Lightness). The parameters should be on the range \[0, 1]. |

| **Color3.fromHex** ( string hex )                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Returns a new Color3 from a six- or three-character <a href="https://en.wikipedia.org/wiki/Hexadecimal">hexadecimal</a> format. A preceding octothorpe (#) is ignored, if present. This function interprets the given string as a typical web hex color in the format RRGGBB or RGB (shorthand for RRGGBB). For example, #FFAA00 produces an orange color, and is the same as #FA0.</p><p>The color returned can be converted back into hex using <code>Color3:toHex</code>, although it is not guaranteed to return the exact same string as passed to this function.</p><p></p><pre><code>print(Color3.fromHex("#FF0000")) --> 1, 0, 0</code></pre> |

### Functions <a href="#functions" id="functions"></a>

| number , number , number **Color3.toHSV** ( Color3 color ) \[static]                                                                                                           |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Returns the [hue, saturation, and value](https://en.wikipedia.org/wiki/HSL\_and\_HSV) of a Color3. This function is the inverse operation of the `Color3.fromHSV` constructor. |

| Color3 **Color3:lerp** ( Color3 color, number alpha )                                    |
| ---------------------------------------------------------------------------------------- |
| Returns a Color3 interpolated between two Color3 objects. Alpha is a number from 0 to 1. |

| number , number , number **Color3:ToHSV** ( )                                                                                                                                  |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Returns the [hue, saturation, and value](https://en.wikipedia.org/wiki/HSL\_and\_HSV) of a Color3. This function is the inverse operation of the `Color3.fromHSV` constructor. |

| string **Color3:ToHex** ( )                                                                                                                                                                                                                                                                                                                                                                                                                           |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| <p>Converts the color to a six-character hexadecimal string representing the color in the format RRGGBB. It is not prefixed with an octothorpe (#), although this can be concatenated easily.</p><p>The returned string can be provided to <code>Color3.fromHex</code> to produce the original color.</p><p></p><pre><code>print(Color3.new(0, 1, 0):ToHex()) --> "00FF00"print(BrickColor.new("Really red").Color:ToHex()) --> "FF0000"</code></pre> |

### Properties <a href="#properties" id="properties"></a>

| number **Color3.R**         |
| --------------------------- |
| The red value of the color. |

| number **Color3.G**           |
| ----------------------------- |
| The green value of the color. |

| number **Color3.B**          |
| ---------------------------- |
| The blue value of the color. |
