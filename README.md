# TUTORIAL GIT

Ini bisa jadi referensi untuk menggunakan git pada saat mengerjakan project bareng dengan team

## Step 1, Cloning Project
cloning project yang ingin di kerjakan
```
git clone <link-remote-repository>
```
setelah clone, pindah ke folder yang di clone dengan cara:
```
cd <nama-folder/directory>
```



## Step 2, Buat Branch Pribadi
buat branch pribadi supaya tidak mengganggu master


buat branch baru dengan code berikut:
```
git checkout -b <nama-branch>
```


pastikan branch yang di buat sudah ada,
cek branch dengan code berikut:
```
git branch -a
```


berikut nama branch yang ada
bagian atas merupakan branch yang ada di lokal
bagian bawah adalah branch yang sudah ada di remote repository
![git branch -a](https://user-images.githubusercontent.com/111379665/208021912-fac2d057-565c-4ce3-96c7-278046cd90ef.png)
sekarang posisi sedang berada di branch master, dilihat dari gambar, branch master berwarna hijau




## Step 3, Pindah branch
tadi saat kita membuat brnach baru dengan cara "git checkout -b <nama-branch>", itu otomatis akan pindah ke branch yang kita buat
  kalau belum pindah, silahkan pindah ke branch masing masing dengan cara:
  
  
  ```
  git checkout <nama-branch>
  ```
  
  
  berikut hasilnya, awalnya bertanda master, skarang sudah berubah ke branch yang kita tuju
  ![git checkout](https://user-images.githubusercontent.com/111379665/208023235-d541b338-a16d-4658-908a-4c8006ef92a8.png)
  
  
  
  ## Step 4, Silahkan ngoding
  
  
  
  ## Step 5, Add to staging and commit
  sebelum push ke remote repository, lakukan langkah add dulu:
  
  berikut cara untuk menambahkan file yang spesifik
  ```
  git add <nama-file>
  ```
  
  berikut untuk menambahkan semua file yang tadi sempat di ubah:
  ```
  git add .
  ```
  
  setelah melakukan add, kita lanjutkan dengan melakukan commit dengan cara:
  ```
  git commit -m "(namai perubahan yang di lakukan)"
  ```
  
  
  
  ## Step 6, Lakukan Push ke branch remote pribadi
  push ke remote repository dengan cara:
  ```
  git push origin <nama-branch>
  ```
  
  
  
  
  ## Step 7, lakukan merge ke branch master
  cara untuk melakukan merge ke branch master adalah dengan pindah branch dulu ke master, lakukan:
  ```
  git checkout master
  ```
  
  
  setelah pindah ke branch master
  lakukan merge dengan branch masing masing, lakukan:
  ```
  git merge <nama-branch>
  ```
  
  seletah merge lakukan push:
  ```
  git push origin master
  ```
  
  ## Step 8, Lakukan peruabahan selalu di branch masing-masing
  setelah melakukan merge di master dan melakukan push
  silahkan pindah ke branch masing masing untuk melakukan perubahan lebih lanjut
  ```
  git checkout <nama-branch>
  ```
  
  
  pastikan branch masing masing sudah up to date dengan branch master, dengan melakukan:
  ```
  git pull origin master
  ```
  kalau sudah up to date,
  
  lanjutkan untuk melakukan perubahan atau penambahan code di branch masing-masing
  
  
  
  ## step 9, ulangi dari Step 4
  
  # Tambahan
  kalau conflict, pada saat merge di branch master lakukan langkah berikut
  
  ## step 1
  ![conflict git](https://user-images.githubusercontent.com/111379665/208026606-bce4b522-33d4-4ebe-83b0-64fe61af2684.png)
  silahkan diskusikan dengan teman yang diajak conflict, dan sepakai code mana yang akan di pakai
  pencet "Resolve in Merge Editor"
  
  ## Step 2
  ![conflict git 1](https://user-images.githubusercontent.com/111379665/208027312-4eb491a3-f812-4ab3-87a6-d3bae2a62213.png)
  silahkan di sepakati, mau pakai yang "Current" atau "Incoming", lalu pencet accept
  lalu pencet "Complate Merge"
  
  ## Step 3, commit dan push
  setelah complete merge, silahkan ketik di terminal:
  ```
  git commit -m "(namai-perubahan-anda)"
  ```
  
  setelah melakukan commit, lakukan push ke master
  ```
  git push origin master
  ```
  
  # Finish
