![DeepSeek-V3](https://img2025.cnblogs.com/other/1737323/202501/1737323-20250107172726505-1206408687.png)

DeepSeek-V3 的价格实在是太香了，简直像不要钱一样：  
**每百万输入 tokens 0.1 元 (缓存命中) / 1 元 (缓存未命中)，每百万输出 tokens 2 元**。

![性价比](https://img2025.cnblogs.com/other/1737323/202501/1737323-20250107172727504-518786279.png)

与其他模型相比，DeepSeek-V3 的性价比极高，堪称“真香”代表。

![Sealos AI Proxy](https://img2025.cnblogs.com/other/1737323/202501/1737323-20250107172728362-1572294905.png)

Sealos 推出的 AI 聚合代理服务 [Sealos AI Proxy](https://bit.ly/bewildcard) 为用户提供了便捷的 AI 模型访问通道，其中包括 DeepSeek-V3 模型。通过 Sealos AI Proxy 使用这些模型时，**价格与官方定价完全一致**，真正做到零溢价，让用户以最实惠的价格享受优质的 AI 服务。

接下来，我将**手把手教你如何让 Cursor 使用 DeepSeek-V3 模型**。

虽然 Cursor 的价格较高且试用时间有限，但它支持用户接入自定义 API。因此，我们可以通过接入 Sealos AI Proxy 的 API，让 Cursor 使用 DeepSeek-V3 模型以及其他各种模型。

> **注意**：Cursor 接入自定义 API 只能使用 Chat 模型，不能使用 Composer 模式。不过已经很香了。

如果你只想接入 DeepSeek-V3 模型，也可以选择使用 DeepSeek 官方的 API。而 **Sealos AI Proxy 的优势在于它可以同时接入多个模型，而不仅仅局限于 DeepSeek**。

## 操作步骤

### 1. 登录 Sealos Cloud 并获取 API Key

首先登录 [Sealos Cloud](https://bit.ly/bewildcard)，打开桌面上的【AI Proxy】：

![Sealos Cloud](https://img2025.cnblogs.com/other/1737323/202501/1737323-20250107172729524-1321332619.png)

新建一个 Key：

![新建 Key](https://img2025.cnblogs.com/other/1737323/202501/1737323-20250107172730523-306007903.png)

创建完成后，你就得到了一个 API Key。

![API Key](https://img2025.cnblogs.com/other/1737323/202501/1737323-20250107172732504-2137584887.png)

### 2. 配置 Cursor 使用 DeepSeek-V3

现在回到 Cursor，点击顶部菜单栏的 `Cursor` → `Settings` → `Cursor Settings`：

![Cursor 设置](https://img2025.cnblogs.com/other/1737323/202501/1737323-20250107172733341-2138705661.png)

以下是具体配置步骤，请仔细阅读并严格按照操作：

1. **取消勾选其他所有模型**  
   打开 Models 界面，取消勾选其他所有模型。

   ![取消勾选](https://img2025.cnblogs.com/other/1737323/202501/1737323-20250107172734098-1554232197.png)

2. **添加自定义模型**  
   点击 “Add Model” 添加一个自定义模型。

   ![添加模型](https://img2025.cnblogs.com/other/1737323/202501/1737323-20250107172735439-212202271.png)

3. **输入模型名称**  
   输入模型名称为 `deepseek-chat`，然后回车。

   ![模型名称](https://img2025.cnblogs.com/other/1737323/202501/1737323-20250107172736244-1524021311.png)

   > **提示**：DeepSeek 的模型 `deepseek-chat` 和 `deepseek-coder` 已经合并，所以这里输入 `deepseek-chat` 即可自动使用最新的 DeepSeek-V3 模型。

4. **配置 API 地址**  
   在 “Override OpenAI Base URL” 下方输入框中输入 Sealos AI Proxy 的 API 地址：  
   `https://aiproxy.hzh.sealos.run/v1`  
   然后点击 “Save” 按钮。

   > **注意**：API 地址末尾的 `/v1` 不能省略。

   ![API 地址](https://img2025.cnblogs.com/other/1737323/202501/1737323-20250107172736949-128127775.png)

5. **输入 API Key 并验证**  
   输入之前在 Sealos AI Proxy 中创建的 API Key，然后点击 “Verify” 按钮。

   ![输入 API Key](https://img2025.cnblogs.com/other/1737323/202501/1737323-20250107172738795-1430379380.png)

   在弹出来的对话框中点击 “Enable OpenAI API Key” 按钮。

   ![启用 API Key](https://img2025.cnblogs.com/other/1737323/202501/1737323-20250107172739568-1593391253.png)

6. **完成验证**  
   验证完成后，界面会变成如下所示：

   ![验证完成](https://img2025.cnblogs.com/other/1737323/202501/1737323-20250107172741035-197466661.png)

### 3. 开始使用 DeepSeek-V3

现在，你可以在 Cursor 中使用 DeepSeek-V3 模型了。直接按下快捷键 `CMD + L` 打开 Cursor 的 Chat 界面，然后开始对话。

![Cursor Chat](https://img2025.cnblogs.com/other/1737323/202501/1737323-20250107172742457-2027520012.png)

写代码也不是问题，直接输入以下提示词，DeepSeek 就能为你生成完整的符合需求的代码。

python
# 示例：让 DeepSeek 生成一个二分查找算法
# 输入注释
"""
实现一个二分查找算法，要求：
1. 使用迭代方式实现
2. 处理目标值不存在的情况
3. 添加详细注释
4. 考虑数组可能为空的情况
5. 返回目标值的索引，如果不存在则返回-1
"""


👉 [WildCard | 一分钟注册，轻松订阅海外线上服务](https://bit.ly/bewildcard)