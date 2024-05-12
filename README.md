# Rocnickovy projekt chytrý displej do tříd

## Popis a funkce projektu
Náš projekt je ve stručnosti **oled displej** který by byl umístěn před třídami. Tento displej by ukazoval kdo momentálně ve třídě učí, jaká je hodina, jestli se zrovna píše test nebo se koná jakákoliv jiná akce a také ukazuje vlhkost a teplotu. Tyto informace se budou **měnit pomocí webové stránky ve které se bude měnit rozvrh**.

## Cíle projektu
Projekt usnadní organizace rozvrhu ve třídách a zabraňuje chaosu. Taky slouží k tomu aby žáci nebyly rušeni u důležitého testu nebo přednášky.

## Technologie použité v projektu 
 - Projekt se skláda z displeje IC I2C OLED displej který jsme zvolili kvůli své velikosti a to tak aby mohl zobrazit všechny důležité informace které dostane ze serveru.
 - Dále je požit DHT22 senzor vlhkosti a teploty. Tyto údaje sbírá a následně zpracuje a pošle na server.
 - No a celé je to realizováno na bázi mikrokontroleru ESP32 ktérý pracuje se vstupními informacemi a pomocí možnosti připojení k WI-FI a spojení se serverem aktualizuje informace zobrazené na oled displeji.

## Kod projektu 
[odkaz na kod](https://github.com/tejdis/Ro-n-kov-projekt-Buchta-Bod-r-/files/15286696/kod_rocnikovyProjekt.txt)

## Myšlenková mapa projektu
- [odkaz na mapu](https://coggle.it/diagram/ZhYxdkyPtrFOtp73/t/%C5%A1koln%C3%AD-info-displej-do-t%C5%99%C3%ADd/49d55cb177ad203f6c6adf9fdd57f5cd9e96b59f15670b15d22ea9015311e86d)

## Fotodokumentace projektu 
![image](https://github.com/tejdis/Ro-n-kov-projekt-Buchta-Bod-r-/assets/167974463/028dd2a5-6b17-432c-ad90-524cbe6f6994)
![image](https://github.com/tejdis/Ro-n-kov-projekt-Buchta-Bod-r-/assets/167974463/c8ff4b43-0f34-450a-a287-57df68c956d5)

##Zdroje
[ChatGPT](https://www.google.com/url?sa=t&rct=j&q=&esrc=s&source=web&cd=&cad=rja&uact=8&ved=2ahUKEwjo77rUtYiGAxUQ7wIHHSgrN00QFnoECAYQAQ&url=https%3A%2F%2Fchat.openai.com%2F&usg=AOvVaw139HWUX4D802zbDuJCdFg9&opi=89978449)
[Dratek.cz](https://www.googleadservices.com/pagead/aclk?sa=L&ai=DChcSEwjW18nttYiGAxV9REECHYL9BvUYABADGgJ3cw&ae=2&gclid=CjwKCAjw0YGyBhByEiwAQmBEWpIzCoz6tDwKvLTWRvyTo1PSzzJDEnRrI9GkYLJCPlnIjxbB04C-bRoC2A4QAvD_BwE&ohost=www.google.com&cid=CAESVeD2HAAkjNmuOBGM72zIXyfo2-R8mO7K3DOdP9j2f7PST6wr8uaHpvDIQ3I2deZvLj5lFWQnfP7DsGzZcJ9gusBwEkPCx2O3XET_4UgbhAqFAzFPNmE&sig=AOD64_0T7KZvoc0seS55GHRkzubwIBSbQA&q&adurl&ved=2ahUKEwipncTttYiGAxV7xAIHHXtIDOEQ0Qx6BAgGEAE)
Informace a inspiraci jsme také čerpali z YouTube videí a různých on-line návodů.
