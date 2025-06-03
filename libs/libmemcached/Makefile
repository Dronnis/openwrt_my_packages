include $(TOPDIR)/rules.mk

PKG_NAME:=libmemcached
PKG_VERSION:=1.1.4
PKG_RELEASE:=1

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/awesomized/libmemcached/tar.gz/$(PKG_VERSION)?
PKG_HASH:=c477e1f6510e1dc698e84f3717ce690a8f65b94c616ecaa62306cce0f5e3116a

PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>

PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/libmemcached
	SECTION:=libs
	CATEGORY:=Libraries
	TITLE:=libmemcached
	URL:=https://github.com/awesomized/libmemcached
	DEPENDS:=+libevent2 +libstdcpp
endef

define Package/libmemcached/description
	libMemcached is designed to provide the greatest number of options to use Memcached. Some of the features provided
endef

CMAKE_OPTIONS +=

define Build/InstallDev
	$(INSTALL_DIR) $(1)/usr/include
	$(CP) $(PKG_INSTALL_DIR)/usr/include/* $(1)/usr/include/
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libhashkit.* $(1)/usr/lib/
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libmemcachedprotocol.* $(1)/usr/lib/
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libmemcached.* $(1)/usr/lib/
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libmemcachedutil.* $(1)/usr/lib/
	$(INSTALL_DIR) $(1)/usr/lib/pkgconfig
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/pkgconfig/libmemcached.pc $(1)/usr/lib/pkgconfig/
	$(INSTALL_DIR) $(1)/usr/share/aclocal
	$(CP) $(PKG_INSTALL_DIR)/usr/share/aclocal/ax_libmemcached.m4 $(1)/usr/share/aclocal/
endef

define Package/libmemcached/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(CP) $(PKG_INSTALL_DIR)/usr/bin/* $(1)/usr/bin/
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libhashkit.* $(1)/usr/lib/
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libmemcached.* $(1)/usr/lib/
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libmemcachedutil.* $(1)/usr/lib/
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libmemcachedprotocol.* $(1)/usr/lib/
endef

$(eval $(call BuildPackage,libmemcached))
