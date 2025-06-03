include $(TOPDIR)/rules.mk

PECL_NAME:=snowflake
PECL_LONGNAME:=The extension implements a PHP extension for a distributed unique ID generator using the Snowflake algorithm. It can generate globally unique and ordered IDs.

PKG_VERSION:=1.2
PKG_RELEASE:=1
PKG_HASH:=skip


PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/wxxiong6/php-ext-snowflake.git
PKG_SOURCE_VERSION:=68f5ba9d591049625dbe489be59138dc1a4f8b8a
PKG_MIRROR_HASH:=215eb4b4aa6b0f12efa43ead4cd1edf4e274bc9aa26f79a004a0ac5291292611

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=PHP License 3.01
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-snowflake


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME)))
$(eval $(call BuildPackage,$(PKG_NAME)))
