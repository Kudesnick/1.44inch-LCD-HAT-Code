DIR_DTO = /boot/overlays/
CONFIG = /boot/config.txt
TARGET = $(DIR_DTO)lcd_hat_keyboard.dtbo
SOURCE = lcd_hat_keyboard-overlay.dts

$(TARGET): $(SOURCE)
	dtc -I dts -O dtb -o $@ $< -W no-unit_address_vs_reg

install: $(TARGET)
	sed -i "$$ a dtoverlay=$(basename $(notdir $(TARGET)))" $(CONFIG)

uninstall:
	rm $(TARGET)
	sed -i "/dtoverlay=$(basename $(notdir $(TARGET)))/d" $(CONFIG)
