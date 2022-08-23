# Implementasi Praktikum Git


## Membuat Repository Di Github

![alt](/ScreenShot/part_1.png)

Melakukan Git init dari penyimpana Local kedalam Penyimpanan Remote

```bash
git init
```
![alt](/ScreenShot/part_2.png)

## Membuat Branch Development dari branch Master

```bash
git checkout -b development
```
![alt](/ScreenShot/part_3.png)

Membuat Branch featureA dari branch Development

```bash
git checkout -b featureA
```
![alt](/ScreenShot/part_4.png)

Membuat file bari feature.dart menambahkan beberapa code
```dart
void main(){
  var featureA = 'this is featureA';
  print(featureA);
}
```
## Melakukan git push pada branch featureA atas perubahan code yang telah di buat pada file feature.dart
```bash
git add .
git commit -m "menambahkan featureA"
git push origin featureA
```

Membuat git branch featureB dari branch development
```bash
git checkout development
git checkout -b featureB
```
![alt](/ScreenShot/part_5.png)

## Melakukan git pull featureB dari branch featureA
```bash
git pull origin featurA
```
![alt](/ScreenShot/part_6.png)

## pada saat kita salah saat coding di branch tertentu maka kita melakukan git stash

kita melakukan pengecekan dahulu perubahan apa yang sudah terjadi pada branch yang ingin kita git stash dengan sintaks git status
```bash
git status
```
![apply](/ScreenShot/part_7.png)

Setelah mengetahui perubahan lalu kita melakukan git stash
```bash
git stash
```
![alt](/ScreenShot/part_8.png)

lalu untuk mengembalikan code yang sudah kita git stash kita bisa menggukana git stash apply
```bash
git stash apply
```
![alt](/ScreenShot/part_9.png)

## Melakukan git merge pada branch development

melakukan git merge dari branch development dengan featureA
```bash
git merge --no--ff featureA
```
![alt](/ScreenShot/part_10.png)

melakukan git merge dari branch development dengan featureB
```bash
git merge --no--ff featureB
```
![alt](/ScreenShot/part_11.png)

melakukan git merge dari branch master dengan development
```bash
git merge --no--ff development
```
![alt](/ScreenShot/part_12.png)

## Melakukan conflict 

membuat sebuah function featureA pada branch featureA
```dart
String featureA(){
    return 'this is function featureA';
}
```

membuat sebuah function featureA pada branch featureB
```dart
String featureB(){
    return 'this is function featureB';
}
```

setelah kita melakukan merge pada branch development dengan fetureA dan featureB , maka akan terjadi konflik

![alt](/ScreenShot/part_13.png)

setelah itu kita buat kode menjadi seperti ini

![alt](/ScreenShot/part_14.png)
