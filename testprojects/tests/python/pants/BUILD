# Copyright 2019 Pants project contributors (see CONTRIBUTORS.md).
# Licensed under the Apache License, Version 2.0 (see LICENSE).

# An example of a BUILD file in a parent directory which shares source files with targets in
# subdirectories. Pants supports this, although some text editors such as IntelliJ will not allow a
# directory containing source files to be shared across more than one module when imported via the
# Pants IntelliJ plugin.
python_tests(
  name = 'secondary_source_file_owner',
  sources = ['dummies/test_pass.py'],
)

files(
  name = 'build_parsing_directory',
  sources = rglobs('build_parsing/*'),
)

files(
  name = 'conf_test_directory',
  sources = rglobs('conf_test/*'),
)

files(
  name = 'constants_only_directory',
  sources = rglobs('constants_only/*'),
  dependencies = [
    'testprojects/src/thrift/org/pantsbuild:constants_only_directory',
  ],
)

files(
  name = 'dummies_directory',
  sources = rglobs('dummies/*'),
)

files(
  name = 'file_sets_directory',
  sources = rglobs('file_sets/*'),
)

files(
  name = 'timeout_directory',
  sources = rglobs('timeout/*'),
)
