set(third_party_folder "ThirdParty")

if(NOT TARGET SDL3::SDL3)
    # Build Settings
    set(SDL_SHARED OFF CACHE BOOL "" FORCE)
    set(SDL_STATIC ON CACHE BOOL "" FORCE)
    set(SDL_LIBC ON CACHE BOOL "" FORCE)
    set(SDL_TEST_LIBRARY OFF CACHE BOOL "" FORCE)
    set(SDL_INSTALL OFF CACHE BOOL "" FORCE)       # SDL3 使用 SDL_INSTALL 控制安装
    set(SDL_EXAMPLES OFF CACHE BOOL "" FORCE)      # 确保不构建示例

    # Disable subsystems we don't care about.
    set(SDL_AUDIO OFF CACHE BOOL "" FORCE)
    set(SDL_RENDER OFF CACHE BOOL "" FORCE)        # SDL_Renderer (2D API)
    set(SDL_HAPTIC OFF CACHE BOOL "" FORCE)
    set(SDL_POWER OFF CACHE BOOL "" FORCE)
    set(SDL_SENSOR OFF CACHE BOOL "" FORCE)
    set(SDL_CAMERA OFF CACHE BOOL "" FORCE)        # SDL3 新增
    set(SDL_JOYSTICK OFF CACHE BOOL "" FORCE)
    set(SDL_HIDAPI OFF CACHE BOOL "" FORCE)
    set(SDL_DIALOG OFF CACHE BOOL "" FORCE)        # SDL3 新增 (系统对话框)
    set(SDL_GPU OFF CACHE BOOL "" FORCE)           # SDL3 新增 (GPU API)

    # Note: SDL_VIDEO is enabled by default and is required for window creation.
    # Note: SDL_TIMERS, SDL_EVENTS, SDL_FILESYSTEM are mandatory/core parts in SDL3.

    add_subdirectory(sdl3)
endif()

if(NOT TARGET glm::glm)
    # GLM Settings
    set(GLM_TEST_ENABLE OFF CACHE BOOL "" FORCE)

    add_subdirectory(glm)
endif()