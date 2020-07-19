#rexx ed25519 module CmakeLists.txt -- librexx_ed25519.a

set(LIB_REXX_ED25519 rexx_ed25519)
aux_source_directory(${REXX_SRC_DIR}/3rd/ed25519-donna/ ED25519_SRC)
add_library(${LIB_REXX_ED25519} ${ED25519_SRC})

target_compile_options(${LIB_REXX_ED25519}
	PUBLIC -DASIO_STANDALONE 
	PUBLIC -fPIC
)
