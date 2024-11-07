# Go-Lang Tutorial

## 1. Basic Go
Dilakukan import dengan cara

` go mod init booking-app `

Lalu Membuat file .go

Contoh Kode:

`

    package main
    
    import "fmt"

    func main() {
        fmt.Print("Hello World")
    }

`

## 2. Data Type
Mendeklarasikan tipe data untuk variabel. Contoh:

`

    var firstName string
	var lastName string
	var email string
	var userTickets uint

`

## 3. User Input
Menambahkan user input untuk memasukkan data
`

    fmt.Println("Enter Your First Name: ")
    fmt.Scanln(&firstName)

	fmt.Println("Enter Your Last Name: ")
	fmt.Scanln(&lastName)

	fmt.Println("Enter Your Email: ")
	fmt.Scanln(&email)

	fmt.Println("Enter number of tickets: ")
	fmt.Scanln(&userTickets)

`

## 4. Array
Membuat array agar tidak perlu memasukkan nama orang masing masing
`

    bookings := []string{}

`

## 5. Loops and Switch Case
Dilakuan looping untuk perulangan dan switch case ketika diberikan pilihan

`

city := "London"

	switch city {
	case "New York":
	case "Singapore", "Hong Kong":
	case "London", "Berlin":
	case "Mexico City":
	default:
		fmt.Print("No valid city selected")
	}

`

## 6. Function
Function digunakan untuk memisahkan tiap bagian dari kode agar lebih mudah untuk dibaca

Contoh :

`

	func printFirstNames() []string {
		firstNames := []string{}

		for _, booking := range bookings {
			firstNames = append(firstNames, booking.firstName)
		}
		return firstNames
	}

`

## 7. Struct
Struct adalah kumpulan dari sebuah variabel. Contoh:

`

	type User struct {
		firstName       string
		lastName        string
		email           string
		numberOfTickets uint
	}

`

# Go Wiki

## Feature

- **Melihat Halaman**: Menampilkan konten halaman wiki yang telah disimpan.
- **Mengedit Halaman**: Membuat atau mengedit halaman menggunakan editor teks sederhana.
- **Menyimpan Halaman**: Menyimpan perubahan ke dalam file `.txt`.

## Project Structure

- **main.go**: File utama yang berisi server dan fungsi handler.
- **Struct Page**: Berisi setiap halaman wiki dengan judul dan konten.
- **Fungsi Handler**: Handler untuk melihat, mengedit, dan menyimpan halaman.

## Code Overview

### Main Function

- `save()`: Menyimpan konten halaman ke dalam file teks.
- `loadPage(title)`: Memuat konten halaman dari file teks.
- `viewHandler`: Menampilkan halaman yang telah disimpan. Jika halaman tidak ada, pengguna akan diarahkan ke halaman edit.
- `editHandler`: Memuat halaman untuk diedit atau menginisialisasi halaman baru jika belum ada.
- `saveHandler`: Menyimpan konten yang telah diedit dan mengarahkan kembali ke halaman view.
- `makeHandler`: Memastikan path URL sesuai dengan `/view/`, `/edit/`, atau `/save/` untuk judul yang valid.

### File HTML

- `edit.html`: Template HTML yang digunakan untuk mengedit atau membuat halaman wiki baru.
- `view.html`: Template HTML yang digunakan untuk melihat halaman wiki yang telah disimpan.

## Contoh Penggunaan

   - Buka [http://localhost:8080/view/YourTitle](http://localhost:8080/view/YourTitle).
   - Jika halaman tidak ada, maka akan diarahkan ke halaman edit untuk membuatnya.
   - Masukkan konten dan simpan.

## Error Handling

- Jika halaman gagal untuk disimpan, maka akan muncul window internal server error.
- Jika path halaman tidak sesuai (`/view/`, `/edit/`, atau `/save/` dengan judul yang valid), maka akan muncul pesan 404 error.

## Website
![alt text](image.png)
