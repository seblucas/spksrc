PKG_NAME = lxml
PKG_VERS = 3.3.6
PKG_EXT = tar.gz
PKG_DIST_NAME = $(PKG_NAME)-$(PKG_VERS).$(PKG_EXT)
PKG_DIST_SITE = http://pypi.python.org/packages/source/l/$(PKG_NAME)
PKG_DIR = $(PKG_NAME)-$(PKG_VERS)

DEPENDS = cross/libxml2 cross/libxslt

HOMEPAGE = http://lxml.de/
COMMENT  = The lxml XML toolkit is a Pythonic binding for the C libraries libxml2 and libxslt
LICENSE  = BSD

BUILD_ARGS = --with-xslt-config=$(STAGING_INSTALL_PREFIX)/bin/xslt-config
ADDITIONAL_CFLAGS = -I $(STAGING_INSTALL_PREFIX)/include/libxml2
ifeq ($(findstring $(ARCH),88f5281),$(ARCH))
ADDITIONAL_CFLAGS += -O1
endif
#ADDITIONAL_CFLAGS = -I$(STAGING_INSTALL_PREFIX)/include/libxml2

include ../../mk/spksrc.python-module.mk
