if(CONFIG_PMW3610)
  # Add source directly to app target to ensure device init is linked
  target_sources(app PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/src/pmw3610.c)
  target_include_directories(app PRIVATE ${APPLICATION_SOURCE_DIR}/include)
else()
  zephyr_library()
  zephyr_include_directories(${APPLICATION_SOURCE_DIR}/include)
endif()
