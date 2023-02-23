# UltraTech_CTF
UltraTech_CTF

İlk Olarak NmapScann aracı ile tarama başlatıyoruz.

![Screenshot 2023-02-23 18-55-44](https://user-images.githubusercontent.com/103064152/220960900-c230351b-8ac1-45a8-ab99-2ec4e019f837.png)

31331 portunda çalışan Web sitesine gidiyoruz.

![webpage](https://user-images.githubusercontent.com/103064152/220961360-49c96553-a7ba-4181-8177-8d1926de754a.png)

8081 portunda çalışan bir adet web sunucusuna gidiyoruz. 
![Screenshot 2023-02-23 19-05-02](https://user-images.githubusercontent.com/103064152/220963375-8e8472fd-fa00-4e9b-a3ca-9316d6325471.png)

İp:31331:js adresine gidince js kodlara ulaşıyoruz.
![Screenshot 2023-02-23 19-05-26](https://user-images.githubusercontent.com/103064152/220963765-1f1b82f4-2421-4afa-9d4d-66f25387409b.png)

Kodları incelediğimizde ping atabildiğimizi anlıyoruz.

![Screenshot 2023-02-23 19-05-36](https://user-images.githubusercontent.com/103064152/220964723-978614da-8750-4016-ae8b-03be328dd12a.png)

ping yerine `ls` komutu yazıyoruz. 

![Screenshot 2023-02-23 19-15-37](https://user-images.githubusercontent.com/103064152/220965799-2aa7321f-4468-4d2f-a229-e83c792cdca0.png)

Daha sonra gördüğümüz dosyayı "cat" komutu ile açıyoruz.

![Screenshot 2023-02-23 12-19-13](https://user-images.githubusercontent.com/103064152/220966099-6f28d4e0-2a7f-41f9-9370-f29982331a26.png)

hash'lenmiş passwordu decoder yaparak şifreyi alıyoruz.

ssh username:r00t
password:n100906

Daha sonra "ssh" giriş yapıyoruz.

![Screenshot 2023-02-23 12-19-30](https://user-images.githubusercontent.com/103064152/220966790-16d693e2-0434-455b-aba6-da49fbbe45f5.png)
!YETKİ YÜKSETME
"id" komutu çalıştırdığımızda "r00t" kullanıcısının "docker" grubuna dahil olduğunu görüyoruz. 
Daha "docker image" komutu kullanarak root yetkilerine bakıyoruz.
"docker run -v /:/mnt --rm -it bash chroot /mnt sh" komutu ile root yetkisine sahip oluyoruz.
![Screenshot 2023-02-23 12-27-48](https://user-images.githubusercontent.com/103064152/220967733-51877865-b668-46f8-b971-d30d756aa4d4.png)


