cmake_minimum_required (VERSION 2.8)

tycho_add_build_tool(lemon "")

add_custom_command(
        TARGET lemon POST_BUILD
        COMMAND ${CMAKE_COMMAND} -E copy
                ${CMAKE_CURRENT_SOURCE_DIR}/lempar.c.in
                $<TARGET_FILE_DIR:lemon>/lempar.c)

