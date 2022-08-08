
sb_moc_input = [
  'MainWindow.h',
]

sb_moc = qt.compile_moc(
  headers: sb_moc_input,
  dependencies: qt_dep,
  extra_args: moc_args)

sb_ui = qt.compile_ui(sources: ['MainWindow.ui'])

sb_src = files(
  'main.cpp',
  'MainWindow.cpp',
)

executable(
    'SidebarExample',
    [sb_moc, sb_src, sb_ui],
    dependencies: qtadvanceddocking_dep
)

