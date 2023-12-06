## Список доменов выборочного роутинга для проекта XKeen

Подробнее о проекте XKeen по ссылке <https://forum.keenetic.com/topic/16899-xray-на-entware-xkeen/>

Список доменов в сборке актуален только для Российской Федерации и рекомендован для НЕ топовых роутеров с небольшим размером оперативной памяти, но может быть использован на всех моделях Keenetic.

Состав включённых в сборку доменов можно посмотеть в файле /data/domains

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

## Самостоятельная сборка `zkeen.dat`

- Установите `golang` и `git` (например `apt install golang git` для Ubuntu 20+)
- Клонируйте код проекта: `git clone https://github.com/jameszeroX/zkeen-domains.git`
- Перейдите в корневую директорию проекта: `cd zkeen-domains`
- Установите зависимости проекта: `go mod download`
- Отредактируйте файл `/data/domains` по необходимости
- Выполните сборку `zkeen.dat` командой: `go run ./`
- Используйте созданный в корневой директории проекта файл `zkeen.dat`
- Be happy!

## Ограничения
Обновление сборки производится по возможности и при наличии у меня свободного времени. Состав сборки определяется мной, и я не гарантирую, что в ней содержатся все необходимые вам домены или, что они будут добавлены в будущих версиях. Если вам необходимы домены, не включенные в сборку, пожалуйста, обратите внимание на предыдущий раздел - "Самостоятельная сборка zkeen.dat"

## О сборке
Является форком <https://github.com/v2fly/domain-list-community/> и <https://github.com/schebotar/antifilter-domain>
