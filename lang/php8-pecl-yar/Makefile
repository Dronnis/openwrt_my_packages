include $(TOPDIR)/rules.mk

PECL_NAME:=yar
PECL_LONGNAME:=PHP extension for light, concurrent RPC framework

PKG_VERSION:=2.3.3
PKG_RELEASE:=1
PKG_HASH:=e5951c7ac813dbd7dcb5738aa33b74ccdeba8a302a0649cd48affa263017b93a

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=PHP
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8 php8-pecl-msgpack
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-yar \
	--with-curl="$(STAGING_DIR)/usr" \
	--enable-msgpack \
	--enable-epoll 





$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libcurl +php8-pecl-msgpack))
$(eval $(call BuildPackage,$(PKG_NAME)))
