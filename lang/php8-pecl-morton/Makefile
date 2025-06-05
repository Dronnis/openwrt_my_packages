include $(TOPDIR)/rules.mk

PECL_NAME:=morton
PECL_LONGNAME:=This extension libmorton C++ library

PKG_VERSION:=0.1.2
PKG_RELEASE:=1
PKG_HASH:=skip


PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/pmmp/ext-morton.git
PKG_SOURCE_VERSION:=7fe332e3403fc2ee951967fecd9a933864acd238
PKG_MIRROR_HASH:=skip


PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=MIT license
PKG_LICENSE_FILES:=LICENSE

PKG_BUILD_DEPENDS:=php8 libstdcpp
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(INCLUDE_DIR)/uclibc++.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-morton 


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libstdcpp))
$(eval $(call BuildPackage,$(PKG_NAME)))
