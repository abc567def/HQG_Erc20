#rexx http module CmakeLists.txt -- librexx_http.a

set(LIB_REXX_HTTP rexx_http)
aux_source_directory(${REXX_SRC_DIR}/3rd/http/ HTTP_SRC)

add_library(${LIB_REXX_HTTP} ${HTTP_SRC})

target_compile_options(${LIB_REXX_HTTP}
    PUBLIC -std=c++11 
    PUBLIC -DASIO_STANDALONE
    PUBLIC -D${OS_NAME}
)
