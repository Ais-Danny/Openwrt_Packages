include $(TOPDIR)/rules.mk

PKG_NAME:=cloudflare-ddns
PKG_VERSION:=1.0
PKG_RELEASE:=1
PKG_MAINTAINER:=aisdannys.top@gmail.com

include $(INCLUDE_DIR)/package.mk

define Package/cloudflare-ddns
	SECTION:=utils
	CATEGORY:=Utilities
	TITLE:=Cloudflare DDNS
	DEPENDS:=+curl +jq
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
	$(CP) ./files/opt/cloudflare/cloudflare_ddns.sh $(1)/opt/cloudflare/cloudflare_ddns.sh
	chmod 755 $(1)/etc/init.d/irq-balance
	$(INSTALL_DIR) $(1)/etc/crontabs
	echo "*/1 * * * * /opt/cloudflare/cloudflare_ddns.sh >/dev/null 2>&1" > $(1)/etc/crontabs/root
endef

$(eval $(call BuildPackage,cloudflare-ddns))
