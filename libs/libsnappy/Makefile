include $(TOPDIR)/rules.mk

PKG_NAME:=libsnappy
PKG_VERSION:=1.2.2
PKG_RELEASE:=1

PKG_LICENSE:=MIT license


PKG_SOURCE_URL:=https://github.com/google/snappy.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=6af9287fbdb913f0794d0148c6aa43b58e63c8e3
PKG_MIRROR_HASH:=4a1f1cad202c1432d7b3c2067d98086db22404e84ec098ec1dd38fdc260101d0


PKG_MAINTAINER:= Dronnis Marvel <dronnis@gmail.com>

PKG_INSTALL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/$(PKG_NAME)
	SECTION:=libs
	CATEGORY:=Libraries
	TITLE:=$(PKG_NAME)
	URL:=https://github.com/google/snappy
	DEPENDS:=+libstdcpp
endef

define Package/$(PKG_NAME)/description
	Snappy, a fast compressor/decompressor.
endef

CMAKE_OPTIONS += \
	-DCMAKE_BUILD_TYPE=Release \
	-DBUILD_SHARED_LIBS=YES \
	-DSNAPPY_BUILD_TESTS=NO \
	-DSNAPPY_BUILD_BENCHMARKS=NO \
	-DSNAPPY_REQUIRE_AVX=YES \
	-DSNAPPY_REQUIRE_AVX2=YES

define Build/InstallDev
	$(INSTALL_DIR) $(1)/usr/include/
	$(CP) $(PKG_INSTALL_DIR)/usr/include/* $(1)/usr/include/
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libsnappy* $(1)/usr/lib/
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/libsnappy* $(1)/usr/lib/
endef


$(eval $(call BuildPackage,$(PKG_NAME)))