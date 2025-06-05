include $(TOPDIR)/rules.mk

PKG_NAME:=libmd4c
PKG_VERSION:=0.5.2
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://github.com/mity/md4c.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=729e6b8b320caa96328968ab27d7db2235e4fb47
PKG_MIRROR_HASH:=bc7bdde89fe85ce4a03d374936f6ce61b171408135f64803d2d9fc9e6c0b63a9


PKG_INSTALL:=1

PKG_MAINTAINER:= Dronnis Marvel <dronnis@gmail.com>
CMAKE_OPTIONS += \
	-DCMAKE_BUILD_TYPE=Release

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/$(PKG_NAME)
	SECTION:=libs
	CATEGORY:=Libraries
	TITLE:=$(PKG_NAME)
	URL:=https://github.com/mity/md4c
	DEPENDS:=+libstdcpp
endef

define Package/$(PKG_NAME)/description
	MD4C stands for "Markdown for C" and that's exactly what this project is about.
endef

define Package/$(PKG_NAME)
	SECTION:=libs
	CATEGORY:=Libraries
	TITLE:=$(PKG_NAME)
	URL:=https://github.com/mity/md4c
	DEPENDS:=+libstdcpp
endef


define Package/md2html
	SECTION:=utils
	CATEGORY:=converter
	TITLE:=md2html
	URL:=https://github.com/mity/md4c
	DEPENDS:=+libmd4c
endef
define Package/md2html/description
	md to html converter
endef
define Package/md2html/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(CP) $(PKG_INSTALL_DIR)/usr/bin/md2html $(1)/usr/bin/md2html
endef

define Build/InstallDev
	$(INSTALL_DIR) $(1)/usr/bin
	$(CP) $(PKG_INSTALL_DIR)/usr/bin/md2html $(1)/usr/bin/md2html

	$(INSTALL_DIR) $(1)/usr/include/
	$(CP) $(PKG_INSTALL_DIR)/usr/include/{md4c.h,md4c-html.h} $(1)/usr/include

	$(INSTALL_DIR) $(1)/usr/lib/
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libmd4c* $(1)/usr/lib/

	$(INSTALL_DIR) $(1)/usr/lib/pkgconfig/
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/pkgconfig/* $(1)/usr/lib/pkgconfig/
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/lib/
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libmd4c* $(1)/usr/lib/
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
$(eval $(call BuildPackage,md2html))

