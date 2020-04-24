> This article is converted from Wikipedia: [모듈:HSV](https://ko.wikipedia.org/wiki/모듈:HSV).


local p = {}

function rgb2hsv(r, g, b)

`   local max = math.max(r, g, b)`
`   local min = math.min(r, g, b)`
`   local c = max - min`
`   `
`   -- calculate hue`
`   local h`
`   if c == 0 then`
`       h = 0`
`   elseif max == r then`
`       h = 60 * (0 + ((g - b)/c))`
`   elseif max == g then`
`       h = 60 * (2 + ((b - r)/c))`
`   elseif max == b then`
`       h = 60 * (4 + ((r - g)/c))`
`   end`
`   if h < 0 then h = h + 360 end`
`   `
`   -- calculate value`
`   local v = max`
`   `
`   -- calculate luminance`
`   -- local l = (max + min) / 2`
`   `
`   -- calculate saturation`
`   local s`
`   if c == 0 then`
`       s = 0`
`   else`
`       s = c/v`
`   end`
`   `
`   return h, s, v`

end

function hsv2rgb(h, s, v)

`   local hi = math.floor(h / 60)`
`   local f = ((h / 60) - hi)`
`   `
`   local p = v * (1 - s)`
`   local q = v * (1 - s * f)`
`   local t = v * (1 - s * (1 - f))`
`   `
`   if hi == 1 then`
`       return q, v, p`
`   elseif hi == 2 then`
`       return p, v, t`
`   elseif hi == 3 then`
`       return p, q, v`
`   elseif hi == 4 then`
`       return t, p, v`
`   elseif hi == 5 then`
`       return v, p, q`
`   else`
`       return v, t, p`
`   end`

end

function decodeRGBHex(rgb)

`   local r = string.sub(rgb, 1, 2)`
`   local g = string.sub(rgb, 3, 4)`
`   local b = string.sub(rgb, 5, 6)`
`   return tonumber(r, 16), tonumber(g, 16), tonumber(b, 16)`

end

function getRGB(args)

`   local r, g, b, i`
`   if string.len(args[1]) == 6 then`
`       r, g, b = decodeRGBHex(args[1])`
`       i = 2`
`   else`
`       r = args[1]`
`       g = args[2]`
`       b = args[3]`
`       i = 4`
`   end`
`   return r / 255, g / 255, b / 255, i`

end

\--\[\[toHSV Description: Converts a RGB color to a HSV color.

Usage: {{\#invoke:HSV|toHSV|R|G|B}} or {{\#invoke:HSV|toHSV|RGBhex}}

Output: hue \[0°..360°\]/saturation \[0..1\]/value \[0..1\] \]\] function p.toHSV(frame)

`   local r, g, b = getRGB(frame.args)`
`   local h, s, v = rgb2hsv(r, g, b)`
`   return h .. "/" .. s .. "/" .. v`

end

\--\[\[hue Description: Returns the hue of a RGB color.

Usage: {{\#invoke:HSV|hue|R|G|B}} or {{\#invoke:HSV|hue|RGBhex}}

Output: hue \[0°..360°\] \]\] function p.hue(frame)

`   local r, g, b = getRGB(frame.args)`
`   local h, s, v = rgb2hsv(r, g, b)`
`   return h`

end

\--\[\[saturation Description: Returns the saturation of a RGB color.

Usage: {{\#invoke:HSV|saturation|R|G|B}} or {{\#invoke:HSV|saturation|RGBhex}}

Output: saturation \[0..1\] \]\] function p.saturation(frame)

`   local r, g, b = getRGB(frame.args)`
`   local h, s, v = rgb2hsv(r, g, b)`
`   return s`

end

\--\[\[value Description: Returns the hue of a RGB color.

Usage: {{\#invoke:HSV|value|R|G|B}} or {{\#invoke:HSV|value|RGBhex}}

Output: value \[0..1\] \]\] function p.value(frame)

`   local r, g, b = getRGB(frame.args)`
`   local h, s, v = rgb2hsv(r, g, b)`
`   return v`

end

\--\[\[saturate Description: Saturates a RGB color by a given factor.

Usage: {{\#invoke:HSV|saturate|R|G|B|factor}} or {{\#invoke:HSV|saturate|RGBhex|factor}} Optionally "factor" can be followed by another parameter with the value "hex" can be given to return the RGB color in a hexadecimal representation.

Output: saturated RGB \]\] function p.saturate(frame)

`   local r, g, b, i = getRGB(frame.args)`
`   -- convert to HSV`
`   local h, s, v = rgb2hsv(r, g, b)`
`   -- saturate`
`   s = s * frame.args[i]`
`   if s < 0 then`
`       s = 0`
`   elseif s > 1 then`
`       s = 1`
`   end`
`   -- convert back to RGB`
`   local r, g, b = hsv2rgb(h, s, v)`
`   r = math.floor(r * 255 + 0.5)`
`   g = math.floor(g * 255 + 0.5)`
`   b = math.floor(b * 255 + 0.5)`
`   -- return values`
`   if frame.args[i + 1] == "hex" then`
`       return string.format("%.2X%.2X%.2X", r, g, b)`
`   else`
`       return r .. "/" .. g .. "/" .. b`
`   end`

end

\--\[\[toRGB Description: Converts a HSV color to a RGB color.

Usage: {{\#invoke:HSV|toRGB|H|S|V}} with H in \[0°..360°\], S in \[0..1\] and V in \[0..1\]. Optionally a 4th parameter with the value "hex" can be given to return the RGB color in a hexadecimal representation.

Output: R/G/B \]\] function p.toRGB(frame)

`   local r, g, b = hsv2rgb(frame.args[1], frame.args[2], frame.args[3])`
`   -- transform from real [0..1] to integer [0..255]`
`   r = math.floor(r * 255 + 0.5)`
`   g = math.floor(g * 255 + 0.5)`
`   b = math.floor(b * 255 + 0.5)`
`   -- return values`
`   if frame.args[4] == "hex" then`
`       return string.format("%.2X%.2X%.2X", r, g, b)`
`   else`
`       return r .. "/" .. g .. "/" .. b`
`   end`

end

return p