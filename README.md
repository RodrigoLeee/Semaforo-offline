# Parte 1 Blink Led Interno Arduino
Este repositório contém um projeto fictício para o Departamento de Engenharia de Trânsito, no qual existe a responsabilidade de controlar o fluxo em uma via movimentada do bairro Butantã. É um desenvolvimento de um sistema essencial para o controle de trânsito. Possui montagem e programação.

### Montagem no TinkerCad
<div align="center">
    <img src="assets/semaforoarduino1.png" alt="Imagem do Arduino 1" width="1000"/>
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

void setup() {
  // Configura os pinos como saída
  pinMode(ledVerde, OUTPUT);
  pinMode(ledAmarelo, OUTPUT);
  pinMode(ledVermelho, OUTPUT);
}

void loop() {
   // Liga o LED vermelho e espera 6 segundos
  digitalWrite(ledVermelho, HIGH);
  delay(6000);
  digitalWrite(ledVermelho, LOW);
  
  // Liga o LED amarelo e espera 2 segundos
  digitalWrite(ledAmarelo, HIGH);
  delay(2000);
  digitalWrite(ledAmarelo, LOW);
  
  // Liga o LED verde e espera 4 segundos
  digitalWrite(ledVerde, HIGH);
  delay(4000);
  digitalWrite(ledVerde, LOW);

  // Liga o LED amarelo e espera 2 segundos
  digitalWrite(ledAmarelo, HIGH);
  delay(2000);
  digitalWrite(ledAmarelo, LOW);
}
```

### Testando Protótipo (Vídeo)




