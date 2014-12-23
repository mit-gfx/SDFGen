
set(LIB_NAME SDFGen)

set(CPP_FILES
    makelevelset3.cpp
    )

set(PUBLIC_HEADERS
    array3.h
    vec.h
    makelevelset3.h
    )

set(PRIVATE_HEADERS
    array1.h
    array2.h
    hashgrid.h
    hashtable.h
    util.h
   )

set(PUBLIC_HEADER_DST_LOCATION "${OF_INST_INC_PATH}/${LIB_NAME}")

add_library(${LIB_NAME} SHARED ${CPP_FILES} ${PUBLIC_HEADERS} ${PRIVATE_HEADERS})
install(TARGETS ${LIB_NAME} DESTINATION ${OF_INST_LIB_PATH})
install(FILES ${PUBLIC_HEADERS} DESTINATION ${PUBLIC_HEADER_DST_LOCATION})
