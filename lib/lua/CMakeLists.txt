
set ( LUA_SRC_CORE src/lapi.c src/lcode.c src/lctype.c src/ldebug.c src/ldo.c src/ldump.c src/lfunc.c src/lgc.c src/llex.c
  src/lmem.c src/lobject.c src/lopcodes.c src/lparser.c src/lstate.c src/lstring.c src/ltable.c
  src/ltm.c src/lundump.c src/lvm.c src/lzio.c )
set ( LUA_SRC_LIB src/lauxlib.c src/lbaselib.c src/lcorolib.c src/ldblib.c src/liolib.c
  src/lmathlib.c src/loslib.c src/lstrlib.c src/ltablib.c src/lutf8lib.c src/loadlib.c src/linit.c )

add_library ( liblua ${LUA_SRC_CORE} ${LUA_SRC_LIB} )
target_include_directories( liblua PUBLIC ${CMAKE_CURRENT_SOURCE_DIR}/src)

# add_library ( libluadll SHARED ${SRC_CORE} ${SRC_LIB} )
# target_compile_definitions ( libluadll PRIVATE _CRT_SECURE_NO_WARNINGS LUA_BUILD_AS_DLL )
# set_target_properties ( libluadll PROPERTIES OUTPUT_NAME lua53 )

# add_executable ( lua ${SRC_LUA} )
# target_link_libraries ( lua libluadll )

# add_executable ( luac ${SRC_LUAC} )
# target_link_libraries ( luac liblua )