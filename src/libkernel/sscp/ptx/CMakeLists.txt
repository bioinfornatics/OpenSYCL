
if(WITH_LLVM_TO_PTX)
  libkernel_generate_bitcode_target(
      TARGETNAME ptx 
      TRIPLE nvptx64-nvidia-cuda
      SOURCES atomic.cpp barrier.cpp core.cpp half.cpp integer.cpp relational.cpp math.cpp native.cpp localmem.cpp subgroup.cpp
      ADDITIONAL_ARGS -Xclang -target-feature -Xclang +sm_60)
endif()
