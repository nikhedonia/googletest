cxx_library(
  name = 'googletest',
  header_namespace = '',
  srcs = [
    'googletest/src/gtest-all.cc',
    'googletest/src/gtest_main.cc',
  ],
  headers = subdir_glob([
    ('googletest', 'src/*.h'),
    ('googletest', 'src/*.cc'),
    ('googletest/include', 'internal/**/*.h'),
  ]),
  exported_headers = subdir_glob([
    ('googletest/include', '**/*.h'),
  ], excludes = [
    'googletest/include/internal/**/*.h',
  ]),
  preprocessor_flags = [
    '-U_STRICT_ANSI_',
  ],
  compiler_flags = [
    '-std=c++14', 
  ],
  visibility = [
    'PUBLIC',
  ],
)

cxx_library(
  name = 'googlemock',
  header_namespace = '',
  srcs = [
    'googlemock/src/gmock-all.cc',
    'googlemock/src/gmock_main.cc',
  ],
  headers = subdir_glob([
    ('googlemock', 'src/*.h'),
    ('googlemock', 'src/*.cc'),
    ('googlemock/include', 'internal/**/*.h'),
  ]),
  exported_headers = subdir_glob([
    ('googlemock/include', '**/*.h'),
  ], excludes = [
    'googlemock/include/internal/**/*.h',
  ]),
  preprocessor_flags = [
    '-U_STRICT_ANSI_',
  ],
  compiler_flags = [
    '-std=c++14', 
  ],
  deps = [
    ':googletest',
  ],
  visibility = [
    'PUBLIC',
  ],
)
