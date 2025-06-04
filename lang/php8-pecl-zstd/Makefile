include $(TOPDIR)/rules.mk

PECL_NAME:=zstd
PECL_LONGNAME:=PHP extension allows Zstandard.

PKG_VERSION:=0.14.0
PKG_RELEASE:=1
PKG_HASH:=207a87de60e3a9eb7993d2fc1a2ce88f854330ef29d210f552a60eb4cf3db79c

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=MIT License
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8 zstd
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-zstd \
	--with-libzstd="$(STAGING_DIR)/usr"


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME), +libzstd))
$(eval $(call BuildPackage,$(PKG_NAME)))
