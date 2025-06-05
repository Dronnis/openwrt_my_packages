include $(TOPDIR)/rules.mk

PECL_NAME:=xdiff
PECL_LONGNAME:=PHP extension for file differences/patches.

PKG_VERSION:=2.1.1
PKG_RELEASE:=1
PKG_HASH:=c8d37e298ad317d89dd717d08093c9669fef97e511b119412ddbbe78189b6c7c

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=PHP License
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8 libxdiff
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--with-xdiff="$(STAGING_DIR)/usr" 



$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libxdiff))
$(eval $(call BuildPackage,$(PKG_NAME)))
