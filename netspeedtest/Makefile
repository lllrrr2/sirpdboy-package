#
# Copyright (C) 2020-2021 sirpdboy <herboy2008@gmail.com>
# The LuCI Network diagnosis and speed test <https://github.com/sirpdboy/NetSpeedTest>
# Use the speed measurement program provided by ookla. 
# This is free software, licensed under the GNU General Public License v3.
#

include $(TOPDIR)/rules.mk

PKG_NAME:=netspeedtest
PKG_VERSION:=1.0.0
PKG_RELEASE:=7

PKG_LICENSE:=GPL-3.0

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
	SECTION:=net
	CATEGORY:=Network
   TITLE:= A Speedtest application 
   DEPENDS:=+python3 +wget
   MAINTAINER:= sirpdboy

endef

define Build/Prepare
	mkdir -p $(PKG_BUILD_DIR)
	$(CP) ./file/* $(PKG_BUILD_DIR)/
endef
define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/bin
	
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/speedtest $(1)/usr/bin
endef


$(eval $(call BuildPackage,netspeedtest))
