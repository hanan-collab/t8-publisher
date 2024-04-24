# Question Tutorial 8

## How many data your publlsher program will send to the message broker in one run?
Fungsi main program publisher memanggil `publish_event` sebanyak 5 kali. Setiap panggilan `publish_event` mengirimkan pesan `UserCreatedEventMessage` yang berisi informasi user ID dan username. Karena `publish_event` dipanggil 5 kali dengan data yang berbeda, maka program publisher secara total mengirimkan 5 pesan ke message broker dalam sekali jalan.

## The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
URL `amqp://guest:guest@localhost:5672` memiliki arti yang sama persis dengan program subscriber sebelumnya. Ini adalah informasi koneksi untuk terhubung ke server AMQP. Program publisher dan subscriber menggunakan URL yang sama untuk terhubung ke server AMQP yang kemungkinan besar berjalan pada mesin lokal.

1. `amqp://:` adalah skema URL yang menunjukkan protokol yang digunakan, yaitu AMQP (Advanced Message Queuing Protocol).
2. `guest:guest@:` adalah kredensial autentikasi yang digunakan untuk terhubung ke server AMQP.
3. `localhost:` adalah hostname yang mengacu ke mesin lokal tempat program publisher dijalankan.
4. `5672`adalah nomor port default yang digunakan oleh RabbitMQ untuk koneksi AMQP.

## Running RabbitMQ
![Running RabbitMQ](image.png)