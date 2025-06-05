#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PECL_NAME:=raphf
PECL_LONGNAME:=A reusable split-off of pecl_http's persistent handle and resource factory API.

PKG_VERSION:=2.0.1
PKG_RELEASE:=1
PKG_HASH:=skip

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=BSD-2-Clause
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-raphf

define Build/InstallDev
	mkdir -p $(STAGING_DIR)/usr/include/php8/ext/raphf
	$(CP) $(PKG_BUILD_DIR)/php_raphf.h $(STAGING_DIR)/usr/include/php8/ext/raphf
	echo "extension=raphf.so" > $(STAGING_DIR)/etc/php8/20_raphf.ini
endef


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME)))
$(eval $(call BuildPackage,$(PKG_NAME)))
