add_library(wasmedgePluginTest
  SHARED
  testplugin.c
)

set_target_properties(wasmedgePluginTest PROPERTIES
  C_STANDARD 11
)

target_compile_options(wasmedgePluginTest
  PUBLIC
  -DWASMEDGE_PLUGIN
)

target_link_libraries(wasmedgePluginTest
  PRIVATE
  wasmedge
)
