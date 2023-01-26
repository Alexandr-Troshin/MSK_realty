# MSK_realty
Скрипт разработан для получения данных с сайтов investmoskow.ru и cian.ru, их транформации и обработки, автоматического составления отчетов в Excel по полученным данным.  
Архитектурная схема скрипта расположена в файле MSK_realty_diagram.drawio.png.  
После получения данных с сайта ЦИАН, данные агрегируются в разбивке по станциям метро, расстояниям до станции (в минутах), количеству комнат, реновации. Агрегированные данные сохраняются в справочник ЦИАН (Excel-документ).   
Данные, полученные с сайта investMoskow.ru преобразуются для формирования датафрейма, на основании которого можно принимать решения.  
Для распознавания адресов в объявлениях используется NER-модуль Natasha, доработанный для текущей задачи.
В случае отсутствия данных о количестве комнат в объекте - используется ML-модель (Decision Tree), обучаемая на исторических данных и определяющая количество комнат в зависимости от площади объекта, года постройки и этажности дома.  
При формировании датиафрейма из справочника ЦИАН подтягиваются агрегированные данные (по актуальным лотам могут обновляться одновременно с формированием отчета).  
Отчет формируется по актуальным лотам, прошедшим лотам, новым лотам (добавленным между обновлениями либо с внесенными изменениями). Дополнительно сформирован лист "Избранное" (в процессе работы в Excel-отчетами бизнес-Заказчик помечает цветом интересующие позиции, которые после даты проведения торгов переносятся в избранное).  
Другие пометки бизнес-Заказчика не изменяются и остаются после обновления отчета.  
Скрипт не может быть выложен в публичный репозиторий.  
При необходимости, можно связаться со мной посредством:  
 - почта Ray_Beam2@mail.ru  
 - телеграмм @grodno_raymond  
  
Трошин Александр
