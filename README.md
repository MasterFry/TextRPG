

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

[General JSON File definition](http://json.org/)

#### Structure

    { Items , Mobs , Places , Regions , Merchants }

#### Items

    Items : [Item , ..]

    Item   : { Id(int) , Name(string) , Weight(int) , Price(int) [, Description(string) ] }
    Weapon : { Id(int) , Name(string) , Weight(int) , Price(int) , AttackPower(int) [, Description(string) ] }
    Armor  : { Id(int) , Name(string) , Weight(int) , Price(int) , ArmorPoints(int) [, Description(string) ] }
    Potion : { Id(int) , Name(string) , Weight(int) , Price(int) , HealValue(int) [, Description(string) ] }
    
#### Mobs

    Mobs : [Mob , ..]

    Mob : { Id(int) , Name(string) , AttackPower(int) , DropItemId(int) , Dialog(string) }

#### Places

    Places : [Place , ..]
    
    Place : { Id(int) , Name(string) , MobId(int) }
    Place : { Id(int) , Name(string) , MerchantId(int) }
    
#### Regions

    Regions : [Region , ..]

    Region : { Name(string) , Description(string) , PlaceIds[int , ..] }

#### Merchants

    Merchants : [Merchant , ..]
    
    Merchant : { Id(int) , Name(string) , SellItemId(int) }
    
