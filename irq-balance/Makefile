
include $(TOPDIR)/rules.mk

PKG_NAME:=irq-balance
PKG_VERSION:=1.0
PKG_RELEASE:=1

include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
  	SECTION:=utils
	CATEGORY:=Utilities
	TITLE:=IRQ Balance
endef

define Package/$(PKG_NAME)/description
	A custom package for irq-balance
endef  

define Build/Compile 
 	$(info Building $(PKG_NAME)...)
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/etc/init.d
	$(CP) ./files/etc/init.d/irq-balance $(1)/etc/init.d/irq-balance
	chmod 755 $(1)/etc/init.d/irq-balance
endef
    
$(eval $(call BuildPackage,$(PKG_NAME)))
