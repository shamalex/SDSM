# Способы подключения

В Packet Tracer’e управлять оборудованием можно следующими способами:

* [GUI](http://ru.wikipedia.org/wiki/Графический_интерфейс_пользователя)
* [CLI](http://ru.wikipedia.org/wiki/Интерфейс_командной_строки) в окне управления
* Терминальное подключение с рабочей станции через консольный кабель
* telnet

Интерфейс последних трёх идентичный – отличается лишь способ подключения. Разумеется, GUI – не наш метод.  
В реальной же жизни доступны:

* Telnet/ssh
* Терминальное подключение с рабочей станции через консольный кабель
* Web-интерфейс \([Cisco SDM](http://www.cisco.com/global/RU/products/sw/secursw/ps5318/index.shtml)\).

Последний вариант даже не упоминайте в приличном обществе. Даже если вы адепт мыши и браузера, очень не советую.  
На своём примере при работе с другим оборудованием я сталкивался с тем, что настроенное через веб не работает. Хоть ты тресни, но не работает. А у того же длинка вообще был баг в одной версии прошивки для свичей: если изменить настройки VLAN в веб-интерфейсе из под линукс, то свич становится недоступным для управления. Это официально признанная проблема\).

[Телнет](http://ru.wikipedia.org/wiki/Telnet) – стандартная, всем известная утилита, как и [ssh](http://ru.wikipedia.org/wiki/SSH). Для доступа к cisco по этим протоколам нужно настроить пароли доступа, об этом позже. Возможность использования ssh зависит от лицензии IOS.
