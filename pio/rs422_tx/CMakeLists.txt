add_executable(rs422_tx)

pico_generate_pio_header(rs422_tx ${CMAKE_CURRENT_LIST_DIR}/rs422_tx.pio)

target_sources(rs422_tx PRIVATE rs422_tx.c)

target_link_libraries(rs422_tx PRIVATE pico_stdlib hardware_pio)
pico_add_extra_outputs(rs422_tx)

# add url via pico_set_program_url
example_auto_set_url(rs422_tx)
