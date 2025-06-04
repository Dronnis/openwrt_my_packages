include $(TOPDIR)/rules.mk

PECL_NAME:=tinyexpr
PECL_LONGNAME:=PHP Extension TinyExpression Math evaluation for strings.

PKG_VERSION:=0.1.0
PKG_RELEASE:=1
PKG_HASH:=skip

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/MehrAlsNix/ext-tinyexpr.git
PKG_SOURCE_VERSION:=80b2a2375e442415310f82e8bffe93d049893fe9
PKG_MIRROR_HASH:=afc6a5dd1b724a6e03d654962c24917c161e6b1d5ce17628eec59be4072106a5

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=MIT license
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-tinyexpression

$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME)))

define Package/php8-pecl-tinyexpr/install
	$(INSTALL_DIR) $(1)/usr/lib/php8
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/modules/tinyexpression.so $(1)/usr/lib/php8/
	$(INSTALL_DIR) $(1)/etc/php8
	echo "extension=tinyexpression.so" > $(1)/etc/php8/20_tinyexpression.ini
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
