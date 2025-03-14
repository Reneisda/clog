# C-Logger clog
## c stb-style header-only library for logging
#### Logging is added pre-compile-time

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
clog_warn("This is a warning!");
clog_error("This is an error!");
clog_extra("This is an extra message!");
```

### Formatted Logging
```c
clogf_info("Test: %d\n", 1234);
clogf_warn("Test: %f\n", 3.14159f);
clogf_extra("Test: %s\n", "string");
clogf_error("Test: %d\n", 1234);
```

### Log-Info
```c
clogf_info("Warnings: %d\n", clog_warn_count());
```

### Extra pre-compile #defines
- LOG_ONLY_COLORS       -> disable Lables [INFO / WARN / ERR / EXTRA]
- LOG_NO_TIMESTAMPS     -> disables timestamps

### 🔴 all defines have to be set before including clog.h 🔴

### Sample Output

<code>2025-03-14 22:40:53]    INFO    This is an info!</code>  
<code style="color : darkorange">[2025-03-14 22:40:53]   WARN    This is a warning!</code>  
<code style="color : red">[2025-03-14 22:40:53]   ERROR   This is an error!</code>  
<code style="color : lightskyblue">[2025-03-14 22:40:53]   EXTRA   This is an extra message!</code>  

