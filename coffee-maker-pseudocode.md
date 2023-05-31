BEGIN
INIT Sink, Coffee-Pot,  Cup, Filter, Coffee_Grounds, Milk, Sugar, Spoon
INIT Coffee_Maker (Coffee-Pot, filter_place)
START Sink
REMOVE Coffee-Pot from Coffee_Maker //pop it from the array
  WHILE Coffee-Pot is empty  //Boolean False
  {
    FILL Coffee-Pot with Water
   }
 TURN Sink OFF
  WHILE Coffee_Maker is empty // boolean false  
 {
  FILL Coffee_Maker with Water
 }
PLACE Coffee-Pot in Coffee_Maker //push into the array
PLACE Filter in Coffee_Maker //push into the array
COMPUTE (amount of Coffee_Grounds) to INSERT Coffee_Maker.filter_place
START Coffee_Maker
//Patiently watch and wait for Coffee to drip down through filter towards the pot
  IF Coffee-Pot is FULL
    TURN OFF Coffee_Maker
    REMOVE Coffee-Pot from Coffee_Maker
    
  ELSE
    Coffee-Pot ++ 
WHEN Coffee_Maker is OFF
    POUR Coffee from Coffee Pot into Cup
    POUR Milk into Cup
    ADD Sugar into Cup
Mix ingredients in Cup



