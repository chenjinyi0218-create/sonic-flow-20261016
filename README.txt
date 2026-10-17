SONIC FLOW · 11 AUDIO-REACTIVE VISUALIZERS

运行方法
1. 解压 zip。
2. 打开 sonic-flow-audio-reactive-11 文件夹。
3. 双击 index.html，用 Chrome 或 Safari 打开。
4. 按照流程选择压力场景、压力等级、声音偏好。

你的声音文件放置方法
把你的 11 个声音文件放到 audio 文件夹里。
支持 mp3 或 wav。文件名必须对应：

自然 소리
- 비 소리：rain.mp3 或 rain.wav
- 파도 소리：waves.mp3 或 waves.wav
- 바람 소리：wind.mp3 或 wind.wav
- 숲 환경음：forest.mp3 或 forest.wav

인공 소리
- 화이트 노이즈：white-noise.mp3 或 white-noise.wav
- 카페 환경음：cafe.mp3 或 cafe.wav
- 책 넘기는 소리：book.mp3 或 book.wav
- 키보드 소리：keyboard.mp3 或 keyboard.wav

음악
- Ambient：ambient.mp3 或 ambient.wav
- Lo-fi：lofi.mp3 或 lofi.wav
- 명상 음악：meditation.mp3 或 meditation.wav

网页读取逻辑
选择声音后，网页会优先读取 mp3：
audio/rain.mp3

如果 mp3 不存在，会自动尝试 wav：
audio/rain.wav

如果两个都没有，可以在最后页面点击 UPLOAD，临时选择一个本地声音文件。

11 个声音对应的视觉化
1. rain：雨点下落 + 水波涟漪，根据高频和音量改变雨速与密度。
2. waves：海浪线条 + 泡沫光点，根据低频改变波浪幅度。
3. wind：风流线条，根据中频改变流速与弯曲程度。
4. forest：萤火虫 + 叶片飘落，根据高频和环境声变化闪烁。
5. white-noise：噪点矩阵，根据高频产生抖动。
6. cafe：暖色气泡和漂浮点，根据中频变化上升速度。
7. book：纸片翻动和页面光扫，根据高频变化翻页速度。
8. keyboard：键盘网格脉冲，根据瞬态和高频点亮。
9. ambient：星云轨道，根据低频和整体音量扩张。
10. lofi：低保真均衡器 + 暖色漂浮粒子，根据频谱柱变化。
11. meditation：曼陀罗呼吸图形，根据低频缓慢扩张收缩。

性能优化
- 已取消最后一页原本很卡的复杂粒子呼吸系统。
- 每个视觉模式使用轻量绘制逻辑。
- 不再进行粒子之间的距离连线计算。
- 使用较少渐变和缓存光点 sprite，减少卡顿。
- 粒子数量会根据压力等级调整，但控制在较流畅范围。


LATEST CHANGE
-------------
- Logo is forced to white.
- Stress level page uses the uploaded droplet UI:
  Low Stress = blue
  Medium Stress = yellow
  High Stress = red
- Other pages and the 11 audio-reactive visualizers are unchanged.


VIDEO INTRO UPDATE
------------------
The previous custom logo intro was removed.

New intro:
- Uses the uploaded MP4 as the first page.
- Video loops and does not automatically jump to the home page.
- Click ENTER SITE to enter the original Sonic Flow home page.
- A matching ambient BGM is generated in-browser.
- BGM starts after the first click/tap/key press due browser autoplay restrictions.
- Use BGM ON/OFF to control the intro music.


SOURCE VIDEO INTRO UPDATE
-------------------------
The intro video was replaced with the uploaded original MP4 source file:
assets/intro-logo-animation.mp4

No upscaling or re-encoding was applied, so the source quality is preserved.
BGM behavior is unchanged from the previous video-intro version.


REBUILT CLEAR INTRO WITH SOUND BUTTON
-------------------------------------
- Intro video regenerated from source MP4.
- 4K resolution preserved.
- Sharpened, contrast adjusted, grayscale-normalized to reduce odd colored artifacts.
- Short fade-in/out added at loop boundary to hide sudden strange frames.
- Video loops continuously.
- BGM ON/OFF button restored.
- Click BGM ON if browser blocks sound autoplay.


CUSTOM ICON UPDATE
------------------
Only the requested icons were changed:
- Stress level icons replaced with uploaded low/mid/high SVGs.
- Sound category icons replaced with uploaded natural/artificial/music SVGs.
All other pages and interactions remain unchanged.


MUSIC ICON FIX
--------------
Only the music category icon was replaced again with the latest uploaded SVG:
assets/sound-music.svg
A cache-busting query was added in index.html to avoid the browser showing the old icon.


MUSIC ICON LOCAL PATH FIX
-------------------------
Fixed the music category icon path for local file opening.
Removed the query string from assets/sound-music.svg so the browser can load the SVG correctly from a local folder.


