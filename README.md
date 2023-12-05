
Форк <https://github.com/v2fly/domain-list-community/> для сборки списков доменов

# Пример использования

```json
{
  "routing": {
      "rules": [
      {
        "domain": [
          "ext:domains.dat:zkeen"
        ],
        "type": "field",
        "outboundTag": "proxy"
      },
      {
        "type": "field",
        "outboundTag": "direct"
      }
    ]
  }
}
```
