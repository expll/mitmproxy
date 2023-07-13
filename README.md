# mitmproxy  安装启动
```
pip install mitmproxy
mitmproxy -s Home.py --mode regular@8082
```
注意端口需要在系统指定

# 处理请求响应

```
Home.py
from mitmproxy import http
import json
import pymongo

# 连接到MongoDB数据库
client = pymongo.MongoClient("mongodb://admin:admin@localhost:27017/?authMechanism=DEFAULT")
db = client["congcong"]
collection = db["apibook"]

def request(flow: http.HTTPFlow) -> None:
    pass
def response(flow: http.HTTPFlow) -> None:
  pass
```
