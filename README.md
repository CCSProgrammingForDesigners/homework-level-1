# homework-level-1
homework with cookies



#include "config.h"
AdafruitIO_Feed *ozcups = io.feed("ozcups");

int cup = 1;
int y = 1;
int oz = 0;
int switcher = 2;



void setup() {
  io.connect();
  Serial.begin(9600);
  pinMode(cup, INPUT);
  pinMode(switcher, INPUT);
  
 }

void loop() {

  io.run();
  int Switch_Switch = digitalRead(switcher);
  int cup_cup = digitalRead(cup);

          
  if (Switch_Switch == HIGH){
      oz =0;
      Serial.println(oz);
      ozcups ->save(oz);
     }

  if(cup_cup == HIGH && oz>=0 && oz<35 && y==1){
      y = 2;
      oz++;
      Serial.println(oz);
      ozcups ->save(oz);
     }
     else if(cup_cup == HIGH && oz >= 35){
      y = 2;
      oz=0;
      ozcups ->save(oz);
     }

     if(cup_cup == LOW && oz>= 0 && oz<35 && y==2){
           y=1;
          }›››››
   } 
    
    
