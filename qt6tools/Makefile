#
# Copyright (C) 2019 Openwrt.org
#
# This is free software, licensed under the Apache License, Version 2.0 .
#

include $(TOPDIR)/rules.mk

PKG_NAME:=qt6tools
PKG_VERSION:=6.9.0
PKG_REAL_VERSION:=$(PKG_VERSION)-rc1
PKG_RELEASE:=1

PKG_SOURCE:=qttools-$(PKG_REAL_VERSION).tar.gz
PKG_SOURCE_URL:=https://codeload.github.com/qt/qttools/tar.gz/v$(PKG_REAL_VERSION)?
PKG_HASH:=9f02d5fc09c7f1e875f548f47bc3889369915811da490fb973cd59e17d5fe121

HOST_BUILD_DIR:=$(BUILD_DIR_HOST)/qttools-$(PKG_REAL_VERSION)

HOST_BUILD_DEPENDS:=qt6base/host
HOST_BUILD_PARALLEL:=1
PKG_HOST_ONLY:=1

include $(INCLUDE_DIR)/package.mk
include $(INCLUDE_DIR)/host-build.mk
include $(INCLUDE_DIR)/cmake.mk

define Package/qt6tools
  SECTION:=utils
  CATEGORY:=Utilities
  SUBMENU:=Qt6
  TITLE:=Qt6 Tools
  URL:=http://qt-project.org
  BUILDONLY:=1
  HIDDEN:=1
endef

CMAKE_HOST_OPTIONS+= \
	-DINPUT_assistant=no \
	-DINPUT_designer=no \
	-DINPUT_clang=no \
	-DINPUT_distancefieldgenerator=no \
	-DINPUT_kmap2qmap=no \
	-DINPUT_pixeltool=no \
	-DINPUT_qdbus=no \
	-DINPUT_qev=no \
	-DINPUT_qtattributionsscanner=no \
	-DINPUT_qtplugininfo=no \
	-DINPUT_qtdiag=no

$(eval $(call BuildPackage,qt6tools))
$(eval $(call HostBuild))
