include $(TOPDIR)/rules.mk

PKG_NAME:=libbrotli
PKG_VERSION:=1.1.0
PKG_RELEASE:=1

PKG_LICENSE:=MIT license


PKG_SOURCE_URL:=https://github.com/google/brotli.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=ed738e842d2fbdf2d6459e39267a633c4a9b2f5d
PKG_MIRROR_HASH:=skip
PKG_HASH:=skip


PKG_MAINTAINER:= Dronnis Marvel <dronnis@gmail.com>

PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/$(PKG_NAME)
	SECTION:=libs
	CATEGORY:=Libraries
	TITLE:=$(PKG_NAME)
	URL:=https://github.com/google/brotli
	DEPENDS:=+libstdcpp
endef

define Package/brotli
	SECTION:=utils
	CATEGORY:=Image
	TITLE:=brotli
	URL:=https://github.com/google/brotli
	DEPENDS:=+$(PKG_NAME)
endef
define Package/brotli/description
	Brunsli is a lossless JPEG repacking library.
endef
define Package/$(PKG_NAME)/description
	Brunsli is a lossless JPEG repacking library.
endef

CMAKE_OPTIONS += \
	-DCMAKE_BUILD_TYPE=Release

define Build/InstallDev
	$(INSTALL_DIR) $(STAGING_DIR)/usr/lib/pkgconfig
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/pkgconfig/{libbrotlicommon,libbrotlidec,libbrotlienc}.pc $(STAGING_DIR)/usr/lib/pkgconfig/
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/{libbrotlicommon.so,libbrotlidec.so,libbrotlienc.so} $(1)/usr/lib/
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/{libbrotlicommon.so,libbrotlidec.so,libbrotlienc.so}.1 $(1)/usr/lib/
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/{libbrotlicommon.so,libbrotlidec.so,libbrotlienc.so}.1.1.0 $(1)/usr/lib/
	$(INSTALL_DIR) $(1)/usr/include/brotli/
	$(CP) $(PKG_INSTALL_DIR)/usr/include/brotli/* $(1)/usr/include/brotli/
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/{libbrotlicommon.so,libbrotlidec.so,libbrotlienc.so} $(1)/usr/lib/
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/{libbrotlicommon.so,libbrotlidec.so,libbrotlienc.so}.1 $(1)/usr/lib/
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/{libbrotlicommon.so,libbrotlidec.so,libbrotlienc.so}.1.1.0 $(1)/usr/lib/
endef

define Package/brotli/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(CP) $(PKG_INSTALL_DIR)/usr/bin/brotli $(1)/usr/bin/brotli
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
$(eval $(call BuildPackage,brotli))