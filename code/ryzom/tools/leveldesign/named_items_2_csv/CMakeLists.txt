FILE(GLOB SRC *.cpp *.h)

ADD_EXECUTABLE(named2csv ${SRC})

TARGET_LINK_LIBRARIES(named2csv nelmisc)

NL_DEFAULT_PROPS(named2csv "Ryzom, Tools: Named Items to CSV")
NL_ADD_RUNTIME_FLAGS(named2csv)

INSTALL(TARGETS named2csv RUNTIME DESTINATION ${RYZOM_BIN_PREFIX} COMPONENT tools)
