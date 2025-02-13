# Halaskar
Hazır Olmayanlar:

Optical Flow Module:
	Optical Flow Module var olmadığından projeye can bus çoğaltıcı eklenmemiştir.
Lidar : https://www.generationrobots.com/media/rplidar/SLAMTEC_rplidar_datasheet_S2M1_v1.0_en.pdf
	Kullanacağımız Lidar UART protokolü kullanıyormuş fakat Jetson Orin nano ve OrangeCube+ da 
	herhangi bir UART çıkışı kalmadı diye gördüm tekrar araştırıcam.


Hazır Olanlar:

OrangeCube+: 
	Datasheet'e göre schematic oluşturuldu.
Battery
Regülatör:
	Eğer LM2596 ise olmayacağından model ismi eklemedim.
MOTOR x4:
	Motorlardaki 3. pini tam anlamadım.
ESC x4:
	ESClere gelen signal 3 kablodan oluşuyor fakat ben onu sadece bir kablo gibi yaptım.
Güç Dağıtım Kartı:
	Power Distrubition Karttaki boşluk termal kamera onu jetson nanoya ekleyeceğimizden eklemedim ve boş kaldı.
	Yerine Servo Motorları ekledim ve PWM modülü kullandık. Çünkü Can bus bulmuyor.
FS5115M Servo x2:
	Servolar OrangeCube+ datasheetinde can bus ile çalışıyor demiş ama farklı model,
	o yüzden pwm output alabileceğimiz main out kısmına bağlanmıştır. 
Dikey motorlar T-Motor mn6007
ESC Hobbywing Platinum 80A V5
GPS Here3+
Pitot Tüpü
Telemetri H16:
	Telemetry için yaptığım şematik datasheette yoktu easyeda platformundan buldum.
	Kamera Telemetrye bağlanmadığından şuanlık eksik.
Jetson Orin Nano UNO:
	http://discuss.px4.io/t/connection-of-pixhawk-cubeorange-to-nvidia-jetson-agx-orin-via-px4-ros-2-bridge-using-uart/29206
	Bu sitedeki bilgiye göre rx, tx pinlerinden bağlandığını gördüm ve o yüzden öyle bağladım.
Jetson Model Kamerası:
	Anladığım kadarıyla özel kamera portu var o yüzden istediğim bir yere entegre ettim.
