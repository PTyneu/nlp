ДИСКЛЕЙМЕР. Данный проект сделан примерно на половину от того, что я хочу увидеть в конце, но вцелом первоочередную задачу (поработать с Бертом) он выполняет. 

Использованные библиотеки указаны в файле requirements.txt.

В данной работе была проведена оценка тональности комментариев, а также получены статистические результаты до и поcле генерации эмбеддингов при помощи Берта, помимо этого в работе проведена классическая для NLP разбивка TF-IDF, лемматизация английского, очистка текста от мусорных символов, удаление стоп слов и приведение текста к нижнему регистру, дабы  не создавать лишних фич в мешке слов. 

Дорабатывать проект планирую следующим образом: для более наглядной визуализации результатов планирую добавить ROC-AUC кривую, разобраться с проблемой инициализации метода опорных векторов с тем же названием во второй раз (после Берта). Также гиперпараметры моделей на даннный момент подобраны чисто эмпирически, их оптимальность не подкреплена приблизительно ничем, поэтому в будущем вполне вероятно придется инициализировать либо поиск параметров на кросс-валидации либо рандомный подбор параметров,с чем я также не работал и что также хотел бы попробовать. 

В плане развития проекта есть желание попробовать в негативных комментариях попытаться заменить слова либо на синонимы, либо  если брать матерные, то на символы типа звездочек и тд, однако для русского языка я еще не нашел аналога nlpaug, поэтому если кто-то будет читать это и будет в курсе, как можно провести аугментацию, буду рад. Также планирую побаловаться с Элмо.

Промежуточные выводы по работе следующие: 1) Вцелом на таком объеме фичей метод опорных векторов даже до генерации эмбеддингов показывает себя неплохо, однако если брать все модели машинного обучения и инициализированный перцептрон, то Берт дает огромный прирост к риколу (полноте), что позволяет говорить о том, что для конкретно данной задачи он мне необходим 2)В колабе инициализировать Берта на относительно большом датасете не имеет особо смысла, тк объем оперативки ограничен.


<img width="488" alt="Снимок экрана 2021-09-29 в 00 13 50" src="https://user-images.githubusercontent.com/90149954/135166686-9a179f6c-5921-4176-a135-f03cbadf466d.png">
