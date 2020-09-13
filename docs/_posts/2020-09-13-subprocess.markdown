---
layout: post
title:  "プログラムからシステムを操作するときの注意点"
date:   2020-09-13 22:11:01 +0900
categories: scope
---
システムに対してシェルコマンドを実行したい時に直接実行するのではなく、ライブラリを介してやった方がいいです。

例えば、pythonでは
```python

import os

os.system('remove -r dir')
```
とかやらない方がいいです。
