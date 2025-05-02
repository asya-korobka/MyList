Першочергово було реалізовано:\
Відображення списку покупок: Завантажує та відображає список товарів з бази даних Room у компоненті LazyColumn.\
Додавання нових товарів: Дозволяє користувачеві вводити назву нового товару та додавати його до списку (і бази даних).\
Позначення товару як купленого: При натисканні на будь-яку частину картки товару, стан чекбоксу змінюється, і товар відмічається як куплений (оновлюється в базі даних).\
Збереження стану: Використовує Room для локального збереження даних, тому список зберігається між запусками застосунку.

Додаткове доповнення:
- Була реалізована підтримка декількох мов (англійська та українська)\
Англійська локалізація
```
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <string name="app_name">MyList</string>
    <string name="add_item_label">Item Name</string>
    <string name="add_button_text">Add</string>
    <string name="edit">Edit</string>
    <string name="delete">Delete</string>
    <string name="bought_count">Bought: %1$d</string>
    <string name="save">Save</string>
    <string name="cancel">Cancel</string>
    <string name="edit_item">Edit Item</string>
    <string name="new_name">New Name</string>
</resources>
```
Українська локалізація
```
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <string name="app_name">MyList</string>
    <string name="add_item_label">Назва товару</string>
    <string name="add_button_text">Додати</string>
    <string name="edit">Редагувати</string>
    <string name="delete">Видалити</string>
    <string name="bought_count">Куплено: %1$d</string>
    <string name="save">Зберегти</string>
    <string name="cancel">Скасувати</string>
    <string name="edit_item">Редагування товару</string>
    <string name="new_name">Нова назва</string>
</resources>
```
- Можливість редагування та видалення товару 

При повторені за прикладом виникли труднощі з 
```
var toggleState by remember { mutableStateOf(false) }
```
але вони швидко вирішились додаванням 
```
import androidx.compose.runtime.getValue
import androidx.compose.runtime.setValue
```
Також були проблеми з використанням локалізації:\
Після перегляду даного відео https://www.youtube.com/watch?v=ehM1JjCs9PM вони були вирішенні.


