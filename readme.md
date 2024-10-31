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