project('alt-regular-backgrounds',
  version: '0.3.2',
  meson_version: '>= 0.56.0',
  license: 'GPL-3.0-or-later'
)

i18n = import('i18n')

prefix = get_option('prefix')

datadir = join_paths(prefix, get_option('datadir'))

if get_option('target_de') == 'all'
  subdir('backgrounds/gnome')
  subdir('backgrounds/kde')
  subdir('backgrounds/phosh')
else
  subdir('backgrounds/@0@'.format(get_option('target_de')))
endif

