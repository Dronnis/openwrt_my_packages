include $(TOPDIR)/rules.mk

PECL_NAME:=gnupg
PECL_LONGNAME:=PHP extension wrapper around the gpgme library

PKG_VERSION:=1.5.2
PKG_RELEASE:=2
PKG_HASH:=ad57aa23b3aef550fa4deddd003ff5322b886d55a67d1b020f5682ab829809fd

PKG_NAME:=php8-pecl-gnupg
PKG_SOURCE:=$(PECL_NAME)-$(PKG_VERSION).tgz
PKG_SOURCE_URL:=http://pecl.php.net/get/

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_LICENSE:=BSD-3-Clause
PKG_LICENSE_FILES:=COPYING

PKG_BUILD_DEPENDS:=php8 libgpgme
PKG_BUILD_DIR:=$(BUILD_DIR)/pecl-php8/$(PECL_NAME)-$(PKG_VERSION)
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/nls.mk
include $(TOPDIR)/package/feeds/packages/php8/pecl.mk

CONFIGURE_ARGS+= \
	--with-gnupg="$(STAGING_DIR)/usr" 


$(eval $(call PHP8PECLPackage,$(PECL_NAME),$(PECL_LONGNAME), +libgpgme))
$(eval $(call BuildPackage,$(PKG_NAME)))
