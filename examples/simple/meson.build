
se_moc_input = [
  'MainWindow.h',
]

se_moc = qt.compile_moc(
  headers: se_moc_input,
  dependencies: qt_dep,
  extra_args: moc_args)

se_ui = qt.compile_ui(sources: ['MainWindow.ui'])

se_src = files(
  'main.cpp',
  'MainWindow.cpp',
)

executable(
    'SimpleExample',
    [se_moc, se_src, se_ui],
    dependencies: qtadvanceddocking_dep
)

