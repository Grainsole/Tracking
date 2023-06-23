#include <NewPing.h>
const int TRIGGER_ PIN = 27;
const int ECHO PIN = 26;
const int BUZZER PIN = 5;
const float MIN_DISTANCE = 10.0;
NewPing sonar (TRIGGER_PIN, ECHO_ PIN);
const int LED _BUILTIN = 14;
void setup(){
pinMode(BUZZER_PIN,OUTPUT);
pinMode(LED _BUILTIN, OUTPUT);

void loop(){
delay(50);//attente de 50 millisecondes pour eviter les lectures erronés
float distance = sonar.ping cm);
if (distance < MIN_DISTANCE) {
digitalwrite (BUZZER_PIN, HIGH);
digitalwrite(LED _BUILTIN, LOW);//activer le buzzer
}
else {
digitalwrite(BUZZER_PIN, LOW);
digitalwrite(LED_BUILTIN, HIGH);//désactiver le buzzer
  }
}
