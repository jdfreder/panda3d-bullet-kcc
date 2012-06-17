panda3d-bullet-kcc
==================

The custom kinematic character controller for Panda3D, replacing the Bullet's default character controller and providing more stability and features.
    
Features included:
    * Walking with penetration prevention
    * Jumping with active and passive jump limiter. Active means limiting the max jump height based on the distance to the "ceiling". Passive means falling automatically when a "ceiling" is hit.
    * Crouching with stand up limiter which prevents the character from standing up if inside a tunnel or other limited space
    * Slope limiter of arbitrary maximum slope values which may or may not affect the movement speed on slopes smaller than maximum
    * Stepping, supports walking steps up and down (prevents "floating" effect)
    * Flying support for no-clip, ladders, swimming or simply flying
    * Simplified state system. Makes double/multiple jumps impossible by default 
    * Callbacks for landing and standing up from crouch
    
The controller is composed of a levitating capsule (allowing stepping), a kinematic body and numerous raycasts accounting for levitation and spacial awareness.
The elements are set up automatically.
