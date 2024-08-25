add_library(cuda_mod OBJECT context.cpp device.cpp hook.cpp event.cpp memory.cpp stream.cpp graph.cpp )
target_compile_options(cuda_mod PUBLIC ${LIBRARY_COMPILE_FLAGS})
target_link_libraries(cuda_mod PUBLIC nvidia-ml -lcuda)
