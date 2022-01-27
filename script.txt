1. Отобразить подключённый девайс в консоли.

$ adb devices
List of devices attached
L7MJZT79HIGUYTS4	device

2. Вывести адрес приложения todolist в системе Android

$ adb shell pm list packages | grep todolist
package:com.android.todolist

3. Установить .apk файл приложениия todolist на телефон с компьютера через  ADB

$ adb install Desktop/ToDoList.apk
Success


4. Сделать скриншот запущенного приложения todolist и сразу скопировать на компьютер в одной команде.

$ adb shell screencap -p /storage/emulated/0/DCIM/Screenshots/screenshot_1.jpg
$ adb pull /storage/emulated/0/DCIM/Screenshots/screenshot_1.jpg /home/me/Desktop/screenshot_1.jpg


5. Вывести в консоль логи приложения todolist

$ adb logcat "com.android.todolist"

6. Скопировать логи приложения todolist на компьютер.

$ adb logcat  "com.android.todolist" > /home/me/Desktop/todolist.log

7. Удалить приложение todolist с телефона через ADB

$ adb uninstall "com.android.todolist"
