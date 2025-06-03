include $(TOPDIR)/rules.mk

PECL_NAME:=cbor
PECL_LONGNAME:=CBOR codec extension for PHP

PKG_VERSION:=0.4.10
PKG_RELEASE:=1
PKG_HASH:=skip


PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/ranvis/php-ext-cbor.git
PKG_SOURCE_VERSION:=b185daa4b7c6fa80ab9a8f6f64e04906d952299f
PKG_MIRROR_HASH:=3e181ee9746c84cd15337d6d1040d16e84017151ddbed8ccefb40b3fea0d679a


PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=BSD-2-Clause license
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-cbor

$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME), ,30))
$(eval $(call BuildPackage,$(PKG_NAME)))
