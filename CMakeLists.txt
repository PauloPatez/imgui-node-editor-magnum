set(IMGUI_NODE_EDITOR_ROOT_DIR ${CMAKE_CURRENT_LIST_DIR})

set(_imgui_node_editor_Sources
    ${IMGUI_NODE_EDITOR_ROOT_DIR}/crude_json.cpp
    ${IMGUI_NODE_EDITOR_ROOT_DIR}/crude_json.h
    ${IMGUI_NODE_EDITOR_ROOT_DIR}/imgui_bezier_math.h
    ${IMGUI_NODE_EDITOR_ROOT_DIR}/imgui_bezier_math.inl
    ${IMGUI_NODE_EDITOR_ROOT_DIR}/imgui_canvas.cpp
    ${IMGUI_NODE_EDITOR_ROOT_DIR}/imgui_canvas.h
    ${IMGUI_NODE_EDITOR_ROOT_DIR}/imgui_extra_math.h
    ${IMGUI_NODE_EDITOR_ROOT_DIR}/imgui_extra_math.inl
    ${IMGUI_NODE_EDITOR_ROOT_DIR}/imgui_node_editor_api.cpp
    ${IMGUI_NODE_EDITOR_ROOT_DIR}/imgui_node_editor_internal.h
    ${IMGUI_NODE_EDITOR_ROOT_DIR}/imgui_node_editor_internal.inl
    ${IMGUI_NODE_EDITOR_ROOT_DIR}/imgui_node_editor.cpp
    ${IMGUI_NODE_EDITOR_ROOT_DIR}/imgui_node_editor.h
)
add_library(imgui_node_editor STATIC
    ${_imgui_node_editor_Sources}
)

target_link_libraries(imgui_node_editor PUBLIC 
    MagnumIntegration::ImGui
)

# source_group(TREE ${IMGUI_NODE_EDITOR_ROOT_DIR} FILES ${_imgui_node_editor_Sources})

# include(${CMAKE_ROOT}/Modules/FindPackageHandleStandardArgs.cmake)

