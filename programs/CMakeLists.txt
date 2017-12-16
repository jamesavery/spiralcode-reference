set(PROGRAMS spiral-to-graph spiral-to-polyhedron graph-to-spiral spiral-examples planarcodes-to-spirals)

foreach(program ${PROGRAMS})
  set(program_source ${program}.cc)
  add_executable(${program} ${program_source})
  target_link_libraries(${program} libgraph ${libs})
endforeach(program ${PROGRAMS})

