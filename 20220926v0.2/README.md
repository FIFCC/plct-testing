## 20220926版本测试说明

# 1.测试目的
本次测试为功能测试，主要目的为了验证软件各项基本功能是否完好，符合用户使用要求。同时对0922版本所提出的缺陷进行回归测试，验证缺陷是否已被修复。

# 2.测试前提
本次0926版本共有两版镜像文件，其中第二版较于第一版修复了音频以及脚本启动问题，本次测试以第二版镜像文件为标准进行测试。

镜像目录地址：https://mirror.iscas.ac.cn/openeuler-sig-riscv/openEuler-RISC-V/testing/20220926/v0.2/QEMU/

本次测试所使用文件为：[fw_payload_oe_qemuvirt.elf](https://mirror.iscas.ac.cn/openeuler-sig-riscv/openEuler-RISC-V/testing/20220926/v0.2/QEMU/fw_payload_oe_qemuvirt.elf),[openeuler-qemu-xfce.qcow2.tar.zst](https://mirror.iscas.ac.cn/openeuler-sig-riscv/openEuler-RISC-V/testing/20220926/v0.2/QEMU/openeuler-qemu-xfce.qcow2.tar.zst),[start_vm_xfce.sh](https://mirror.iscas.ac.cn/openeuler-sig-riscv/openEuler-RISC-V/testing/20220926/v0.2/QEMU/start_vm_xfce.sh)。

# 3.测试方法
本次测试以各项软件的帮助手册作为参考进行了功能测试。

# 4测试结果
本次测试openEuler 22.03 RISC-V 20220926 版本共发现问题 27个，P1 0 个，P2 0 个，P3 12 个，P4 12 个，P5 3 个。

## 缺陷汇总：

|    软件名称         | P1   | P2         | P3                             | P4                 | P5                         |
| ----------- | ---- | ---------- | ------------------------------ | ------------------ | -------------------------- |
| Firefox     |      |            | 语言设置选项出现乱码           |                    |                            |
|             |      |            | 设置语言后页面无法正常显示     |                    |                            |
|             |      |            | 无法停止下载                  |                    |                            |
|             |      |            | 安装报错                     |                      |                           |
|             |      |            | 下载项显示空白                   |                            |
|             |      |            | 安装报错                   |                            |
|             |      |            |                                | 数据不能同步                           |
|             |      |            |                                | 打不开b站          |                            |
|             |      |            |                                | 不能进入阅读模式   |                            |
| VLC         |      |            | 无显卡环境（QEMU, VisionFive），视频播放黑屏，需手工更改视频输出方式X11                 |                    |                            |
|             |      |            | 播放卡顿                       |                    |                            |
|             |      |            | 文件标题显示错误               |                    |                            |
|             |      |            |                                | 字幕列表部分显示乱码       |                            |
| GIMP        |      |            |                                |                    | 无法打开使用手册           |
| Thunderbird |      |            |                                |                    | 无法修改语言为英语外的语言 |
|             |      |            |                                | 无法保存邮件内容为样例   |                      |
| Chromuim    |      |            |                                | 谷歌账号数据同步失败   |                            |
|             |      |            |                                |                     | 命令行启动需添加—browser |
| Xfce        |      |            | 自动锁屏无法解锁（QEMU，VisionFive）               |                    |                            |
|             |      |            | 应用程序查找器无法查看历史命令 |                    |                            |
|             |      |            | 改伸缩比例                     |                    |                            |
|             |      |            |                                | 回收站没有默认显示 |                            |
|             |      |            |                                | 设置桌面为纯色，无变化     |                            |
|             |      |            |                                | 改变桌面朝向左，无变化     |                            |
|             |      |            |                                | 改变桌面朝向右，无变化     |                            |
|             |      |            |                                | 改变桌面朝向上，无变化     |                            |
|             |      |            |                                | 改变桌面朝向下，无变化     |                            |

