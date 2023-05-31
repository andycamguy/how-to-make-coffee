BEGIN
INIT Sink, Coffee_Pot, Coffee_Maker, Cup, Filter, Coffee_Grounds

START Sink
REMOVE Coffee_Pot from Coffee_Maker
  WHILE Coffee_Pot.full = 'false'
  {
    FILL Coffee_Pot with Water
   }
