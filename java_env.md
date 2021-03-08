### 我使用的是jdk8,但是vscode提示java11 or more recent is required？

因为Eclipse平台决定将JDK11作为9月发布的最低要求，而vscode是依赖eclipsejdt.ls服务器的，所以需要更新到JDK11

解决方法：
在settings.json中配置java.configuration.runtimes：
```
"java.home": "/path/to/jdk-11",
"java.configuration.runtimes": [
  {
    "name": "JavaSE-1.8",
    "path": "/path/to/jdk-8",
    "default": true
  },
  {
    "name": "JavaSE-11",
    "path": "/path/to/jdk-11",
  },
]
```
