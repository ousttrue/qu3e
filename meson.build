project('qu3e', ['c', 'cpp'],
	version: '1.1',
	default_options: ['cpp_std=c++11'],
)

# option(qu3e_build_shared "Build qu3e shared libraries" OFF)
# option(qu3e_build_static "Build qu3e static libraries" ON)
# option(qu3e_build_demo "Build qu3e demo" ON)

subdir('src')
if get_option('build_demo')
	# find_package(OpenGL REQUIRED)
	subdir('imgui')
	subdir('freeglut')
	subdir('demo')
endif
