include $(TOPDIR)/rules.mk

PKG_NAME:=librabbitmq
PKG_VERSION:=0.15.0
PKG_RELEASE:=1
PKG_MAINTAINER:=Dronnis Marvel <dronnis@gmail.com>
PKG_LICENSE:=MIT license
PKG_LICENSE_FILES:=COPYING
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/alanxz/rabbitmq-c/tar.gz/refs/tags/v$(PKG_VERSION)?
PKG_HASH:=skip
PKG_BUILD_DIR:=$(BUILD_DIR)/rabbitmq-c-$(PKG_VERSION)
PKG_FIXUP:=autoreconf
PKG_INSTALL:=1
PKG_BUILD_PARALLEL:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/$(PKG_NAME)
  SECTION:=libs
  CATEGORY:=Libraries
  TITLE:=$(PKG_NAME)
  URL:=$(PKG_SOURCE_URL)
  DEPENDS:=+libopenssl
endef

define Package/$(PKG_NAME)/description
 This is a C-language AMQP client library for use with v2.0+ of the RabbitMQ broker.
endef

define Build/InstallDev
	$(INSTALL_DIR) $(STAGING_DIR)/usr/include
	$(CP) $(PKG_INSTALL_DIR)/usr/include/{amqp,amqp_framing,amqp_ssl_socket,amqp_tcp_socket}.h $(STAGING_DIR)/usr/include/
	$(INSTALL_DIR) $(STAGING_DIR)/usr/include/rabbitmq-c
	$(CP) $(PKG_INSTALL_DIR)/usr/include/rabbitmq-c/{amqp,framing,ssl_socket,tcp_socket}.h $(STAGING_DIR)/usr/include/rabbitmq-c/
	$(INSTALL_DIR) $(STAGING_DIR)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/librabbitmq* $(STAGING_DIR)/usr/lib/
	$(INSTALL_DIR) $(STAGING_DIR)/usr/lib/pkgconfig
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/pkgconfig/librabbitmq.pc $(STAGING_DIR)/usr/lib/pkgconfig/librabbitmq.pc
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/lib
	$(CP) $(PKG_INSTALL_DIR)/usr/lib/librabbitmq.s* $(1)/usr/lib/
#	$(LN) $(PKG_INSTALL_DIR)/usr/lib/librabbitmq.so.$(PKG_VERSION) $(1)/usr/lib/librabbitmq.so.4
endef

$(eval $(call BuildPackage,$(PKG_NAME)))