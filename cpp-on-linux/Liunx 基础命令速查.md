# Linux 基础命令速查

| 类别       | 命令                                      | 说明                                      |
|------------|-------------------------------------------|-------------------------------------------|
| 文件操作   | `ls -lhtr`                                | 按修改时间倒序查看                        |
|            | `tree -L 2`                               | 显示目录结构（2 层）                      |
|            | `find . -name "*.cpp" -o -name "*.h"`     | 查找所有 cpp/h 文件                       |
|            | `grep -r "TODO" . --include="*.cpp"`      | 递归搜索代码里的 TODO                     |
|            | `du -sh * \| sort -h -r`                  | 查看当前目录大小并从大到小排序（全兼容）  |
| 进程与资源 | `ps aux \| grep app`                      | 查找进程                                  |
|            | `top` / `htop`                            | 实时查看进程资源                          |
|            | `kill -9 PID`                             | 强杀进程                                  |
|            | `pstack PID`                              | 查看线程调用栈                            |
|            | `strace -p PID -f`                        | 跟踪系统调用                              |
|            | `lsof -p PID`                             | 查看进程打开的文件                        |
| 编译运行   | `g++ -std=c++23 -Wall -Wextra -g -O2 main.cpp -pthread -o app` | 标准生产编译命令                          |
|            | `./app > log.txt 2>&1 &`                  | 后台运行 + 全日志                         |
|            | `nohup ./app &`                           | 守护进程                                  |
| 网络       | `ss -tunlp \| grep 8080`                  | 查看端口占用（推荐）                      |
|            | `curl -v http://localhost:8080/health`    | 测试接口                                  |
| 系统监控   | `free -h`                                 | 查看内存                                  |
|            | `df -h`                                   | 查看磁盘                                  |
|            | `iostat -xz 1`                            | 实时磁盘 IO                               |
|            | `vmstat 1`                                | 系统整体负载                              |
