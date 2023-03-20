<p align="center">
  <a href="https://github.com/jerrylum/topmost2"><img src="https://i.imgur.com/r7PW6a2.png" alt="IntroIcon" width="100"></a>
</p>
<h3 align="center">TopMost2</h3>
<p align="center">此工具允许您使任何窗口始终位于顶部。</p>

<h4 align="center"><a href="https://github.com/jerrylum/topmost2/releases">现在下载</a></h4>

---

### 双击

双击任务栏图标，使当前选定的窗口保持置顶。

<h5 align="left">
<img src="https://i.imgur.com/kuBflkz.gif">
</h5>

<br>

### 全局热键

使用默认热键“Ctrl+Alt+Space”使当前选定的窗口保持置顶。
<h5 align="left">
<img src="https://i.imgur.com/NokjMLd.gif">
</h5>
<br>

### 更改热键

右键单击任务栏图标，然后转到“选项”页面，将热键更改为您自己喜欢的组合。

<h5 align="left">
<img src="https://i.imgur.com/LfNdpHR.gif">
</h5>

<br>

### 窗口列表

单击“窗口列表”中的菜单项可以固定或取消固定任何窗口。

<h5 align="left">
<img src="https://i.imgur.com/6KIfi3d.gif">
</h5>

<br>

### 其他功能

- 动态图标
- 清除所有置顶
- 自启动选项
- 启用/禁用键盘快捷方式选项
- 可自由自定义热键
- 全局热键
- 命令行支持
- 与其他程序的高度兼容性 
- 可忽略的系统资源使用情况



---

### 为什么我需要这个？

`Topmost` 或 `Always On Top` 是您电脑上每个可视窗口的属性。当窗口属性 Topmost 设置为 `true` 那么届时窗口将置于所有窗口的 Topmost 属性值为 `false` 之上.  <br>

但许多 Windows 应用程序不提供使自己应用置顶的选项。当您同时浏览多个窗口时，这可能会让您因频繁切换到不同的窗口而感到恼火。使用TopMost2，您可以将此功能添加到任何应用程序中并解决上述问题。



### 详情 

- **任务栏图标**  
  图标的颜色表示当前选定窗口的置顶状态。
  🟥红 = 正常, 🟩绿 = 置顶
  
- **Clear All Function**  
  This function will set all windows to normal states.
  
- **Elevated Privileges**  
  If you are trying to set an elevated window, TopMost2 will ask you to elevate the privileges in order to have higher permission to finish the action. Obviously, the reason is that they are protected by the operating system. You can also start TopMost2 as administrator to avoid the above problem.
  
- **Hotkey**  
  You can freely set any hotkey combinations. By clicking the `Edit` button, you can then press a new combination. After that, click `Done` to finish. If you leave or close the option form. The hotkey setting will be auto-saved by the system.  
  ![Hot Key Demo](https://i.imgur.com/jGFi1tC.gif)  
  If TopMost2 starts with normal permission, it may not be able to read the input of the keyboard in the elevated window.

- **Exit**  
  This function will set all windows to normal state and shut down the program.


### Command Line

Usage:

```powershell
.\topmost2 [--autostart] {action hWnd}
```

**action:**

- Set top-most: `--set` or `-S` or `/S`
- Remove top-most: `--remove` or `-R` or `/R`

**hWnd:**

The handle pointer in hexadecimal. HWND is a "handle to a window" and is part of the Win32 API.

<br>

For example:

```powershell
.\topmost2 -S 0x311A0 -S 0x190D4E
.\topmost2 -R 0x311A0
```



---

### Other Software

There are similar software like [DeskPins](https://efotinis.neocities.org/deskpins/) and [Window TopMost Control](https://www.sordum.org/9182/window-topmost-control-v1-2/). I am trying to compare them in several ways. Keep in mind, everyone has different opinion so this comparison is for reference only.



|                                                 | TopMost2          | DeskPins                 | Window TopMost Control |
| ----------------------------------------------- | ----------------- | ------------------------ | ---------------------- |
| Set Elevated application's Window <sup>#0</sup> | ✔️                 | ✔️ <sup>#1</sup>          | ✔️                      |
| Command Line Support                            | ✔️                 | ❌                        | ✔️                      |
| Portable                                        | ✔️                 | ❌                        | ✔️                      |
| Auto Start                                      | ✔️                 | ❌                        | ✔️                      |
| Auto Pin                                        | ❌                 | ✔️                        | ❌                      |
| Open Source                                     | ✔️                 | ✔️                        | ❌                      |
| State visibility                                | 🟡Good             | 🟢Excellent <sup>#2</sup> | 🟠Limited <sup>#3</sup> |
| CPU Usage                                       | 🟢Least            | 🟠Highest                 | 🟡Medium                |
| Customize                                       | 🟡Good             | 🟢Excellent               | 🟡Good                  |
| Compatibility With Programs                     | 🟢Excellent        | 🟡Good <sup>#4</sup>      | 🟢Excellent             |
| Hotkey                                          | More Combinations | More shortcuts           | Limited                |
| Size                                            | 47KB              | 103KB                    | 680KB                  |

#0 Able to change a window that belongs to a process with elevated privileges (run as the administrator).  
#1 Only if the application starts as administrator. Otherwise, trying to do that will cause unknown behavior.  
#2 Pin icon at the top-right corner of the top-most window.  
#3 Only provide the "Window List" feature.  
#4 Not Compatible with windows which also have top-most setting.  

<br> 

---

### Download

Please go to [the release page](https://github.com/jerrylum/topmost2/releases) to download the latest version.  
This tool requires .Net Framework 4.7.2 (or above). Support Windows 7 SP1 or later.  

<br>

### Special Thanks

Thanks you [SamNg](https://github.com/ngkachunhlp) and [COMMANDER.WONG](https://github.com/COMMANDERWONG) for their suggestions and  software testing.
