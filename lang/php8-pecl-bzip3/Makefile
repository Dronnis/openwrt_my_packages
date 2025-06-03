include $(TOPDIR)/rules.mk

PECL_NAME:=bzip3
PECL_LONGNAME:=This extension allows Bzip3 compression.

PKG_VERSION:=0.1.1
PKG_RELEASE:=1
PKG_HASH:=skip


PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/kjdev/php-ext-bzip3.git
PKG_SOURCE_VERSION:=f2f1ca5bdb002adece623829adb886ba449ed08b
PKG_MIRROR_HASH:=9f8d46fdbb5f678be976fba4c7efc46a588c2a29c03d1af6768f0493baeca5fc


PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=MIT license
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8 libbbzip3
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-bzip3 \
	--with-libbzip3="$(STAGING_DIR)/usr"


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME), +libbbzip3 ,30))
$(eval $(call BuildPackage,$(PKG_NAME)))
