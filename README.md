## ajs
# Легенда
Вы решили создать библиотеку, которую можно будет использовать как в браузере, так и в Node.js. Если вы помните, то мы рассматривали Moment.js, в котором бы хитрый код.

Давайте попробуем создать библиотеку, в которой будет такой же код, но генерироваться он, естественно, будет автоматически.

Для этого мы воспользуемся возможностями Webpack.

Цель этого задания следующая: научить вас публиковать пакеты и познакомить с тем, как публикуется большинство пакетов, с которыми мы будем работать в дальнейшем.

Описание
# Шаг 0. Создание репозитория
Перейдите на GitHub и создайте пустой репозиторий для вашего проекта (он нам понадобится для всех остальных действий). Мы будем подразумевать в рамках всей лабораторной работы, что вы назвали репозиторий ajs.

Склонируйте этот репозиторий на вашу локальную машину и все дальнейшие действия выполняйте в каталоге склонированного репо.

# Шаг 1. Генерация проекта
Важно: везде далее под:

USERNAME будет пониматься имя вашего пользователя на GitHub в нижнем регистре (все буквы маленькие)
REPO будет пониматься название вашего репозитория на GitHub в нижнем регистре (все буквы маленькие)
TOKEN будет access token (см. ниже), который вы сгенерируете на GitHub
Создайте репозиторий на GitHub, после чего с помощью npm init --scope=@username (где username - имя вашего пользователя на GitHub в нижнем регистре, например, если на GitHub у меня логин Netology-Code, то команда будет npm init --scope=@netology-code) сгенерируйте package:

package name - @username/ajs (вам предложат автоматически)
version - 1.0.0 (по умолчанию)
description - оставьте пустым (по умолчанию)
entry point - dist/index.js (!надо поменять на dist/index.js)
остальное всё по умолчанию (просто нажимайте enter)
Убедитесь, что в packages.json автоматически прописался адрес вашего репозитория.

Добавьте .gitignore, который мы для вас приготовили.

Сделайте commit и push, убедитесь, что код попал в ваш репозиторий на GitHub

# Шаг 2. Получение Access Token
Мы будем использовать сервис GitHub Packages (куда вы опубликуете свою библиотеку), чтобы не замусоривать npmjs.com.

Для этого, нам нужно получить Access Token.

Перейдите в настройки:

