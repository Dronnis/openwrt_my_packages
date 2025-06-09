include $(TOPDIR)/rules.mk

PECL_NAME:=recursionguard
PECL_LONGNAME:=This extension lightweight PHP extension to hard-cap function call depth.

PKG_VERSION:=0.1.0
PKG_RELEASE:=1
PKG_HASH:=skip


PKG_NAME:=php8-pecl-$(PECL_NAME)
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/pmmp/ext-recursionguard.git
PKG_SOURCE_VERSION:=1a5c570119dade96a304d452600042d078cc5259
PKG_MIRROR_HASH:=1443b7183fa6bada80b7ae3630a21c9c0409df44f87a377e2c5799ed1934b3a5



PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/php8-pecl-$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--enable-recursionguard 


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME)))
$(eval $(call BuildPackage,$(PKG_NAME)))
