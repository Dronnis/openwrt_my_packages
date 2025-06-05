include $(TOPDIR)/rules.mk


PECL_NAME:=encoding
PECL_LONGNAME:=High-performance `ByteBuffer` implementation for PHP, planned for use in a future version of PocketMine-MP

PKG_VERSION:=0.3.0
PKG_RELEASE:=1
PKG_HASH:=skip


PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/pmmp/ext-encoding.git
PKG_SOURCE_VERSION:=324d6a3d45181839cf8e6887d913a59c6a932d87
PKG_MIRROR_HASH:=1280478c42a0008d8a118dd41b539c44a9f67f254acb93f0dabef0ff97199a46
PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>
PKG_BUILD_DEPENDS:=php8 libstdcpp
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1
PKG_FIXUP:=patch-libtool

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-encoding


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME),+libstdcpp))
$(eval $(call BuildPackage,$(PKG_NAME)))
