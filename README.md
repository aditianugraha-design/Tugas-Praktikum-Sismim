# Tugas-Praktikum-Sismim
git ini dibuat untuk melunasi atau mengerjakan tugas praktikum mata kuliah sismik

 int led[] = {2, 3, 4, 5, 6, 7};//Digunakan untuk menyimpan nomor pin Arduino yang terhubung ke LED.
LED dibagi menjadi:
Kiri → indeks 0–2 (pin 2, 3, 4)

Kanan → indeks 3–5 (pin 5, 6, 7)

for(int i = 0; i < 6; i++){
  pinMode(led[i], OUTPUT);
}//Semua pin LED diatur sebagai OUTPUT agar dapat mengontrol nyala/mati LED.

for(int i = 0; i < 3; i++){
  digitalWrite(led[i], HIGH);
}//Perulangan ini menyalakan 3 LED pertama secara bersamaan.

for(int i = 3; i < 6; i++){
  digitalWrite(led[i], LOW);
}//Digunakan agar LED kanan tidak menyala bersamaan dengan LED kiri.

delay(500);//Memberikan jeda agar perubahan nyala LED terlihat jelas oleh mata.

for(int i = 0; i < 3; i++){
  digitalWrite(led[i], LOW);
}//Semua LED kiri dimatikan sebelum berpindah ke LED kanan.

for(int i = 3; i < 6; i++){
  digitalWrite(led[i], HIGH);
}//LED bagian kanan menyala secara bersamaan.
