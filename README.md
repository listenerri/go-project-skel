# go-project-skel

go （基于模块的）项目基础结构，参考：https://go.dev/doc/modules/layout

## 项目结构

此项目结构包含了以下目标：

- 以模块的形式发布，并被其他项目使用
- 部分代码被拆分到包内，且包可被其他项目使用
- 部分代码不希望外部程序使用，放在私有包里
- 包含自己的可执行程序

结构释义：

- go-project-skel // 项目根目录
    - go.mod // 项目依赖管理文件
    - module_file1.go // 项目未划分到包内的源码
    - cmd // 存放所有可执行程序源码
        - my_exe1 // 可执行程序 1 的源码目录
            - main.go // 可执行程序 1 的源码
    - package1 // 包 1 的源码目录
        - package1_file1.go // 包 1 的源码
    - internal // 存放所有私有包源码
        - internal_package1 // 私有包 1 的源码目录
            - internal_package1_file1.go // 私有包 1 的源码
