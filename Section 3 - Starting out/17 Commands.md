```
public class HealCommand implements CommandExecutor {  
  
  
@Override  
public boolean onCommand(CommandSender commandSender, Command command, String s, String[] strings) {  
  
if (commandSender instanceof Player) {  
Player player = (Player) commandSender;  
player.sendMessage("Santé est remis");  
player.setHealth(20);  
player.playSound(player.getLocation(), Sound.BLOCK_NOTE_BLOCK_HARP, 1.0f, 1.0f);  
player.  
}  
  
  
  
return false;  
}  
}
```

```
@Override  
public void onEnable() {  
System.out.println("[Clara] Start");  
Bukkit.getPluginManager().registerEvents(this, this);  
  
getCommand("heal").setExecutor(new HealCommand());  
  
}
```

```
commands:  
heal:  
description: descriptionx
```