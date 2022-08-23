# Alta.id

## Implementasi Praktikum Git


Membuat Repository Di Github

![alt](/ScreenShot/part_1.png)

Melakukan Git init dari penyimpana Local kedalam Penyimpanan Remote

```bash
git init
```
![alt](/ScreenShot/part_2.png)

Membuat Branch Development dari branch Master

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
```bash
void main(){
  var featureA = 'this is featureA';
  print(featureA);
}
```
Melakukan git push pada branch featureA atas perubahan code yang telah di buat pada file feature.dart
```bash
git add .
git commit -m "menambahkan featureA"
git push origin featureA
```