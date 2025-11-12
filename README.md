流放之路掉落语音生成器

服务使用火山的语音合成大模型 https://console.volcengine.com/ark/region:ark+cn-beijing/tts/speechSynthesis
需要开通按量付费的服务或者新用户开通试用  语音合成大模型-字符版 冲个两块钱就能用

开通火山语音的语音合成大模型服务，并获取到以下信息:
APP ID  /  Access Token  / 	 Voice_type (音色)  /  Cluster (默认就行)
确保data.txt和names.txt在当前目录下:


------------------------

data.txt格式为:

{
    "appid": "你的appid(类似812121212)",
    "access_token": "你的access_token(类似asdasd_FtiR91HxGylLICQVaQXHZk5)",
    "voice_type": "你喜欢的voice_type(类似zh_female_meilinvyou_moon_bigtts)",
    "cluster": "volcano_tts"
}

------------------------

names.txt格式为:

神圣石
改造石
富豪石
                  
------------------------