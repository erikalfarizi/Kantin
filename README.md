# Project_UAS

| NAMA   | ERIK ALFARIZI |
| --- | --- |
| NIM    | 312310622 |
| KELAS  | TI.23.A6 |
| DOSEN  | Agung Nugroho,S.Kom.,M.Kom |



<h1> Berikut adalah penjelasan tentang cara membuat program kasir di kantin <h1>
  
<h3> Membuat Class Kantin: <h3>

<h4>- &nbsp; Program dimulai dengan membuat kelas Kantin.<h4>
<h4>- &nbsp; Constructor __init__ digunakan untuk menginisialisasi atribut seperti menu, keranjang belanja, dan total harga.<h4>

<h3> Menu Kantin dalam Dictionary: <h3> 

<h4>- &nbsp; Menu kantin disusun dalam bentuk dictionary, di mana setiap item memiliki nomor, nama, dan harga.<h4>
<h4>- &nbsp; Ini mempermudah pengelolaan dan pemanggilan menu saat pengguna memilih makanan.<h4>

<h3> Menampilkan Menu Kantin: <h3> 

<h4>- &nbsp; Metode show_menu digunakan untuk menampilkan menu kantin ke pengguna.<h4>
<h4>- &nbsp; Pengguna dapat melihat nomor, nama, dan harga setiap item.<h4>

<h3> Menerima Pesanan Pengguna: <h3> 

<h4>- &nbsp; Metode take_order meminta input pengguna untuk memilih nomor menu dan jumlah pesanan.<h4>
<h4>- &nbsp;  pesanan disimpan dalam keranjang belanja.<h4>

<h3> Menghitung Total Harga: <h3> 

<h4>- &nbsp; Metode calculate_total_price menghitung total harga dari item yang dipesan dalam keranjang belanja.<h4>

<h3> Menghasilkan Struk Pembelian: <h3> 

<h4>- &nbsp; Metode generate_receipt digunakan untuk mencetak struk pembelian.<h4>
<h4>- &nbsp; Struk mencantumkan setiap item, jumlah, dan harga total, serta total keseluruhan pembelian.<h4>

<h3> Menjalankan Program:<h3> 

<h4>- &nbsp; Metode run mengatur urutan operasi utama program, termasuk menampilkan menu, menerima pesanan, menghitung total harga, dan mencetak struk pembelian.<h4>

<h1> Berikut adalah contoh codingannya <h1>

<h5>

```python
menu = {
    'mie ayam': {'price': 12000},
    'bakso': {'price': 15000},
    'soto': {'price': 18000},
    'es teh': {'price': 5000},
    'kopi': {'price': 7000}
}

def show_menu():
    print("Menu makanan/minuman:")
    for item, details in menu.items():
        print(f"{item.capitalize()}-Rp{details['price']}")

def calculate_total(selected_items):
    total = 0
    for item in selected_items:
        total += menu[item]['price']
    return total

def generate_receipt(selected_items, total_price):
    print("\nStruk pembelian:")
    for item in selected_items:
        print(f"{item.capitalize()}: Rp{menu[item]['price']}")
    print(f"\nTotal harga: Rp{total_price}")

def main():
    selected_items = []
    show_menu()

    while True:
        choice = input("\nPilih makanan/minuman (atau ketik 'selesai' untuk selesai): ")

        if choice.lower() == 'selesai':
            break

        if choice in menu:
            selected_items.append(choice)
        else:
            print("menu tidak valid, silahkan pilih lagi.")

    total_price = calculate_total(selected_items)
    generate_receipt(selected_items, total_price)

if __name__ == "__main__":
    main()
```
<h5>

<h1> Berikut adalah link video cara membuatnya <h1>
<h4> https://youtu.be/aQcLVkgOXPM?si=2FccI72HuJrm3kkW</h4>
