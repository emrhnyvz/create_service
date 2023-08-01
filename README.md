# create_service
#ilk olarak dosya oluşturmalıyız ve bunun için gerekn kod
sudo vim /lib/systemd/system/myshellscript.service
#bundan sonra shel script olusturmalıyız
#shel script olusturma aşamalarısu şekilde
[Unıt]
Description=My Shell Script Name
[Service]
ExectStart=/usr/bin/script.sh
[Install]
WantedBy=multi-user.target
#işlemimiz bu kadar şimdi servisi etkinleştirip başlatma aşamasına geçiyoruz
sudo systemctl enable myshellscript
#yukarıdaki kodda etkinleştirdik şimdide başlatmamız gerek
sudo systemctl start myshellscript
#şimdi son işeme geçiyoruz yaptıgımız servisin çalışıp çalışmadıgına bakıcagız bu işem içinde bu kod yazlıyor
systemctl status myshellscript
