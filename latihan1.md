# percobaan 1 :  Melihat ps (process status) dan status direktori /proc  Catatan : Pastikan tidak dalam akses root 
# 1. ps menampilkan PID (Process ID) untuk shel dan proses ps itu sendiri [$ ps,$ ls -l /proc/[Nomor PID]]
(<img width="661" height="451" alt="l1" src="https://github.com/user-attachments/assets/ac4eccb8-90c9-4f4f-b008-e4d4d10be433" />)

# 2. Melihat status proses
   $ cat /proc/[Nomor PID]/status
![Teks Alternatif]()

# 3. Melihat nilai pada variabel /proc
   $ ls /proc/sys/net/ipv4
 ![Teks Alternatif]()
  
# 4. Melihat isi salah satu variabel
   $ cat /proc/sys/net/ipv4/ip_forward
   $ echo 1 > /proc/sys/net/ipv4/ip_forward (tidak bekerja)
![Teks Alternatif]()

# 5. Mengubah kernel variable harus dengan ijin akses root.
   Menjadi root dengan utilitas su (subtitute user)
   $ sudo su   [sudo] password for mahasiswa :  password)
   # echo 1 > /proc/sys/net/ipv4/ip_forward   
![Teks Alternatif]()
