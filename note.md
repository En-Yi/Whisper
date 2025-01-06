轉出的 json 可用以下程式讀取 Unicode 字符
```
import json

# Whisper 的 JSON 输出内容
data = '{"text": "\\u65e5\\u672c\\u7684\\u9996"}'

# 解析 JSON 数据
parsed_data = json.loads(data)

# 获取并解码 `text` 字段
text = parsed_data.get("text", "")
# decoded_text = text.encode().decode('unicode_escape')

print("原始 Unicode 字符:", text)
```
