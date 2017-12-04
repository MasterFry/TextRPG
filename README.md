

### Gameplay

All of the games content are stored in a .json file.
See JSON section for details.

You can:
 - encounter and battle enemies, get loot if enemies are defeated
 - sell loot at merchants
 - buy new items at merchants
 - un-/equip items
 - level up
 
### COMMANDS:

#### General:
    inv  - shows inventory
    help - shows helpdesk
    eqp [name] - equip item from inventory
    go [place] - go somewhere else, ? to list available places
    
#### Combat:
    atk [n] - use the attack [n] ([n] e{1-9} = number of the attack, ? to list avaliable attacks)
    pot [n] - use the pot [n] (see above)
    run   - run away
    
### JSON File

#### Structure

{ Items , Monsters , Regions , Merchants }

#### Items

Items : [Item , ..]

Item : { Name(string) , Weight(int) , Price(int) , Type(int) [, Type-Specific-Values ] [, Description(string) ] }
    
Types :
 * Trash  = 0:
 * Weapon = 1: AttackPower(int) , AttackSpeed(int)
 * Armor  = 2: Slot(int) , ArmorPoints(int)
 * Potion = 3: HealValue(int)
    
#### Monsters

Monsters : [Monster , ..]

Monster : { Name(string) , Rarity(int) , AttackPower(int) , AttackSpeed(int) , LootTable(LootTable) , Dialog(Dialog) }
    
#### Regions

Regions : [Region , ..]

Region : { Name(string) , Description(string) , Places : [Place , ..] , Cities : [City , ..] }


    
    
