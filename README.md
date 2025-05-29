# Bookshelf API

API untuk mengelola koleksi buku menggunakan Node.js dan Hapi.js.

## Fitur

- Menambahkan buku baru
- Menampilkan semua buku
- Menampilkan detail buku berdasarkan ID
- Mengubah data buku
- Menghapus buku
- Filter buku berdasarkan nama, status reading, dan status finished

## Instalasi

1. Clone repository ini
2. Install dependencies:
   ```bash
   npm install
   ```
3. Jalankan aplikasi:
   ```bash
   npm start
   ```
   Atau untuk development:
   ```bash
   npm run start-dev
   ```

## API Endpoints

### 1. Menambahkan Buku
- **Method:** POST
- **URL:** `/books`
- **Body:**
  ```json
  {
    "name": "string",
    "year": "number",
    "author": "string",
    "summary": "string",
    "publisher": "string",
    "pageCount": "number",
    "readPage": "number",
    "reading": "boolean"
  }
  ```

### 2. Menampilkan Semua Buku
- **Method:** GET
- **URL:** `/books`
- **Query Parameters (optional):**
  - `name`: Filter berdasarkan nama buku
  - `reading`: 0 (tidak sedang dibaca) atau 1 (sedang dibaca)
  - `finished`: 0 (belum selesai) atau 1 (sudah selesai)

### 3. Menampilkan Detail Buku
- **Method:** GET
- **URL:** `/books/{bookId}`

### 4. Mengubah Data Buku
- **Method:** PUT
- **URL:** `/books/{bookId}`
- **Body:** (sama seperti POST)

### 5. Menghapus Buku
- **Method:** DELETE
- **URL:** `/books/{bookId}`

## ESLint

Proyek ini menggunakan ESLint dengan konfigurasi Airbnb. Untuk menjalankan linting:

```bash
npm run lint
```

Untuk memperbaiki masalah linting otomatis:

```bash
npm run lint:fix
```

## Port

Aplikasi berjalan pada port 9000.