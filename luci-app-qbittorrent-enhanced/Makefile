# SPDX-License-Identifier: Apache-2.0
#
# Copyright (C) 2023 ImmortalWrt.org

include $(TOPDIR)/rules.mk

PKG_NAME:=luci-app-qbittorrent-enhanced
PKG_VERSION:=1.0.1
PKG_RELEASE:=1

LUCI_TITLE:=LuCI app for qBittorrent Enhanced Edition
LUCI_DEPENDS:= \
	+PACKAGE_QBITTORRENT_ENHANCED:qBittorrent-Enhanced-Edition \
	+PACKAGE_QBITTORRENT_ENHANCED_STATIC:qBittorrent-Enhanced-Edition_static
LUCI_PKGARCH:=all

define Package/luci-app-qbittorrent-enhanced/config
  choice
    prompt "Build mode"
    default PACKAGE_QBITTORRENT_ENHANCED

    config PACKAGE_QBITTORRENT_ENHANCED
    bool "Dynamic build"

    config PACKAGE_QBITTORRENT_ENHANCED_STATIC
    bool "Static build"
  endchoice
endef

include $(TOPDIR)/feeds/luci/luci.mk

# call BuildPackage - OpenWrt buildroot signature
