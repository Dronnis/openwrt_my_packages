include $(TOPDIR)/rules.mk


PECL_NAME:=libdeflate
PECL_LONGNAME:=This extension for libdeflate, a zlib replacement with significantly better performance.

PKG_VERSION:=0.2.1
PKG_RELEASE:=1


PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/pmmp/ext-libdeflate.git
PKG_SOURCE_VERSION:=808da3ba16b835f4b69e7a558563abb0558840ad
PKG_MIRROR_HASH:=4ade1d59f6b4c12ece32fa2b85f1d0cf55fb95d5212235eb2e73880b280af98f


PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=MIT license
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8 libdeflate
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--with-libdeflate="$(STAGING_DIR)/usr"


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libdeflate))
$(eval $(call BuildPackage,$(PKG_NAME)))
