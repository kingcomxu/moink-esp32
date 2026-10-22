
set(JKINK_SRCS
    "main.c" "epd_drv.c" "settings.c" "netif_ap.c" "captive.c"
    "ota_web.c" "frame.c" "power.c" "store.c")


idf_component_register(SRCS ${JKINK_SRCS}
                       PRIV_REQUIRES driver nvs_flash esp_wifi esp_netif esp_event
                  esp_http_server esp_adc esp_hw_support
                  app_update spi_flash esp_partition esp_timer lwip
                  esp_driver_gpio esp_driver_spi
                       INCLUDE_DIRS "."
                       EMBED_FILES
                            "www/index.html"
                       ) 
