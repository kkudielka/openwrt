include $(TOPDIR)/rules.mk
include $(INCLUDE_DIR)/kernel.mk

PKG_NAME := leds-omnia
PKG_RELEASE := 1

include $(INCLUDE_DIR)/package.mk

define KernelPackage/leds-omnia
  SUBMENU:=LED modules
  DEPENDS:=@TARGET_mvebu_cortexa9
  TITLE:=Turris Omnia LED support
  FILES:=$(PKG_BUILD_DIR)/leds-omnia.ko
endef

define KernelPackage/leds-omnia/description
  Driver for the Turris Omnia LED controller.
endef

define Build/Compile
	$(KERNEL_MAKE) M="$(PKG_BUILD_DIR)" modules
endef

$(eval $(call KernelPackage,leds-omnia))
