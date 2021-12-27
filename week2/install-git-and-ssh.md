# Install Git & SSH  Key
Pada Pembahasan ini saya akan membahas tentang bagaimana cara untuk install git & ssh key pada server aws kita, berikut langkah langkah nya :

## Membuat AWS Server 

### step 1
- pertama kita akan membuat 3 instance EC2, untuk backend, frontend, dan database
- masuk ke aws.educate.com
- kemudian masuk ke dashboard EC2 nya
- kemudian pilih instance
- lalu pilih launch instance

![1](assets/ssh1.png)

### step 2
- pada bagian ini kita pilih ubuntu
- setelah itu klik select untuk melanjutkan

![2](assets/ssh2.png)

## step 3
- pada bagian ini kita pilih type dari instance kita, di sini saya menggunakan t2 micro
- jika sudah selesai klik next untuk melanjutkan

![3](assets/ssh3.png)

## step 4
- pada bagian ini saya menggunakan 2 instance, karena saya sudah membuat server untuk frontend nya
- dan disable auto assign ip pubblic karena kita tidak ingin menggunakan DHCP

![4](assets/ssh4.png)

## step 5
- pada bagian ini saya menggunakan size memory untuk server nya sebesar 8 GB
- dan jika sudah selesai klik next untuk melanjutkan

![5](assets/ssh5.png)

## step 6
- pada bagian security group saya menggunakan all trafic karena agar semua port nya bisa di akses
- setelah itu klik rivew and launch

![6](assets/ssh6.png)

## step 7
- pada bagian ini kita bisa langsung klik launch saja

![7](assets/ssh7.png)

## step 8
- pada bagian ini kita pilih choose an exciting key pairs karena kita sudah bikin key pairs sebelum nya
- dan klik launch instance untuk melanjutkan

![8](assets/ssh8.png)

## step 9
- dan jika sudah berhasil membuat instance nya maka akan tampil seperti gambar berikut

![9](assets/ssh9.png)







