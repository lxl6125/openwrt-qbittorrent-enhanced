# Copyright (C) 2019 Openwrt.org
#
# This is a free software, use it under Apache Licene 2.0 & GNU General Public License v3.0.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=luci-app-qbittorrent-ee
PKG_VERSION:=1.0.0
PKG_RELEASE:=1

LUCI_TITLE:=LuCI support for qBittorrent-Enhanced-Edition
LUCI_PKGARCH:=all
LUCI_DEPENDS:= \
	+PACKAGE_luci-app-qbittorrent-ee_static:qBittorrent-Enhanced-Edition-static \
	+PACKAGE_luci-app-qbittorrent-ee_dynamic:qBittorrent-Enhanced-Edition

define Package/$(PKG_NAME)/config
	choice
		prompt "Build Version Selection"
		default PACKAGE_luci-app-qbittorrent-ee_static

		config PACKAGE_luci-app-qbittorrent-ee_static
			bool "Static Build"
			depends on arm||aarch64||x86_64

		config PACKAGE_luci-app-qbittorrent-ee_dynamic
			bool "Dynamic Build"

	endchoice
endef

include $(TOPDIR)/feeds/luci/luci.mk

# call BuildPackage - OpenWrt buildroot signature
