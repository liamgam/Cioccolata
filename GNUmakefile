include $(GNUSTEP_MAKEFILES)/common.make

CIOCCOLATA_ROOT_DIR = $(abspath .)

GNUSTEP_BUILD_DIR = ${CIOCCOLATA_ROOT_DIR}/build/GNUstep
GNUSTEP_INSTALLATION_DIR = @executable_path/../Frameworks

PACKAGE_NAME = Cioccolata
FRAMEWORK_NAME = Cioccolata

Cioccolata_NEEDS_GUI = no
Cioccolata_OBJC_FILES = \
	CTFastCGIAcceptLoop.m \
	CTFastCGIAcceptWorkerThread.m \
	CTFastCGIAcceptWorkerOperation.m \
	CTRequest.m \
	CTRequest+FCGX.m

Cioccolata_HEADER_FILES = \
	CTFastCGIAcceptLoop.h \
	NSThread+GNUStep.h \
	Cioccolata.h

Cioccolata_OBJC_PRECOMPILED_HEADERS = Cioccolata_Prefix.h

ADDITIONAL_OBJCFLAGS += -include Cioccolata_Prefix.h -Winvalid-pch -std=gnu99
ADDITIONAL_LDFLAGS += -install_name @executable_path/../Frameworks/Cioccolata.framework/Cioccolata

LIBRARIES_DEPEND_UPON = -lfcgi

GUI_LIB = no

include $(GNUSTEP_MAKEFILES)/framework.make
