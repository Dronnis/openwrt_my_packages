include $(TOPDIR)/rules.mk

PECL_NAME:=brotli
PECL_LONGNAME:=PHP extension for compression and decompression with Brotli library.

PKG_VERSION:=0.17.0
PKG_RELEASE:=1
PKG_HASH:=1f56c4580a644d40ed3e0658a90fb087098639a15ceaf297cdabd0a9d10884a9

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8 libbrotli
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-brotli \
	--with-libbrotli="$(STAGING_DIR)/usr"


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libbrotli,30))
$(eval $(call BuildPackage,$(PKG_NAME)))
