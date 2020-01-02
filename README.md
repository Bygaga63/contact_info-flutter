# Contact info

![image](/images/сapture.PNG)

#### Stateless widgets
*Stateless widgets* - это компоненты, которые не могут содержать состояния, с помощью него уже начинает работать *hot reload*.
Удобная команда для создания виджета *stless*: 
```
class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
```
Hot reload распространяется только на функцию build.
Если изменять глобальные переменные, или создавать эти переменные внутри класса, *hot reload* не подхватывает обнавление

#### pubspec.yaml
*pubspec.yaml* является смесью maven и application.properties если сравнивать с миром java. 
Тут можно как добавлять картинки, шрифты, так и скачивать новые зависимости. 

#### Fonts
Если семейство шрифта меняется, нужно добавлять новое семейство, по нему в коде будет определяться, какой именно шрифт я хочу использовать.
```
  fonts:
    - family: Pacifico
      fonts:
        - asset: fonts/Pacifico-Regular.ttf

    - family: Source Sans Pro
      fonts:
        - asset: fonts/SourceSansPro-Regular.ttf
        
        
    title: Text(
     'bygaga**@gmail.com',
      style: TextStyle(
      color: Colors.teal.shade900,
      fontFamily: 'Source Sans Pro',
      fontSize: 20.0,
    ),
```

#### Цвета 
Цвета можно записывать разными способами
```
Colors.teal.shade100,
Colors.teal[100]
```

#### Margin/Padding
Для отступов используется класс *EdgeInsets*:
```
EdgeInsets.symmetric(vertical: 10.0, horizontal: 25.0),
EdgeInsets.only({})
EdgeInsets.all(double)
...
```