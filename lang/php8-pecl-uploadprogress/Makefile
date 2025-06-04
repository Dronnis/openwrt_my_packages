include $(TOPDIR)/rules.mk

PECL_NAME:=uploadprogress
PECL_LONGNAME:=PHP extension for interfacing with uploadprogress

PKG_VERSION:=2.0.2
PKG_RELEASE:=2
PKG_HASH:=2c63ce727340121044365f0fd83babd60dfa785fa5979fae2520b25dad814226

PKG_NAME:=php8-pecl-uploadprogress
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-uploadprogress

$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME), ,30))
$(eval $(call BuildPackage,$(PKG_NAME)))
