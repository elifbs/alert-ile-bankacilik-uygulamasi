# alert-ile-bankacilik-uygulamasi
alert-ile-bankacilik-uygulamasi


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Alert ile Banka Uygulaması Ödevi</title>
</head>
<body>
    

    <script>

    alert("Hoşgeldiniz! İşlem yapmak için TAMAM'a basınız")
    let userName = 'user'
    let loginName = prompt('Adınız nedir').toLowerCase()
    let password = 123456
    let loginPassword = Number(prompt('Parolanızı giriniz'))
    let bakiye = 1000
    if (userName === loginName && password === loginPassword) {
        for(let i = 0; i < 4; i++){
            let anaSayfa = Number(prompt('Hoşgeldiniz ne yapmak istersiniz \n 1-Bakiye sorgulama \n 2-Para çekme \n 3-Para yatırma \n 4-Çıkış'))
            if (anaSayfa === 1) {
            let bakiyeGoster = alert(`${bakiye} TL bakiyeniz bulunmaktadır`)
            }else if (anaSayfa === 2) {
                let cekilecekMiktar = Number(prompt('Çekmek istediğiniz miktarı giriniz'))
                if (cekilecekMiktar < bakiye) {
                bakiye = bakiye - cekilecekMiktar
                alert(`${cekilecekMiktar} TL çektiniz ${bakiye} TL bakiyeniz kaldı.`)
                }else{
                    alert(`Bakiyeniz ${bakiye} TL dir. Bakiyeden daha fazla para çekemezsiniz`)
                }
            }else if (anaSayfa === 3) {
                let yatirilacakMiktar = Number(prompt('Yatırmak istediğiniz miktarı giriniz'))
                bakiye = bakiye + yatirilacakMiktar
                alert(`${yatirilacakMiktar} TL yatırdınız ${bakiye} TL bakiyeniz var.`)
            }else if (anaSayfa === 4) {
                alert('İyi günler dileriz...')
                break
            }else{
                alert('Hatalı işlem numarası girdiniz')
            }
        }
    }else{
        alert('Yanlış kullanıcı adı veya parola girdiniz')
            
    }

    </script>
</body>
</html>
