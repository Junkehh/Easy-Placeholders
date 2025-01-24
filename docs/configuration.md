# Configuration Guide

## Basic Structure

The configuration file uses YAML format and follows this structure:

```yaml
placeholders:
  easyph_yourplaceholder:
    placeholders:
      - 'condition1'
      - 'condition2'
    output: 'result'
```

## Placeholder Types

### 1. Simple Placeholder

```yaml
placeholders:
  easyph_custom1:
    placeholders:
      - '%player_name% == Junkeh'
    output: '<red>Yes'
```

### 2. Multi-Type Placeholder

```yaml
easyph_meow:
  types:
    - priority: 1
      placeholders:
        - '%player_name% == Junkeh'
        - '%player_is_op% == yes'
      output: '&#ff00ff:33'
    
    - priority: 2
      placeholders:
        - '%player_is_op% == yes'
      output: '<gold>:3'
```

## Comparison Operators

| Operator | Description | Example |
|----------|-------------|---------|
| == | Equals | `'%player_name% == Junkeh'` |
| != | Not equals | `'%player_name% != Junkeh'` |
| > | Greater than | `'%player_level% > 50'` |
| < | Less than | `'%player_level% < 25'` |
| >= | Greater than or equal | `'%player_level% >= 50'` |
| <= | Less than or equal | `'%player_level% <= 25'` |

## Color Formatting

### RGB Colors
Use the `&#RRGGBB` format:
```yaml
output: '&#ff0000This is red'
```

### Named Colors
Use `<color>` format:
```yaml
output: '<red>This is red'
```

Available colors:
- `<black>`
- `<dark_blue>`
- `<dark_green>`
- `<dark_aqua>`
- `<dark_red>`
- `<dark_purple>`
- `<gold>`
- `<gray>`
- `<dark_gray>`
- `<blue>`
- `<green>`
- `<aqua>`
- `<red>`
- `<light_purple>`
- `<yellow>`
- `<white>`

## Priority System

Lower numbers have higher priority:
```yaml
types:
  - priority: 1  # Highest priority
    placeholders:
      - '%player_level% >= 50'
    output: '<gold>High Level'
  
  - priority: 2  # Medium priority
    placeholders:
      - '%player_level% >= 25'
    output: '<yellow>Mid Level'
```

Types without priority get lowest priority.
