
add_library(multiprocess_mod OBJECT multiprocess_memory_limit.cpp multiprocess_utilization_watcher.cpp)
target_compile_options(multiprocess_mod PUBLIC ${LIBRARY_COMPILE_FLAGS})
target_link_libraries(multiprocess_mod PUBLIC nvidia-ml)

add_executable(shrreg-tool shrreg_tool.cpp)
target_link_libraries(shrreg-tool multiprocess_mod -lpthread -lcuda)

