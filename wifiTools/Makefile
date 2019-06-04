##############################################
# OpenWrt Makefile for wifiTools program
##############################################

include $(TOPDIR)/rules.mk

# Name and release number of this package
PKG_NAME:=wifiTools
PKG_REV:=28ab7b93d3ba763b23c57cc006c2d15f0eaeda05
PKG_VERSION:=2019-06-04
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/embedCreativity/wifiTools.git
PKG_SOURCE_VERSION:=$(PKG_REV)
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_REV).tar.gz
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)/$(PKG_SOURCE_SUBDIR)

include $(INCLUDE_DIR)/package.mk

# Specify package information for this program.
# The variables defined here should be self explanatory.
define Package/wifiTools
  TITLE:=wifiTools
  SECTION:=embedCreativity
  CATEGORY:=embedCreativity
  DEPENDS:=
endef

# Openwrt will default config/compile definitions that make sense.
# Do not override unless necessary
#define Build/Configure
#
#endef
#
#define Build/Compile
#
#endef

define Package/wifiTools/install
	$(INSTALL_DIR) $(1)/bin
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/scanWifi $(1)/bin/
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/connectWiFi.sh $(1)/usr/bin/connectWiFi
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/createWAP.sh $(1)/usr/bin/createWAP
endef

# This line executes the necessary commands to compile our program.
# The above define directives specify all the information needed, but this
# line calls BuildPackage which in turn actually uses this information to
# build a package.
$(eval $(call BuildPackage,wifiTools))
