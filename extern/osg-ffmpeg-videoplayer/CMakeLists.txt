set(OSG_FFMPEG_VIDEOPLAYER_LIBRARY "osg-ffmpeg-videoplayer")

# Sources

set(OSG_FFMPEG_VIDEOPLAYER_SOURCE_FILES
    videoplayer.cpp
    videostate.cpp
    videodefs.hpp
    libavwrapper.cpp
    audiodecoder.cpp
    audiofactory.hpp
)

include_directories(${FFMPEG_INCLUDE_DIRS})
add_library(${OSG_FFMPEG_VIDEOPLAYER_LIBRARY} STATIC ${OSG_FFMPEG_VIDEOPLAYER_SOURCE_FILES})
target_link_libraries(${OSG_FFMPEG_VIDEOPLAYER_LIBRARY} ${FFMPEG_LIBRARIES} ${Boost_THREAD_LIBRARY})

link_directories(${CMAKE_CURRENT_BINARY_DIR})
