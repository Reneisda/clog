# C-Logger clog
## c stb-style header-only library for logging

## Log-level
- LOG_LEVEL_ERR
- LOG_LEVEL_WARN
- LOG_LEVEL_INFO
- LOG_LEVEL_EXTRA

## Examples
```c
#define LOG_LEVEL_ERROR     // defaults to Info, when undefined
#include "clog.h"

clog_info("This is an info!");
clog_error("This is an error!");
clog_warn("This is a warning!");
clog_extra("This is an extra message!");
clog_warn("Another Warning!");
```

### Formatted Logging
```c
clogf_info("Test: %d\n", 1234);
clogf_warn("Test: %f\n", 3.145f);
clogf_extra("Test: %s\n", "string");
clogf_error("Test: %d\n", 1234);
```

### Log-Info
```c
clogf_info("Warnings: %d\n", clog_warn_count());
```

