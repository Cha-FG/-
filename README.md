未来世界的 “记忆收纳盒”
The "Memory Storage Box" of the Future World
产品背景故事
Product Backstory
公元 2145 年，人类因为“信息过载” ，记忆不断衰退。人们沉溺于虚拟世界里面，连家门钥匙、常用工具这类日常生活中常用的实体物品的存放位置都频繁遗忘。为了解决这一问题，“记忆收纳盒”诞生了，它旨在帮助人们记住实体物品的存放处，解决人们经常遗忘、丢失实体物品的问题。
In the year 2145 AD, human memory was declining due to "information overload." People were indulged in the virtual world, frequently forgetting where everyday physical objects like house keys and common tools were stored. To address this issue, the "Memory Storage Box" was invented. It aims to help people remember where their physical objects are kept, solving the problem of frequently forgetting and losing such items.
使用场景举例
Examples of Usage Scenarios
在2145年10月30日，杰克刚结束一天的工作。他走向玄关旁的收纳盒 —— 木质激光切割的盒身由卡槽拼接而成（如下图1），顶部有一块蓝色的 3D 打印推拉板（如下图2），这是它的 “开关”。他将推拉板拉开，里面的Arduino Uno 主板瞬间亮起指示灯。“滴 ——” 传感器扫描他刚放入的家门磁卡钥匙，Arduino 随即启动物品识别程序：“物品已归档，存储时间2145年10月30日，家门钥匙 ，应储存在家门口鞋柜的右侧第二个的抽屉里”，杰克按照指示把钥匙放到相应的位置上。
On October 30, 2145, Jack had just finished his work for the day. He walked over to the storage box by the entryway — its wooden, laser-cut body was assembled with slot joints (as shown in Figure 1 below), and on top was a blue 3D-printed sliding plate (as shown in Figure 2 below), which served as its "switch." He slid the plate open, and the Arduino Uno motherboard inside immediately lit up its indicator lights."Beep—" The sensor scanned the house key card he had just placed inside, and the Arduino immediately activated the item recognition program: "Item archived. Storage time: October 30, 2145. House key. Should be stored in the second drawer from the right in the shoe cabinet by the entrance." Jack followed the instructions and placed the key in the corresponding position.
![6a4ed8bb68a7018561ddd333406b10b1](https://github.com/user-attachments/assets/e79c46c6-fecf-4c5d-928b-0b36e6d25f66)
![5f0c0e4a8f002754e9f06714fed6f6f3](https://github.com/user-attachments/assets/25cc3613-05c5-4fce-9cb8-17cf5972023f)
这个盒子是他的的 “记忆收纳盒”—— 每当他存放一件物品，Arduino 就会记录下物品特征、存放时间与存放地点，他甚至可以语音录入一段使用场景（如 “这是公寓新换的磁卡钥匙，门禁密码更新为 2145001，需在感应区停留 1 秒”）。
This box is his "Memory Storage Box" — every time he stores an item, the Arduino records the item's characteristics, storage time, and location. He can even voice-record a usage scenario (e.g., "This is the newly replaced key card for the apartment. The access code has been updated to 2145001, and it needs to stay in the sensor area for 1 second.").
记忆收纳盒运作全流程
Full Operational Process of the Memory Storage Box
一、物品存储与记忆绑定
激活设备：将顶部蓝色 3D 打印推拉板拉开，Arduino Uno 主板的电源指示灯亮起，设备进入就绪状态。
放入物品：将物品直接放入盒内，触发红外识别传感器。
多维记录：
自动采集：Arduino 通过传感器获取物品外形、材质数据，生成唯一 ID，同步记录存放时间与地点。
手动补充：跟盒子说“我要补充信息”，可录入语音进行补充说明。
I. Item Storage and Memory Binding
Activate the device: Pull open the blue 3D-printed sliding plate on top, and the power indicator of the Arduino Uno motherboard lights up, putting the device in a ready state.
Place the item: Put the item directly into the box, triggering the infrared recognition sensor.
Multi-dimensional recording:
Automatic collection: The Arduino acquires data on the item’s shape and material via the sensor, generates a unique ID, and synchronously records the storage time and location.
Manual supplement: Say "I want to add information" to the box, and you can record a voice to provide supplementary explanations.
二、信息检索与快速定位
本地查询：滑开推拉板，Arduino上LED 显示屏自动显示最近的存储记录。
规律提示：当同类物品（如 “钥匙类”）存储次数≥3 次时，Arduino 会归纳存放规律（如 “家门钥匙常放于左侧腔，工具类小零件集中在中间腔”），并在下次存放时主动提示 “建议存放至左侧腔，便于钥匙类物品管理”。
II. Information Retrieval and Quick Location
Local query: Slide open the sliding plate, and the LED display on the Arduino will automatically show the latest storage records.
Pattern prompts: When items of the same category (e.g., "keys") are stored 3 or more times, the Arduino will summarize storage patterns (e.g., "House keys are often stored in the left compartment; small tool parts are concentrated in the middle compartment"). It will then proactively prompt during the next storage, such as "It is recommended to store in the left compartment for easier management of key items."
三、关闭
休眠与断电：将推拉板向左侧推回至完全闭合，Arduino 自动进入低功耗休眠模式；若需长期断电，可拔下盒身侧边的 USB 供电线。
II. Shutdown
Sleep and power-off: Push the sliding plate back to the left until fully closed, and the Arduino will automatically enter a low-power sleep mode. For long-term power-off, unplug the USB power cable on the side of the box.
设计逻辑与工艺解析
Arduino Uno 的核心作用：作为 “记忆中枢”，它通过红外传感器实现物品自动识别，借助存储模块与交互接口，将钥匙、小零件等实体物品与人类日常记忆深度绑定，让 “找东西” 从难题变成一键操作。
激光切割工艺：盒身是由激光切割木板形成，用 AutoCAD 图纸的设计，通过激光切割出的精密卡槽实现无胶拼接，既保证结构强度，又让组装过程像拼积木一样简单高效。
<img width="3071" height="1761" alt="ed0cd69814e99c41ba9ccac20d13220c" src="https://github.com/user-attachments/assets/45493326-66bc-4ebc-837f-d2278aa36f73" />
![60d325c70b30035a99ba9992f9676b85](https://github.com/user-attachments/assets/431c3401-66bd-436e-b36f-bbf7d230dfce)
![fed3a3b9fb02299b20a1abdb94daf514](https://github.com/user-attachments/assets/0611f136-7385-48b8-9a31-e8aad61fb565)
3D 打印推拉板：顶部的蓝色推拉板是由 3D 打印（我先在SketchUp里面吗进行建模），它既是 Arduino Uno 主板的防护外壳，又通过滑动结构实现 “滑开激活、闭合休眠” 的交互。
<img width="3071" height="1809" alt="77cb9504c1799e8e469831ae8f3ad342" src="https://github.com/user-attachments/assets/46819990-2906-411f-a4c5-e188949a3b9a" />
![5f0c0e4a8f002754e9f06714fed6f6f3](https://github.com/user-attachments/assets/43a6d0eb-a1a9-4d9c-8874-e2688c5a2a3f)


