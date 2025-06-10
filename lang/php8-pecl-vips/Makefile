include $(TOPDIR)/rules.mk

PECL_NAME:=vips
PECL_LONGNAME:=PHP extension for interfacing with libvips

PKG_VERSION:=1.0.13
PKG_RELEASE:=1
PKG_HASH:=4e655843e5ee8150c927c10853dfa0d2a3b924bc2453ed8fb5e5a2a90e686f8f

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8 vips
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--with-vips="$(STAGING_DIR)/usr"


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+vips,30))
$(eval $(call BuildPackage,$(PKG_NAME)))
