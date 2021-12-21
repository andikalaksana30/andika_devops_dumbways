# Setup server AWS for frontend
    Pada Pembahasan ini kita akan membahas bagaimana cara mengcreate dan mensetup server di AWS, berikut langkah-langkahnya:
    
### step 1
* Pertama kita login ke awseducate.com dan masuk ke akun kalian, dan jika sudah berhasil maka akan tampil halaman berikut

![1](assets/AWS1.PNG)

### step 2
* Langkah selanjut nya yaitu kita membuat  instance EC2 nya dengan masuk ke menu dashboard EC2
* selanjutnya pilih instance >> pilih launch instance

![2](assets/AWS2.PNG)

### step 3
* setelah itu pilih OS yang mau kita gunakan, di sini saya menggunakan ubuntu 20 lts
* jika sudah selesai klik select

![3](assets/AWS3.PNG)

### step 4
* kemudian pada bagian Choose an Instance Type pilih t2 micro, atau sesuai kan kebutuhan anda
* jika sudah, pilih next config

![4](assets/AWS4.PNG)

### step 5
* Pada bagian configure instance detail kita atur Auto-assign Public IP disable karena kita menggunakan ip static
* setelah itu klik next config

![5](assets/AWS5.PNG)

### step 6
* pada bagian add storage, pilih sesuai kebutuhan anda dan jika sudah sesuai klik next config

![6](assets/AWS6.PNG)

### step 7
* pada bagian add tag klik next untuk melanjutkan

![7](assets/AWS7.PNG)

### step 8
* pada bagian configure security group kita pilih settingan yang all traffic agar apps kita bisa di akses dari mana saja
* setelah itu klik review and launch

![8](assets/AWS8.PNG)

### step 9
* pada bagian ini silahkan klik launch

![9](assets/AWS9.PNG)

### step 10
* pada bagian ini pilih create new key pair, dan beri nama sesuai kebutuhan anda
* kemudian klik download key pair

![10](assets/AWS10.PNG)

### step 11
* jika telah berhasil maka akan tampil seperti berikut

![11](assets/AWS11.PNG)

## Setup Elastic Ips

### step 1
* pada bagian network & security, pilih elastic Ips

![1](assets/elastic1.PNG)

### step 2
* Kemudian pilih alocate elastic ip

![2](assets/elastic2.PNG)

### step 3
* pada bagian ini langsung klik allocate saja untuk melanjutkan

![3](assets/elastic3.PNG)

### step 4
* setelah itu kita associate ip kita dengan cara klik action >> pilih associate elastic ip address

![4](assets/elastic4.PNG)

### step 5
* setelah itu kita pilih instance kita >> kemudian klik associate

![5](assets/elastic5.PNG)

### step 6
* jika telah berhasil maka akan tampil seperti gambar berikut 

![6](assets/elastic6.PNG)

## Connect to server aws with ssh key

### step 1
* masuk ke folder penyimpanan ssh key yang sudah kita download tadi
* kemudian ketikan perintah berikut `ssh -I dumbflix.pem ubuntu@ip public`

![1](assets/ssh1.PNG)

### step 2
* jika sudah berhasil masuk maka akan tampil seperti berikut

![2](assets/ssh2.PNG)

### step 3
* Langkah selanjutnya yaitu kita update dan upgrade server kita dengan mengetikan perintah berikut `sudo apt update`
* `sudo apt upgrade`

![3](assets/ssh3.PNG)

## Install Aplication on server AWS

### step 1
* install nvm terlebih dahulu dengan mengetikan perintah berikut `curl https://raw.githubusercontent.com/creationix/nvm/master/install.sh | bash`

![1](assets/app-aws1.PNG)

### step 2
* setelah itu kita Muat ulang lingkungan sistem menggunakan perintah ini `source ~/.profile`

![2](assets/app-aws2.PNG)

### step 3
* instal versi node.js yang perlu Anda gunakan dengan perintah `nvm install 14` dan nvm sudah berhasil terpasangan di server kita

![3](assets/app-aws3.PNG)

### step 4
* langkah selanjutnya yaitu kita install dependencies yang di butuhkan oleh aplikasi dengan perintah berikut, masuk de directory aplikasi 
* kemudian tuliskan perintah `npm install`

![4](assets/app-aws4.PNG)

### step 5
* jika sudah selesai, setelah itu run apps kita dengan perintah `npm start`
* dan sekarang apps kita sudah bisa di akses melalui port 3000, berikut tampilan nya

![5](assets/app-aws5.PNG)


  
