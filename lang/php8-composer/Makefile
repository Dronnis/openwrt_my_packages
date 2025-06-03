include $(TOPDIR)/rules.mk

PKG_NAME:=php8-composer
PKG_VERSION:=2.8.9
PKG_RELEASE:=1
COMPOSER_FILE=composer.phar-$(PKG_VERSION)

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
	MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>
	PKGARCH:=all
	SUBMENU:=PHP8
	SECTION:=lang
	CATEGORY:=Languages
	TITLE:=PHP8 Composer
	URL:=https://getcomposer.org/
	DEPENDS:=php8 unzip
endef

define Download/composer
	FILE=$(COMPOSER_FILE)
	URL_FILE=composer.phar
	URL=https://github.com/composer/composer/releases/download/$(PKG_VERSION)/
	HASH:=8e8829ec2b97fcb05158236984bc252bef902e7b8ff65555a1eeda4ec13fb82b
endef

define Build/Prepare
   $(eval $(call Download,composer))
endef

define Build/Compile
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/sbin $(1)/usr/lib $(1)/usr/lib/php8-composer
	$(INSTALL_BIN) ./files/composer $(1)/usr/sbin/composer
	$(LN) $(1)/usr/sbin/composer $(1)/usr/sbin/composer.phar
	$(INSTALL_DATA) $(DL_DIR)/$(COMPOSER_FILE) $(1)/usr/lib/php8-composer/composer.phar
endef

$(eval $(call BuildPackage,$(PKG_NAME)))































