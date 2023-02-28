#
# Copyright (C) 2017-2020
#
# This is free software, licensed under the GNU General Public License v2.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=qBittorrent-Enhanced-Edition-static
PKG_VERSION:=4.5.2.10
PKG_RELEASE=1

STRIP:=true

ifeq ($(ARCH),arm)
	PKG_ARCH:=arm-linux-musleabi
endif

ifeq ($(ARCH),aarch64)
	PKG_ARCH:=aarch64-linux-musl
endif

ifeq ($(ARCH),x86_64)
	PKG_ARCH:=x86_64-linux-musl
endif

PKG_SOURCE:=qbittorrent-enhanced-nox_$(PKG_ARCH)_static.zip
PKG_SOURCE_URL:=https://github.com/c0re100/qBittorrent-Enhanced-Edition/releases/download/release-$(PKG_VERSION)/
PKG_HASH:=skip

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
	SECTION:=net
	CATEGORY:=Network
	SUBMENU:=BitTorrent
	TITLE:=bittorrent client programmed in C++ / Qt
	URL:=https://www.qbittorrent.org/
endef

define Package/$(PKG_NAME)/description
  qBittorrent is a bittorrent client programmed in C++ / Qt that uses
  libtorrent (sometimes called libtorrent-rasterbar) by Arvid Norberg.
  It aims to be a good alternative to all other bittorrent clients out
  there. qBittorrent is fast, stable and provides unicode support as
  well as many features.
endef

define Build/Compile
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(BUILD_DIR)/qbittorrent-nox $(1)/usr/bin
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
