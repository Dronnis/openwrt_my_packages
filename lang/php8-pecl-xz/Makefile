include $(TOPDIR)/rules.mk

PECL_NAME:=xz
PECL_LONGNAME:=This extension allows XZ (liblzma).

PKG_VERSION:=0.2.0
PKG_RELEASE:=1
PKG_HASH:=skip


PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/kjdev/php-ext-xz.git
PKG_SOURCE_VERSION:=ce135de88b54db4811a1aff567b6d54839bb7cae
PKG_MIRROR_HASH:=864d63a99a047eeb8cd72a662437bd8e025ba8903dedd66d8a9baab398e55466

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=MIT license
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8 liblzma
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-xz


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+liblzma))
$(eval $(call BuildPackage,$(PKG_NAME)))
