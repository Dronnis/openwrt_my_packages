include $(TOPDIR)/rules.mk

PECL_NAME:=xmldiff
PECL_LONGNAME:=PHP extension for XML diff and merge

PKG_VERSION:=1.1.5
PKG_RELEASE:=1
PKG_HASH:=57f9d99b6e4dab76a0552aeeec9dee6b272218b3fcf422a715e543f55c800f7d

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=BSD 2-clause
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8 libxml2 php8-mod-dom libstdcpp
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--with-xmldiff \
	--with-libxml-dir="$(STAGING_DIR)/usr" 


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libxml2 +php8-mod-dom +libstdcpp))
$(eval $(call BuildPackage,$(PKG_NAME)))
