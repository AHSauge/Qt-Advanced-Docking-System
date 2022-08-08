
#When building with Qt5 on Windows, we need to pull in another dependency
if host_machine.system() == 'windows' and qt_dep.version().split('.')[0] < 6
    qt_dep = dependency('qt5', modules: ['Core', 'Gui', 'Widgets', 'AxContainer'], private_headers: true)
endif

demo_moc_input = [
  'MainWindow.h',
  'StatusDialog.h',
]

demo_cpp = qt.compile_resources(sources: ['demo.qrc'])
demo_moc = qt.compile_moc(
  headers: demo_moc_input,
  dependencies: qt_dep,
  extra_args: moc_args)

demo_ui = qt.compile_ui(sources: ['mainwindow.ui', 'StatusDialog.ui'])

demo_src = files(
  'main.cpp',
  'MainWindow.cpp',
  'StatusDialog.cpp',
)

executable(
    'AdvancedDockingSystemDemo',
    [demo_cpp, demo_moc, demo_src, demo_ui],
    dependencies: qtadvanceddocking_dep
)
