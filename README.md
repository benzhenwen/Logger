# Logger
A very basic logger for c++
- has colors - pretty facy~

## CMake
###include FetchContent:
```
include(FetchContent)

FetchContent_Declare(
    Logger
    GIT_REPOSITORY https://github.com/benzhenwen/Logger.git
    GIT_TAG main
)

FetchContent_MakeAvailable(Logger)
```
### link
```
target_link_libraries(particles PRIVATE Logger::Logger)
```

## Meson
### add as subprojects/logger.wrap
```
[wrap-git]
url = https://github.com/benzhenwen/Logger.git
revision = main 
```

## then include
```
#include <logger/logger.hpp>
```
