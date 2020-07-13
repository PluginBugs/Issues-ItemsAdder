# Impossible de récupérer l'entité à partir de l'ID

To fix this please install latest ProtocolLib [http://ci.dmulloy2.net/job/ProtocolLib%20Gradle/lastStableBuild/artifact/build/libs/ProtocolLib.jar](http://ci.dmulloy2.net/job/ProtocolLib%20Gradle/lastStableBuild/artifact/build/libs/ProtocolLib.jar)​

```text
[ItemsAdder] Unhandled exception occured in onPacketReceiving(PacketEvent) for ItemsAdder
java.lang.RuntimeException: Cannot retrieve entity from ID.
	at com.comphenix.protocol.wrappers.BukkitConverters$9.getSpecific(BukkitConverters.java:646) ~[?:?]
	at com.comphenix.protocol.wrappers.BukkitConverters$9.getSpecific(BukkitConverters.java:625) ~[?:?]
	at com.comphenix.protocol.reflect.StructureModifier.readInternal(StructureModifier.java:227) ~[?:?]
	at com.comphenix.protocol.reflect.StructureModifier.read(StructureModifier.java:195) ~[?:?]
	at dev.lone.itemsadder.Spigot.SpigotEntityFix$1.onPacketReceiving(Unknown Source) ~[?:?]
	at com.comphenix.protocol.injector.SortedPacketListenerList.invokeReceivingListener(SortedPacketListenerList.java:114) ~[?:?]
	at com.comphenix.protocol.injector.SortedPacketListenerList.invokePacketRecieving(SortedPacketListenerList.java:67) ~[?:?]
	at com.comphenix.protocol.injector.PacketFilterManager.handlePacket(PacketFilterManager.java:590) ~[?:?]
	at com.comphenix.protocol.injector.PacketFilterManager.invokePacketRecieving(PacketFilterManager.java:557) ~[?:?]
	at com.comphenix.protocol.injector.netty.ProtocolInjector.packetReceived(ProtocolInjector.java:352) ~[?:?]
	at com.comphenix.protocol.injector.netty.ProtocolInjector.onPacketReceiving(ProtocolInjector.java:317) ~[?:?]
​
```

