# oe22.03-v1版本测试说明

# 1.测试目的
本次测试为功能测试，主要目的为了验证软件各项基本功能是否完好，符合用户使用要求。同时对0926版本所测试出的缺陷进行回归测试，验证缺陷是否继续存在。

# 2.测试前提
本次测试所使用镜像为openEuler-22.03-V1版本，此版本较于0926版本软件包内容并无更改，因此0926版本进行过的功能测试将不再进行详细测试，测试重点在缺陷验证上。

镜像目录地址：https://mirror.iscas.ac.cn/openeuler-sig-riscv/openEuler-RISC-V/preview/openEuler-22.03-V1-riscv64/QEMU/

本次测试所使用文件为：[fw_payload_oe_qemuvirt.elf](https://mirror.iscas.ac.cn/openeuler-sig-riscv/openEuler-RISC-V/preview/openEuler-22.03-V1-riscv64/QEMU/fw_payload_oe_qemuvirt.elf),[openEuler-22.03-V1-riscv64-qemu-xfce.qcow2.tar.zst](https://mirror.iscas.ac.cn/openeuler-sig-riscv/openEuler-RISC-V/preview/openEuler-22.03-V1-riscv64/QEMU/openEuler-22.03-V1-riscv64-qemu-xfce.qcow2.tar.zst),[preview_start_vm_xfce.sh](https://mirror.iscas.ac.cn/openeuler-sig-riscv/openEuler-RISC-V/preview/openEuler-22.03-V1-riscv64/QEMU/preview_start_vm_xfce.sh)。

# 3.测试方法
本次测试以0926版本的缺陷汇总为基准进行了回归测试，并增加了新的测试用例以测试软件功能。

# 4测试结果
本次测试openEuler-22.03-V1-riscv64 版本共发现问题 28个，P1 0 个，P2 0 个，P3 12 个，P4 11 个，P5 5 个，对缺陷进行了重新分级。


## 较于20220926版本22.03：

修复了缺陷P2 1个，P3 1个，删除了P5 1个。

|    软件名称         | P1   | P2         | P3                      | P4                 | P5                         | 备注            |
| ----------- | ---- | ---------- | ------------------------------ | ------------------ | -------------------------- |-------------------------| 
| Firefox            |      |            | 安装报错                |                    |                   | 原先存在97与100两个版本，目前删除了100只保留了97，此缺陷解决 |
| Chromium           |      |            |                        |                    |命令行命令行启动需添加—browser| 站会上决定删除此缺陷       |
| Xfce               |      |自动锁屏无法解锁（QEMU，VisionFive） |              |                     |              | 重新发布了一版删除屏保的镜像，此缺陷解决 |
 
## 缺陷汇总：

|    软件名称  | P1   | P2         | P3                             | P4                 | P5                         |
| ----------- | ---- | ---------- | ------------------------------ | ------------------ | -------------------------- |
| Firefox     |      |            | 语言设置选项出现乱码           |                    |                              |
|             |      |            | 设置语言后页面无法正常显示     |                    |                              |                             
|             |      |            | 无法停止下载                  |                    |                              |                              
|             |      |            | 下载项显示空白                   |                            |                                                
|             |      |            |                                | 数据不能同步                           |                                      
|             |      |            |                                | 打不开b站          |                            |
|             |      |            |                                |                   | 不能进入阅读模式              |
| VLC         |      |            | 无显卡环境（QEMU, VisionFive），视频播放黑屏，需手工更改视频输出方式X11                 |                    |                            |
|             |      |            | 播放卡顿                       |                    |                            |
|             |      |            | 文件标题显示错误               |                    |                            |
|             |      |            |                                | 字幕列表部分显示乱码       |                            |
| GIMP        |      |            |                                |                    | 无法打开使用手册           |
| Thunderbird |      |            |                                |                    | 无法修改语言为英语外的语言 |
|             |      |            |                                | 无法保存邮件内容为样例   |                      |
| Chromuim    |      |            |                                |                      | 谷歌账号数据同步失败       |
| Xfce        |      |            |                                |                    | 应用程序查找器无法查看历史命令 |
|             |      |            | 改伸缩比例                     |                    |                            |
|             |      |            |                                | 回收站没有默认显示 |                            |
|             |      |            |                                | 设置桌面为纯色，无变化     |                            |
|             |      |            |                                | 改变桌面朝向左，无变化     |                            |
|             |      |            |                                | 改变桌面朝向右，无变化     |                            |
|             |      |            |                                | 改变桌面朝向上，无变化     |                            |
|             |      |            |                                | 改变桌面朝向下，无变化     |                            |
| Ecilpse     |      |            | 不能打开已有项目                |                          |                             |
|             |      |            | 无法配置tomcat                  |                          |                            |
|             |      |            |                                | 软件启动时间较长           |                            |
| Libreoffice |      |            | 无法卸载                        |                          |                            |
|             |      |            | 无法验证安装问题                |                           |                            |
