include $(TOPDIR)/rules.mk

PECL_NAME:=lzf
PECL_LONGNAME:=PHP extension for LZF compression.

PKG_VERSION:=1.7.0
PKG_RELEASE:=1
PKG_HASH:=f9a51510ab52da51c2b39ba9329036247a3784b3a32788cbf199326b90f8bc78

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE:=LZF-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=PHP License 3.01
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8 liblzf
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/LZF-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-lzf 


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+liblzf,30))
$(eval $(call BuildPackage,$(PKG_NAME)))
