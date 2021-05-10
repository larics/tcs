set(SUBSYS_NAME hungarian)

set(HUNGARIAN_SOURCE_DIR ${PROJECT_SOURCE_DIR}/third-party/hungarian-v2.0)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_CXX_EXTENSIONS OFF)

include_directories(${PROJECT_SOURCE_DIR}/include/${SUBSYS_NAME})
include_directories(${HUNGARIAN_SOURCE_DIR})

add_library(hungarian
  hungarian.cpp
  ${HUNGARIAN_SOURCE_DIR}/Assignment.cpp
  ${HUNGARIAN_SOURCE_DIR}/BipartiteGraph.cpp
  ${HUNGARIAN_SOURCE_DIR}/Hungarian.cpp
  ${HUNGARIAN_SOURCE_DIR}/PlotGraph.cpp
  ${HUNGARIAN_SOURCE_DIR}/plot/Cgnuplot.cpp
  ${HUNGARIAN_SOURCE_DIR}/plot/graph_hungarian.cpp
)
