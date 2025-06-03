include $(TOPDIR)/rules.mk


PECL_NAME:=dotenv
PECL_LONGNAME:=A PHP extension that sets environment variables from a file on request startup.

PKG_VERSION:=0.0.1
PKG_RELEASE:=1
PKG_HASH:=skip


PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/sjinks/php-ext-dotenv.git
PKG_SOURCE_VERSION:=3ad8a0f1d741401a39c4624cc45d8cba90ac42c8
PKG_MIRROR_HASH:=81572a6ac4796e31f7c3d5ccdce015b91e13bb8c281546b859422df974de957d


PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=MIT license
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-dotenv


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME)))
$(eval $(call BuildPackage,$(PKG_NAME)))
