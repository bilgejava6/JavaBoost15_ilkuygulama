# REACT JS GEREKLİ KURULUMLAR VE NOTLARIM

## Kurulum

        ilk olarak reactjs çalıştıra bilmek için bunu yayınlayacak ve kodları yorumlayacak
    bir sunucuya ihtiyaç var ayrıca paket kurulumları için bir paket yöneticisine ihtiyaç
    bulunmaktadır.
        NodeJS tüm gerekli servis ve paket yönetim araçlarını içerisinde barındırmaktadır.
```link
    https://nodejs.org/en/download/package-manager
```

```bash
# node js kurulumunu kontrol etmek için 
node -v
# paket yöneticisini kontrol etmek için
npm -v
```

        reactJS uygulamalarını kurmak için ve dökümantasyonlar için aşağıdaki linkleri 
    ziyaret ediniz.
    - https://react.dev/learn/start-a-new-react-project
    - https://create-react-app.dev/docs/getting-started

    JS doğası gereği tip güvenliği sağlamamaktadır, bu nedenle kodlarımızı daha güvenli 
    ve yönetilebilir yapmak için projelerimizi TypeScript(TS) ile kuracağız yada önceden 
    standart olarak kurmuş isek ek olarak TS kurulumu ekleyerek TS haline getireceğiz.

```bash
    # TS olmadan kurulum yapmak yani JS
    npx create-react-app uygulama-adi
```

```bash
    # TypeScript destekli şekilde uygulamayı kurmak
    npx create-react-app uygulama-adi --template typescript
```

    Örnek Proje:
     npx create-react-app ilkuygulama --template typescript

    DİKKAT!!! kurulumlar ve başlatma işlemler için öncelikle terminal ekranına geçiniz. 
    NOT!! terminal ekranına geçmeden önce uygulamayı kapatıp açmak gerekebilir. Ayrıca,windows sistemler için  powershell yerine cmd kullanılmalı. bu ayrımı + ikonun yanındaki aşağı ok tuşuna basarak command prompt seçilerek yapılır.
    burada hangi dizin içerisine projeyi atacak iseniz öncelikle o klasöre geçin.
    [> cd Uygulamalarim]
    sonra buraya oluşturmak istediğini proje komutunu giriyorsunuz
    [Uygulamalarim>npx create-react-app ilkuygulama --template typescript]

## Çalıştırmak - Uygulamyı başlatmak

    Uygulamayı başlatmak için "npm start" yeterlidir. Ancak, uygulamanın başlaması için uygulama configlerini içeren package.json dosyasına gerek vardır. Eğer konum olarak uygulamın dizininde değil iseniz npm start hata verecektir.
    Örn:
    uygulamanızın paket yapısı şöyle olsun
    - REACTJS (Ana Klasör)
    --- ilkislemler(alt klasör)
    --- Uygulamalarim(alt klasör)
    ------ ilkuygulama(uygulama klasörü)
    CMD: ReactJS>Uygulamalarim>npm start
    Hata verecektir. çünkü konum olarak projenin içinde değilsin.
    ÇÖZÜM:
    uygulamanızın dizinine geçeceksiniz
    CMD: ReactJS>Uygulamalarim>cd ilkuygulama
    CMD: ReactJS>Uygulamalarim>ilkuygulama>npm start

## Uygulamanın Portunu değiştirmek

    Aşağıdaki şekillede kendine uygun işletim sistemini seçerek port bilgisini güncelleyebilirsiniz. Bu işlemi yapmak için package.json dosyasında scripts alanında değişiklik yapacaksınız.

```json

 "scripts": {
    // default olarak çalışır 3000 portu kullanılır.
    // "start": "react-scripts start",
    // windows için
    // "start":"set PORT=9990 && react-scripts start",
    // MACOS & farklı versiyonlar
    // Yeni veryion "start": "PORT=9990 react-scripts start",
    // Eski versiyon MACOS = "start": "export PORT=9990 react-scripts start",
    "start": "PORT=9990 react-scripts start",
    "build": "react-scripts build",
    "test": "react-scripts test",
    "eject": "react-scripts eject"
  }

```

