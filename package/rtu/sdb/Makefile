include $(TOPDIR)/rules.mk
 
PKG_NAME:=sdb
PKG_RELEASE:=1
 
PKG_SOURCE_PROTO:=git
PKG_SOURCE_URL:=git@github.com:yeryomin/student-db.git
PKG_SOURCE_DATE:=2024-12-20
PKG_SOURCE_VERSION:=2166f0a0
PKG_MIRROR_HASH:=skip

PKG_MAINTAINER:=Roman Yeryomin <roman@advem.lv>
 
include $(INCLUDE_DIR)/package.mk

define Package/$(PKG_NAME)
	SECTION:=RTU
	CATEGORY:=RTU
	DEPENDS:=+libc
	TITLE:=Student database read/write app
endef

define Package/$(PKG_NAME)/description
CLI application which allows to enter student
data and read that afterwise.
endef

define Package/$(PKG_NAME)/install
	$(INSTALL_DIR) $(1)/usr/bin
	$(INSTALL_BIN) $(PKG_BUILD_DIR)/student_db $(1)/usr/bin/
endef

$(eval $(call BuildPackage,$(PKG_NAME)))
