# pico.green.js
JS face detection tool, build from pico.js x camvas.js

## Require libraries
* <a href='https://github.com/tehnokv/picojs'>pico.js</a> - face detection library
* <a href='https://github.com/diewland/camvas'>camvas</a> - render webcam to canvas ( custom edition )

## How to use
html
```html
<canvas width='640' height='480'></canvas>
```

javascript
```javascript
var pg = new PicoGreen();
var camvas_obj = pg.init();
```

## Configurations
```javascript
var pg = new PicoGreen({ /* config as kv here */ });
```
| Name               | Description                           | Type     | Default    | Values                        |
| ------------------ | ------------------------------------- | -------- | ---------- | ----------------------------- |
| mode               | Webcam profile                        | String   | vga        | qvga, vga, hd, fullhd, 4k, 8k |
| cascade_url        | Binary file for face detection        | String   | github url |                               |
| min_face_score     | Face score threshold ( not percent )  | Float    | 50.0       |                               |
| min_detect_size    | Min width to draw yellow rect (px)    | Int      | 60         |                               |
| min_recognize_size | Min width to draw green rect (px)     | Int      | 100        |                               |
| draw_video_fn      | run every frame: Draw video on canvas | Function | basic draw |                               |
| end_of_frame_fn    | run every frame: After filter faces   | Function |            |                               |

## TODO
* add more examples
