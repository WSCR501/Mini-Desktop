# Small-Desktop
微型的桌面，适合充当PE桌面，也可以在维护的时候用

> [!IMPORTANT]
> 运行此程序需要有一个能运行exe的64位Windows环境

+ 基本的维护软件
+ 与系统组件联动
+ 仿真桌面
+ 配置要求极低

里面打包了一个文件管理器，那是我的另一个仓库里发的，别混了

> [!CAUTION]
> 杀毒软件报毒请信任

> [!TIP]
> 确保拥有自己账户以及Windows的administrator权限

## 应用模糊修复
在高分辨率显示屏上会出现应用字体生硬，文字模糊，此时请使用下列办法修复（如果你在PE当我没说）

按照下列图片操作：

![屏幕截图 2025-01-11 145509](https://github.com/user-attachments/assets/a7fe1a20-84ab-4708-9bf4-d313df940c28)

点按属性按钮

![屏幕截图 2025-01-11 145528](https://github.com/user-attachments/assets/08e0b82c-a4cc-4678-b4e5-67199bab5d8f)

切换到兼容性选项卡后点击所有用户的设置

![屏幕截图 2025-01-11 145533](https://github.com/user-attachments/assets/c0006014-f411-48cf-8443-4b854d3093bc)

点击图上的高DPI设置

![屏幕截图 2025-01-11 145542](https://github.com/user-attachments/assets/f8e91e3d-b17a-4bce-a135-6e80facb722a)

按照图示勾选两个框并且设置后点击确定

## 如何编写插件
这是必须的文件（目前仅支持code类插件）
```
readme.txt    用于标识您的插件名
Do.txt        插件激活后要运行的代码(cmd代码)
Code          标识您的插件类型
```

以下是文件/文件夹的规范存放方式
```
-pu（插件文件夹）
 -（您的插件文件夹名,需与readme.txt内容相同，否则无法加载）
  -（插件文件）
```

示例：

```
-pu
 -SB
  -readme.txt(内容:SB)
  -Do.txt(内容:cmd.exe)
  -Code(无内容)
```

效果：在插件管理器中启用后会弹出cmd窗口，但执行过程中主程序会未响应，直至关闭cmd窗口，同时插件会取消激活状态

> [!TIP]
> Do.txt中只能填入代码（填入多行效果未知）否则后果自负