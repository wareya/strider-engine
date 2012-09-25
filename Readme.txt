the strider engine aims to be a basic engine for platformer development in game maker, with support for arbitrary collision geometry between a "character" and the "wall"

the "character" is any entity that should slide or walk up slopes or stairs, have friction, and not have a rotating collision shape
the "wall" is an arbitrarily shaped stationary solid with which the character's movement interacts. the wall acts as a floor, slope, ceiling, and wall at the same time. all "wall" solids are interacted with the same way in the same code, so they are considered the same object for simplification purposes.

note: CPU usage increases linear to character speed. optimizations and hacks are possible but impractical in complex collision situations, only very dumb ones, and they would incur extra cost in complex collisions.

included is a basic room using tiles as testing material. sloped ceilings are not currently supported, but trivial to implement.

There is a precision issue with pressing against walls that I haven't quite figured out yet: http://www.ganggarrison.com/forums/index.php?topic=32536.msg1107323#msg1107323

WARNING: Do not run for extended periods of time with debug log enabled. It writes to a file on disk more than 60 times per second, with more text when you're moving faster. Its sole purpose is for debugging errors in the tracer.

either zlib or ISC license apply

Known issues:
- Wallpressing causes precision/consistency loss
- Ceiling slopes are not yet supported
