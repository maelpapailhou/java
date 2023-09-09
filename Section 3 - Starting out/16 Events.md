https://hub.spigotmc.org/javadocs/bukkit/org/bukkit/event/Event.html

---
```
public final class Main extends JavaPlugin implements Listener {  
  
@Override  
public void onEnable() {  
// Plugin startup logic  
System.out.println("[CLARA] : OK");  
Bukkit.getPluginManager().registerEvents(this, this);  
  
}  
  
@EventHandler  
public void onPlayerMove(PlayerMoveEvent e) {  
  
e.setCancelled(true);  
e.getPlayer().sendMessage("Stop moving!");  
  
}
```

---
```
@EventHandler  
public void onPlayerMove(PlayerMoveEvent e) {  
Player player = e.getPlayer();  
e.setCancelled(true);  
  
String titre1 = "Tu bouges pas";  
String title = "Votre titre";  
String subTitle = "Votre sous-titre";  
int fadeIn = 10; // Temps d'apparition en ticks  
int stay = 70; // Temps d'affichage en ticks  
int fadeOut = 20; // Temps de disparition en ticks  
  
player.sendTitle(title, subTitle, fadeIn, stay, fadeOut);  
}
```