# Spigot-ItemBuilder
Item Builder class for spigot

This is a builder class for easy building of ItemStacks

Both the ItemBuilder and CustomItem classes are required to use this

To use the builder class create create a new instance of ItemBuilder and pass in a Material, then use the methods to set the item values and call the build method.

Examples:

ItemStack item = new ItemBuilder(Material.DIAMOND_SWORD).name("Test").addEnchant(Enchantment.DAMAGE_ALL, 10).addLore("Hello").build();

ItemStack item = new ItemBuilder(Material.POTATO).name(ChatColor.RED + "Hot Potato").addEnchant(Enchantment.FIRE_ASPECT, 5).amount(10).addFlag(ItemFlag.HIDE_ENCHANTS).build();

There are also methods for setting potion, armor, and enchanted book metas.

Examples:

ItemStack item = new ItemBuilder(Material.POTION).type("potion").addPotionEffect(new PotionEffect(PotionEffectType.SPEED, 1200, 10)).potionColor(Color.AQUA).build();

ItemStack item = new ItemBuilder(Material.LEATHER_CHESTPLATE).type("leatherarmor").name("Red Shirt").armorColor(Color.RED).build();

ItemStack item = new ItemBuilder(Material.ENCHANTED_BOOK).type("enchantedbook").addStoredEnchant(Enchantment.LOOT_BONUS_BLOCKS, 100).build();
