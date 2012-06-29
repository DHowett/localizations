include $(THEOS)/makefiles/common.mk

SUBPROJECTS = preferences

include $(THEOS_MAKE_PATH)/aggregate.mk

ifeq ($(findstring RELEASE,$(THEOS_SCHEMA)),)
PACKAGE_BUILDNAME = private
endif

internal-stage::
	-find $(THEOS_STAGING_DIR) -iname 'en.lproj' -exec rm -rf {} \;
	$(FAKEROOT) chown -R 0:80 $(THEOS_STAGING_DIR)
