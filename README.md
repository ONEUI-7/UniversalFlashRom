# UniversalFlashRom
这是一个通用的刷机脚本，只需把相应的 img 文件扔进 images 文件夹，就能确保刷入，但是文件名一定要和分区名保持一致，文件名不用带 ab 分区标识，会自动识别，建议从官方卡刷包提取，能够确保文件名与分区名相等，应该适用于任何能通过 fastboot 线刷的 ROM

该刷机脚本既可以作为 fastboot 模式线刷，也可以 fastbootd 模式线刷，取决于你是否打包了 super

该脚本基于 TIK 工具的刷机脚本大量修改，加入了首次刷入分区失败重试，更好的提示，以及默认自带 vbmeta 校验移除，针对含 vbmeta 分区的镜像文件，无论有多少个与 vbmeta 相关的镜像文件，都能自动识别并在刷入时移除校验，机型需要你打开 bat 文件，手动填写，以免刷入和你机型不对应的 ROM

在 hyperos 测试通过，在其它 ROM 应该也适用，除非有特殊校验，MIUI14 及 hyperos 只需移除 vbmeta 校验，无需额外修改移除卡米验证，就能开机，其它 ROM 待测试
警告：不要把错误的甚至是和你机型不匹配的分区文件刷入了，这可能导致设备不能正常开机甚至更严重的问题，
