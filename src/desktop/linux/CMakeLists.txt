# Desktop Integration
# Copyright (C) 2016 Gabriel Rauter

# Desktop shortcut
install(FILES aseprite.desktop DESTINATION share/applications)
install(FILES ../../../data/icons/ase16.png DESTINATION share/icons/hicolor/16x16/apps RENAME aseprite.png)
install(FILES ../../../data/icons/ase24.png DESTINATION share/icons/hicolor/24x24/apps RENAME aseprite.png)
install(FILES ../../../data/icons/ase32.png DESTINATION share/icons/hicolor/32x32/apps RENAME aseprite.png)
install(FILES ../../../data/icons/ase48.png DESTINATION share/icons/hicolor/48x48/apps RENAME aseprite.png)
install(FILES ../../../data/icons/ase64.png DESTINATION share/icons/hicolor/64x64/apps RENAME aseprite.png)
install(FILES ../../../data/icons/ase128.png DESTINATION share/icons/hicolor/128x128/apps RENAME aseprite.png)
install(FILES ../../../data/icons/ase256.png DESTINATION share/icons/hicolor/256x256/apps RENAME aseprite.png)

# GNOME Thumbnailer
install(FILES mime/aseprite.xml DESTINATION share/mime/packages)
install(PROGRAMS aseprite-thumbnailer DESTINATION bin)
install(FILES gnome/aseprite.thumbnailer DESTINATION share/thumbnailers)

# Qt Thumbnailer
if(ENABLE_QT_THUMBNAILER)
  add_subdirectory(kde)
endif()
