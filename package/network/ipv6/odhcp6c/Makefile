#
# Copyright (C) 2012 OpenWrt.org
#
# This is free software, licensed under the GNU General Public License v2.
# See /LICENSE for more information.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=odhcp6c
PKG_VERSION:=2013-01-02
PKG_RELEASE=$(PKG_SOURCE_VERSION)

PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION).tar.bz2
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)
PKG_SOURCE_URL:=git://github.com/sbyx/odhcp6c.git
PKG_SOURCE_PROTO:=git
PKG_SOURCE_VERSION:=ee149f5fe141ca6c34d562e26ab7300a644ee7b0
PKG_MAINTAINER:=Steven Barth <steven@midlink.org>

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/odhcp6c
  SECTION:=ipv6
  CATEGORY:=IPv6
  TITLE:=Embedded DHCPv6-client for OpenWrt
  DEPENDS:=+kmod-ipv6
endef

define Package/odhcp6c/install
	$(INSTALL_DIR) $(1)/usr/sbin/
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/odhcp6c $(1)/usr/sbin/
endef

$(eval $(call BuildPackage,odhcp6c))
