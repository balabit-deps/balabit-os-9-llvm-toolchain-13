add_mlir_dialect_library(MLIRAsyncTransforms
  AsyncParallelFor.cpp
  AsyncRuntimeRefCounting.cpp
  AsyncRuntimeRefCountingOpt.cpp
  AsyncToAsyncRuntime.cpp

  ADDITIONAL_HEADER_DIRS
  ${MLIR_MAIN_INCLUDE_DIR}/mlir/Dialect/Async

  DEPENDS
  MLIRAsyncPassIncGen

  LINK_LIBS PUBLIC
  MLIRIR
  MLIRAsync
  MLIRPass
  MLIRSCF
  MLIRSCFToStandard
  MLIRStandard
  MLIRTransforms
  MLIRTransformUtils
)
