include $(TOPDIR)/rules.mk

PECL_NAME:=brunsli
PECL_LONGNAME:=PHP extension for interfacing with google libbrunsli

PKG_VERSION:=0.0.1
PKG_RELEASE:=1
PKG_HASH:=skip

PKG_NAME:=php8-pecl-brunsli
PKG_SOURCE_URL:=https://github.com/kjdev/php-ext-brunsli.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=cc4dc2aab656acbb1b4792c29128ca6cae9a409d
PKG_MIRROR_HASH:=405a9093b5ae9949fa84b632b1554ee49c1127679ffc994462afb61f0a3cb8c8
PKG_SOURCE_DATE:=2020-08-26


PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=XZ
PKG_LICENSE_FILES:=README.md

PKG_BUILD_DEPENDS:=php8 libbrunsli
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-brunsli-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--with-brunsli="$(STAGING_DIR)/usr" 

$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libbrunsli,30))
$(eval $(call BuildPackage,$(PKG_NAME)))
