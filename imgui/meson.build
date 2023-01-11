imgui_inc = include_directories('.')
imgui_lib = static_library('imgui', [
	'imgui.cpp',
])
imgui_dep = declare_dependency(
    link_with: imgui_lib,    
    include_directories: imgui_inc,
)
