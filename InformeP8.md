# Codi:

```
#include <Arduino.h>

void setup() {
  Serial.begin(115200);
  Serial2.begin(115200);
}

void loop() {
  if(Serial.available()){
    Serial2.write(Serial.read());
    delay(2);
    if(Serial2.available()){
      Serial.write(Serial2.read());
    } 
  }
}
```

## Funcionament:

Primer de tot es declaren les llibreries.

```
#include <Arduino.h>
```

Seguidament al setup inicialitzem el serial.

```
void setup() {
  Serial.begin(115200);
  Serial2.begin(115200);
}
```

Al loop es guardaran els caracters introduïts per teclat, que seran llegits pel serial i afegim un petit delay de escriptura.

```
void loop() {
  if(Serial.available()){
    Serial2.write(Serial.read());
    delay(2);
    if(Serial2.available()){
      Serial.write(Serial2.read());
    } 
  }
}
```

Per últim aquest es el resultat obtingut per pantalla mostrat en foto i vídeo:

![P8foto](https://user-images.githubusercontent.com/100867309/171399558-22a9160d-6e47-40d0-891d-f701703c0fc5.jpeg)



https://user-images.githubusercontent.com/100867309/171399679-15b0c372-90f3-49b7-aeb8-a6376e00ae06.mp4
