if(IOS OR (NOT HAVE_HIP AND NOT BUILD_CUDA_STUBS))
  ocv_module_disable(cudabgsegm)
endif()

set(the_description "CUDA-accelerated Background Segmentation")

ocv_warnings_disable(CMAKE_CXX_FLAGS /wd4127 /wd4324 /wd4512 -Wundef -Wmissing-declarations -Wshadow)

ocv_define_module(cudabgsegm opencv_video WRAP python)
