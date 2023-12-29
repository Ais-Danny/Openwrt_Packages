include $(TOPDIR)/rules.mk

PKG_NAME:=irq-balance
PKG_VERSION:=1.0
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/irq-balance
  SECTION:=utils
  CATEGORY:=Utilities
  TITLE:=IRQ Balance
endef

define Package/irq-balance/description
  A custom package for irq-balance
endef

define Build/Compile
endef

define Package/irq-balance/install
  $(INSTALL_DIR) $(1)/etc/init.d
  $(INSTALL_BIN) ./files/etc/init.d/irq-balance $(1)/etc/init.d/irq-balance
endef

$(eval $(call BuildPackage,irq-balance))
