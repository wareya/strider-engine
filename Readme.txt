the strider engine aims to be a basic engine for platformer development in game maker, with support for arbitrary collision geometry between a "character" and the "wall"

the "character" is any entity that should slide or walk up slopes or stairs, have friction, and not have a rotating collision shape
the "wall" is an arbitrarily shaped stationary solid with which the character's movement interacts. the wall acts as a floor, slope, ceiling, and wall at the same time. all "wall" solids are interacted with the same way in the same code, so they are considered the same object for simplification purposes.

note: CPU usage increases linear to character speed. optimizations and hacks are possible but impractical for simply coded and "perfect" interaction between the character and wall.

indluded is a basic room using tiles as testing material. sloped ceilings are not currently supported, but trivial to implement. don't fall off or you'll have a CPU usage runaway as described above.

either zlib or ISC license apply