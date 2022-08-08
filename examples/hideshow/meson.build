
hs_moc_input = [
  'MainWindow.h',
]

hs_moc = qt.compile_moc(
  headers: hs_moc_input,
  dependencies: qt_dep,
  extra_args: moc_args)

hs_ui = qt.compile_ui(sources: ['MainWindow.ui'])

hs_src = files(
  'main.cpp',
  'MainWindow.cpp',
)

executable(
    'HideShowExample',
    [hs_moc, hs_src, hs_ui],
    dependencies: qtadvanceddocking_dep
)

