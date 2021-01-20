# Saplings

## Example

```yaml
items:
  orange_tree_sapling:
    display_name: Sapling
    permission: orange_tree_sapling
    resource:
      material: ORANGE_WOOL
      generate: true
      textures:
      - block/orange/sapling.png
    behaviours:
      sapling:
        tree_populator: orange_tree
```

```yaml
trees_populators:
  orange_tree:
    worlds:
    - world
    chance: 5.0
    max_height: 100
    min_height: 50
    amount: 3
    iterations: 2
    log: newtrees:orange_tree_log
    leaves: newtrees:orange_tree_leaves
    tree_type: 
    biomes:
    - MOUNTAINS
```

