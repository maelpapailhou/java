```
public class ArgsCommand implements CommandExecutor {  
  
  
@Override  
public boolean onCommand(CommandSender commandSender, Command command, String s, String[] strings) {  
  
if (commandSender instanceof Player) {  
  
if (strings.length == 1) {  
if (strings[0].equalsIgnoreCase("hello")) {  
((Player) commandSender).sendMessage("yop");  
  
}  
  
}  
  
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
getCommand("cc").setExecutor(new ArgsCommand());  
  
Bukkit.getServer().setDefaultGameMode(GameMode.SURVIVAL);  
  
}
```