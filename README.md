<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Simulasi Pembayaran THR</title>
</head>
<body>
<html>
<h2>Input Data</h2>
<p>Gaji Pokok: <input type="number" id="gajiPokok"></p>
<p>Tunjangan Tetap: <input type="number" id="tunjanganTetap"></p>
<p>Masa Kerja (dalam tahun): <input type="number" id="masaKerja"></p>
<button onclick="hitungTHR()">Hitung THR</button>
<button onclick="hitungTHRdanPPH()">Hitung THR dan PPH</button>

<h2>Output</h2>
<p>THR: <span id="outputTHR"></span></p>
<p>PPH: <span id="outputPPH"></span></p>
<p>Total Pembayaran: <span id="outputTotal"></span></p>


<script>
function hitungTHR() {
  var gajiPokok = parseFloat(document.getElementById("gajiPokok").value);
  var tunjanganTetap = parseFloat(document.getElementById("tunjanganTetap").value);
  var masaKerja = parseInt(document.getElementById("masaKerja").value);
}
  
  // Logika Perhitungan THR
  var thr = 0;
  if (masaKerja < 12) {
    thr = 0;
  } else if (masaKerja >= 1 && masaKerja < 6) {
    thr = gajiPokok * 1;
  } else if (masaKerja >= 6 && masaKerja < 12) {
    thr = gajiPokok * 2;
  } else {
    thr = gajiPokok * 3;
  }
  
  // Total THR
  var totalTHR = thr + tunjanganTetap;
 





function hitungTHRdanPPH() {
  var gajiPokok = parseFloat(document.getElementById("gajiPokok").value);
  var tunjanganTetap = parseFloat(document.getElementById("tunjanganTetap").value);
  
  // Logika Perhitungan THR
  var thr = gajiPokok * 0.05; // 5% dari gaji pokok
  
  // PPH (Pajak Penghasilan)
  var ptkp = 4500000; // PTKP (Pendapatan Tidak Kena Pajak)
  var totalGaji = gajiPokok + tunjanganTetap + thr;
  var pph = 0;
  if (totalGaji > ptkp) {
    pph = (totalGaji - ptkp) * 0.05;
  }
  
  // Total Pembayaran
  var totalPembayaran = thr - pph;
  
  // Menampilkan Output
  var outputTHR = document.getElementById("outputTHR");
  outputTHR.innerHTML = "Rp " + thr.toFixed(2);
  
  var outputPPH = document.getElementById("outputPPH");
  outputPPH.innerHTML = "Rp " + pph.toFixed(2);
  
  var outputTotal = document.getElementById("outputTotal");
  outputTotal.innerHTML = "Rp " + totalPembayaran.toFixed(2);
}
</script>

</body>
</html>

<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Document</title>
</head>
<body>
<h1>Look Into Yourself</h1>
<p>
<b><u>Look into yourself, </u></b>
<br>Release your heart free<br> Look into yourself, and be the master of your destiny
</p>
</body>
</html>
