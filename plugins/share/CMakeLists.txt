option(EMAIL "Enable Email plugin" ON)
option(INSTAPAPER "Enable Instapaper plugin" ON)
option(POCKET "Enable Pocket plugin" ON)
option(TWITTER "Enable Twitter plugin" ON)
option(WALLABAG "Enable Wallabag plugin" ON)


MESSAGE(STATUS "Plugin EMAIL:	" ${EMAIL})
MESSAGE(STATUS "Plugin INSTAPAPER:	" ${INSTAPAPER})
MESSAGE(STATUS "Plugin POCKET:	" ${POCKET})
MESSAGE(STATUS "Plugin TWITTER:	" ${TWITTER})
MESSAGE(STATUS "Plugin WALLABAG:	" ${WALLABAG})

if(EMAIL)
	add_subdirectory(Email)
endif(EMAIL)

if(INSTAPAPER)
	add_subdirectory(Instapaper)
endif(INSTAPAPER)

if(POCKET)
	add_subdirectory(Pocket)
endif(POCKET)

if(TWITTER)
	add_subdirectory(Twitter)
endif(TWITTER)

if(WALLABAG)
	add_subdirectory(Wallabag)
endif(WALLABAG)
