# If the pyx file is a C++ file, we should specify that here.
set_source_files_properties(
  ${CYTHON_CMAKE_EXAMPLE_SOURCE_DIR}/src/c_ladoshki.pxd
  PROPERTIES CYTHON_IS_CXX TRUE )

# Multi-file cython modules do not appear to be working at the moment.
cython_add_module( ladoshki ladoshki.pyx /home/stas/workspace/ladoshki/ladoshki_cppserver/server.cxx )
