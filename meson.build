project('QtAdvancedDockingSystem', 'cpp', meson_version: '>=0.60')

#First checking for Qt6 unless we want to force Qt5
if get_option('force_qt5')
    qt_search = ['qt5']
else
    qt_search = ['qt6', 'qt5']
endif
qt_dep = dependency(qt_search, modules: ['Core', 'Gui', 'Widgets'], private_headers: true)
qt = import('qt@0@'.format(qt_dep.version().split('.')[0]))

lib_deps = [qt_dep]

#Applying some OS specific flags and settings to the library build
host_os = host_machine.system()
#NOTE: Defining these flags are needed to ensure correct moc'ing occurs depending on the intended host platform
# Without the define, Linux builds are known to crash and others are likely to crash
if host_os == 'windows'
    moc_args = ['-DQ_OS_WIN']
elif host_os == 'linux'
    moc_args = ['-DQ_OS_LINUX']

    #xcb is a Linux specific dependency
    xcb = dependency('xcb')
    lib_deps += [xcb]
elif host_os == 'darwin'
    moc_args = ['-DQ_OS_MAC']
endif

subdir('src')

if get_option('build_examples')
    subdir('demo')
    subdir('examples')
endif