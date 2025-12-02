# 已删除的Windows和macOS相关文件清单

本文档列出了从netdata代码库中删除的所有Windows和macOS相关文件。

## 删除的目录

### 1. packaging/windows/ (31个文件)
整个Windows打包目录，包含以下文件：
- BackGround.bmp
- bash_execute.sh
- build.ps1
- clion-msys-mingw64-environment.bat
- clion-msys-msys-environment.bat
- compile-on-windows.sh
- copy_files.ps1
- eula.rtf
- fetch-msys2-installer.py
- find-sdk-path.sh
- functions.ps1
- get-win-build-path.sh
- install-dependencies.ps1
- invoke-msys2.ps1
- msi-extension.bat
- msys2-dependencies.sh
- netdata.wxs.in
- NetdataWhite.ico
- package-windows.sh
- package.ps1
- protoc.bat
- resources/netdata_claim.manifest.in
- resources/netdata_claim.rc
- resources/netdata.manifest.in
- resources/netdata.rc
- resources/netdatacli.manifest.in
- resources/netdatacli.rc
- Top.bmp
- win-build-dir.sh
- windows-openssh-to-msys.bat
- WINDOWS_INSTALLER.md

### 2. src/collectors/windows.plugin/ (整个目录)
Windows插件收集器目录，包含所有Windows特定的收集器代码和集成文档。

### 3. src/collectors/windows-events.plugin/ (整个目录)
Windows事件日志插件目录，包含所有Windows事件日志相关的代码。

### 4. src/libnetdata/os/windows-wmi/ (整个目录)
Windows WMI接口目录，包含以下文件：
- windows-wmi.c
- windows-wmi.h
- windows-wmi-GetDiskDriveInfo.c
- windows-wmi-GetDiskDriveInfo.h

### 5. src/libnetdata/os/windows-perflib/ (整个目录)
Windows性能库目录，包含以下文件：
- perflib.c
- perflib.h
- perflib-dump.c
- perflib-names.c

### 6. src/health/guides/windows/ (整个目录)
Windows健康检查指南目录，包含以下文件：
- windows_10min_cpu_usage.md
- windows_disk_in_use.md
- windows_inbound_packets_discarded.md
- windows_inbound_packets_errors.md
- windows_outbound_packets_discarded.md
- windows_outbound_packets_errors.md
- windows_ram_in_use.md
- windows_swap_in_use.md

## 删除的单独文件

### 核心库文件
1. `src/libnetdata/spawn_server/spawn_server_windows.c` - Windows进程生成服务器实现
2. `src/libnetdata/os/os-windows-wrappers.c` - Windows操作系统包装器实现
3. `src/libnetdata/os/os-windows-wrappers.h` - Windows操作系统包装器头文件
4. `src/libnetdata/log/nd_log-to-windows-events.c` - Windows事件日志记录实现
5. `src/libnetdata/log/wevt_netdata_compile.bat` - Windows事件日志编译脚本

### 守护进程文件
6. `src/daemon/win_system-info.c` - Windows系统信息收集实现
7. `src/daemon/win_system-info.h` - Windows系统信息收集头文件

### 收集器文件
8. `src/collectors/apps.plugin/apps_os_windows.c` - Windows应用插件实现
9. `src/collectors/apps.plugin/apps_os_windows_nt.c` - Windows NT应用插件实现

### 文档文件
10. `docs/install/windows-release-channels.md` - Windows发布渠道文档
11. `docs/diagrams/windows.xml` - Windows相关图表

### 集成文件
12. `integrations/logs/integrations/windows_event_logs.md` - Windows事件日志集成文档

### 工具脚本
13. `packaging/utils/compile-and-run-windows.sh` - Windows编译和运行脚本
14. `src/web/mcp/bridges/stdio-golang/build.bat` - Windows构建脚本

## 统计信息

- **删除的目录数**: 6个
- **删除的单独文件数**: 14个
- **packaging/windows/目录中的文件数**: 31个
- **总计删除的文件数**: 约100+个文件（包括目录中的所有文件）

---

# macOS相关文件删除清单

## 删除的目录

### 1. src/collectors/macos.plugin/ (整个目录)
macOS插件收集器目录，包含以下文件：
- macos_fw.c - macOS防火墙相关代码
- macos_mach_smi.c - macOS Mach系统调用接口代码
- macos_sysctl.c - macOS系统控制接口代码
- plugin_macos.c - macOS插件主实现
- plugin_macos.h - macOS插件头文件
- metadata.yaml - 插件元数据
- README.md - 插件说明文档
- integrations/macos.md - macOS集成文档

