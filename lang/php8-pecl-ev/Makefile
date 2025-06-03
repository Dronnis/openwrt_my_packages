include $(TOPDIR)/rules.mk

PECL_NAME:=ev
PECL_LONGNAME:=PHP extension for interfacing with ev

PKG_VERSION:=1.2.0
PKG_RELEASE:=2
PKG_HASH:=6fd80e3cf55c6fbc57a9045c8b738120c794662c9226f8de4837097ba36d03b9

PKG_NAME:=php8-pecl-ev
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8 libev
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-ev

$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libev,30))
$(eval $(call BuildPackage,$(PKG_NAME)))
