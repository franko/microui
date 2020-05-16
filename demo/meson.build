# The config-tool method should not be needed but SDL2 2.10.2
# provide a pkg-config file that is inaccurate as it does not include
# the libraries -lm -ldl -lrt (on linux).
# By using the config-tool method we require the sdl2-config tool instead
# of pkg-config.
libsdl2 = dependency('sdl2', method: 'config-tool', required: false)

opengl = dependency('GL', required: false)

if libsdl2.found() and opengl.found()
    executable('microui-demo',
        ['renderer.c', 'main.c'],
        include_directories: microui_include,
        link_with: libmicroui,
        dependencies: [libsdl2, opengl],
        install: true,
        gui_app: true,
    )
endif
