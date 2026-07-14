**CS:GO / CS2 Demo 观战与录屏控制台指令指南**：

# CS:GO & CS2 Demo 观战与录屏控制台指令指南

在观看 Demo 或录制视频素材时，合理使用控制台指令可以帮助你快速隐藏不必要的 UI，获取纯净的画面。请确保已在「设置 - 游戏设置」中启用了**开发者控制台（`~` 键）**。

## 一、 快捷键绑定与基础画面设置

将常用的 X光 切换、UI 隐藏等功能绑定至快捷键，方便在观战时实时操作。

Shell

```
// 快捷键绑定
bind p "radio2;slot12"                  // 绑定 P 键（执行无线电与特定槽位切换）
bind x "toggle spec_show_xray 1 0"      // 绑定 X 键：一键开关 X光（透视）

// 观战画面精简
cl_spec_show_bindings 0                 // 关闭画面下方的小字按键提示
cl_drawhud_force_radar -1               // 强制关闭雷达
r_drawskybox 0                          // 关闭天空盒（天空变黑，方便突出主体）
```

## 二、 快速全隐藏（录屏/截图专用）

适用于需要完全纯净、无任何 UI 干扰的电影级录屏或截图。

- **一键清空画面指令（血条、地图、准星全消）：**
    
    Shell
    
    ```
    sv_cheats 1; cl_drawhud 0; net_graph 0; cl_showfps 0
    ```
    
    _(注：CS2 玩家请使用 `cl_drawhud false` 代替 `cl_drawhud 0`)_
    
- **分项隐藏指令：**
    

|**想要隐藏的内容**|**控制台指令**|**备注说明**|
|---|---|---|
|**Demo 播放条**|`demoui 0`|亦可使用快捷键 `Shift + F2` 呼出/隐藏播放面板|
|**右上角状态/比分**|`cl_demo_drawstatus 0`|隐藏顶部的双方比分与存活人数|
|**屏幕中央提示**|`hud_centertext_time 0`|隐藏类似于“等待下一局”等中央提示文字|
|**击杀信息**|`hud_takesshots 0`|隐藏右上角的击杀右上角红框提示|
|**武器与手臂模型**|`impulse 200`|隐藏持枪手（仅在 `sv_cheats 1` 开启时有效）|

## 三、 精细化 UI 隐藏（保留关键赛况）

如果你希望在保留部分关键信息（如击杀提示）的同时，让画面看起来更加专业，可以使用以下指令：

- **仅保留右上角击杀信息（去血条、去头像）：**
    
    Shell
    
    ```
    cl_draw_only_deathnotices 1
    ```
    
- **仅隐藏小地图：**
    
    Shell
    
    ```
    cl_radar_always_visible 0
    ```
    
- **仅隐藏网络数据（Ping/FPS/Packet Loss 等）：**
    
    Shell
    
    ```
    net_graph 0
    ```
    
- **隐藏比分板 / 隐藏指向玩家时的 ID 提示：**
    
    观战时按下 `G` 键，或在控制台输入：
    
    Shell
    
    ```
    hud_showtargetid 0
    ```
    
- **隐藏左下角版本号水印：**
    
    Shell
    
    ```
    r_show_build_info 0
    ```
    

## 四、 进阶脚本与一键恢复

### 1. HLAE 工具配合使用

如果你使用 **HLAE (Half-Life Advanced Effects)** 导入 Demo：

- 启动 HLAE 并载入游戏后，打开 **「Render」** $\rightarrow$ **「HUD Editor」**。
    
- 在面板中直接取消勾选需要隐藏的 HUD 元素或击杀信息，操作更加直观。
    

### 2. F12 一键切换纯净模式脚本 (Toggle Script)

将以下代码写入你的 `autoexec.cfg` 或直接粘贴进控制台。按下 `F12` 键即可在“纯净画面”与“常规观战画面”之间快速切换：

Shell

```
alias +cleanhud "cl_drawhud 0; cl_demo_drawstatus 0"
alias -cleanhud "cl_drawhud 1; cl_demo_drawstatus 1"
bind F12 +cleanhud 
```

### 3. 一键恢复默认状态

录制完毕后，复制并执行以下指令，即可快速找回所有丢失的 UI 元素：

Shell

```
cl_drawhud 1; demoui 1; cl_spec_show_bindings 1; cl_demo_drawstatus 1
```

## 五、 CS2 (Counter-Strike 2) 版本差异特别提醒

在 **CS2** 中，Valve 优化并重构了部分控制台代码，主要差异如下：

1. **布尔值变化**：CS2 的部分隐藏指令不再使用 `0` 或 `1`，而是使用 `false` 或 `true`。
    
    - **CS:GO**: `cl_drawhud 0`（隐藏）/ `cl_drawhud 1`（显示）
        
    - **CS2**: `cl_drawhud false`（隐藏）/ `cl_drawhud true`（显示）
        
2. **其余通用性**：除 `cl_drawhud` 外，诸如 `cl_spec_show_bindings`、`r_drawskybox` 和按键绑定（`bind`）等指令在 CS2 中均可完美兼容。