include $(TOPDIR)/rules.mk

PECL_NAME:=seaslog
PECL_LONGNAME:=PHP extension for an effective,fast,stable log extension for PHP.

PKG_VERSION:=2.2.0
PKG_RELEASE:=1
PKG_HASH:=e40a1067075b1e0bcdfd5ff98647b9f83f502eb6b2a3d89e67b067704ea127da

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE:=SeasLog-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=PHP 3.01
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8 libstdcpp
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/SeasLog-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--with-seaslog


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME), +libstdcpp))
$(eval $(call BuildPackage,$(PKG_NAME)))
