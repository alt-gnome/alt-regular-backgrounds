backgrounddir = join_paths(datadir, 'backgrounds', 'alt-regular-phosh')
metadatadir = join_paths(datadir, 'gnome-background-properties')

conf = configuration_data()
conf.set('BACKGROUNDDIR', backgrounddir)
conf.set('datadir', datadir)

backgrounds = [
  'orange-hex-d.png',
  'orange-hex-l.png',
  'orange-hex-lockscreen.png',
]

metadatas = [
  'alt-regular-phosh-orange-hex.xml',
]

install_data(backgrounds, install_dir: backgrounddir)

foreach metadata : metadatas
  configure_file(
    input: metadata + '.in',
    output: metadata,
    configuration: conf,
    install: true,
    install_dir: metadatadir
  )
endforeach
