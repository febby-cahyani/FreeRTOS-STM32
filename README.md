# FreeRTOS-STM32F103C8T6
Proyek ini menunjukkan penggunaan FreeRTOS pada mikrokontroler STM32F103C8T6 untuk menjalankan beberapa task secara bersamaan. Sistem ini membaca input dari button, mengambil nilai ADC (Analog-to-Digital Converter), mengontrol LED, dan mengirim data melalui UART. Setiap fungsi ditangani dalam task terpisah yang dijadwalkan dan dikelola oleh FreeRTOS, sehingga memungkinkan multitasking dalam lingkungan realtime.

Diagram Task :

![diagram task](https://github.com/user-attachments/assets/7f98999a-78df-44ca-911e-e0b99c56135a)

Hardware yang diperlukan :
1. STM32F103C8T6
2. Push button for input
3. Input yang mendukung ADC seperti Potensiometer
4. LED
5. Koneksi UART

Software yang diperlukan :
1. STM32CubeIDE
2. FreeRTOS

Cara Kerja :
- Sistem terus memantau button menggunakan sinyal debounced. Status button mengontrol apakah sistem beroperasi dalam mode "LED blink" atau mode "Indikator nilai ADC".
- Data input analog dibaca secara berkala. dikonversi menjadi nilai digital oleh ADC, lalu disimpan dalam variable global untuk diakses oleh task LED dan UART.
- Jika button ditekan, semua LED berkedip. Jika button tidak ditekan, LED menyala sesuai dengan nilai ADC.
- sistem akan mengirimkan hasil pembacaan status button, angka "1" akan muncul pembacaan tegangan ADC, dan angka "2" akan menampilkan kata "HELLO WORLD" ke perangkat yang terhubung melalui UART.

Pinout Hardware :

![Pinout Hardware FreeRTOS](https://github.com/user-attachments/assets/8a5312a5-574a-4175-9b8d-5f23355ca97f)

Hasil Hardware :

![FreeRTOS using STM32](https://github.com/user-attachments/assets/95304953-fb30-4f89-af88-ab4ef416cdb7)

Hasil Keseluruhan :

https://youtube.com/shorts/w-dF6c37Ar8?feature=share 
