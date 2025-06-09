include $(TOPDIR)/rules.mk

PECL_NAME:=uopz
PECL_LONGNAME:=PHP extension for interfacing with uopz

PKG_VERSION:=7.1.1
PKG_RELEASE:=1

PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/krakjoe/uopz.git
PKG_SOURCE_VERSION:=b1015ae5e7ceb0cb879abd29e991723206a9e201
PKG_MIRROR_HASH:=275aaa5ce06c891c9f122f2def7195393a0f839877591863df03c8d2238de2e2
PKG_HASH:=skip


PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=PHP 3.01
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8
#PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1


include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--with-uopz-sanitize="no" \
	--enable-uopz

$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME)))
$(eval $(call BuildPackage,$(PKG_NAME)))
