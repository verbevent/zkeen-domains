## Список доменов выборочного роутинга для проекта XKeen

Подробнее о проекте XKeen по ссылке <https://forum.keenetic.com/topic/16899-xray-на-entware-xkeen/>

Telegram чат - <https://t.me/+SZWOjSlvYpdlNmMy>

Дополнение к zkeen, содержащее IP-подсети - <https://github.com/jameszeroX/zkeen-ip> 

Список доменов в сборке актуален только для Российской Федерации и рекомендован для не дорогих роутеров Keenetic с небольшим объемом оперативной памяти, но может быть использован и на топовых моделях. Так же данный список доменов имеет формат, совместмый с geosite.dat, и может быть использован в любых других проектах, на основе xray-core. Внимание: список доменов zkeen.dat не совместим с sing-box!

Состав включённых в сборку доменов можно посмотеть в файле `/data/domains`

Для тестирования подключения в сборку включены следующие ресурсы:
- <http://myip.tf> - определение вашего IP-адреса
- <https://browserleaks.com> - комплексное тестирование подключения
- <https://nperf.com> - замер скорости подключения

## Ссылка для загрузки крайней версии

- <https://github.com/jameszeroX/zkeen-domains/releases/latest/download/zkeen.dat>

## Пример использования

```json
{
  "routing": {
      "rules": [
      {
        "domain": [
          "ext:zkeen.dat:domains"
        ],
        "inboundTag": ["redirect", "tproxy"],
        "outboundTag": "vless-reality",
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

## Ограничения
Обновление сборки производится по возможности и при наличии у меня свободного времени. Состав сборки определяется мной, и я не гарантирую, что в ней содержатся все необходимые вам домены или, что они будут добавлены в будущих версиях. Если вам необходимы домены, не включенные в сборку, напишите мне об этом в личные сообщения на форуме Keenetic <https://forum.keenetic.com/messenger/compose/?to=20945> или через форму обратной связи <https://jameszero.net/contacts.htm>

## О сборке
Является форком <https://github.com/v2fly/domain-list-community/>
