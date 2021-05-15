# Nombre del proyecto y lenguaje de programación
project('com.github.pgonzalezc.eos-vala-hello-again','vala','c')

# Creación del ejecutable, enumera los programas a compilar,
# llas dependencias e instala
executable(
    meson.project_name(),
    'src/Application.vala',
    dependencies: [
        dependency('gtk+-3.0')
    ],
    install: true
)

# Instala el fichero .desktop para que los vea el menu de aplicaciones
install_data(
    join_paths('data','hello-again.appdata.xml'),
    install_dir: join_paths(get_option('datadir'),'metainfo'),
    rename: meson.project_name() + '.appdata.xml'
)

# Instala el icono en todos los tamaños requeridos
icon_sizes = ['16','32','48','64','128']

foreach i : icon_sizes
    install_data(
        join_paths('data',i + '.svg'),
        install_dir: jpin_paths(get_option('data_dir'),'icons','hicolor', i +'x' + 1, 'apps'),
        rename: meson.poject_name() + '.svg'
    )
    install_data(
        join_paths('data',i + '.svg'),
        install_dir: join_paths(get_option('datadir'), 'icons', 'hicolor', i + 'x' + i + '@2', 'apps')
    )
endforeach
