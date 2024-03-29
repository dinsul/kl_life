# Игра "Жизнь"

[![Build Status](https://travis-ci.org/Dinsul/kl_life.svg?branch=master)](https://travis-ci.org/Dinsul/kl_life)

Правила игры взяты из wikipedia
https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life

## Установка и загрузка

Игра будет доступна в виде исходников на gitbub и в виде deb пакета на bintray.
Тестовые сборки для других ОС будут, но куда размещать ещё не знаю.

## Зависимости

Для успешной сборки понадобится SFML-2.5.1, cmake версии 3.10 и manager пакетов conan версии 1.10.
Остальные зависимости: Boost-1.69 и spdlog-1.2.1 установятся автоматически (с помощью conan)

## Сборка

Для сборки понадобится скачать SFML-2.5.1 [ссылка на официальный сайт](https://www.sfml-dev.org/download.php),
содержимое архива распаковать в директорию проекта.

Пример для Linux:
```
wget https://www.sfml-dev.org/files/SFML-2.5.1-linux-gcc-64-bit.tar.gz
tar xvzf SFML-2.5.1-linux-gcc-64-bit.tar.gz
```

Для сборки проекта используйте cmake.

Пример сборки:
```
mkdir Release && cd Release
cmake .. -DCMAKE_BUILD_TYPE=Release
cmake --build .
```

Запуск тестов:

``` cmake --build . --target test ```

Подготовка пакета:

``` cmake --build . --target package ```

## Запуск


## Управление

- MouseLeft   - добавить (оживить) ячейку
- MouseRight  - убрать (убить) ячейку
- MouseMiddle - пермещение поля мышкой
- W, A, S, D  - пермещение поля вверх, налево, вниз, направо соответственно
- Space       - запустить/остановить процесс
- Escape      - выйти
- Delete или BackSpace   - очистить вселенную
- +/-         - изменить размер ячейки
- Enter       - сделать один шаг эволюции
- PageUp      - увеличить скорость эволюции
- PageDown    - уменьшить скорость эволюции

## Поддержка

Если у вас возникли сложности или вопросы пишите мне на e-mail: dinsul@rambler.ru

## Документация

Пользовательскую документацию можно получить по [ссылке](). TODO сделать страничку на gitbub

Документацию API можно получить из исходных кодов пакета с помощью утилиты
[Doxygen](http://www.doxygen.nl/), набрав команду ``` cmake --build . --target doc ```
