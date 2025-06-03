include $(TOPDIR)/rules.mk

PECL_NAME:=yaml
PECL_LONGNAME:=PHP extension for interfacing with yaml

PKG_VERSION:=2.2.4
PKG_RELEASE:=2
PKG_HASH:=8eb353baf87f15b1b62ac6eb71c8b589685958a1fe8b0e3d22ac59560d0e8913

PKG_NAME:=php8-pecl-yaml
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=MIT
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8 yaml
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--with-yaml="$(STAGING_DIR)/usr" 

$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libyaml,30))
$(eval $(call BuildPackage,$(PKG_NAME)))
