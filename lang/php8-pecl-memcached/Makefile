include $(TOPDIR)/rules.mk

PECL_NAME:=memcached
PECL_LONGNAME:=PHP extension for interfacing with memcached

PKG_VERSION:=3.3.0
PKG_RELEASE:=2
PKG_HASH:=2b85bf6699497170801fb4d06eb9c9a06bfc551cdead04101dd75c980be9eebf

PKG_NAME:=php8-pecl-memcached
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=PHP License 3.01
PKG_LICENSE_FILES:=COPYING
 

PKG_BUILD_DEPENDS:=php8 php8-pecl-msgpack php8-pecl-igbinary zlib libmemcached php8-mod-session libzstd
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1
PKG_FIXUP:=patch-libtool

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-memcached \
    --with-libmemcached-dir="$(STAGING_DIR)/usr" \
    --enable-memcached-session \
    --enable-memcached-json \
    --enable-memcached-msgpack \
    --enable-memcached-igbinary \
    --enable-memcached-protocol \
    --disable-memcached-sasl \
    --with-zstd \
    --with-zlib-dir="$(STAGING_DIR)/usr" 
#    --with-system-fastlz 

$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME), +zlib +libmemcached +php8-mod-session +php8-pecl-msgpack +php8-pecl-igbinary +libzstd,30))
$(eval $(call BuildPackage,$(PKG_NAME)))


