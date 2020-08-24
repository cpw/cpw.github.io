# Modding, the EULA and name files

## Automatic Copyright

Copyright, under the Berne Convention, is implicit in all works by [Article 5 (2) of the Berne Convention](https://en.wikisource.org/wiki/Convention_for_the_Protection_of_Literary_and_Artistic_Works/Articles_1_to_21#Article_5).

> (2) The enjoyment and the exercise of these rights shall not be subject to any formality; such enjoyment and such exercise shall be independent of the existence of protection in the country of origin of the work. Consequently, apart from the provisions of this Convention, the extent of protection, as well as the means of redress afforded to the author to protect his rights, shall be governed exclusively by the laws of the country where protection is claimed.

Note that this applies to all creative works. Your mod _has_ copyright associated with it.

## The game's copyright

Now, Mojang also owns a very important copyright: the game. This has been true since the beginning, and remains true today.

Mojang has the right to control distribution of anything relating to the game and it's copyright from [Article 2 of the Berne Convention](https://en.wikisource.org/wiki/Convention_for_the_Protection_of_Literary_and_Artistic_Works/Articles_1_to_21#Article_2).


Mojang has, through the action of the [EULA](https://account.mojang.com/documents/minecraft_eula), permitted others to alter the game under the terms of the EULA.

> If you've bought the Game, you may play around with it and modify it by adding modifications, tools, or plugins, which we will refer to collectively as "Mods." By "Mods," we mean something original that you or someone else created that doesn't contain a substantial part of our copyrightable code or content. When you combine your Mod with the Minecraft software, we will call that combination a "Modded Version" of the Game. We have the final say on what constitutes a Mod and what doesn't. You may not distribute any Modded Versions of our Game or software, and we’d appreciate it if you didn’t use Mods for griefing. Basically, Mods are okay to distribute; hacked versions or Modded Versions of the Game client or server software are not okay to distribute.

This is the primary permission to "Mod" the game from the EULA. Note that Mojang does not give laissez-faire permission to mod anything you want - it's clear that the "don't be a dick" rules apply here.

## Right to mod

As such, our "right" to distribute our mods, as derivative works of the game, comes from the permission granted in the EULA. If this were to change, it is likely that we would lose the right to mod from the point in time of the change, but not retroactively (we have a persuasive argument that we had the right to mod at the time).

If you believe the EULA in it's current incarnation does not apply to you, then you should probably stop modding, as you have no legal permission to mod the game, in that case.

## The name files

The "name files" are a set of reverse mapping data allowing the derivation of the original naming of the source code of the game. They have been distributed by Mojang in an effort to ease development of mods and especially mod platforms, and it has been hoped to allow signficantly greater interoperability.

The discussion to date revolved around the fact that these files did not have the same permissions as granted by the EULA, thereby probably causing a significant copyright risk. See my discussion [here](http://cpw.github.io/MinecraftMappingData.html) for more on why I believe that that was the case.

_This has now, in my opinion, been fixed_. The naming files have had their copyright statement amended to explicitly allow all permissions existing from the EULA.


```
© 2020 Microsoft Corporation. These mappings are provided"as-is" and you bear the risk of using them. You may copy and use the mappings for development purposes, but you may not redistribute the mappings complete and unmodified. Microsoft makes no warranties, express or implied, with respect to the mappings provided here.  Use and modification of this document or the source code (in any form) of Minecraft: Java Edition is governed by the Minecraft End User License Agreement available at https://account.mojang.com/documents/minecraft_eula.
```

Note that this file is now explicitly allowed to be used in the same manner as other parts of the game, under the permission of the EULA. `Use and modification of this document ...`.

In my opinion, this change means that the mapping file data is now part of the data and permissions granted by the EULA. In other words, if you were allowed to do it by the existing EULA, you are still allowed to do it, _with these mapping files as part of your workflow_ by the new statement.

## Conclusion

We are allowed to distribute our mods by permission from the EULA, and we are now also allowed to distribute mods using the naming derived from the name files provided by Microsoft, under the same permission.