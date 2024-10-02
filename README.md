# Определение эмоциональности текста 
Данный код позволяет определить эмоциональность текста, негативный, нейтральный и позитивный.
## Содержание
* [Установка](#установка)  
* [Процесс обработки данных](#процесс-обработки-данных)  
* [Выбор алгоритма](#выбор-алгоритма)  
* [Результаты оценки модели](#результаты-оценки-модели) 
* [Выводы](#выводы)  

## Установка
* *Установите  необходимые  библиотеки:*  `pip install -r requirements.txt` 
## Процесс обработки данных
* *Очистка текстов от ссылок, специальных символов и чисел* 
* *Приведение текстов к нижнему регистру.* 
* *Удаление стоп-слов.*
## Выбор алгоритмов
 В качестве алгоритма я решил рассмотреть все 3 предложенных алгоритма с перебором гиперпараметров:  
* Logistic Regression
* Naive Bayes
* Decision Tree  

В качестве векторного представления я рассматрел 2 вариации:
* Bag-of-Words 
* TF-IDF  
## Результаты оценки модели 
### Для logistic Regression:
#### Bag-of-Words:  
* Accuracy: 0.70  
* Precision: 0.71  
* Recall: 0.70  
* F1 Score: 0.70  
* Confusion matrix  

 <img src="images\log_bow.png" width="400" height="350">   

### TF-IDF:
* Accuracy: 0.63  
* Precision: 0.69  
* Recall: 0.63  
* F1 Score: 0.59  
* Confusion matrix 

<img src="images\log_tf.png" width="400" height="350">

## Naive Bayes: 
#### Bag-of-Words:
* Accuracy: 0.70
* Precision: 0.72
* Recall: 0.70
* F1 Score: 0.70
* Confusion matrix 

<img src="images\ba_bow.png" width="400" height="350">

### TF-IDF:
* Accuracy: 0.72
* Precision: 0.72
* Recall: 0.72
* F1 Score: 0.72
* Confusion matrix 

<img src="images\ba_tf.png" width="400" height="350">

## Decision Tree:
### Bag-of-Words:
* Accuracy: 0.58
* Precision: 0.58
* Recall: 0.58
* F1 Score: 0.57
* Confusion matrix

<img src="images\tree_bow.png" width="400" height="350">

### TF-IDF
* Accuracy: 0.60
* Precision: 0.62
* Recall: 0.60
* F1 Score: 0.57
* Confusion matrix

<img src="images\tree_tf.png" width="400" height="350">

# Выводы
## Logistic Regression:
* Модель показала лучшие результат c Bag-of-Words, особенно по Precision и по F1 Score
* Использование TF-IDF привело к снижению всех метрик
* Матрица ошибок показала, что лучше всего определяется нетральный текст, а хуже всего негативный.
##  Naive Bayes
* Обе модели показали сопоставимые результаты с Bag-of-Words и TF-IDF, но все же немного лучше с TF-IDF.
* Матрица ошибок для  Bag-of-Words показала, что лучше всего определяется негативный текст, а хуже всего нейтральный. А для TF-IDF  лучше всего определяется нейтральный, а хуже всего негативный
## Decision Tree
* Результаты были наименее удовлетворительными среди всех моделей.
* Матрица ошибок показала, что лучше всего определяется нетральный текст, а хуже всего негативный.