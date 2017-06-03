include $(MTK_PATH_BUILD)/common.mk
$(call all-modules-src-or-makefile,$(obj),CUSTOM_KERNEL_)
obj-n := dummy.o
ifeq ($(VANZO_TOUCHPANEL_GESTURES_SUPPORT), yes)
ifeq ($(findstring focaltech,$(CUSTOM_KERNEL_TOUCHPANEL)), focaltech)
obj-y += ft_gesture_lib.a
$(obj)/ft_gesture_lib.a: $(srctree)/../$(obj)/touchpanel/ft_gesture_lib.a
	cp $(srctree)/../$(obj)/touchpanel/ft_gesture_lib.a $(obj)/ft_gesture_lib.a
endif
endif

