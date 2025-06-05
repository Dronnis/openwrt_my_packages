include $(TOPDIR)/rules.mk

PKG_NAME:=libxdiff
PKG_VERSION:=0.23
PKG_RELEASE:=1

PKG_SOURCE_URL:=https://github.com/MentalPower/libxdiff.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=a84620f20cb33caa8d06a3ac399feac5207e8ed9
PKG_MIRROR_HASH:=3ac935a3970c7f45eb918feb030c8999b4c87188921e40e2c99889e9781c2f8a

PKG_MAINTAINER:= Dronnis Marvel <dronnis@gmail.com>

PKG_INSTALL:=1
PKG_FIXUP:=autoreconf

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
	SECTION:=libs
	CATEGORY:=Libraries
	TITLE:=$(PKG_NAME)
	URL:=https://github.com/MentalPower/libxdiff
	DEPENDS:=+libstdcpp
endef

define Package/$(PKG_NAME)/description
	The LibXDiff library implements basic and yet complete functionalities to create file differences/patches to both binary and text files.
endef


define Build/InstallDev
	$(INSTALL_DIR) $(1)/usr/include
	$(CP) $(PKG_INSTALL_DIR)/usr/include/xdiff.h $(1)/usr/include/
	$(INSTALL_DIR) $(1)/usr/lib 
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libxdiff* $(1)/usr/lib/
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/lib 
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libxdiff.s* $(1)/usr/lib/
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
