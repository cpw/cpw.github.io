# A brief statement on Minecraft Mapping data

## Overview

On 4th September, 2019, Mojang published [snapshot 19w36a][1]. A feature highlight is the following:

> In an effort to help make modding the game easier, we have decided to publish our game obfuscation maps with all future releases of the game, starting today. This means that anyone who is interested may deobfuscate the game and find their way around the code without needing to spend a few months figuring out what’s what. It is our hope that mod authors and mod framework authors use these files to augment their updating processes that they have today. These mappings will always be available, instantly and immediately as part of every newly released version. This does not, however, change the existing restrictions on what you may or may not do with our game code or assets. The links to the obfuscation mappings are included as part of the version manifest json, and may be automatically pulled for any given version.

On first glance, this looks amazing! We have finally been given public access to the obfuscation data used by Mojang themselves.
However, this data comes with a very significant problem:

>  Prefixed to every obfuscation map is the following legal disclaimer:
>
> © 2019 Microsoft Corporation. All rights reserved. This information is provided “as-is” and you bear the risk of using it. This information does not provide you with any legal rights to any intellectual property in any Microsoft product. You may copy and use this information for your internal, reference purposes. Microsoft makes no warranties, express or implied, with respect to the information provided here.

## The legal problem

Firstly, a **huge great big fat caveat**. This is not legal advice. This is an extremely pessimistic view of what was clearly intended as a goodwill gesture from Mojang and Microsoft.

However, today's friendly demeanor does not represent all possible future states. We have to exercise the most extreme caution when we really want something and are seemingly given it, out of the blue.

Finally, legal matters are boring, pragmatic, but ultimately very important. Many members of the modding community are adults leading normal lives. The impact of a high profile copyright violation case would be devastating to them. Modding has lots of unilluminated legal areas. Let us not walk into obvious well lit legal traps.

### `internal, reference purposes`

There is a very significant legal problem with this statement. It seems that any use of this information in a public fashion will render them in direct violation of an explicitly stated
copyright notice expressing the desire *not* to use this information in any public fashion. This means that any project exposing this mapping data in a public fashion, such as by publishing
source using this naming scheme would be in direct violation of Microsoft's license.

Is this a valid legal analysis? I don't know. But the safest approach seems to be that we should continue as if this information had never existed, for *public* consumption. This discussion comes from that vantage point.

Note that private formal arrangements have existed for sharing similar data with Minecraft Mod platform projects prior to this information release. We take it on good faith that Microsoft permits that use to continue, as it does
not result in published artifacts containing this data in any fashion.

## What does this mean

This means that Forge will not be:
1. Publishing an "official mapping" version of Forge.
2. Providing an "officially mapped" deobfuscation map to be used at runtime.
3. Supporting mods distributed using "officially mapped" naming in their compiled names.

The MCP project will:
1. Continue to exist (sorry Searge!). It was needed anyway, but it will remain in its current form in its entirety.
2. Strive to avoid accepting names from the official naming into the MCP repository from now on. We cannot completely avoid pollution from
official names, but we should try and avoid it where we can.
3. The MCP project recommends similar safeguards be put in place for our fellow naming project, Yarn, used by Fabric.

No mod should:
1. Knowingly publish source or artifacts that use these names in any form.

## Clarification

Myself and LexManos have reached out to Mojang in an effort to clarify the license above. We have only received "we realize there's a problem here and we're looking into it" in response. We hope to receive clarification in future that mods and forge are able to refer these names in their source and compiled forms _as published artifacts_, thereby releasing us from this binding.

It is a pity that they failed to consult with us before this move, as we could have quickly apprised them of the _real_ uses of this information, as "internal reference" is very much a poison chalice, and offers nothing we 
didn't already have, and potentially puts in jeopardy abilities we previously _did_ have.

## TLDR
The mapping information has the potential to be truly transformative, and I'm certain that Mojang and Microsoft had nothing but those intentions in mind when they did this. However, in my opinion, the mapping information with this license is legal poison, and should not be used in any published artifact by any mod or mod framework. I sincerely hope Mojang can clarify this and remove the poison, to allow impactful transformation of modding.

[1]: https://www.minecraft.net/en-us/article/minecraft-snapshot-19w36a

## Update: August 2020 changes

On 11th August 2020, Dinnerbone tweeted: https://twitter.com/Dinnerbone/status/1293597326561488897?s=20 


