### TODO:
  - 1.为啥通过多个 port 进行通信?一个port多个 command/message 不好?

### 代码分析
- 杀毒程序,在访问数据时进行进行(transaction-aware file scanner)
- 通过 avlib.h 提供给 Kernel/User 端公用的接口定义,比如 PortName宏, 命令的结构体定义等.
  注意: 为了避免头文件依赖, 尽量用通用的类型,而且放在 包含文件列表的最后(不用特意包含其他头文件)
  ```
    #define AV_INVALID_SECTION_HANDLE   ((HANDLE)((LONG_PTR)(-1)))
  ```
