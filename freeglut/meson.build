# add_definitions( -DFREEGLUT_EXPORTS -DFREEGLUT_STATIC -D_CRT_SECURE_NO_WARNINGS )

# set(MULTIMEDIA_LIB X11)

# if(APPLE)
# 	include_directories( /usr/X11/include )
# endif(APPLE)

# if(UNIX)
# 	add_definitions( -D__unix__ -DHAVE_FCNTL_H -DHAVE_GETTIMEOFDAY )
# endif(UNIX)

# if(WIN32)
# 	set(MULTIMEDIA_LIB winmm)
# endif(WIN32)

gl_dep = dependency('opengl')
freeglut_inc = include_directories('.')

c_compiler = meson.get_compiler('c')
winmm_lib = c_compiler.find_library('winmm', required: true)

freeglut_lib = static_library('freeglut', [
	'freeglut_callbacks.c',
	'freeglut_callbacks.c',
	'freeglut_cursor.c',
	'freeglut_display.c',
	'freeglut_ext.c',
	'freeglut_font_data.c',
	'freeglut_font.c',
	'freeglut_gamemode.c',
	'freeglut_geometry.c',
	'freeglut_glutfont_definitions.c',
	'freeglut_init.c',
	'freeglut_input_devices.c',
	'freeglut_internal.h',
	'freeglut_joystick.c',
	'freeglut_main.c',
	'freeglut_menu.c',
	'freeglut_misc.c',
	'freeglut_overlay.c',
	'freeglut_spaceball.c',
	'freeglut_state.c',
	'freeglut_stroke_mono_roman.c',
	'freeglut_stroke_roman.c',
	'freeglut_structure.c',
	'freeglut_teapot_data.h',
	'freeglut_teapot.c',
	'freeglut_videoresize.c',
	'freeglut_window.c',
	'freeglut.h',
	'freeglut_ext.h',
	'freeglut_std.h',
],
)
freeglut_dep = declare_dependency(
    include_directories: freeglut_inc,
    link_with: freeglut_lib,
    dependencies: [gl_dep, winmm_lib],
)
