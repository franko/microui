project('microui', 'c', version: '2.01', default_options : [
    'c_std=c11',
    'default_library=static',
])

microui_include = include_directories('src')

subdir('src')
subdir('demo')

pkg = import('pkgconfig')

pkg.generate(libmicroui,
    filebase : 'microui',
    name : 'microui',
    description : 'MicroUI, a tiny immediate-mode UI library',
    url : 'github.com/rxi/microui',
)
