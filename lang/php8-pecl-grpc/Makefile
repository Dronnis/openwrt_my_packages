include $(TOPDIR)/rules.mk

PECL_NAME:=grpc
PECL_LONGNAME:=PHP extension for interfacing with grpc

PKG_VERSION:=1.64.1
PKG_RELEASE:=2
PKG_HASH:=7eedbce54e29281d8fb97b0924e34d6cb315c5ba12e8a55706ccdde977497d43

PKG_NAME:=php8-pecl-grpc
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=Apache 2.0
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8 libstdcpp libpthread
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-grpc 

$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME), +libstdcpp +libpthread))
$(eval $(call BuildPackage,$(PKG_NAME)))
