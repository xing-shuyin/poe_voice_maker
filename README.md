

# 流放之路掉落语音生成器

这是一个基于 **火山引擎语音合成大模型** 的《流放之路》物品掉落语音提示生成器，可用于生成游戏内语音播报，提升游戏体验。

---

## 🧩 功能描述

- 通过火山引擎的语音合成大模型，将《流放之路》中的物品名称（如神圣石、改造石等）转换为语音。
- 支持自定义音色，实时生成语音文件或进行流式播放。
- 适用于游戏内自动化提醒、直播辅助、挂机提示等场景。

---

## 🔧 使用步骤

### 1. 开通火山语音合成大模型服务

- 前往 https://console.volcengine.com/ark/region:ark+cn-beijing/tts/speechSynthesis
- 开通 **按量付费服务（1 元即可）** 或使用 **新用户试用**。
- 开通后获取以下必要信息：

| 参数名称     | 说明                                       | 示例/格式                     |
|--------------|--------------------------------------------|-------------------------------|
| APP ID       | 你的火山引擎应用ID                         | 如：812121212                 |
| Access Token | 你的访问令牌                               | 如：asdasd_FtiR91HxGylLICQVaQXHZk5 |
| Voice Type   | 你想要的音色，如女声/男声/特色音色         | 如：zh_female_meilinvyou_moon_bigtts |
| Cluster      | 集群，默认填写 `volcano_tts` 即可          | volcano_tts                   |

---

### 2. 准备配置文件：`data.txt`

在与脚本相同的目录下创建一个 `data.txt` 文件，内容格式如下（请替换为你自己的信息）：

```json
{
    "appid": "你的appid(类似812121212)",
    "access_token": "你的access_token(类似asdasd_FtiR91HxGylLICQVaQXHZk5)",
    "voice_type": "你喜欢的voice_type(类似zh_female_meilinvyou_moon_bigtts)",
    "cluster": "volcano_tts"
}
```

> ⚠️ 请将上述内容中的示例值替换为你从火山平台获取的真实值。

---

### 3. 准备物品名称列表：`names.txt`

在同一目录下创建 `names.txt` 文件，每行一个物品名称，例如：

```
神圣石
改造石
富豪石
```


---

### 4. 运行语音生成脚本

（此处假设你有相应的 Python 或客户端脚本，根据你的实际代码补充运行方式，例如：）

```bash
poe_voice_maker.exe
```

确保 `data.txt` 和 `names.txt` 都位于脚本运行的当前目录下。

---

## 📂 文件说明

| 文件名       | 作用                          |
|--------------|-------------------------------|
| data.txt     | 存放火山语音服务的鉴权与配置信息 |
| names.txt    | 存放需要合成语音的物品名称列表   |
| poe_voice_maker.exe （示例） | releases下载 |

---

## 🎵 支持的音色（部分示例）

火山语音提供多种风格的音色，可根据不同场景选择使用：

### 🌟 方言趣味类
| 音色名称   | 语种 | 实例ID                              | 推荐场景   | 操作 |
|------------|------|-------------------------------------|------------|------|
| 湾区大叔   | 中文 | zh_female_wanqudashu_moon_bigtts    | 趣味方言   | -    |
| 呆萌川妹   | 中文 | zh_female_daimengchuanmei_moon_bigtts | 趣味方言   | -    |
| 广州德哥   | 中文 | zh_male_guozhoudege_moon_bigtts     | 趣味方言   | -    |
| 北京小爷   | 中文 | zh_male_beijingxiaoye_moon_bigtts   | 趣味方言   | -    |
| 浩宇小哥   | 中文 | zh_male_haoyuxiaoge_moon_bigtts     | 趣味方言   | -    |

### 🎤 通用场景类
| 音色名称   | 语种       | 实例ID                          | 推荐场景   | 操作 |
|------------|------------|---------------------------------|------------|------|
| 少年梓辛/Brayan | 中/英 | zh_male_shaonianzixin_moon_bigtts | 通用场景   | -    |

### 🎭 角色扮演类
| 音色名称     | 语种 | 实例ID                          | 推荐场景     | 操作 |
|--------------|------|---------------------------------|--------------|------|
| 魅力女友     | 中文 | zh_female_meilinvyou_moon_bigtts | 角色扮演     | -    |
| 深夜播客     | 中文 | zh_male_shenyeboke_moon_bigtts   | 角色扮演     | -    |
| 柔美女友     | 中文 | zh_female_sajiaonvyou_moon_bigtts | 角色扮演     | -    |
| 撒娇学妹     | 中文 | zh_female_yuanqinvyou_moon_bigtts | 角色扮演     | -    |

> 💡 提示：您可以根据个人喜好在 `data.txt` 中设置不同的 `voice_type` 参数。
---
