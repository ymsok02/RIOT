PKG_NAME=driver_atwinc15x0
PKG_URL=https://github.com/arduino-libraries/WiFi101
PKG_VERSION=3301d03f82e53f60e07434a9f07ca677d992d121
PKG_LICENSE=LGPL-2.1

include $(RIOTBASE)/pkg/pkg.mk

CFLAGS += -Wno-discarded-qualifiers
CFLAGS += -Wno-empty-body
CFLAGS += -Wno-old-style-definition
CFLAGS += -Wno-unused-parameter
CFLAGS += -Wno-incompatible-pointer-types-discards-qualifiers

CFLAGS += -DETH_MODE
CFLAGS += -I$(PKG_SOURCE_DIR)/src

all:
	"$(MAKE)" -C $(PKG_SOURCE_DIR)/src/driver/source -f $(RIOTBASE)/Makefile.base MODULE=driver_atwinc15x0
	"$(MAKE)" -C $(PKG_SOURCE_DIR)/src/common/source -f $(RIOTBASE)/Makefile.base MODULE=driver_atwinc15x0_common
	"$(MAKE)" -C $(PKG_SOURCE_DIR)/src/spi_flash/source -f $(RIOTBASE)/Makefile.base MODULE=driver_atwinc15x0_spi_flash
