
set(NEOVIM_QT_SOURCES util.cpp neovimconnector.cpp neovimconnectorhelper.cpp function.cpp msgpackrequest.cpp auto/neovim.cpp msgpackiodevice.cpp)
add_library(neovim-qt STATIC ${NEOVIM_QT_SOURCES})
target_link_libraries(neovim-qt Qt5::Network ${MSGPACK_LIBRARIES})

add_subdirectory(gui)
