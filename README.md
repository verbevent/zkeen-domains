## Список доменов выборочного роутинга для проекта XKeen

Подробнее о проекте XKeen по ссылке <https://forum.keenetic.com/topic/16899-xray-на-entware-xkeen/>

Список доменов в сборке актуален только для Российской Федерации и рекомендован для НЕ топовых роутеров с небольшим размеров оперативной памяти, но может быть использован на всех моделях Keenetic.

Состав включённых в сборку доменов можно посмотеть в файле /data/zkeen

## Ссылка для загрузки крайней версии

- **domains.dat**：<https://github.com/jameszeroX/domains-zkeen/releases/latest/download/domains.dat>

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

- Установите `golang` и `git` (например `apt install golang git` для Ubuntu 20+)
- Клонируйте код проекта: `git clone https://github.com/jameszeroX/domains-zkeen.git`
- Перейдите в корневую директорию проекта: `cd domains-zkeen`
- Установите зависимости проекта: `go mod download`
- Отредактируйте файл `/data/zkeen` по необходимости
- Выполните сборку `domains.dat` командой: `go run ./`
- Используйте созданный в корневой директории проекта файл `domains.dat`
- Be happy!

## Ограничения
Обновление сборки производится по возможности и при наличии у меня свободного времени. Состав сборки определяется мной и я не гарантирую, что в ней содержатся все необходимые вам домены или, что они будут добавлены в будущих версиях. Если вам необходимы домены не включенные в сборку, пожалуйста, обратите внимение на предыдщущий раздел - "Самостоятельная сборка domains.dat"

## О сборке
Является форком <https://github.com/v2fly/domain-list-community/> и <https://github.com/schebotar/antifilter-domain>
