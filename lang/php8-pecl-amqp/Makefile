include $(TOPDIR)/rules.mk

PECL_NAME:=amqp
PECL_LONGNAME:=PHP extension for communicate with any AMQP compliant server

PKG_VERSION:=2.1.2
PKG_RELEASE:=1
PKG_HASH:=0cb16d63752a0055de55a22062a6c1744908696d92268d76181284669025d993

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=PHP License
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8 librabbitmq
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk


CONFIGURE_ARGS+= \
	--with-amqp 


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME), +librabbitmq))
$(eval $(call BuildPackage,$(PKG_NAME)))