### 2. system/launchd/ (整个目录)
macOS launchd服务配置目录，包含以下文件：
- netdata.plist.in - macOS launchd服务配置文件模板

## 删除的单独文件

### 核心库文件
1. `src/libnetdata/os/os-macos-wrappers.c` - macOS操作系统包装器实现
2. `src/libnetdata/os/os-macos-wrappers.h` - macOS操作系统包装器头文件

### 守护进程文件
3. `src/daemon/static_threads_macos.c` - macOS静态线程配置

### 收集器文件
4. `src/collectors/apps.plugin/apps_os_macos.c` - macOS应用插件实现

### 文档和安装文件
5. `packaging/installer/methods/macos.md` - macOS安装方法文档
6. `packaging/installer/dependencies/macos.sh` - macOS依赖安装脚本

### 集成文件
7. `src/go/plugin/go.d/collector/prometheus/integrations/apple_time_machine.md` - Apple Time Machine集成文档

## macOS删除统计信息

- **删除的目录数**: 2个
- **删除的单独文件数**: 7个
- **src/collectors/macos.plugin/目录中的文件数**: 8个
- **总计删除的文件数**: 约17个文件

---

## 总体说明

所有Windows和macOS相关的文件和目录已从代码库中删除。这些文件仅用于Windows和macOS平台，由于项目现在只在Linux系统上使用，因此不再需要这些文件。

### Windows删除统计
- **删除的目录数**: 6个
- **删除的单独文件数**: 14个
- **packaging/windows/目录中的文件数**: 31个
- **总计删除的文件数**: 约100+个文件（包括目录中的所有文件）

### macOS删除统计
- **删除的目录数**: 2个
- **删除的单独文件数**: 7个
- **总计删除的文件数**: 约17个文件

### 总计
- **删除的目录总数**: 8个
- **删除的单独文件总数**: 21个
- **总计删除的文件数**: 约117+个文件

注意：代码中可能仍存在一些条件编译指令（如 `#ifdef OS_WINDOWS`、`#ifdef OS_MACOS`），这些是正常的跨平台代码结构，用于在编译时排除Windows和macOS相关代码。

---

# IBM插件相关文件删除清单

## 删除的目录

### 1. src/go/plugin/ibm.d/ (整个目录)
IBM生态系统监控插件目录，包含以下模块：
- **modules/as400/** - IBM i (AS/400) 监控模块
- **modules/db2/** - IBM DB2 数据库监控模块
- **modules/mq/** - IBM MQ 消息队列监控模块
- **modules/websphere/** - WebSphere Application Server 监控模块
  - jmx/ - JMX监控
  - mp/ - MicroProfile Metrics监控
  - pmi/ - PMI监控
- **protocols/** - 协议实现（PCF、JMX、ODBC等）
- **pkg/** - 共享包（ODBC驱动、数据库驱动等）
- **config/** - 配置文件
- **samples.d/** - 示例数据

### 2. src/go/cmd/ibmdplugin/ (整个目录)
IBM插件主程序入口，包含：
- main.go - 主程序入口
- stub.go - 存根文件

### 3. packaging/cmake/pkg-files/deb/plugin-ibm/ (整个目录)
Debian包安装后处理脚本目录，包含：
- postinst - 安装后脚本

## 删除的单独文件

### CMake构建文件
1. `packaging/cmake/Modules/NetdataIBMPlugin.cmake` - IBM插件CMake构建配置

### 安装脚本
2. `packaging/installer/install-ibm-libs.sh.in` - IBM MQ客户端库安装脚本模板

### 配置文件修改
3. `CMakeLists.txt` - 删除了IBM插件相关的构建代码（第156行、第284行、第2968-2993行）
4. `packaging/cmake/Modules/Packaging.cmake` - 删除了IBM插件组件配置（第571-574行）
5. `packaging/build-package.sh` - 删除了IBM插件构建选项（第65、70、75、80行）
6. `netdata.spec.in` - 删除了IBM插件RPM包定义和相关配置

## IBM插件删除统计信息

- **删除的目录数**: 3个
- **删除的单独文件数**: 2个
- **修改的配置文件数**: 4个
- **src/go/plugin/ibm.d/目录中的文件数**: 约200+个文件
- **总计删除的文件数**: 约200+个文件

## 说明

IBM插件（ibm.d.plugin）用于监控IBM生态系统，包括：
- IBM i (AS/400) 系统监控
- IBM DB2 数据库监控
- IBM MQ 消息队列监控
- WebSphere Application Server 监控

由于项目不需要这些功能，所有相关代码、配置和构建脚本已从代码库中删除。

