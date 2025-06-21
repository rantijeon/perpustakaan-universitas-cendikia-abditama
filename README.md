selamat datang di library uca
<html lang="id">
<head>
    <meta charset="UTF-8" />
    <title>Form Peminjaman Buku</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-image: url('https://images.unsplash.com/photo-1524995997946-a1c2e315a42f');
            background-size: cover;
            color: #fff;
            padding: 20px;
        }
        .container {
            background: rgba(0, 0, 0, 0.6);
            padding: 20px;
            border-radius: 10px;
        }
        table {
            width: 100%;
            margin-bottom: 20px;
        }
        td {
            padding: 10px;
        }
        input, select, textarea {
            width: 100%;
            padding: 8px;
            border-radius: 5px;
            border: none;
        }
        .book-category {
            margin-bottom: 30px;
        }
        .books {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        .book {
            cursor: pointer;
            border: 2px solid transparent;
            transition: border 0.3s;
        }
        .book img {
            width: 120px;
            height: 180px;
            border-radius: 5px;
        }
        .book.selected {
            border: 2px solid yellow;
        }
        .btn {
            background-color: yellow;
            border: none;
            padding: 10px 15px;
            border-radius: 5px;
            cursor: pointer;
            color: black;
            font-weight: bold;
        }
        .btn:hover {
            background-color: gold;
        }
        .riwayat {
            margin-top: 30px;
            background: rgba(255, 255, 255, 0.1);
            padding: 15px;
            border-radius: 8px;
        }
        .riwayat h3 {
            margin-top: 0;
        }
        .riwayat-item {
            background: rgba(255, 255, 255, 0.2);
            padding: 10px;
            margin-bottom: 10px;
            border-radius: 5px;
        }
    </style>
</head>
<body>
<div class="container">
    <h1>Form Peminjaman Buku</h1>
    <form id="borrowForm">
        <table>
            <tr><td>Nama</td><td><input type="text" id="nama" /></td></tr>
            <tr><td>NIM</td><td><input type="text" id="nim" /></td></tr>
            <tr><td>Prodi</td><td><input type="text" id="prodi" /></td></tr>
            <tr><td>Tanggal Peminjaman</td><td><input type="date" id="tglPinjam" /></td></tr>
            <tr><td>Tanggal Kembalian</td><td><input type="date" id="tglKembali" /></td></tr>
            <tr><td>Judul Buku</td><td><input type="text" id="judulBuku" readonly /></td></tr>
            <tr><td>Keperluan</td><td><textarea id="keperluan"></textarea></td></tr>
            <tr><td colspan="2" align="right">
                <button type="button" class="btn" onclick="simpanRiwayat()">Simpan</button>
            </td></tr>
        </table>
    </form>

    <h2>Pilih Buku</h2>

    <div class="book-category">
        <h3>Teknik</h3>
        <div class="books">
            <div class="book" data-title="Buku Mesin"><img src="https://iili.io/36hKTgt.jpg" /></div>
            <div class="book" data-title="Buku Codingan C++"><img src="https://iili.io/36XbeTP.jpg" /></div>
            <div class="book" data-title="Buku Python"><img src="https://iili.io/36h3R4t.jpg" /></div>
            <div class="book" data-title="Buku Metode Penelitian"><img src="https://iili.io/36hdd9j.jpg" /></div>
        </div>
    </div>

    <div class="book-category">
        <h3>Ilmu Keperawatan</h3>
        <div class="books">
            <div class="book" data-title="Buku Gizi"><img src="https://iili.io/36hYOHG.jpg"></div>
            <div class="book" data-title="Buku Kesehatan"><img src="https://iili.io/36h0dJe.jpg"></div>
            <div class="book" data-title="Buku Psikologi"><img src="https://iili.io/36hVmsj.jpg"></div>
            <div class="book" data-title="Buku Keperawatan Kritis"><img src="https://iili.io/36hhAVs.jpg"></div>
            <div class="book" data-title="Buku Kegawatdaruratan"><img src="https://iili.io/36hNHR2.jpg"></div>
            <div class="book" data-title="Buku Komunitas"><img src="https://iili.io/36hOfII.jpg"></div>
            <div class="book" data-title="Buku Promkes"><img src="https://iili.io/36heqyQ.jpg"></div>
            <div class="book" data-title="Buku Klinis"><img src="https://iili.io/36hkBls.jpg"></div>
            <div class="book" data-title="Buku Jiwa"><img src="https://iili.io/36hvApR.jpg"></div>
            <div class="book" data-title="Buku Pediatri"><img src="https://iili.io/36h8rSs.jpg"></div>
        </div>
    </div>

    <div class="book-category">
        <h3>Tarbiyah dan Keguruan</h3>
        <div class="books">
            <div class="book" data-title="Buku Agama"><img src="https://iili.io/36h69tf.jpg"></div>
            <div class="book" data-title="Buku Agama Islam"><img src="https://iili.io/36hPzen.jpg"></div>
            <div class="book" data-title="Buku Ulumul Qur'an dan Hadits"><img src="https://iili.io/36hs1ob.jpg"></div>
        </div>
    </div>

    <div class="book-category">
        <h3>Ekonomi dan Bisnis</h3>
        <div class="books">
            <div class="book" data-title="Buku Sejarah Ekonomi"><img src="https://iili.io/36hDS8Q.jpg"></div>
            <div class="book" data-title="Buku Kepemimpinan"><img src="https://iili.io/36hmdmB.jpg"></div>
            <div class="book" data-title="Buku Akuntansi"><img src="https://iili.io/36hyTiX.jpg"></div>
            <div class="book" data-title="Buku Manajemen"><img src="https://iili.io/36jH5u4.jpg"></div>
            <div class="book" data-title="Buku Bisnis"><img src="https://iili.io/36jJP5b.jpg"></div>
        </div>
    </div>

    <div class="riwayat">
        <h3>Riwayat Peminjaman</h3>
        <div id="riwayatList"></div>
    </div>
</div>

<script>
    const books = document.querySelectorAll('.book');
    const judulInput = document.getElementById('judulBuku');
    const form = document.getElementById('borrowForm');

    books.forEach(book => {
        book.addEventListener('click', () => {
            books.forEach(b => b.classList.remove('selected'));
            book.classList.add('selected');
            judulInput.value = book.getAttribute('data-title');
            saveForm();
        });
    });

    form.addEventListener('input', saveForm);

    function saveForm() {
        const formData = ambilDataForm();
        localStorage.setItem('formPeminjaman', JSON.stringify(formData));
    }

    function loadForm() {
        const saved = JSON.parse(localStorage.getItem('formPeminjaman'));
        if (saved) {
            document.getElementById('nama').value = saved.nama;
            document.getElementById('nim').value = saved.nim;
            document.getElementById('prodi').value = saved.prodi;
            document.getElementById('tglPinjam').value = saved.tglPinjam;
            document.getElementById('tglKembali').value = saved.tglKembali;
            document.getElementById('judulBuku').value = saved.judulBuku;
            document.getElementById('keperluan').value = saved.keperluan;

            books.forEach(b => {
                if (b.getAttribute('data-title') === saved.judulBuku) {
                    b.classList.add('selected');
                } else {
                    b.classList.remove('selected');
                }
            });
        }
    }

    function ambilDataForm() {
        return {
            nama: document.getElementById('nama').value,
            nim: document.getElementById('nim').value,
            prodi: document.getElementById('prodi').value,
            tglPinjam: document.getElementById('tglPinjam').value,
            tglKembali: document.getElementById('tglKembali').value,
            judulBuku: document.getElementById('judulBuku').value,
            keperluan: document.getElementById('keperluan').value
        };
    }

    function simpanRiwayat() {
        const data = ambilDataForm();
        if (!data.nama || !data.nim || !data.judulBuku) {
            alert("Harap lengkapi data terlebih dahulu!");
            return;
        }

        let riwayat = JSON.parse(localStorage.getItem('riwayatPeminjaman')) || [];
        riwayat.push(data);
        localStorage.setItem('riwayatPeminjaman', JSON.stringify(riwayat));

        alert("Data berhasil disimpan ke riwayat!");
        localStorage.removeItem('formPeminjaman');
        form.reset();
        books.forEach(b => b.classList.remove('selected'));
        judulInput.value = '';
        tampilkanRiwayat();
    }

    function tampilkanRiwayat() {
        const list = document.getElementById('riwayatList');
        const riwayat = JSON.parse(localStorage.getItem('riwayatPeminjaman')) || [];

        list.innerHTML = "";
        riwayat.forEach((item, index) => {
            list.innerHTML += `
                <div class="riwayat-item">
                    <strong>No:</strong> ${index + 1}<br>
                    <strong>Nama:</strong> ${item.nama}<br>
                    <strong>NIM:</strong> ${item.nim}<br>
                    <strong>Judul Buku:</strong> ${item.judulBuku}<br>
                    <strong>Tanggal Pinjam:</strong> ${item.tglPinjam} → <strong>Kembali:</strong> ${item.tglKembali}<br>
                    <strong>Keperluan:</strong> ${item.keperluan}
                </div>
            `;
        });
    }

    window.onload = function () {
        loadForm();
        tampilkanRiwayat();
    };
</script>
</body>
</html>

