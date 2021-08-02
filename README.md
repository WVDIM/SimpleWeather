# :partly_sunny: Simple Weather - приложение прогноза погоды

<p align="center">
  <img src="https://i.postimg.cc/CMDRG38p/All-Screens.jpg" alt="All screens"/>
</p>

## :calling: Экраны

### Главный экран

<p align="center">
  <img src="https://i.postimg.cc/nhYDC43x/Main-Screen.jpg" alt="Main screen"/>
</p>

* На этом экране отображается загружаемая из сети текущая погода и прогноз погоды на 8 дней (для отображения используется UITableView)
* При совершении pull-to-refresh происходит обновление погодных данных для текущего места
* Для индикации процесса загрузки погодных данных применяется кастомная анимация shimmer
* С главного экрана можно перейти на экран избранных мест (тап по кнопке с изображением "сендвича" в левом верхнем углу экрана или свайп по экрану вправо) и на экран настроек (тап по кнопке с изображением шестеренки в правом верхнем углу экрана или свайп по экрану влево). Переходы на указанные экраны и возврат с них на главный экран сопровождаются кастомными анимациями
* По умолчанию погодные данные загружаются для геолокации пользователя (используется CoreLocation). Место по умолчанию можно изменить на экране настроек

____

### Экран избранных мест

<p align="center">
  <img src="https://i.postimg.cc/dtCdKPdL/Favorites-Screen.jpg" alt="Favorites screen"/>
</p>

* На этом экране отображается список избранных мест (используется UITableView для отображения и CoreData для хранения данных)
* Избранные места можно добавлять (тап по кнопке с изображением знака "плюс" в правой верхней части экрана) и удалять (свайп влево по избранному месту)
* При тапе по избранному месту происходит возврат на главный экран с последующей загрузкой и отображением погодных данных

____

### Экран настроек

<p align="center">
  <img src="https://i.postimg.cc/W1PZNW6S/Settings-Screen.jpg" alt="Settings screen"/>
</p>

* На этом экране отображается место по умолчанию, для которого загружаются погодные данные
* При тапе по кнопке "Мое местоположение" в качестве места по умолчанию устанавливается геолокация пользователя
* При тапе по кнопке "Ручной ввод" в качестве места по умолчанию устанавливается место, введенное пользователем
* При тапе по кнопке "Выбор на карте" происходит возврат на главный экран с последующим переходом на экран с картой, описание которого представлено ниже. Экран с картой находится в одном navigation-стеке вместе с главным экраном (используется UINavigationController)
* Нажатия на кнопки для изменения места по умолчанию сопровождаются кастомными анимациями
* Для хранения места, установленного по умолчанию, используется UserDefaults
* Аватарка рядом с ником автора приложения в нижней части экрана загружается из сети

____

### Экран с картой

<p align="center">
  <img src="https://i.postimg.cc/GpLsY4fy/Map-Screen.jpg" alt="Map screen"/>
</p>

* На этом экране отображается карта (используется MapKit) и метка по центру карты, координатам которой соответствует адрес, находящийся в верхней части экрана (используется CLGeocoder). При перемещении карты для индикации процесса определения адреса применяется кастомная анимация shimmer
* При тапе по кнопке с изображением галочки в правом верхнем углу экрана происходит возврат на главный экран с последующей установкой в качестве места по умолчанию выбранного места на карте
* При тапе по кнопке с изображением стрелки в левом верхнем углу экрана происходит вовзрат на главный экран

____

## :information_source: Примечания

- [X] Архитектурный паттерн - MVP
- [X] Покрытие тестами различных видов (Unit, UI, Snapshot с использованием библиотеки SnapshotTesting) > 10%
- [X] Использован SwiftLint
- [X] Операционная система, необходимая для работы приложения: iOS 13+
