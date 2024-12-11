# 本项目不计运行效率地为 vscode 添加样式与动画。

- 纯 CSS 编写，一定程度上保证了运行效率。（起码我用着不卡）
- 有一个全局的线性窗口过渡，但是大部分常用的 UI 我都专门加上了非线性动画。

# 目录
- [一、预览列表](#1-主区域)
    - [1. 主区域](#1-主区域)
    - [2. 片区1](#2-片区-1)
    - [3. 游离窗口](#3-游离窗口)
- [二、使用方法](#使用方法)
- [三、更新日志](#更新日志)


## 1. 主区域
- 切换动画 🎇
  - 动画：添加进入动画。
  - 
    <img src="./Preview\GIF\主区域-切换动画.gif" />
    
- 标签栏动画 🔮
  - 动画：添加进入动画，非线性移动动画与交互动画。
  - 
    <img src="./Preview\GIF\主区域-标签栏动画.gif" />

- 代码提示 🔎
  - 样式：添加毛玻璃，圆角，适当排版。
  - 动画：添加非线性移动动画与进入动画。
  - 
    <img src="./Preview\GIF\主区域-代码提示.gif" />
    
- 顶部定位导航 📘
  - 动画：添加进入动画。
  - 
    <img src="./Preview\GIF\主区域-顶部定位导航.gif" />

- 顶部的粘性代码导航 🧲
  - 样式：毛玻璃。
  - 动画：添加非线性进入动画，为高度变化添加线性动画。
  - 
    <img src="./Preview\GIF\主区域-顶部粘性代码导航.gif" />

- 关键字高亮 💡
  - 动画：添加高亮动画
  - 注意：每个主题的关键字类名都不一样，我这里的是 `span.mtk4`。
  - 
    <img src="./Preview\GIF\主区域-关键字高亮(mtk4).gif" />

- 光标动画 📍
  - 动画：
    1. 添加炫酷的 RGB 光效。🌈🌈🌈
    2. 自调了光标运动的贝塞尔曲线。（ GIF 帧率太低看不太出来，但实际上效果很棒！）
       
    <img src="./Preview\GIF\主区域-光标动画.gif" />

- 快捷操作窗口 🛠
  - 样式：老样子，毛玻璃，圆角。
  - 动画：非线性进入动画与交互动画。
  - 
    <img src="./Preview\GIF\主区域-快捷操作窗口.gif" />

- 鼠标悬停提示窗口 🎈
  - 样式：老样子，圆角毛玻璃。
  - 动画：非线性进入动画与移动动画。
  - 
    <img src="./Preview\GIF\主区域-鼠标悬停代码提示.gif" />

- 所在行数显眼提示 🕯
  - 动画：变大变亮。
  - 
    <img src="./Preview\GIF\主区域-所在行数.gif" />

## 2. 片区 1
- 切换动画 🔮
  - 动画：套用主区域的动画。
  - 
    <img src="./Preview\GIF\片区1-切换动画.gif" />

- 资源管理器 🗂
  - 动画：
    1. 添加进入动画与交互动画。
    2. 添加文件状态指示图标。
       
    <img src="./Preview\GIF\片区1-资源管理器.gif" />

- 查找替换 🔍
  - 动画：老样子添加动画。
  - 
    <img src="./Preview\GIF\片区1-查找替换.gif" />

## 3. 游离窗口
- 右键菜单
  - 样式：圆角毛玻璃。
  - 动画：添加进入动画和交互动画。
  - 
    <img src="./Preview\GIF\游离窗口-右键菜单.gif" />

#### 还有很多以前写的边边角角的小动画和样式，由于以前没有写 README 所以没办法记全，懒得全部写上来了。

---

# 使用方法：
1. 安装 CSS 加载器，我用的是 <a href="https://marketplace.visualstudio.com/items?itemName=drcika.apc-extension">Apc Customize UI++</a>, 当然你可以选择诸如 `Custom CSS and JS Loader` 之类的，能加载 CSS 文件就行。
2. 导入里面所有 CSS 文件：
   ```
   # 文档撰写日期为 2024 年 7 月 20 日 00:24:46，该文件列表可能具有时效性。
   vscode-teriri-custom-style/index.css
   vscode-teriri-custom-style/temp.css
   vscode-teriri-custom-style/Style/Active/index.css
   vscode-teriri-custom-style/Style/teriri-style.css
   vscode-teriri-custom-style/Animate/teriri-animate.css
   vscode-teriri-custom-style/Animate/Active/index.css
   vscode-teriri-custom-style/Animate/Scrolling/index.css
   vscode-teriri-custom-style/Animate/Misc/index.css
   vscode-teriri-custom-style/Animate/Tabs/index-flip.css
   ```
3. 适用于我自己
   ```shell
    "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/index.css",
    "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/Style/Active/index.css",
    "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/Style/teriri-style.css",
    "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/Animate/teriri-animate.css",
    "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/Animate/Active/index.css",
    "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/Animate/Scrolling/index.css",
    "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/Animate/Misc/index.css",
    "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/Animate/Tabs/index-flip.css"
    ```
4. vscode 配置中
   ```json
     "vscode_custom_css.imports": [
         // 部分使用
        // "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/Animate/teriri-animate.css",
        // "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/Animate/Scrolling/index.css",
        // "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/Style/teriri-style.css",
        // "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/index.css",
        // 全使用
        "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/index.css",
        "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/Style/Active/index.css",
        "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/Animate/teriri-animate.css",
        "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/Animate/Active/index.css",
        "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/Animate/Scrolling/index.css",
        "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/Animate/Misc/index.css",
        "file:///C:/Users/16143/AppData/Roaming/Code/User/custom/Animate/Tabs/index-flip.css"
      ]
   ```
---

# 更新日志：
- 2024.7.9: 
  - 代码提示框
    - 样式: 添加圆角与毛玻璃效果。
    - 动画: 添加非线性交互动画，添加移动过渡。
- 2024.7.9: 初始化远程仓库。