INLINE MUSIC ICON FIX
---------------------
The music category icon is now embedded directly inside index.html as inline SVG.
This avoids local file path, cache, and SVG loading issues that caused a broken-image box.
Only the music icon handling was changed.


FINAL MUSIC ICON FIX
--------------------
The music category was fixed by matching title:"음악" directly instead of depending on its rgb values.
The latest uploaded SVG is embedded inline through MUSIC_ICON_INLINE, so it cannot show as a broken image.


VISUAL SYSTEM REFINEMENT
------------------------
- Unified interface typography around Pretendard and removed the remaining serif display rules.
- Simplified the three sound-category icons and seven stress-scene icons into one geometric symbol system.
- Localized the main interface and experience controls in Korean for a quieter language hierarchy.
- Added restrained, sound-specific accent colors, including a subtle forest green and ocean cyan.
- Rebuilt the ocean-wave visual with layered currents, smoother trajectories, finer overlap, and stronger bass/mid/treble response.
- Preserved the existing page order, audio filenames, selection logic, and all eleven visualizer modes.


INTRO AUDIO SMOOTHING · 2026-09-01
----------------------------------
- 开场动画与背景音乐已合并为同一个 MP4 文件。
- 删除了播放过程中反复校正音频时间的逻辑，避免声音跳顿、断续。
- 浏览器会先静音播放；点击画面中的声音按钮后即可连续播放声音。
- 字体、图标、海浪、森林和其他页面内容保持不变。


GRADUATION EXHIBITION LOOP + AUDIO CHECK · 2026-09-01
-----------------------------------------------------
- 开场动画与内嵌声音已设为无限循环，播放结束后不会自动进入主页。
- 只有点击“시작하기”按钮才会进入后续页面。
- 开场媒体及现有 10 个后续音源均已完成全文件解码检查，未发现损坏。
- 当前缺少咖啡店环境音：请补充 audio/cafe.mp3 或 audio/cafe.wav。
- 缺少该文件时，网页会显示文件缺失提示，并允许现场手动选择音频。


STYLE-ONLY UPDATE
-----------------
This version changes only visual styling:
- Layout, page order, HTML content, and JavaScript flow are preserved.
- Visual direction: Sonic Flow identity, sound signal, wave lines, pressure particles, quiet instrument mood.
- Reduced generic AI glass-template feeling by changing surface texture, borders, glow, card corners, button treatment, and visual rhythm.


MAJOR STYLE REWORK
------------------
This version strongly changes the visual style while preserving the existing website structure, page content, page order, and JavaScript functionality.

Design direction:
- Less generic AI template feeling.
- More Sonic Flow identity: sound signal, pressure, particles, flow, dark blue device/system mood.
- Stronger surface language: asymmetric corners, thin signal lines, field grid, wave sweeps, pressure glow, and instrument-like panels.


SOUND PAGE FIX
--------------
Fixed only the sound selection screen:
- Adjusted sound-selection page proportions so the three cards stay inside the viewport.
- Reduced card height, icon size, and option height.
- Added internal scrolling only inside option lists when needed.
- Fixed top-left text overlap by reducing and repositioning the sound page title/header spacing.
Other screens, content, and functions are unchanged.


SOUND PAGE FINAL FIX
--------------------
Fixed the sound selection page according to screenshot notes:
- Increased font line-height and spacing to avoid tight/overlapping text.
- Removed the vertical decorative line on the left side of each sound card.
- Moved option-row dash/dot decoration away from text.
- Increased sound card height and padding so the option list is not cut by the frame.
Only CSS styling was changed; layout structure, content, and functions remain unchanged.


MP4 BACKGROUND UPDATE
---------------------
- Added assets/flow-gradient-background.mp4 as a looping background video.
- The MP4 background is visible from the start/home page through the selection pages.
- The final audio visualization / sound display page hides the MP4 background.
- The original bgCanvas firefly-like floating particles are preserved and remain visible above the MP4 background.
- Page content, layout, sound options, and functions were not intentionally changed.


THREE-ZONE SOUND CATEGORY UPDATE
--------------------------------
- The first sound page is divided into three equal image regions.
- Category names stay hidden until the pointer hovers over an icon.
- Clicking an icon opens a second page containing only that category's sounds.
- The original 11 sound experiences remain connected to the new second page.
- Open the site by fully extracting the ZIP and double-clicking index.html.


INTRO-TO-SCENE TRANSITION UPDATE
--------------------------------
- Removed the redundant logo/description/start-button home screen.
- The intro now fades directly into the stress-situation screen.
- The intro sound fades smoothly instead of stopping abruptly.
- A temporary logo moves from the center toward the fixed top-left logo.
- The title and seven situation icons enter with a restrained staggered fade.
- The transition runs once per entry and does not create repeated audio or animation instances.
