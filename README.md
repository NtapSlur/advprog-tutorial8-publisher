## Reflection Publisher
1. How many data your publlsher program will send to the message broker in one run?
    - 5 kali karena terdapat 5 kali publish_event

1. The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean?
    - Sama. Kedua url ini sama-sama mengirimkan request ke server rabbitMQ, tetapi perbedaannya adalah hasil request dari publisher akan mengirimkan pesan ke queue, sedangkan untuk subscriber dibuat listener untuk mengambil pesan dari queue tersebut.