include $(TOPDIR)/rules.mk

PKG_NAME:=cloudflare-ddns
PKG_VERSION:=1.0
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/cloudflare-ddns
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=Cloudflare DDNS
  DEPENDS:=+bash +curl +jq
  MENU:=1
  SUBMENU:=ddns Utilities
endef

define Package/cloudflare-ddns/description
  Cloudflare DDNS script for OpenWRT
endef

define Build/Compile
endef

define Package/cloudflare-ddns/install
  $(INSTALL_DIR) $(1)/opt/cloudflare/
  $(INSTALL_BIN) ./files/opt/cloudflare/cloudflare_ddns.sh $(1)/opt/cloudflare/cloudflare_ddns.sh
endef

$(eval $(call BuildPackage,cloudflare-ddns))
