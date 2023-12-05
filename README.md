
Форк <https://github.com/v2fly/domain-list-community/> сборки списков доменов для проекта XKeen

Список доменов в сборке актуален только для Российской Федерации

Подробности и обсуждение проекта XKeen по ссылке <https://forum.keenetic.com/topic/16899-xray-на-entware-xkeen/>

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
