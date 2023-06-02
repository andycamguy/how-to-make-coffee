## // Assign Variables
INIT Sink, Cup, Filter, Coffee_Grounds, Milk, Sugar, Spoon
INIT Coffee-Maker (Coffee-Pot, filter-place, water-tank)
# Variables

## Sink
 - a sink is a water dispenser used for washing and acquiring refreshment.

## Coffee-Pot

-a piece of the coffee maker used to hold the finished coffee of the brewing process

## Filter
-a piece of permeable paper that strains water through the coffee grounds 
## Cup
- a container with a small handle to insert a person's fingers to hold the object with its fluids


## Coffee_Grounds
these are the ground seeds of the coffee cherries, as a crucial part of the brewing process.

## Milk
- the result of pasteurized cow milk to soothe out the harshness of the coffee
## Sugar
- used to dampen the bitterness of coffee and replace the taste with a sweeter one.
## Spoon
- a kitchen utensil to be used to mix the coffee, milk and sugar into a homogenous solution.

# Functions
## POUR
- to pour a liquid from a container to another
## ADD
- to add a solid from a place to a a container
## REMOVE
- to take something out of a device or area for a purpose
## INSERT
- reverse function of REMOVE
## MIX
- the combining force of ingredients
# BREW COFFEE ---
  (
  START Coffee_Maker
//Patiently watch and wait for Coffee to drip down through filter towards the pot
  IF Coffee-Pot is FULL
    TURN OFF Coffee_Maker
    REMOVE Coffee-Pot from Coffee_Maker
    
  ELSE
    wait for Coffee-pot to fill
    )


# Process
## Procedural 
BEGIN
INIT
COMPUTE
RENDER
END
## Functional / OBJECT ORIENTED
BEGIN
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
END


