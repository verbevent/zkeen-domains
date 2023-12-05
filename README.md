
Форк <https://github.com/v2fly/domain-list-community/> сборки списков доменов для проекта XKeen

Список доменов в сборке актуален только для Российской Федерации

Подробности и обсуждение проекта XKeen по ссылке <https://forum.keenetic.com/topic/16899-xray-на-entware-xkeen/>

## Пример использования

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

## Самостоятельная сборка `domains.dat`

- Установите `golang` и `git` (например `apt get golang git` для Ubuntu 20+)
- Клонируйте код проекта: `git clone https://github.com/jameszeroX/domains-zkeen.git`
- Перейдите в корневую директорию проекта: `cd domains-zkeen`
- Установите зависимости проекта командой: `go mod download`
- Отредактируйте файл `/data/zkeen` по необходимости
- Выполните сборку `domains.dat` командой: `go run ./`
- Используйте созданный в корневой директории проекта файл `domains.dat`
- Be happy!
