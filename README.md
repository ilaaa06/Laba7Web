## Nur Laila
## 312310149

## PHP Dasar
Buat file baru dengan nama php_dasar.php pada directory tersebut. Kemudian buat
kode seperti berikut.
```sh
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>PHP Dasar</title>
</head>
<body>
    <h1>Belajar PHP Dasar</h1>
    <?php
        echo "Hello World";
    ?>
</body>
</html>
```
![image](https://github.com/user-attachments/assets/36b8889d-452a-4e26-9f92-b853e5a0f7b8)   
HTML Structure:   
HTML untuk struktur dasar halaman web (`<!DOCTYPE html>, <html>, <head>, <body>`).   
PHP Code:   
Di dalam tag PHP (`<?php ?>`), fungsi echo digunakan untuk mencetak teks "Hello World" ke browser.   

## Variable PHP
Menambahkan variable pada program.
```sh
<body>
    <h2>Menggunakan Variable</h2>
</body>
<?php
$nim = "312310149";
$nama = 'Nur Laila';
echo "NIM : " . $nim . "<br>";
echo "Nama : $nama";
?>
```
![image](https://github.com/user-attachments/assets/23a77ff9-4bb0-4f40-9d81-41ec3fc2d8f9)   
Program ini menampilkan form input di mana pengguna bisa memasukkan nama. Setelah tombol kirim ditekan, nama akan dikirimkan menggunakan metode POST.   
Nilai yang dimasukkan diambil menggunakan `$_POST['nama']` dan ditampilkan di halaman yang sama.   

## Predefine Variable $_GET
```sh
<h1>Predefine Variable</h1>
    <?php
    echo 'Selamat Datang ' . $_GET['nama'];
    ?>
```
![image](https://github.com/user-attachments/assets/fc10039b-8296-4bd4-8b4f-34ae4ba30f90)   
Program ini menggunakan `$_GET` untuk mengambil nilai yang dikirim melalui URL. Misalnya, jika URL-nya seperti `?nama=John`, maka program akan menampilkan "Selamat Datang John".   
Contoh penggunaan:   
URL: `example.com/?nama=John`   
Output: "Selamat Datang John"   

## Membuat Form Input
```sh
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>PHP Dasar</title>
</head>
<body>
<h2>Form Input</h2>
<form method="post">
<label>Nama: </label>
<input type="text" name="nama">
<input type="submit" value="Kirim">
</form>
    <?php
    echo 'Selamat Datang ' . $_POST['nama'];
    ?>
</body>
</html>
```
![image](https://github.com/user-attachments/assets/bdfb7cb4-0189-4bc0-b677-1387417f1fc5)   

## Operator
```sh
<?php
$gaji = 1000000;
$pajak = 0.1;
$thp = $gaji - ($gaji*$pajak);
echo "<br> Gaji sebelum pajak = Rp. $gaji <br>";
echo "Gaji yang dibawa pulang = Rp. $thp";
?>
```
![image](https://github.com/user-attachments/assets/ee0e4fc4-78c4-4bb6-93ba-f4ed6fae962e)  
Program ini menggunakan operator aritmatika untuk menghitung gaji setelah dipotong pajak:   

Menghitung pajak:   
Gaji dipotong pajak 10% dengan rumus $gaji * $pajak.  

Menghitung gaji yang dibawa pulang:    
Gaji setelah pajak dihitung dengan $gaji - ($gaji * $pajak).  

## Kondisi IF
```sh
<?php
$nama_hari = date("l");
if ($nama_hari == "Sunday") {
echo "Minggu";
} elseif ($nama_hari == "Monday") {
echo "Senin";
} else {
echo "Selasa";
}
?>
```
![image](https://github.com/user-attachments/assets/5d9f94cd-c6bc-4dfd-a0b8-032477e04ab1)    
Program ini menggunakan **kondisi `if`** untuk mencetak nama hari dalam bahasa Indonesia:   

1. Jika hari adalah "Sunday", mencetak "Minggu".   
2. Jika hari adalah "Monday", mencetak "Senin".   
3. Jika bukan "Sunday" atau "Monday", mencetak "Selasa".  

## Kondisi Switch
```sh
<?php
$nama_hari = date("l");
switch ($nama_hari) {
case "Sunday":
echo "Minggu";
break;
case "Monday":
echo "Senin";
break;
```
![image](https://github.com/user-attachments/assets/f68670c7-4c19-44e9-90c0-9d6d8d44c67b)   
Program menggunakan **`switch`** untuk mencetak nama hari dalam bahasa Indonesia berdasarkan nama hari dalam bahasa Inggris. Contoh: "Sunday" menjadi "Minggu," "Monday" menjadi "Senin."   

## Perulangan For
```sh
<?php
echo "Perulangan 1 sampai 10 <br />";
for ($i=1; $i<=10; $i++) {
echo "Perulangan ke: " . $i . '<br />';
}
echo "Perulangan Menurun dari 10 ke 1 <br />";
for ($i=10; $i>=1; $i--) {
echo "Perulangan ke: " . $i . '<br />';
}
?>
```
![image](https://github.com/user-attachments/assets/00da1a4c-7972-4a89-9d0f-73c43b2370fd)   
Program ini menggunakan **perulangan `for`** untuk dua hal:    

1. **Perulangan naik (1 sampai 10)**:     
   - Dimulai dari `$i = 1`, kondisi `$i <= 10` diperiksa.  
   - Pada setiap iterasi, `$i` dinaikkan (`$i++`).   
   - Perulangan berhenti saat `$i > 10`.   

2. **Perulangan turun (10 ke 1)**:     
   - Dimulai dari `$i = 10`, kondisi `$i >= 1` diperiksa.   
   - Pada setiap iterasi, `$i` diturunkan (`$i--`).  
   - Perulangan berhenti saat `$i < 1`.  
   

## Perulangan While
```sh
<?php
echo "Perulangan 1 sampai 10 <br />";
$i=1;
while ($i<=10) {
echo "Perulangan ke: " . $i . '<br />';
$i++;
}
?>
```
![image](https://github.com/user-attachments/assets/c2716968-0ac6-4798-b0dd-53c5ff261c09)   
Program ini menggunakan **perulangan `while`** untuk mencetak angka dari 1 hingga 10. Perulangan hanya akan dijalankan jika kondisi `($i <= 10)` terpenuhi. Nilai `$i` meningkat setiap iterasi hingga kondisi tidak lagi benar.   

## Perulangan dowhile
```sh
<?php
echo "Perulangan 1 sampai 10 <br />";
$i=1;
do {
echo "Perulangan ke: " . $i . '<br />';
$i++;
} while ($i<=10);
?>
```
![image](https://github.com/user-attachments/assets/20124986-d96f-47a5-8afb-60f9319d8e56)   
Program ini menggunakan **perulangan `do...while`** untuk mencetak angka dari 1 hingga 10. Perulangan dijalankan minimal sekali, karena kondisi diperiksa setelah blok perulangan selesai dijalankan.    

## Jawaban dan Tugas
```sh
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Program PHP Sederhana</title>
</head>
<body>
    <h1>Form Input Data</h1>
    <form method="post" action="">
        <label for="nama">Nama:</label><br>
        <input type="text" id="nama" name="nama" required><br><br>

        <label for="tgl_lahir">Tanggal Lahir:</label><br>
        <input type="date" id="tgl_lahir" name="tgl_lahir" required><br><br>

        <label for="pekerjaan">Pekerjaan:</label><br>
        <select id="pekerjaan" name="pekerjaan" required>
            <option value="Programmer">Programmer</option>
            <option value="Designer">Designer</option>
            <option value="Manager">Manager</option>
        </select><br><br>

        <button type="submit" name="submit">Submit</button>
    </form>

    <?php
    if (isset($_POST['submit'])) {
        // Mengambil data dari form
        $nama = $_POST['nama'];
        $tgl_lahir = $_POST['tgl_lahir'];
        $pekerjaan = $_POST['pekerjaan'];

        // Menghitung umur
        $tanggal_lahir = new DateTime($tgl_lahir);
        $sekarang = new DateTime();
        $umur = $sekarang->diff($tanggal_lahir)->y;

        // Menentukan gaji berdasarkan pekerjaan
        $gaji = 0;
        switch ($pekerjaan) {
            case "Programmer":
                $gaji = 10000000;
                break;
            case "Designer":
                $gaji = 8000000;
                break;
            case "Manager":
                $gaji = 15000000;
                break;
            default:
                $gaji = 0;
                break;
        }

        // Menampilkan output
        echo "<h2>Hasil Output:</h2>";
        echo "Nama: $nama<br>";
        echo "Tanggal Lahir: $tgl_lahir<br>";
        echo "Umur: $umur tahun<br>";
        echo "Pekerjaan: $pekerjaan<br>";
        echo "Gaji: Rp " . number_format($gaji, 0, ',', '.') . "<br>";
    }
    ?>
</body>
</html>
```
![image](https://github.com/user-attachments/assets/dc007d75-9c05-4193-b76f-98341a1dff6e)   
![image](https://github.com/user-attachments/assets/b018c76d-a35d-4b2e-96d9-ab6aa565231e)  
Nama: Nama yang Anda masukkan di form.   
Tanggal Lahir: Tanggal lahir yang Anda input.  
Umur: Umur Anda yang dihitung dari tanggal lahir hingga hari ini.   
Pekerjaan: Pekerjaan yang Anda pilih di form.   
Gaji: Gaji sesuai pekerjaan yang dipilih, dalam format rupiah.  
















