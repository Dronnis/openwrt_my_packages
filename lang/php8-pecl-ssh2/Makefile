include $(TOPDIR)/rules.mk

PECL_NAME:=ssh2
PECL_LONGNAME:=PHP extension bindings for the libssh2 library

PKG_VERSION:=1.4.1
PKG_RELEASE:=1
PKG_HASH:=7bca5b23f731db9d8ed0aea5db9bb15da8ff133b0fbba96102b82e95da4d8764

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=PHP License
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8 libssh2
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--with-ssh2="$(STAGING_DIR)/usr"

$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libssh2,30))
$(eval $(call BuildPackage,$(PKG_NAME)))
