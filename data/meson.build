icon_sizes = ['32', '48', '64']

foreach i : icon_sizes
    install_data(
        join_paths('icons/', i, meson.project_name() + '.svg'),
        install_dir: join_paths(get_option('datadir'), 'icons', 'hicolor', i + 'x' + i, 'apps')
    )
    install_data(
        join_paths('icons/', i, meson.project_name() + '.svg'),
        install_dir: join_paths(get_option('datadir'), 'icons', 'hicolor', i + 'x' + i + '@2', 'apps')
    )
    install_data(
        join_paths('icons/', i, meson.project_name() + '.svg'),
        install_dir: join_paths(get_option('datadir'), 'icons/hicolor', i + 'x' + i, 'mimetypes')
    )
    install_data(
        join_paths('icons/', i, meson.project_name() + '.svg'),
        install_dir: join_paths(get_option('datadir'), 'icons/hicolor', i + 'x' + i + '@2', 'mimetypes')
    )
endforeach

install_data(
    join_paths('icons', '64', meson.project_name() + '.svg'),
    install_dir: join_paths(get_option('datadir'), 'icons/hicolor/scalable/apps')
)

i18n.merge_file(
    input: meson.project_name() + '.desktop.in',
    output: meson.project_name() + '.desktop',
    po_dir: join_paths(meson.source_root(), 'po', 'extra'),
    type: 'desktop',
    install: true,
    install_dir: join_paths(get_option('datadir'), 'applications')
)

i18n.merge_file(
    input: meson.project_name() + '.appdata.xml.in',
    output: meson.project_name() + '.appdata.xml',
    po_dir: join_paths(meson.source_root(), 'po', 'extra'),
    install: true,
    install_dir: join_paths(get_option('datadir'), 'metainfo')
)