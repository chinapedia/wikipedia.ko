> This article is converted from Wikipedia: [모듈:Ddy-map](https://ko.wikipedia.org/wiki/모듈:Ddy-map).


local p = {}

function p.fromGeo(frame)

` x = frame.args['lng'] * 1.395 + frame.args['lat'] * 0.063 - 175.692`
` y = frame.args['lng'] * 0.018 - frame.args['lat'] * 2.248 + 95.163`
` templates = argsFromXY(frame, x, y, frame.args['zoom'], frame.args['width'], frame.args['aspectRatio'])`
` return (`
`   "{| cellspacing='0' cellpadding='0'\n|" ..`
`   templates[1] .. "\n|" .. templates[2] .. "\n|-\n|" ..`
`   templates[3] .. "\n|" .. templates[4] .. "\n|}"`
` )`

end

function p.fromXY(frame)

` templates = argsFromXY(frame, frame.args['x'], frame.args['y'], frame.args['zoom'], frame.args['width'], frame.args['aspectRatio'])`
` return (`
`   "{| cellspacing='0' cellpadding='0'\n|" ..`
`   templates[1] .. "\n|" .. templates[2] .. "\n|-\n|" ..`
`   templates[3] .. "\n|" .. templates[4] .. "\n|}"`
` )`

end

function argsFromXY(frame, x, y, zoom, crop_width, aspect_ratio)

` TILE_WIDTH = 4000`
` TILE_HEIGHT = 3000`
` x_int = math.floor(x + 0.5)`
` y_int = math.floor(y + 0.5)`
` tile_width = 4000 / (2 ^ (14 - zoom))`
` tile_height = tile_width / TILE_WIDTH * TILE_HEIGHT`
` crop_height = crop_width / aspect_ratio`
` center_x = (x - x_int) * tile_width + tile_width / 2`
` center_y = (y - y_int) * tile_height + tile_height / 2`

` left_needed = center_x < crop_width / 2`
` right_needed = center_x + crop_width / 2 > tile_width`
` top_needed = center_y < crop_height / 2`
` bottom_needed = center_y + crop_height / 2 > tile_height`

` if left_needed then`
`   left_width = crop_width / 2 - center_x`
`   if top_needed then`
`     top_height = crop_height / 2 - center_y`
`     return {`
`       getTile(frame, x_int - 1, y_int - 1, {`
`         bSize = tile_width,`
`         cWidth = left_width,`
`         cHeight = top_height,`
`         oLeft = tile_width - left_width,`
`         oTop = tile_height - top_height,`
`       }),`
`       getTile(frame, x_int, y_int - 1, {`
`         bSize = tile_width,`
`         cWidth = crop_width - left_width,`
`         cHeight = top_height,`
`         oLeft = 0,`
`         oTop = tile_height - top_height,`
`       }),`
`       getTile(frame, x_int - 1, y_int, {`
`         bSize = tile_width,`
`         cWidth = left_width,`
`         cHeight = crop_height - top_height,`
`         oLeft = tile_width - left_width,`
`         oTop = 0,`
`       }),`
`       getTile(frame, x_int, y_int, {`
`         bSize = tile_width,`
`         cWidth = crop_width - left_width,`
`         cHeight = crop_height - top_height,`
`         oLeft = 0,`
`         oTop = 0,`
`       }),`
`     }`
`   elseif bottom_needed then`
`     top_height = tile_height - center_y + crop_height / 2`
`     return {`
`       getTile(frame, x_int - 1, y_int, {`
`         bSize = tile_width,`
`         cWidth = left_width,`
`         cHeight = top_height,`
`         oLeft = tile_width - left_width,`
`         oTop = tile_height - top_height,`
`       }),`
`       getTile(frame, x_int, y_int, {`
`         bSize = tile_width,`
`         cWidth = crop_width - left_width,`
`         cHeight = top_height,`
`         oLeft = 0,`
`         oTop = tile_height - top_height,`
`       }),`
`       getTile(frame, x_int - 1, y_int + 1, {`
`         bSize = tile_width,`
`         cWidth = left_width,`
`         cHeight = crop_height - top_height,`
`         oLeft = tile_width - left_width,`
`         oTop = 0,`
`       }),`
`       getTile(frame, x_int, y_int + 1, {`
`         bSize = tile_width,`
`         cWidth = crop_width - left_width,`
`         cHeight = crop_height - top_height,`
`         oLeft = 0,`
`         oTop = 0,`
`       }),`
`     }`
`   else`
`     return {`
`       getTile(frame, x_int - 1, y_int, {`
`         bSize = tile_width,`
`         cWidth = left_width,`
`         cHeight = crop_height,`
`         oLeft = tile_width - left_width,`
`         oTop = center_y - crop_height / 2,`
`       }),`
`       getTile(frame, x_int, y_int, {`
`         bSize = tile_width,`
`         cWidth = crop_width - left_width,`
`         cHeight = crop_height,`
`         oLeft = 0,`
`         oTop = center_y - crop_height / 2,`
`       }),`
`       "", "",`
`     }`
`   end`
` elseif right_needed then`
`   left_width = tile_width - center_x + crop_width / 2`
`   if top_needed then`
`     top_height = crop_height / 2 - center_y`
`     return {`
`       getTile(frame, x_int, y_int - 1, {`
`         bSize = tile_width,`
`         cWidth = left_width,`
`         cHeight = top_height,`
`         oLeft = tile_width - left_width,`
`         oTop = tile_height - top_height,`
`       }),`
`       getTile(frame, x_int + 1, y_int - 1, {`
`         bSize = tile_width,`
`         cWidth = crop_width - left_width,`
`         cHeight = top_height,`
`         oLeft = 0,`
`         oTop = tile_height - top_height,`
`       }),`
`       getTile(frame, x_int, y_int, {`
`         bSize = tile_width,`
`         cWidth = left_width,`
`         cHeight = crop_height - top_height,`
`         oLeft = tile_width - left_width,`
`         oTop = 0,`
`       }),`
`       getTile(frame, x_int + 1, y_int, {`
`         bSize = tile_width,`
`         cWidth = crop_width - left_width,`
`         cHeight = crop_height - top_height,`
`         oLeft = 0,`
`         oTop = 0,`
`       }),`
`     }`
`   elseif bottom_needed then`
`     top_height = tile_height - center_y + crop_height / 2`
`     return {`
`       getTile(frame, x_int, y_int, {`
`         bSize = tile_width,`
`         cWidth = left_width,`
`         cHeight = top_height,`
`         oLeft = tile_width - left_width,`
`         oTop = tile_height - top_height,`
`       }),`
`       getTile(frame, x_int + 1, y_int, {`
`         bSize = tile_width,`
`         cWidth = crop_width - left_width,`
`         cHeight = top_height,`
`         oLeft = 0,`
`         oTop = tile_height - top_height,`
`       }),`
`       getTile(frame, x_int, y_int + 1, {`
`         bSize = tile_width,`
`         cWidth = left_width,`
`         cHeight = crop_height - top_height,`
`         oLeft = tile_width - left_width,`
`         oTop = 0,`
`       }),`
`       getTile(frame, x_int + 1, y_int + 1, {`
`         bSize = tile_width,`
`         cWidth = crop_width - left_width,`
`         cHeight = crop_height - top_height,`
`         oLeft = 0,`
`         oTop = 0,`
`       }),`
`     }`
`   else`
`     return {`
`       getTile(frame, x_int, y_int, {`
`         bSize = tile_width,`
`         cWidth = left_width,`
`         cHeight = crop_height,`
`         oLeft = tile_width - left_width,`
`         oTop = center_y - crop_height / 2,`
`       }),`
`       getTile(frame, x_int + 1, y_int, {`
`         bSize = tile_width,`
`         cWidth = crop_width - left_width,`
`         cHeight = crop_height,`
`         oLeft = 0,`
`         oTop = center_y - crop_height / 2,`
`       }),`
`       "", "",`
`     }`
`   end`
` else`
`   if top_needed then`
`     top_height = crop_height / 2 - center_y`
`     return {`
`       getTile(frame, x_int, y_int - 1, {`
`         bSize = tile_width,`
`         cWidth = crop_width,`
`         cHeight = top_height,`
`         oLeft = center_x - crop_width / 2,`
`         oTop = tile_height - top_height,`
`       }),`
`       "",`
`       getTile(frame, x_int, y_int, {`
`         bSize = tile_width,`
`         cWidth = crop_width,`
`         cHeight = crop_height - top_height,`
`         oLeft = center_x - crop_width / 2,`
`         oTop = 0,`
`       }),`
`       "",`
`     }`
`   elseif bottom_needed then`
`     top_height = tile_height - center_y + crop_height / 2`
`     return {`
`       getTile(frame, x_int, y_int, {`
`         bSize = tile_width,`
`         cWidth = crop_width,`
`         cHeight = top_height,`
`         oLeft = center_x - crop_width / 2,`
`         oTop = tile_height - top_height,`
`       }),`
`       "",`
`       getTile(frame, x_int, y_int + 1, {`
`         bSize = tile_width,`
`         cWidth = crop_width,`
`         cHeight = crop_height - top_height,`
`         oLeft = center_x - crop_width / 2,`
`         oTop = 0,`
`       }),`
`       "",`
`     }`
`   else`
`     return {`
`       getTile(frame, x_int, y_int, {`
`         bSize = tile_width,`
`         cWidth = crop_width,`
`         cHeight = crop_height,`
`         oLeft = center_x - crop_width / 2,`
`         oTop = center_y - crop_height / 2,`
`       }),`
`       "", "", "",`
`     }`
`   end`
` end`

end

\-- y x0123456789 -- 1: 8765 -- 2: 65 4321 -- 3: 7654321 -- 4: 7654321 -- 5: 7654321 -- 6: 87654321 -- 7: 7654321 -- 8: 654321 -- 9: 4321 -- 10: 654321 -- 11: 654321 -- 12: 654321 -- 13: 654321 -- 14: 654321 -- 15: 654321 -- 16: 654321 -- 17: 54321 -- 18: 654321 -- 19: 654321 -- 20: 54321 -- 21: 1 -- 22: 1 -- y x0123456789 function getPageFromXY(x, y)

` if y == 1 and (6 <= x and x <= 9) then return {y, 14 - x}`
` elseif y == 2 then`
`   if 6 <= x and x <= 9 then`
`     return {y, 10 - x}`
`   elseif 3 <= x and x <= 4 then`
`     return {y, 9 - x}`
`   else return nil end`
` elseif y == 3 and (3 <= x and x <= 9) then return {y, 10 - x}`
` elseif (y == 4 or y == 5) and (2 <= x and x <= 8) then return {y, 9 - x}`
` elseif y == 6 and (1 <= x and x <= 8) then return {y, 9 - x}`
` elseif y == 7 and (0 <= x and x <= 6) then return {y, 7 - x}`
` elseif y == 8 and (0 <= x and x <= 5) then return {y, 6 - x}`
` elseif y == 9 and (2 <= x and x <= 5) then return {y, 6 - x}`
` elseif (10 <= y and y <= 12) and (1 <= x and x <= 6) then return {y, 7 - x}`
` elseif (y == 13 or y == 15 or y == 16 or y == 18 or y == 19) and (2 <= x and x <= 7) then return {y, 8 - x}`
` elseif y == 14 and (3 <= x and x <= 8) then return {y, 9 - x}`
` elseif y == 17 and (3 <= x and x <= 7) then return {y, 8 - x}`
` elseif y == 20 and (2 <= x and x <= 6) then return {y, 7 - x}`
` elseif (y == 21 or y == 22) and (x == 3) then return {y, 1}`
` end`
` return nil`

end function getPageImageFromXY(x, y)

` args = getPageFromXY(x, y)`
` if args == nil then`
`   return nil`
` end`
` return string.format("Daedongyeojido (Gyujanggak) %02d-%02d.jpg", args[1], args[2])`

end

function getTile(frame, x, y, args)

` image = getPageImageFromXY(x, y)`
` if image == nil then`
`   return ""`
` end`
` args['Image'] = image`
` return frame:expandTemplate{`
`   title = 'CSS image crop',`
`   args = args,`
` }`

end

return p