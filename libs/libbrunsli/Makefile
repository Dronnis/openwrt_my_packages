include $(TOPDIR)/rules.mk

PKG_NAME:=libbrunsli
PKG_VERSION:=0.0.1
PKG_RELEASE:=1

#PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://github.com/google/brunsli.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=cbbc39ada0600725a82f25f142352143ebb2763d
PKG_MIRROR_HASH:=skip
PKG_HASH:=skip


PKG_MAINTAINER:= Dronnis Marvel <dronnis@gmail.com>

PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/libbrunsli
	SECTION:=libs
	CATEGORY:=Libraries
	TITLE:=libbrunsli
	URL:=https://github.com/google/brunsli
	DEPENDS:=+libstdcpp
endef

define Package/libbrunsli/description
	Brunsli is a lossless JPEG repacking library.
endef

CMAKE_OPTIONS += \
	-DCMAKE_BUILD_TYPE=Release

define Build/InstallDev
	$(INSTALL_DIR) $(1)/usr/include
	$(CP) $(PKG_INSTALL_DIR)/usr/include/* $(1)/usr/include/
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libbrunslidec-c.so $(1)/usr/lib/
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libbrunslienc-c.so $(1)/usr/lib/
endef

define Package/libbrunsli/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libbrunslidec-c.so $(1)/usr/lib/
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libbrunslienc-c.so $(1)/usr/lib/
endef

$(eval $(call BuildPackage,libbrunsli))
