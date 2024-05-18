## Список доменов выборочного роутинга для проекта XKeen

Подробнее о проекте XKeen по ссылке <https://forum.keenetic.com/topic/16899-xray-на-entware-xkeen/>

Telegram <https://t.me/+SZWOjSlvYpdlNmMy>

С помощью данного списка вы можете помочь Роскомнадзору и заблокировать себе сайты, посещение которых в России запрещено.

Дополнение к zkeen, содержащее IP-подсети - <https://github.com/jameszeroX/zkeen-ip> 

Состав включённых в сборку доменов можно посмотеть в файле `/data/domains`

Для тестирования в сборку включены следующие ресурсы:
- <http://myip.tf> - определение вашего IP-адреса
- <https://browserleaks.com> - комплексное тестирование
- <https://nperf.com> - замер скорости

## Ссылка для загрузки крайней версии

- <https://github.com/jameszeroX/zkeen-domains/releases/latest/download/zkeen.dat>

## Пример использования

```json
{
  "routing": {
      "rules": [
      {
        "domain": [
          "ext:zkeen.dat:domains",
          "ext:zkeen.dat:other"
        ],
        "inboundTag": ["redirect", "tproxy"],
        "outboundTag": "block",
        "type": "field"
      },
      {
        "inboundTag": ["redirect", "tproxy"],
        "outboundTag": "direct",
        "type": "field"
      }
    ]
  }
}
```

## Самостоятельная сборка `zkeen.dat`

- Установите `golang` и `git` (например `apt install golang git` для Ubuntu 20+)
- Клонируйте код проекта: `git clone https://github.com/jameszeroX/zkeen-domains.git`
- Перейдите в корневую директорию проекта: `cd zkeen-domains`
- Установите зависимости проекта: `go mod download`
- Отредактируйте по необходимости файл `/data/domains`
- Выполните сборку командой: `go run ./`
- Используйте созданный в корневой директории проекта файл `zkeen.dat`
- Be happy!

## Источники
- https://community.antifilter.download
- https://github.com/itdoginfo/allow-domains
- Собственные наблюдения
