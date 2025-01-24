# Examples

## Basic Examples

### Player Name Check
```yaml
easyph_isadmin:
  placeholders:
    - '%player_name% == Junkeh'
  output: '<red>Server Admin'
```

### Level System
```yaml
easyph_level:
  types:
    - priority: 1
      placeholders:
        - '%player_level% >= 50'
      output: '<gold>High Level'
    
    - priority: 2
      placeholders:
        - '%player_level% >= 25'
        - '%player_level% < 50'
      output: '<yellow>Mid Level'
    
    - priority: 3
      placeholders:
        - '%player_level% < 25'
      output: '<gray>Low Level'
```

## Advanced Examples

### Rank Display with RGB Colors
```yaml
easyph_rank:
  types:
    - priority: 1
      placeholders:
        - '%vault_rank% == Owner'
      output: '&#ff0000Owner &#ffff00✦'
    
    - priority: 2
      placeholders:
        - '%vault_rank% == Admin'
      output: '&#ff4400Admin &#ffaa00★'
    
    - priority: 3
      placeholders:
        - '%vault_rank% == Mod'
      output: '&#00ff00Mod ✔'
```

### Complex Conditions
```yaml
easyph_status:
  types:
    - priority: 1
      placeholders:
        - '%player_health% <= 5'
        - '%player_is_flying% == false'
      output: '<red>⚠ Low Health!'
    
    - priority: 2
      placeholders:
        - '%player_is_flying% == true'
      output: '<aqua>✈ Flying'
    
    - priority: 3
      placeholders:
        - '%player_is_sneaking% == true'
      output: '<gray>🦊 Sneaking'
```

### Money Display
```yaml
easyph_money:
  types:
    - priority: 1
      placeholders:
        - '%vault_eco_balance% >= 1000000'
      output: '&#ffd700$%vault_eco_balance% &#ffff00💰'
    
    - priority: 2
      placeholders:
        - '%vault_eco_balance% >= 100000'
      output: '<gold>$%vault_eco_balance% 💰'
    
    - priority: 3
      placeholders:
        - '%vault_eco_balance% < 100000'
      output: '<yellow>$%vault_eco_balance%'
```
