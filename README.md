# anoxrtx

Notes:

1. For game to display correctly install:
https://github.com/whisperglen/QindieGL/releases/
Also add:
```
enable_camera_detection = 1
camera_detection_mode = 1
```
to QindieGL.ini that fixes post effects such as eye adaptation, fixes transforms when exporting captures.

2. Add the lines:
```
set r_nocull 1
set gl_cull 0
set gl_cleartoblack 1
```
to /anoxdata/CONFIGS/Default.cfg
That ensures culling is disabled as much as possible.
The last line prevents green background leaking through geometry.

3. The game relies a lot on id tech phong shading. So most character models have bad normals.
I raise roughness and metalicity of character materials to the max to mask the problem. 
