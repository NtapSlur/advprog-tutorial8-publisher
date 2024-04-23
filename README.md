## Reflection Publisher
1. How many data your publlsher program will send to the message broker in one run?
    - 5 kali karena terdapat 5 kali publish_event

1. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
    - Sama. Kedua url ini sama-sama mengirimkan request ke server rabbitMQ, tetapi perbedaannya adalah hasil request dari publisher akan mengirimkan pesan ke queue, sedangkan untuk subscriber dibuat listener untuk mengambil pesan dari queue tersebut.

# Image of RabbitMQ Running
![Pic](image.png)

# Image of Console When Subscriber and Publisher Are Running Simultaneously With RabbitMQ
![Pic Publisher](image-2.png)
![Pic Subscriber](image-1.png)
Explanation:
    - Gambar tersebut merupakan screenshot dari cargo run untuk package subscriber dan publisher, di mana saat kita menjalankan package subscriber dan publisher, publisher akan mengirimkan data yang di hard-code ke message queue. Kemudian, subscriber akan mendapat data di message queue tersebut dan ditampilkan ke console.

# Image of Spiking Chart
![Spike](image-3.png)
Explanation: 
    - Spiking yang terjadi pada chart terjadi karena adanya peningkatan queue message dalam interval waktu tertentu. Jika kita melihat ke bagaimana program bekerja, publisher akan mengirimkan data ke message queue. Jika publisher dijalankan selama beberapa kali, maka message yang dimasukkan ke message queue akan menjadi semakin banyak sehingga terjadi lonjakan untuk message yang masuk ke queue di RabbitMQ
