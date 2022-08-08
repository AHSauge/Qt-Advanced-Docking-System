
ads_moc_input = [
  'DockAreaTabBar.h',
  'DockAreaTitleBar.h',
  'DockAreaTitleBar_p.h',
  'DockAreaWidget.h',
  'DockContainerWidget.h',
  'DockFocusController.h',
  'DockManager.h',
  'DockOverlay.h',
  'DockSplitter.h',
  'DockWidget.h',
  'DockWidgetTab.h',
  'ElidingLabel.h',
  'FloatingDockContainer.h',
  'FloatingDragPreview.h',
  'linux/FloatingWidgetTitleBar.h',
]

ads_cpp = qt.compile_resources(sources: ['ads.qrc'])
ads_moc = qt.compile_moc(
  headers: ads_moc_input,
  dependencies: qt_dep,
  extra_args: moc_args)

qtadvanceddocking_inc = include_directories('.')

qtadvanceddocking_src = files(
  'ads_globals.cpp',
  'DockAreaTabBar.cpp',
  'DockAreaTitleBar.cpp',
  'DockAreaWidget.cpp',
  'DockContainerWidget.cpp',
  'DockManager.cpp',
  'DockOverlay.cpp',
  'DockSplitter.cpp',
  'DockWidget.cpp',
  'DockWidgetTab.cpp',
  'DockingStateReader.cpp',
  'DockFocusController.cpp',
  'ElidingLabel.cpp',
  'FloatingDockContainer.cpp',
  'FloatingDragPreview.cpp',
  'IconProvider.cpp',
  'DockComponentsFactory.cpp',
  'linux/FloatingWidgetTitleBar.cpp',
)

qtadvanceddocking = both_libraries(
  'qtadvanceddocking',
  [ads_cpp, ads_moc, qtadvanceddocking_src],
  install : true,
  cpp_args: ['-DADS_SHARED_EXPORT'],
  dependencies: lib_deps
)

qtadvanceddocking_dep = declare_dependency(
  link_with : qtadvanceddocking,
  include_directories: qtadvanceddocking_inc,
  dependencies: lib_deps
)