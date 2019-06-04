##############################################
# OpenWrt Makefile for helloDaemon program
##############################################

include $(TOPDIR)/rules.mk

# Name and release number of this package
PKG_NAME:=helloDaemon
PKG_REV:=f4e6552190af7b378a552d363eb1af9aaf53c58c
PKG_VERSION:=2017-02-11
PKG_RELEASE:=1

PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=https://github.com/embedCreativity/helloDaemon.git
PKG_SOURCE_VERSION:=$(PKG_REV)
PKG_SOURCE:=$(PKG_NAME)-$(PKG_VERSION)-$(PKG_REV).tar.gz
PKG_SOURCE_SUBDIR:=$(PKG_NAME)-$(PKG_VERSION)

PKG_BUILD_DIR:=$(BUILD_DIR)/$(PKG_NAME)/$(PKG_SOURCE_SUBDIR)

include $(INCLUDE_DIR)/package.mk

# Specify package information for this program.
# The variables defined here should be self explanatory.
define Package/helloDaemon
  TITLE:=helloDaemon example program that starts automatically upon boot
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

define Package/helloDaemon/install
	$(INSTALL_DIR) $(1)/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/helloDaemon $(1)/bin/
	$(INSTALL_DIR) $(1)/etc/init.d
	$(INSTALL_BIN) ./files/helloDaemon.init $(1)/etc/init.d/helloDaemon
endef

# This line executes the necessary commands to compile our program.
# The above define directives specify all the information needed, but this
# line calls BuildPackage which in turn actually uses this information to
# build a package.
$(eval $(call BuildPackage,helloDaemon))
