# Parte 1 Blink Led Interno Arduino
Este repositório contém um projeto fictício para o Departamento de Engenharia de Trânsito, no qual existe a responsabilidade de controlar o fluxo em uma via movimentada do bairro Butantã. É um desenvolvimento de um sistema essencial para o controle de trânsito. Possui montagem e programação.

### Montagem no TinkerCad
<div align="center">
    <img src="assets/semaforoarduino1.jpg" alt="Imagem do Arduino 1" width="1000"/>
    <br>
    <sup>Imagem do Arduino 1 - Fonte: TinkerCAD</sup>
</div>

### Montagem Física
<div align="center">
    <img src="assets/123.png" alt="Imagem do Arduino 1" width="1000"/>
    <br>
    <sup>Imagem do Arduino 1 - Fonte: TinkerCAD</sup>
</div>

### Código
Aqui está o código:
``` C++
// Definindo os pinos dos LEDs
int ledVerde = 9;
int ledAmarelo = 6;
int ledVermelho = 3;
int ldrPin = A5; // Pino do sensor LDR

void setup() {
  // Inicia a comunicação serial e configura os pinos dos LEDs como saída
  Serial.begin(9600);
  pinMode(ledVerde, OUTPUT);
  pinMode(ledAmarelo, OUTPUT);
  pinMode(ledVermelho, OUTPUT);
  //pinMode(ldrPin, INPUT);
}

void loop() {
  // Leitura do valor do sensor LDR
  int LDR = analogRead(ldrPin);
  Serial.print("Luminosidade: ");
  Serial.println(LDR);

  if (LDR > 200) {
    // Quando a luminosidade está baixa, executa a sequência do semáforo
    digitalWrite(ledVermelho, HIGH);
    delay(1000);
    digitalWrite(ledVermelho, LOW);
  
    digitalWrite(ledAmarelo, HIGH);
    delay(1000);
    digitalWrite(ledAmarelo, LOW);

    digitalWrite(ledVerde, HIGH);
    delay(4000);
    digitalWrite(ledVerde, LOW);

    digitalWrite(ledAmarelo, HIGH);
    delay(1000);
    digitalWrite(ledAmarelo, LOW);

  } else {
    // Quando a luminosidade está alta, executa a sequência do semáforo
    digitalWrite(ledVermelho, HIGH);
    delay(6000);
    digitalWrite(ledVermelho, LOW);
  
    digitalWrite(ledAmarelo, HIGH);
    delay(2000);
    digitalWrite(ledAmarelo, LOW);
  
    digitalWrite(ledVerde, HIGH);
    delay(4000);
    digitalWrite(ledVerde, LOW);

    digitalWrite(ledAmarelo, HIGH);
    delay(2000);
    digitalWrite(ledAmarelo, LOW);
  }
}
```

### Testando Protótipo (Vídeo)




