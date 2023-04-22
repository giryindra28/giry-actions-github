# giry-actions-github
a. Buatlah Script Github Actions untuk Deploy GitHub Repo ke SSH Instance!

Disini saya mebuat script untuk mendploy file js yang  berisikan alerts yang nantinya akan di panggil di index.html, yang nantinya akan terhubung dengan webpack.
Jadi ketika kita mau push projek ke github, github nanti akan menjalankan perinta otomatis "npm run production" untuk membundling javascript kita secara otomatis.

### Stepnya:
1. membuat workflows
    - didalam folder workflows ada main.yml
    - name: Ci, ini hanya nama yang nanti ada di tabs actions github
    - on: push, artinya script di dalam workflow dijalankan pas github mendeteksi puush dari repotersebut
    - jobs, ini berisi work yang nantinya dikerjakan,terus nanti berisi langkah-langkah perintah yang disebut steps
    contoh : name: testing
        runs-on: ubuntu-latest
        steps:
            - name: perintah 1
              run: echo "hello world"
     => artinya ada sebuah job namanya testing, berjalan di os ubuntu-latest, kemudian steps yang di kerjajakn itu run echo "hello world" misal gitu
 2. membuat token untuk secret keys di repo kita, jadi karena projek bersifat public jadi wajib kita amankan dengan bantuan fitur secrets, ini mirip sama env
 

### Hasil pengeerjaan :
1. ![image](https://user-images.githubusercontent.com/108140011/233801549-4de9ee66-2ade-440e-84bd-9b75bf884991.png)
github actions berjalan dengan baik, github actions tersebut sesuai job yang telah kita tentukan yang berada di file main.yml

2. ![image](https://user-images.githubusercontent.com/108140011/233801622-ff60732c-f1d3-4982-a512-3ed293eedb1d.png)
Github adtions untuk deploy file js berhasil di jalankan

3. ![image](https://user-images.githubusercontent.com/108140011/233801661-c0e013d5-fa33-42f6-9618-0325e9c3e9a6.png)
Berhasil deploy file js
#### Selesai
