backgrounddir = join_paths(datadir, 'backgrounds', 'alt-regular-gnome')
metadatadir = join_paths(datadir, 'gnome-background-properties')

conf = configuration_data()
conf.set('BACKGROUNDDIR', backgrounddir)
conf.set('datadir', datadir)

backgrounds = [
  'hex-black-ld.png',
  'hex-blue-d.png',
  'hex-blue-l.png',
  'hex-orange-d.png',
  'hex-orange-l.png',
  'liberation-blue-d.png',
  'liberation-blue-l.png',
  'liberation-green-d.png',
  'liberation-green-l.png',
  'liberation-yellow-d.png',
  'liberation-yellow-l.png',
  'liberation-d.png',
  'liberation-l.png',
]

metadatas = [
  'alt-regular-gnome-hex-black.xml',
  'alt-regular-gnome-hex-blue.xml',
  'alt-regular-gnome-hex-orange.xml',
  'alt-regular-gnome-liberation-blue.xml',
  'alt-regular-gnome-liberation-green.xml',
  'alt-regular-gnome-liberation-yellow.xml',
  'alt-regular-gnome-liberation.xml',
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
