include $(TOPDIR)/rules.mk

PKG_NAME:=syslogfc
PKG_RELEASE:=1
PKG_VERSION:=0.9.5
PKG_RELEASE:=1
PKG_HASH:=skip

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/namedun/syslog_fc.git
PKG_SOURCE_VERSION:=873ae0a6224e9b2829507966545be2e438f3a9d4
PKG_MIRROR_HASH:=skip

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>
PKG_LICENSE:=WTFPL license
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_FLAGS:=no-lto

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/$(PKG_NAME)
	SECTION:=utils
	CATEGORY:=Utilities
	TITLE:=Syslog File Converter (syslog_fc)
	URL:=https://github.com/namedun/syslog_fc.git
	DEPENDS:=$(DRV_DEPENDS) 
endef

define Package/$(PKG_NAME)/description
  This utility is designed to convert syslog files to various other text formats, such as CSV, HTML or JSON.
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_INSTALL_DIR)/usr/bin/syslog_fc $(1)/usr/bin/
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
