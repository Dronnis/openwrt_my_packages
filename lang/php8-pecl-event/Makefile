include $(TOPDIR)/rules.mk

PECL_NAME:=event
PECL_LONGNAME:=PHP extension for provides interface to libevent library

PKG_VERSION:=3.1.4
PKG_RELEASE:=1
PKG_HASH:=5c4caa73bc2dceee31092ff9192139df28e9a80f1147ade0dfe869db2e4ddfd3

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8 libevent2
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk



CONFIGURE_ARGS+= \
	--with-event-core="$(STAGING_DIR)/usr" \
	--with-event-pthreads="$(STAGING_DIR)/usr" \
	--with-event-extra="$(STAGING_DIR)/usr" \
	--with-event-openssl="$(STAGING_DIR)/usr" \
	--with-openssl-dir="$(STAGING_DIR)/usr" \
	--with-event-libevent-dir="$(STAGING_DIR)/usr" \
	--enable-event-sockets


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libopenssl3 +libevent2 +libevent2-core +libevent2-extra +libevent2-openssl +libevent2-pthreads +php8-mod-sockets))
$(eval $(call BuildPackage,$(PKG_NAME)))
