include $(TOPDIR)/rules.mk

PECL_NAME:=json_post
PECL_LONGNAME:=This extension provides a PHP content type handler for "application/json" and "text/json" to PHP's form data parser. If the `Content-Type` of an incoming request is `text/json`, the JSON contents of the request body will by parsed into `$_POST`.

PKG_VERSION:=1.1.0
PKG_RELEASE:=2
PKG_HASH:=31af67f0f08e6a928750a3bff863d5caa5fbc29d3568d117d5a0e74857cde376

PKG_NAME:=php8-pecl-$(PECL_NAME)
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
	--enable-json-post


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME)))
$(eval $(call BuildPackage,$(PKG_NAME)))
