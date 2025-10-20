## PRAKTIKUM 5

Universitas Pelita Bangsa, Bekasi
Dosen: Agung Nugroho
Mata Kuliah: Pemrograman Web

## nama: Ananda Friezy Eka Cahya
## TI24A1 
## 312410151

## Membuat File HTML Dasar
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Mengenal JavaScript</title>
</head>
<body>
  <h1>Pengenalan JavaScript</h1>
  <h3>Contoh document.write dan console.log</h3>
  <script>
    document.write("Hello World");
    console.log("Hello World");
  </script>
</body>
</html>
```
Output: Tulisan “Hello World” muncul di halaman, dan juga di konsol browser.
<img width="972" height="507" alt="image" src="https://github.com/user-attachments/assets/566e2468-8ea4-46dd-bf2d-84df14810cb0" />


## Eksternal Script & Fungsi Dasar
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Latihan JavaScript Eksternal</title>
  <script type="text/javascript" src="eksternal.js"></script>
</head>
<body>
  <h2>Contoh JavaScript Eksternal dan Fungsi</h2>
  <script>
    function sapa() {
      alert("Halo, Selamat Belajar JavaScript!");
    }
  </script>
  <button onclick="sapa()">Klik untuk Sapa</button>

  <script>
    var nama = prompt("Masukkan Nama Anda:");
    document.write("Halo, " + nama + "!");
  </script>
</body>
</html>

```
output <img width="769" height="183" alt="image" src="https://github.com/user-attachments/assets/996b2ea0-c5de-447b-a8b0-4b55754f2e17" />


## oprasi dan kondisi
```html <!DOCTYPE html>
<html lang="en">
<head>
  <title>Operasi dan DOM JavaScript</title>
</head>
<body>
  <h3>Operasi Aritmatika dan Kondisi</h3>
  <script>
    var a = 10;
    var b = 5;
    var hasil = a + b;
    document.write("Hasil penjumlahan: " + hasil + "<br>");
    if (hasil > 10) {
      document.write("Hasil lebih dari 10<br>");
    } else {
      document.write("Hasil kurang dari atau sama dengan 10<br>");
    }
  </script>

  <h3>Perhitungan Total Harga (DOM)</h3>
  <input type="checkbox" id="item1" value="5000" onclick="hitungTotal()"> Nasi Goreng (Rp5000)<br>
  <input type="checkbox" id="item2" value="3000" onclick="hitungTotal()"> Es Teh (Rp3000)<br>
  <p>Total: Rp<span id="total">0</span></p>

  <script>
    function hitungTotal() {
      let total = 0;
      if (document.getElementById('item1').checked) total += 5000;
      if (document.getElementById('item2').checked) total += 3000;
      document.getElementById('total').innerText = total;
    }
  </script>
</body>
</html>
```
output <img width="539" height="418" alt="image" src="https://github.com/user-attachments/assets/61b423e5-e454-4651-8e55-a70f6030e9d7" />

## validasi form
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Validasi Form JavaScript</title>
  <script>
    function validateForm() {
      const nama = document.forms["formValidasi"]["nama"].value.trim();
      const email = document.forms["formValidasi"]["email"].value.trim();
      const pesan = document.forms["formValidasi"]["pesan"].value.trim();
      const emailPattern = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;

      if (nama === "") {
        alert("Nama harus diisi!");
        return false;
      } else if (!email.match(emailPattern)) {
        alert("Email tidak valid!");
        return false;
      } else if (pesan === "") {
        alert("Pesan harus diisi!");
        return false;
      } else {
        alert("Form berhasil dikirim!");
        return true;
      }
    }
  </script>
</head>
<body>
  <h3>Form Validasi</h3>
  <form name="formValidasi" onsubmit="return validateForm()">
    Nama: <input type="text" name="nama"><br><br>
    Email: <input type="text" name="email"><br><br>
    Pesan: <textarea name="pesan"></textarea><br><br>
    <input type="submit" value="Kirim">
  </form>
</body>
</html>
```
output 
<img width="631" height="389" alt="image" src="https://github.com/user-attachments/assets/d2208f92-4956-4e0f-8e82-118712094b7f" />
