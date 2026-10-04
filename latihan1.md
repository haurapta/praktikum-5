# percobaan 1 :  Melihat ps (process status) dan status direktori /proc  Catatan : Pastikan tidak dalam akses root 
# 1. ps menampilkan PID (Process ID) untuk shel dan proses ps itu sendiri                                                                  [$ ps]                                                                                                                                    [$ ls -l /proc/[Nomor PID]
<img width="661" height="451" alt="l1" src="https://github.com/user-attachments/assets/ac4eccb8-90c9-4f4f-b008-e4d4d10be433" />

# 2. Melihat status proses                                                                                                                 [$ cat /proc/[Nomor PID]/status]
<img width="663" height="447" alt="l2" src="https://github.com/user-attachments/assets/dc93cad9-4611-4b52-abe8-98474e514d2c" />

# 3. Melihat nilai pada variabel /proc                                                                                                     [$ ls /proc/sys/net/ipv4]
 <img width="656" height="443" alt="l3" src="https://github.com/user-attachments/assets/04cbb519-7efd-48ea-91c3-37bda14584a4" />
  
# 4. Melihat isi salah satu variabel                                                                                                      [$ cat /proc/sys/net/ipv4/ip_forward]                                                                                                   [$ echo 1 > /proc/sys/net/ipv4/ip_forward (tidak bekerja)]
<img width="651" height="63" alt="l4" src="https://github.com/user-attachments/assets/5cd94267-1758-43eb-a95c-0fa3486a4b4d" />
<img width="650" height="70" alt="l5" src="https://github.com/user-attachments/assets/cff18d57-cc01-406c-ac03-e0632f1f48b9" />

# 5. Mengubah kernel variable harus dengan ijin akses root. Menjadi root dengan utilitas su (subtitute user)                             [$ sudo su   [sudo] password for mahasiswa :  password)]                                                                                [# echo 1 > /proc/sys/net/ipv4/ip_forward]   
<img width="650" height="100" alt="l6" src="https://github.com/user-attachments/assets/42cbc1a2-20af-43f9-8552-47ce5fb3a018" />
