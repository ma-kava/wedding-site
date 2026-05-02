---
title: "Místo"
subtitle: "Kde se to celé odehraje"
comments: false
---

## Místo konání

Luhová 104, 464 01 Raspenava-Frýdlant v Čechách

---

## Mapa

<div style="text-align: center; margin-bottom: 1.5em; display: flex; justify-content: center; gap: 10px; flex-wrap: wrap;">
  <button id="toggle-parking-btn" class="btn btn-primary" style="font-family: 'Lora', 'Georgia', serif; font-size: 1.05em; padding: 10px 20px;">Parkoviště</button>
  <button id="toggle-ceremony-btn" class="btn btn-primary" style="font-family: 'Lora', 'Georgia', serif; font-size: 1.05em; padding: 10px 20px;">Místo obřadu</button>
  <button id="reset-map-btn" class="btn btn-default" style="font-family: 'Lora', 'Georgia', serif; font-size: 1.05em; padding: 10px 20px; display: none; background: #dfcdb6; color: #1f2a18; border: none; font-weight: bold;">Zpět na statek</button>
</div>

<iframe id="venue-map" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2516.2013667548663!2d15.134136912630662!3d50.90149005466718!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47092f1ef3b8e2ff%3A0xd137e00719189cf8!2zUGVuemlvbiBSeWNodMOhxZnFr3Ygc3RhdGVr!5e0!3m2!1scs!2scz!4v1777733200541!5m2!1scs!2scz" width="100%" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>

<script>
document.addEventListener('DOMContentLoaded', function() {
  var parkingBtn = document.getElementById('toggle-parking-btn');
  var ceremonyBtn = document.getElementById('toggle-ceremony-btn');
  var resetBtn = document.getElementById('reset-map-btn');
  var mapIframe = document.getElementById('venue-map');
  var originalSrc = mapIframe.src;
  
  // Coordinates
  var parkingLat = "50.90123941657493";
  var parkingLng = "15.135456754020593";
  var ceremonyLat = "50.90475768055269";
  var ceremonyLng = "15.140216642160588";
  
  var parkingSrc = "https://maps.google.com/maps?q=" + parkingLat + "," + parkingLng + "&t=m&z=17&output=embed";
  var ceremonySrc = "https://maps.google.com/maps?q=" + ceremonyLat + "," + ceremonyLng + "&t=m&z=17&output=embed";
  
  parkingBtn.addEventListener('click', function() {
    mapIframe.src = parkingSrc;
    parkingBtn.style.display = 'none';
    ceremonyBtn.style.display = 'inline-block';
    resetBtn.style.display = 'inline-block';
  });
  
  ceremonyBtn.addEventListener('click', function() {
    mapIframe.src = ceremonySrc;
    ceremonyBtn.style.display = 'none';
    parkingBtn.style.display = 'inline-block';
    resetBtn.style.display = 'inline-block';
  });
  
  resetBtn.addEventListener('click', function() {
    mapIframe.src = originalSrc;
    resetBtn.style.display = 'none';
    parkingBtn.style.display = 'inline-block';
    ceremonyBtn.style.display = 'inline-block';
  });
});
</script>

---

## Doprava

### Autem
- Parkování je k dispozici téměř u statku. Je to louhý štěrový plac, který bude po vaší levé straně, když budete stát před mostem hledíce na statek.
- GPS souřadnice: 50.90123941657493, 15.135456754020593 
    - podívejte se na mapu výše, pomocí tlačítek si můžete snadno přepínat mezi zobrazením statku, parkoviště a místa obřadu.

### MHD
- **Nejbližší zastávka**: Raspenava, lékárna
- **Spojení**: 
    - Z Liberce jezdí autobus 630 do zasávky *Raspenava, lékárna*, ze které je to k nám pár metrů. 
    - Vlak z Liberce do Raspenavy jezdí taky, ale od statku je to skoro 2 km.

---

## Ubytování v okolí

Žel, pokoje na přespání na místě konání svatby jsou již obsazeny, ale můžeme nabídnout matrace pro přespání na zemi v teplé místnosti (vlastní spacáky nutné).
