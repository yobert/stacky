project('stacky', 'c')

add_project_arguments([
	'-DWLR_USE_UNSTABLE',
], language: 'c')

wlroots        = dependency('wlroots')
wayland_server = dependency('wayland-server')
xkbcommon      = dependency('xkbcommon')

wayland_client = dependency('wayland-client')
wayland_protos = dependency('wayland-protocols')

subdir('protocol')

executable('stacky', 'main.c',
	dependencies: [
		wlroots,
		wayland_server,
		xkbcommon,
	],
	include_directories: [
		include_directories('protocol'),
	],
)
