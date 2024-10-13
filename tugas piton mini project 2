from prettytable import PrettyTable
table = PrettyTable()
import time

admin = {
    "Zidan": "123"
}

data_user = {
    "didi": "234",
    "spontan": "1123",
    "gratis": "421",
    "pelis": "235",
    "akbar": "354",
    "takbir": "355",
    "kanan": "67567",
    "kiri": "789",
    "Bintang": "7467"
}


def login():
    while True:
        username = input("Masukkan username: ")
        password = input("Masukkan password: ")
        
        if username in admin and admin[username] == password:
            print("Selamat datang, Admin!")
            return menu_admin()
        for user in data_user:
            if user[1] == username and user[2] == password:
                print("Selamat datang, User!")
                return buyer_menu(username)
        else:
            print('username ato password salah')

data_user = [
    [1, "didi", "234", "3 jam"],
    [2, "spontan", "1123", "1 jam 20 menit"],
    [3, "gratis", "421", "2 jam"],
    [4, "pelis", "235", "10 jam"],
    [5, "akbar", "354", "30 menit"],
    [6, "takbir", "355", "3 menit"],
    [7, "kanan", "67567", "2 jam"],
    [8, "kiri", "789", "4 jam"],
    [9, "Bintang", "7467", "4 jam"]
]
user = data_user

def menu_admin():
    while True:
        print('\nMenu Mimin')
        print('1. Tambah pengguna')
        print('2. Lihat Pengguna')
        print('3. Update Pengguna')
        print('4. Hapus Pengguna')
        print('5. Keluar')
        opsi = input('Pilih opsi: ')

        if opsi == '1':
            tambah_user()
        elif opsi == '2':
            lihat_user()
        elif opsi == '3':
            update_user()
        elif opsi == '4':
            hapus_user()
        elif opsi == '5':
            print('kembali lagi lain waktu ya min!!')
            break
        else:
            print('Opsi tidak valdi.')

def tambah_user():
    username = input('Masukkan username baru: ')
    password = input('Masukkan password baru: ')
    waktu = input('Masukkan waktu: ')
    for user in data_user:
        if user[1] == username:
            print('Username sudah ada!')
            return
    user_baru = len(data_user) + 1
    data_user.append([user_baru, username, password, waktu])
    print(f'Pengguna {username} berhasil ditambahkan.')

def lihat_user():
    table = PrettyTable()
    table.field_names = ['No.', 'Username', 'Password', 'Waktu']
    for user in data_user:
        table.add_row(user)
    print(table)

def update_user():
    username = input('Masukkan username yang mau diupdate: ')
    for user in data_user:
        if user[1] == username:
            Password_baru = input('Masukkan password baru: ')
            waktu_baru = input('Masukkan total waktu: ')
            user[2] = Password_baru
            user[3] = waktu_baru
            print(f'Pengguna {username} berhasil diupdate.')
            return
        else:
            print('Pengguna tidak ditemukan.')

def hapus_user():
    username = input('Masukkan username yang ingin dihapus: ')
    if user in data_user:
        del user[data_user]
        print(f'Pengguna {data_user} berhasil dihapus.')
    else:
        print('Pengguna tidak ditemukan.')

def buyer_menu(username):
    while True:
        print('\nMenu Pembeli')
        print('1. Transaksi')
        print('2. Keluar')
        choice = input('Pilih opsi: ')

        if choice == '1':
            buat_transaksi(username)
        elif choice == '2':
            break
        else:
            print('Opsi tidak valid.')

def buat_transaksi(username):
    duration = input('masukkan tambahan jam pada akun: ')
    print('1. dana')
    print('2. gopay')
    print('3. cash')
    payment = input('masukkan metode pembayaran: ')
    if payment == '1':
        print('dana Payment : 085787584274')
        print('menunggu transfer masuk:')
        time.sleep(6)
        print('Pembayaran berhasil, terimakasih')
        return buyer_menu(username)
    elif payment == '2':
        print('gopay Payment : 085787584274')
        print('menunggu transfer masuk:')
        time.sleep(6)
        print('Pembayaran berhasil, terimakasih')
        return buyer_menu(username)
    elif payment == '3':
        print('silahkan ke kasir')
        return buat_transaksi(username)
    else:
        print('opsi tidak valdi!!!')

login()
