cmake_minimum_required(VERSION 3.5)

project(vcpkg_vendor)

find_package(ament_cmake REQUIRED)

set(PACKAGE_VERSION "1.0.0")

if(WIN32)
  ament_environment_hooks(env_hook/vcpkg_vendor_library_path.bat)
  set(PATH_ENV_VAR_NAME "PATH")
  set(PATH_ENV_VAR_VALUE "E:/work/vcpkg_coco_install/x64-windows/bin")
  set(QT_ENV_VAR_NAME "Qt5_DIR")
  set(QT_ENV_VAR_VALUE "E:/work/vcpkg_coco_install/x64-windows")
  set(QT_PLATFORM_ENV_VAR_NAME "QT_QPA_PLATFORM_PLUGIN_PATH")
  set(QT_PLATFORM_ENV_VAR_VALUE "E:/work/vcpkg_coco_install/x64-windows/plugins/platforms")
  ament_environment_hooks(env_hook/vcpkg_vendor_library_path.dsv.in)
endif()

ament_package(
)
