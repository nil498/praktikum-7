class DaftarNilaiMahasiswa:
    def __init__(self):
        self.data = []

    def tambah(self):
        print("\n=== Tambah Data Mahasiswa ===")
        nama = input("Masukkan nama: ")
        tugas = float(input("Masukkan nilai Tugas: "))
        uts = float(input("Masukkan nilai UTS: "))
        uas = float(input("Masukkan nilai UAS: "))

        akhir = (tugas * 0.30) + (uts * 0.35) + (uas * 0.35)

        self.data.append({
            "nama": nama,
            "tugas": tugas,
            "uts": uts,
            "uas": uas,
            "akhir": akhir
        })

        print("Data berhasil ditambahkan!\n")

    def tampilkan(self):
        print("\n=== Daftar Nilai Mahasiswa ===")
        if len(self.data) == 0:
            print("Belum ada data.\n")
            return

        for i, mhs in enumerate(self.data, start=1):
            print(f"{i}. {mhs['nama']} | Tugas: {mhs['tugas']} | UTS: {mhs['uts']} | UAS: {mhs['uas']} | Akhir: {mhs['akhir']:.2f}")
        print()

    def hapus(self, nama):
        for mhs in self.data:
            if mhs["nama"].lower() == nama.lower():
                self.data.remove(mhs)
                print(f"Data mahasiswa '{nama}' berhasil dihapus!\n")
                return
        print(f"Data dengan nama '{nama}' tidak ditemukan.\n")

    def ubah(self, nama):
        for mhs in self.data:
            if mhs["nama"].lower() == nama.lower():
                print("\n=== Ubah Data Mahasiswa ===")
                mhs["tugas"] = float(input("Nilai Tugas baru: "))
                mhs["uts"] = float(input("Nilai UTS baru: "))
                mhs["uas"] = float(input("Nilai UAS baru: "))
                mhs["akhir"] = (mhs["tugas"]*0.30) + (mhs["uts"]*0.35) + (mhs["uas"]*0.35)

                print("Data berhasil diubah!\n")
                return
        print(f"Data dengan nama '{nama}' tidak ditemukan.\n")


# MENU UTAMA
if __name__ == "__main__":
    app = DaftarNilaiMahasiswa()

    while True:
        print("=== MENU ===")
        print("1. Tambah Data")
        print("2. Tampilkan Data")
        print("3. Hapus Data")
        print("4. Ubah Data")
        print("5. Keluar")

        pilihan = input("Pilih menu (1-5): ")

        if pilihan == "1":
            app.tambah()
        elif pilihan == "2":
            app.tampilkan()
        elif pilihan == "3":
            nama = input("Masukkan nama yang ingin dihapus: ")
            app.hapus(nama)
        elif pilihan == "4":
            nama = input("Masukkan nama yang ingin diubah: ")
            app.ubah(nama)
        elif pilihan == "5":
            print("Program selesai.")
            break
        else:
            print("Pilihan tidak valid!\n")
    # praktikum-7
