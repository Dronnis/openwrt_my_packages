include $(TOPDIR)/rules.mk

PECL_NAME:=qrencode
PECL_LONGNAME:=This extension wrapper of libqrencode to generate qr code.

PKG_VERSION:=0.8.0
PKG_RELEASE:=1

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/vanillahsu/pecl-qrencode.git
PKG_SOURCE_VERSION:=6ff1906167e43aab445406e05333ac393c7f0be2
PKG_MIRROR_HASH:=3356876d6c896d686997d6952865e3ad5325a95fd9498b142a67559c845ec65c


PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8 libqrencode libpng
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--with-qrencode="$(STAGING_DIR)/usr"


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libqrencode +libpng))
$(eval $(call BuildPackage,$(PKG_NAME)))
