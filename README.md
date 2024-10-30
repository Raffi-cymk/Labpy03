# Labpy03
Latihan 1: Menampilkan n Bilangan Acak yang Lebih Kecil dari 0.5

[](<Flowchart Latihan 1.png>)

Python Code↓

Import random

# Meminta input jumlah bilangan acak
n = int(input("Masukkan jumlah bilangan acak yang ingin ditampilkan: "))

# Menghasilkan dan menampilkan bilangan acak yang lebih kecil dari 0.5
for i in range(n):
    bilangan_acak = random.random()
    if bilangan_acak < 0.5:
        print(f"Bilangan acak ke-{i + 1}: {bilangan_acak}")


Alur Algoritma:

1. Import modul random untuk mengakses fungsi random().

2. Minta input dari pengguna untuk memasukkan nilai n, yaitu jumlah bilangan acak yang akan ditampilkan.

3. Gunakan perulangan for atau while untuk menghasilkan dan menampilkan bilangan acak sebanyak n kali.

4. Setiap iterasi, gunakan random() untuk menghasilkan bilangan acak antara 0 dan 1.

5. Cek jika bilangan tersebut kurang dari 0.5, lalu cetak bilangan tersebut.


6. Ulangi langkah 4 hingga jumlah bilangan acak yang ditampilkan mencapai n.

---

Latihan 2: Menghitung Total Keuntungan Selama 8 Bulan

Python Code↓
# Inisialisasi modal awal dan keuntungan total
modal_awal = 100000000
total_keuntungan = 0

# Persentase keuntungan per bulan selama 8 bulan
persentase_keuntungan = [0, 0, 0.01, 0.01, 0.05, 0.05, 0.05, 0.03]

# Menghitung keuntungan tiap bulan
for bulan in range(8):
    keuntungan_bulanan = modal_awal * persentase_keuntungan[bulan]
    total_keuntungan += keuntungan_bulanan
    print(f"Bulan ke-{bulan + 1}: Keuntungan = {keuntungan_bulanan}")

# Menampilkan total keuntungan selama 8 bulan
print(f"Total keuntungan selama 8 bulan adalah: {total_keuntungan}")


Alur Algoritma:

1. Inisialisasi variabel modal_awal dengan nilai 100 juta (100000000) dan total_keuntungan dengan nilai 0.


2. Buat variabel untuk menyimpan persentase keuntungan per bulan sesuai dengan ketentuan berikut:

Bulan ke-1 dan ke-2: Keuntungan 0%.

Bulan ke-3 dan ke-4: Keuntungan 1%.

Bulan ke-5 hingga ke-7: Keuntungan 5%.

Bulan ke-8: Keuntungan 3%.


3. Gunakan perulangan untuk menghitung keuntungan tiap bulan selama 8 bulan.

4. Di dalam perulangan, tambahkan keuntungan bulanan ke total_keuntungan berdasarkan persentase keuntungan yang telah ditentukan.


5. Setelah perulangan selesai, cetak total_keuntungan sebagai hasil dari akumulasi keuntungan selama 8 bulan.

---

Latihan 3: Simulasi Mesin ATM Sederhana

Python Code↓
# Inisialisasi saldo awal
saldo = 1000000

while True:
    # Menampilkan menu
    print("\n=== Mesin ATM Sederhana ===")
    print("1. Cek Saldo")
    print("2. Tarik Uang")
    print("3. Keluar")
    pilihan = input("Pilih menu (1/2/3): ")

    # Cek Saldo
    if pilihan == "1":
        print(f"Saldo Anda saat ini: Rp {saldo}")

    # Tarik Uang
    elif pilihan == "2":
        jumlah_tarik = int(input("Masukkan jumlah penarikan: "))
        if jumlah_tarik <= saldo:
            saldo -= jumlah_tarik
            print(f"Penarikan berhasil. Saldo Anda sekarang: Rp {saldo}")
        else:
            print("Saldo tidak mencukupi untuk penarikan.")

    # Keluar
    elif pilihan == "3":
        print("Terima kasih telah menggunakan ATM ini.")
        break

    # Pilihan tidak valid
    else:
        print("Pilihan tidak valid. Silakan coba lagi.")


Alur Algoritma:

1. Tentukan saldo awal sebesar Rp1.000.000.


2. Tampilkan menu opsi kepada pengguna:

Cek Saldo

Tarik Uang

Keluar


3. Jika pengguna memilih opsi "Cek Saldo", tampilkan jumlah saldo saat ini.

4. Jika pengguna memilih "Tarik Uang":

Minta pengguna untuk memasukkan jumlah penarikan.

Cek apakah jumlah penarikan tidak melebihi saldo yang ada.

Jika saldo mencukupi, kurangi saldo dengan jumlah penarikan dan tampilkan saldo yang tersisa.

Jika saldo tidak mencukupi, tampilkan pesan bahwa saldo tidak mencukupi.

5. Jika pengguna memilih "Keluar", akhiri program.

6. Ulangi langkah 2 hingga pengguna memilih untuk keluar.
