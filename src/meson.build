custom_target(
    'cantarell-static-fonts',
    input: 'Cantarell.designspace',
    output: [
        'Cantarell-Thin.otf',
        'Cantarell-Light.otf',
        'Cantarell-Regular.otf',
        'Cantarell-Medium.otf',
        'Cantarell-Semibold.otf',
        'Cantarell-Bold.otf',
        'Cantarell-ExtraBold.otf',
    ],
    command: [python3, make_static_fonts, '@INPUT@', psautohint, '@OUTDIR@'],
    install: true,
    install_dir: fontsdir,
)

custom_target(
    'cantarell-variable-font',
    input: 'Cantarell.designspace',
    output: 'Cantarell-VF.otf',
    command: [
        python3,
        make_variable_font,
        '@INPUT@',
        join_paths(meson.current_source_dir(), 'Cantarell.stylespace'),
        psautohint,
        tx,
        sfntedit,
        '@OUTPUT@'
    ],
    install: true,
    install_dir: fontsdir,
)
