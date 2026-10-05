# percobaan 1 :  Melihat ps (process status) dan status direktori /proc  Catatan : Pastikan tidak dalam akses root 
## 1. ps menampilkan PID (Process ID) untuk shel dan proses ps itu sendiri
### [$ ps]
### [$ ls -l /proc/[Nomor PID]
<img width="661" height="451" alt="l1" src="https://github.com/user-attachments/assets/ac4eccb8-90c9-4f4f-b008-e4d4d10be433" />

## 2. Melihat status proses  
### [$ cat /proc/[Nomor PID]/status]
<img width="663" height="447" alt="l2" src="https://github.com/user-attachments/assets/dc93cad9-4611-4b52-abe8-98474e514d2c" />

## 3. Melihat nilai pada variabel /proc                                                                       
### [$ ls /proc/sys/net/ipv4]
 <img width="656" height="443" alt="l3" src="https://github.com/user-attachments/assets/04cbb519-7efd-48ea-91c3-37bda14584a4" />
  
## 4. Melihat isi salah satu variabel                                                          
### [$ cat /proc/sys/net/ipv4/ip_forward]                                                                                       
### [$ echo 1 > /proc/sys/net/ipv4/ip_forward (tidak bekerja)]
<img width="651" height="63" alt="l4" src="https://github.com/user-attachments/assets/5cd94267-1758-43eb-a95c-0fa3486a4b4d" />
<img width="650" height="70" alt="l5" src="https://github.com/user-attachments/assets/cff18d57-cc01-406c-ac03-e0632f1f48b9" />

## 5. Mengubah kernel variable harus dengan ijin akses root. Menjadi root dengan utilitas su (subtitute user)         
### [$ sudo su   [sudo] password for mahasiswa :  password)]                                                                           
### [# echo 1 > /proc/sys/net/ipv4/ip_forward]   
<img width="650" height="100" alt="l6" src="https://github.com/user-attachments/assets/42cbc1a2-20af-43f9-8552-47ce5fb3a018" />

## 6. Kembali ke user semula dan tampilkan variable kernel dengan nilai baru 
### [$ cat  /proc/sys/net/ipv4/ip_forward]
<img width="661" height="444" alt="l7" src="https://github.com/user-attachments/assets/07481b0e-0cf2-400f-8790-fee572aa0f01" />


# Percobaan 2 : Melihat tipe file 
## 1. Melihat block device (peralatan I/O) $ ls -l /dev/fd/1
## 2. Melihat character device (peralatan I/O) $ ls -l /dev/tty0
## 3. Melihat $ ls -l /dev/console
## 4. Melihat direktori $ ls -ld /dev
## 5. Melihat ordinary file $ ls -l /etc/passwd
<img width="649" height="195" alt="percobaan 2 " src="https://github.com/user-attachments/assets/36653bec-b467-4ec7-a455-a82f820d57a6" />

# Percobaan 3 : Direktori 
## 1. Melihat direktori HOME [$ pwd]   [$ echo $HOME]
<img width="664" height="106" alt="percobaan 3 1 " src="https://github.com/user-attachments/assets/b1491b67-3eac-49d1-889f-2adf14ed3f20" />

## 2. Melihat direktori aktual dan parent direktori [$ pwd] [$ cd ..] [$ pwd] [$ cd ..] [$ pwd]
<img width="656" height="198" alt="percobaan 3 2 " src="https://github.com/user-attachments/assets/5327b52d-78ff-4397-b8d1-cc841d3dc4e0" />

## 3.Membuat satu direktori, lebih dari satu direktori atau sub direktori [$ pwd] [$ mkdir A B C A/D A/E B/F A/D/A] [$ ls -l] [$ ls -l A] [$ ls -l A/D]
<img width="654" height="646" alt="percobaan 3 3 " src="https://github.com/user-attachments/assets/11a28da1-ca61-42a8-91db-4bc51acec056" />

## 4.Menghapus satu atau lebih direktori hanya dapat dilakukan pada direktori kosong dan hanya dapat dihapus oleh pemiliknya kecuali bila diberikan ijin aksesnya [$ rmdir B (Terdapat pesan error)] [$ ls -l B] [$ rmdir B/F B] [$ ls -l B] 
<img width="677" height="649" alt="percobaan 3 4 " src="https://github.com/user-attachments/assets/51c8a09f-6ac1-41e7-be29-f025b0d81c54" />

## 5.Navigasi direktori dengan instruksi cd untuk pindah dari satu direktori ke  direktori lain. [$ pwd] [$ ls -l] [$ cd A] [$ pwd] [$ cd ..] [$ pwd] [$ cd /home/mahasiswa/C] [$ pwd] [$ cd] [$ pwd]
<img width="677" height="662" alt="percobaan 3 5 " src="https://github.com/user-attachments/assets/34767b7e-b575-4735-8c28-45be349b504d" />

# Percobaan 6 : Simbolic Link 
## 1. Link file [$ echo "Hallo apa khabar" > halo.txt] [$ ls -l] [$ ln halo.txt z] [$ ls -l] [$ cat z] [$ mkdir mydir] [$ ln z mydir/halo.juga] [$ cat mydir/halo.juga] [$ ls -l mydir]
<img width="656" height="668" alt="percobaan 6 1 " src="https://github.com/user-attachments/assets/412533ff-5f5a-4de3-b45f-53ec434ee34d" />
<img width="680" height="641" alt="percobaan 6 2 " src="https://github.com/user-attachments/assets/f14d8645-8001-4f13-86ec-5a966232e575" />

## 2. Symbolic Link file [$ mount] [$ ln /home/mahasiswa/z /tmp/halo.txt] [$ ln -s /home/mahasiswa/z /tmp/halo.txt] [$ ls -l /tmp/halo.txt] [$ cat /tmp/halo.txt]
<img width="675" height="654" alt="percobaan 6 3 " src="https://github.com/user-attachments/assets/79b8cf28-e906-4547-b5f4-3f3f57435214" />
<img width="659" height="437" alt="percobaan 6 4 " src="https://github.com/user-attachments/assets/f2d98df8-f345-47e1-ad1b-528f5626fff0" />
