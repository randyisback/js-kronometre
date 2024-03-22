# Glitch Timer

Bu proje, HTML, CSS ve JavaScript kullanılarak oluşturulmuş basit bir kronometre uygulamasıdır. Bu kronometre, zamanı saymak için başlat, duraklat ve sıfırlama işlevlerine sahiptir.

## Nasıl Kullanılır?

Kronometreyi çalıştırmak için `index.html` dosyasını tarayıcınızda açmanız yeterlidir. Ardından, başlat/duraklat ve sıfırla düğmelerini kullanarak kronometreyi kontrol edebilirsiniz.

## Kurulum

Projeyi kendi bilgisayarınıza klonlayın:

```bash
git clone https://github.com/randyisback/js-kronometre.git
``` 

## Örnek Kod
```javascript
 function start() {
      startBtn.classList.add("active");
      stopBtn.classList.remove("stopActive");

      startTimer = setInterval(() => {
        ms++
        ms = ms < 10 ? "0" + ms : ms;

        if (ms == 100) {
          sec++;
          sec = sec < 10 ? "0" + sec : sec;
          ms = "0" + 0;
        }
        if (sec == 60) {
          min++;
          min = min < 10 ? "0" + min : min;
          sec = "0" + 0;
        }
        if (min == 60) {
          hr++;
          hr = hr < 10 ? "0" + hr : hr;
          min = "0" + 0;
        }
        putValue();
      }, 10); //1000ms = 1s

    }

```
Burada start butonuna basılınca sayaç başlatılır ve belirtilen süreye göre artar.



## Katkıda Bulunma

Bu proje katkılara açıktır. Eğer bir hata bulursanız veya bir öneriniz varsa, lütfen bir konu açın veya bir pull talebi gönderin. Katkılarınızı bekliyorum!

## Lisans

Bu proje MIT lisansı altında lisanslanmıştır. Daha fazla bilgi için [LICENSE](LICENSE) dosyasına bakın.
