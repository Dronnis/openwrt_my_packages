include $(TOPDIR)/rules.mk


PECL_NAME:=bsdiff
PECL_LONGNAME:=PHP extension to build and apply patches to binary files.

PKG_VERSION:=0.1.2
PKG_RELEASE:=1
PKG_HASH:=283f40aec16895f602d5053c74c6c4769f150ca252995c5866e7dd7e1d11bc45

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=PHP License
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8 bzip2
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-bsdiff \
	--with-bz2="$(STAGING_DIR)/usr"



$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libbz2,30))
$(eval $(call BuildPackage,$(PKG_NAME)))
