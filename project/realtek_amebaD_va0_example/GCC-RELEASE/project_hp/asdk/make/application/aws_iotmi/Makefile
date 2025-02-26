include $(MAKE_INCLUDE_GEN)

.PHONY: all clean

AWS_IOTMI_DIR = $(BASEDIR)/component/common/application/aws_iotmi
AWS_IOTMI_SDK_DIR = $(AWS_IOTMI_DIR)/IoT-Smarthome-Device-SDK
ASDK_TOOLCHAIN   = $(TOOLCHAINDIR)/linux/asdk-6.4.1/linux/newlib

all:
	mkdir -p build
	cd build
	cmake -S $(AWS_IOTMI_DIR) -B build -DAMEBAD_SDK_ROOT=${BASEDIR} -DASDK_TOOLCHAIN=$(ASDK_TOOLCHAIN)
	cmake --build build

clean:
	rm -rf build
