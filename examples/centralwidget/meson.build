
cwe_moc_input = [
  'mainwindow.h',
]

cwe_moc = qt.compile_moc(
  headers: cwe_moc_input,
  dependencies: qt_dep,
  extra_args: moc_args)

cwe_ui = qt.compile_ui(sources: ['mainwindow.ui'])

cwe_src = files(
  'main.cpp',
  'mainwindow.cpp',
)

executable(
    'CentralWidgetExample',
    [cwe_moc, cwe_src, cwe_ui],
    dependencies: qtadvanceddocking_dep
)

