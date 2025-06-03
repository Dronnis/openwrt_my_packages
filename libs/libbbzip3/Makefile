include $(TOPDIR)/rules.mk

PKG_NAME:=libbbzip3
PKG_VERSION:=1.5.2
PKG_RELEASE:=1

PKG_SOURCE:=bzip3-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/kspalaiologos/bzip3/releases/download/$(PKG_VERSION)/
PKG_HASH:=skip
PKG_BUILD_DIR:=$(BUILD_DIR)/bzip3-$(PKG_VERSION)

PKG_MAINTAINER:= Dronnis Marvel <dronnis@gmail.com>

PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/$(PKG_NAME)
	SECTION:=libs
	CATEGORY:=Libraries
	TITLE:=$(PKG_NAME)
	URL:=https://github.com/kspalaiologos/bzip3
	DEPENDS:=+libstdcpp
endef

define Package/bzip3
	SECTION:=tools
	CATEGORY:=compression
	TITLE:=bzip3
	URL:=https://github.com/kspalaiologos/bzip3
	DEPENDS:=+$(PKG_NAME)
endef
define Package/bzip3/description
	A better, faster and stronger spiritual successor to BZip2. Features higher compression ratios and better performance thanks to a order-0 context mixing entropy coder, a fast Burrows-Wheeler transform code making use of suffix arrays and a RLE with Lempel Ziv+Prediction pass based on LZ77-style string matching and PPM-style context modeling.
endef

define Package/$(PKG_NAME)/description
	A better, faster and stronger spiritual successor to BZip2. Features higher compression ratios and better performance thanks to a order-0 context mixing entropy coder, a fast Burrows-Wheeler transform code making use of suffix arrays and a RLE with Lempel Ziv+Prediction pass based on LZ77-style string matching and PPM-style context modeling.
endef

CMAKE_OPTIONS += \
	-DCMAKE_BUILD_TYPE=Release

define Build/InstallDev
	$(INSTALL_DIR) $(STAGING_DIR)/usr/lib/pkgconfig
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/pkgconfig/bzip3.pc $(STAGING_DIR)/usr/lib/pkgconfig/bzip3.pc
	$(INSTALL_DIR) $(1)/usr/include
	$(CP) $(PKG_INSTALL_DIR)/usr/include/libbz3.h $(1)/usr/include/libbz3.h
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libbzip3.* $(1)/usr/lib/
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libbzip3.* $(1)/usr/lib/
endef

define Package/bzip3/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(CP) $(PKG_INSTALL_DIR)/usr/bin/{bunzip3,bz3cat,bz3grep,bz3less,bz3more,bz3most,bzip3} $(1)/usr/bin/brotli
endef




$(eval $(call BuildPackage,$(PKG_NAME)))
