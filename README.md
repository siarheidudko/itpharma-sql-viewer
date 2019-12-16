## ITPharma SQL Viewer

Оболочка для Microsoft SQL Server Management Studio на базе ElectronJS

## Совместимость

К сожалению, данная оболочка не совместима с Microsoft SQL Server Management Studio 2018 и более поздних версий, т.к. в них отсутствует возможность полноценного запуска Ssms.exe с SQL-Авторизацией.

## Использование

[Установщик](https://github.com/siarheidudko/itpharma-sql-viewer/releases)

Программное обеспечение ITPharma SQL Viewer (далее ПО) позволяет инициализировать Microsoft SQL Server Management Studio с предварительно заданными host, port, database, user, password настройками, а также синхронизировать настройки подключений с *.json-файлом или с помощью GET-запроса.

Общий вид ПО:  

![Screenshot_1](https://github.com/siarheidudko/itpharma-sql-viewer/raw/master/img/Screenshot_1.jpg)

Меню ПО:  

![Screenshot_2](https://github.com/siarheidudko/itpharma-sql-viewer/raw/master/img/Screenshot_2.jpg)

Настройка соединения (выбор пути к Microsoft SQL Server Management Studio/Ssms.exe):  

![Screenshot_3](https://github.com/siarheidudko/itpharma-sql-viewer/raw/master/img/Screenshot_3.jpg)

Настройка синхронизации данных (данные синхронизируются при запуске программы и кликом на Настройки->Обновить список соединений):  

![Screenshot_4](https://github.com/siarheidudko/itpharma-sql-viewer/raw/master/img/Screenshot_4.jpg)

Запуск приложения Microsoft SQL Server Management Studio с надстройками (Прочее->Запустить SSMS):  

![Screenshot_5](https://github.com/siarheidudko/itpharma-sql-viewer/raw/master/img/Screenshot_5.jpg)

Поиск подключения (регистронезависимый, поиск только по текущей группе):  

![Screenshot_6](https://github.com/siarheidudko/itpharma-sql-viewer/raw/master/img/Screenshot_6.jpg)

## Пример API для синхронизации (*.json-файл или get-запрос)
```
{
	"ООО \"Тест\"": {
		"ООО \"Тест\", Аптека 01": {
			"host": "10.0.0.74",
			"port": "1433",
			"database": "aptekajet",
			"user": "login",
			"password": "password"
		},
		"ООО \"Тест\", Аптека 02": {
			"host": "10.0.0.74",
			"port": "1433",
			"database": "aptekajet_back",
			"user": "login",
			"password": "password"
		}
	}
}
```

## Лицензирование

- Apache-2.0 (Только оболочка)