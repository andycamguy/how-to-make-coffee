## // Define Variables
INIT Sink, Coffee-Pot,  Cup, Filter, Coffee_Grounds, Milk, Sugar, Spoon
## // Define Functions
INIT Coffee-Maker (Coffee-Pot, filter-place)
START Sink
REMOVE Coffee-Pot from Coffee_Maker //pop it from the array
  WHILE Coffee-Pot is empty  //Boolean False
  {
    FILL Coffee-Pot with Water
   }
 TURN Sink OFF
  WHILE Coffee-Maker is empty // boolean false  
 {
  FILL Coffee-Maker with Water
 }
PLACE Coffee-Pot in Coffee-Maker //push into the array
PLACE Filter in Coffee-Maker //push into the array
COMPUTE (amount of Coffee-Grounds) to INSERT Coffee-Maker's filter-place
START Coffee-Maker
//Patiently watch and wait for Coffee to drip down through filter towards the pot
  IF Coffee-Pot is FULL
    TURN OFF Coffee-Maker
    REMOVE Coffee-Pot from Coffee-Maker
    
  ELSE
    Wait for Coffee-Pot to fill up
WHEN Coffee_Maker is OFF
    POUR Coffee from Coffee Pot into Cup
    POUR Milk into Cup
    ADD Sugar into Cup
Mix ingredients in Cup

## //END


