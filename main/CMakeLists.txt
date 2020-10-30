set(srcs 	"tft_demo.c")

idf_component_register(SRCS  "${srcs}"
                       INCLUDE_DIRS "."
					   PRIV_REQUIRES spiffs tft spidriver)

spiffs_create_partition_image(storage ../components/spiffs_image/image/ FLASH_IN_PROJECT)