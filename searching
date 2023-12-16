#include <stdio.h>
#include <string.h>

// Struktur untuk menyimpan informasi tiket
struct Tiket {
    char namaKereta[50];
    char kelas[20];
    char rute[50];
    int harga;
};

// Fungsi untuk mencari tiket berdasarkan nama kereta
struct Tiket* cariTiket(const char* namaKereta, struct Tiket* daftarTiket, int jumlahTiket) {
    for (int i = 0; i < jumlahTiket; i++) {
        if (strcmp(daftarTiket[i].namaKereta, namaKereta) == 0) {
            return &daftarTiket[i]; // Mengembalikan pointer ke tiket yang ditemukan
        }
    }
    return NULL; // Mengembalikan NULL jika tidak ditemukan
}

// Fungsi untuk menampilkan tiket berdasarkan rute
void tampilkanTiketByRute(const char* rute, struct Tiket* daftarTiket, int jumlahTiket) {
    printf("\nTiket untuk rute '%s':\n", rute);
    for (int i = 0; i < jumlahTiket; i++) {
        if (strcmp(daftarTiket[i].rute, rute) == 0) {
            printf("%s (%s)\n", daftarTiket[i].namaKereta, daftarTiket[i].kelas);
        }
    }
}

int main() {
    // Inisialisasi daftar tiket
    struct Tiket daftarTiket[] = {
        {"Argo Bromo", "Eksekutif", "Jakarta - Surabaya", 150000},
        {"Gajayana1", "Ekonomi", "Jakarta - Surabaya", 120000},
        {"Gajayana2", "Eksekutif", "Surabaya - Malang", 180000},
        {"Malioboro Express1", "Ekonomi", "Surabaya - Malang", 130000},
        {"Malioboro Express2", "Eksekutif", "Malang - Yogyakarta", 200000},
        {"Taksaka1", "Ekonomi", "Malang - Yogyakarta", 135000},
        {"Taksaka2", "Eksekutif", "Semarang - Jakarta", 220000},
        {"Bima", "Ekonomi", "Semarang - Jakarta", 90000},
        {"Gajayana3", "Ekonomi", "Surabaya - Bandung", 170000},
        {"Gajayana4", "Eksekutif", "Surabaya - Bandung", 240000},
        {"Cirebon Express5", "Ekonomi", "Bandung - Jakarta", 120000},
        {"Cirebon Express6", "Eksekutif", "Bandung - Jakarta", 180000},
        // ... tambahkan tiket lain jika diperlukan
    };

    int jumlahTiket = sizeof(daftarTiket) / sizeof(daftarTiket[0]);

    // Menampilkan tiket berdasarkan rute
    tampilkanTiketByRute("Jakarta - Surabaya", daftarTiket, jumlahTiket);
    tampilkanTiketByRute("Surabaya - Malang", daftarTiket, jumlahTiket);
    tampilkanTiketByRute("Malang - Yogyakarta", daftarTiket, jumlahTiket);
    tampilkanTiketByRute("Semarang - Jakarta", daftarTiket, jumlahTiket);
    tampilkanTiketByRute("Surabaya - Bandung", daftarTiket, jumlahTiket);
    tampilkanTiketByRute("Bandung - Jakarta", daftarTiket, jumlahTiket);

    // Meminta input nama kereta yang dicari
    char namaKeretaCari[50];
    printf("\nMasukkan nama kereta yang ingin dicari: ");
    scanf(" %[^\n]s", namaKeretaCari);

    // Memanggil fungsi cariTiket
    struct Tiket* tiketDitemukan = cariTiket(namaKeretaCari, daftarTiket, jumlahTiket);

    // Menampilkan hasil pencarian
    if (tiketDitemukan != NULL) {
        printf("\nInformasi Tiket Ditemukan:\n");
        printf("Nama Kereta: %s\n", tiketDitemukan->namaKereta);
        printf("Kelas: %s\n", tiketDitemukan->kelas);
        printf("Rute: %s\n", tiketDitemukan->rute);
        printf("Harga Tiket: Rp %d\n", tiketDitemukan->harga);
    } else {
        printf("\nTiket dengan nama kereta '%s' tidak ditemukan.\n", namaKeretaCari);
    }

    return 0;
}
