---
layout: post
title: Python数据操作
categories: Analytics
---

pandasql

```
from pandasql import sqldf
pysqldf = lambda q: sqldf(q, globals())

print(pysqldf("SELECT * FROM meat LIMIT 10;"))
```

时快时慢