# NOTE

This version of ofxBlur support GLSL version 4.50


# ofxBlur is an addon for [openFrameworks](http://openframeworks.cc)

ofxBlur uses a ping-pong technique on the graphics card to do a very fast, configurable blur. ofxBlur can also simulate bloom given the right parameters.

Only call `setup()` once. You must specify the `width` and `height` so the internal FBOs can be allocated. `radius`describes the radius of the blur kernel. The larger the `radius`, the longer it takes to compute the blur. If you want a larger apparent radius at the same speed, use `setScale(x)` where `x>1`. This yields a lower-quality but faster blur. `shape` describes the circularity/squareness of the kernel. For a more circular kernel, use smaller values like `.2` and for a more square kernel use larger values like `10`. For more square kernels, rotating the kernel has an obvious visual effect. use `setRotation()` to set the rotation of the kernel in radians. Finally, using the `passes` and `downsample` arguments, you can run the blur filter multiple times at different scales and ofxBlur will combine the results for you. This can be used to create a more bloom-like or fog-like effect.

ofxBlur was originally written for [Eyeshine](https://github.com/kylemcdonald/Eyeshine), a collaboration between Golan Levin and Kyle McDonald.
