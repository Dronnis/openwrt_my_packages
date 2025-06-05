include $(TOPDIR)/rules.mk

PECL_NAME:=simdutf
PECL_LONGNAME:=Unicode and Base64 routines at billions of characters per second in PHP using the simdutf library. Accelerates Unicode routines (UTF8, UTF16, UTF32) and Base64 using SSE2, AVX2, NEON, AVX-512, RISC-V Vector Extension, LoongArch64, etc.

PKG_VERSION:=1.0.0
PKG_RELEASE:=1
PKG_HASH:=skip


PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/awesomized/simdutf-php-ext.git
PKG_SOURCE_VERSION:=88b8d1bb5887b528aa0942b8a7ee2e73a8b6c387
PKG_MIRROR_HASH:=38ebbb4202a0643a3d639de4ef51b7403f547e6aec088181733fb6c16d972575
PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8 
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1
PKG_FIXUP:=patch-libtool


include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-simdutf

#define Build/InstallDev
	#mkdir -p $(STAGING_DIR)/usr/include/php8/ext/$(PECL_NAME)
	#cp $(PKG_BUILD_DIR)/php_phalcon.h $(STAGING_DIR)/usr/include/php8/ext/$(PECL_NAME)/
#endef

$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME), +libstdcpp,30))
$(eval $(call BuildPackage,$(PKG_NAME)))
