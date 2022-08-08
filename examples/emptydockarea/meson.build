
eda_moc_input = [
  'mainwindow.h',
]

eda_moc = qt.compile_moc(
  headers: eda_moc_input,
  dependencies: qt_dep,
  extra_args: moc_args)

eda_ui = qt.compile_ui(sources: ['mainwindow.ui'])

eda_src = files(
  'main.cpp',
  'mainwindow.cpp',
)

executable(
    'EmptyDockAreaExample',
    [eda_moc, eda_src, eda_ui],
    dependencies: qtadvanceddocking_dep
)

