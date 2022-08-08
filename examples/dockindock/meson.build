
did_moc_input = [
  'dockindock.h',
  'dockindockmanager.h',
  'mainframe.h',
  'perspectiveactions.h',
  'perspectives.h',
]

did_moc = qt.compile_moc(
  headers: did_moc_input,
  dependencies: qt_dep,
  extra_args: moc_args)

did_src = files(
  'dockindock.cpp',
  'dockindockmanager.cpp',
  'main.cpp',
  'mainframe.cpp',
  'perspectiveactions.cpp',
  'perspectives.cpp',
)

executable(
    'DockInDockExample',
    [did_moc, did_src],
    dependencies: qtadvanceddocking_dep
)

