# tikal

* [Imgui](https://github.com/ocornut/imgui)
* Physics
  * [Box2D](https://github.com/erincatto/box2d)
* Audio
  * [sokol_audio](https://github.com/floooh/sokol/blob/master/sokol_audio.h)
  * [miniaudio](https://github.com/mackron/miniaudio)
    * More features than sokol_audio according to @floooh.
  * [soloud](https://github.com/jarikomppa/soloud)
    * Even more features than sokol_audio, accoding to @floooh.
  * [cute_sound](https://github.com/RandyGaul/cute_headers/blob/master/cute_sound.h)
    * No clue how many features.
  * FMOD?
* Fonts
  * [fontstash](https://github.com/memononen/fontstash)
    * Not actively maintained
    * Uses stb_truetype
  * [sbt_truetype](https://github.com/nothings/stb/blob/master/stb_truetype.h) ([example](https://github.com/justinmeiners/stb-truetype-example))
  * [cute_font](https://github.com/RandyGaul/cute_headers/blob/master/cute_font.h)
  * [SDL_ttf](https://github.com/libsdl-org/SDL_ttf)
  * https://github.com/suikki/sdf_text_sample
    * Uses fontstash and stb_truetype.
* ECS
  * [flecs](https://github.com/SanderMertens/flecs)
* Graphics
  * Just use OpenGL. Both bgfx and sokol-gfx are 3D-graphics libs. Which is not needed.
  * [bgfx](https://github.com/bkaradzic/bgfx)
  * [sokol-gfx](https://github.com/floooh/sokol/blob/master/sokol_gfx.h)
* Spine2D
  * Look at how [spine-sfml](https://github.com/EsotericSoftware/spine-runtimes/tree/4.2-beta/spine-sfml/cpp) works.
    * They only import a handful of stuff from SFML which should be available in bgfx. Could also just copy the relevant SFML code.
    * Don't use stable version. They recently got rid of vertex effects, which should make the rendering a lot easier.
  * If sokol-gfx: Maybe look at using [sokol-gl](https://github.com/floooh/sokol/blob/master/util/sokol_gl.h). It should be easier to translate what we have done so far in [spine-raylib](https://github.com/tapir2342/spine-raylib).
    * No support for vertex arrays might be a problem?
