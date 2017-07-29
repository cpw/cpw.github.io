# On Mod Verification
*This is intended as a discussion document on how to verify mods. It is not a solution. It is to stimulate discussion around developing a solution*

### What we can know at runtime
1. The certificate used to sign the JAR.
  - This certificate could be customized with additional X509 fields.
  - It signs all the code, therefore the code is expected to be signed, and can't easily be replaced with alternatively signed code.
2. Any metadata we wish to add to the JAR to provide additional vectors for identification for authorship.
  - We could add a field to mcmod.info or MANIFEST.MF for example, indicating some kind of authorship identification token.
  - These fields are implicitly signed so cannot easily be tampered with

### What we want to know
1. The mod was compiled by a toolchain authorized to compile it.
  - Mods compiled by unauthorized entities, with unknown additional changes to the mod, have started surfacing in the ecosystem.
  - Mods pretending to be official have been surfacing.
2. The identification data is valid.
  - There is an element of the community that wishes to imposter "famous" modders.
 
 
## Identity

Ultimately, the goal is that a certificate signing a mod, is published by a known actor, and the known actor issued the certificate for that mod.
Note, identity isn't intended to be real world identity. No one in modded minecraft cares what the author's real name is. They care that the apparent author is the actual author (to the extent they care at all).

This presents the first problem, however. Trust. Trust is at the heart of the issue. Any third party authorized to act as an identity provider needs to be trusted by all. There is no one in that place within the minecraft community. Many trust no one (because paranoia?). The people who care most about this kind of problem are probably also the least trusting.

Ultimately, the only commonly manageable way to handle identity is to have someone act as a source of truth. Distributed identity systems are very nascent, and technologically sophisticated, and probably require a level of effort far beyond what most mod authors would care to do (blockchain techniques? en-masse cross signing of certificates? Perspectives style?).

## Verification
Once we have solved the problem of tracking identity, we need to then verify that a particular load of mods on a system is valid. Specifically, we need to create some kind of validation artifact that asserts that every mod is signed with a correct identification based on known metadata for that mod.

My thoughts are that a separately distributed verification tool can be run to generate a secure token containing the verification state of the mod list for a particular minecraft home. Note: having an external tool allows both client *and* server verification. It can be strongly secured as well, since it would be a binary under separate control. Maybe it could be hosted externally, and deliver tokens via an API?

## Runtime
At runtime, forge's only task would be to inspect the token and present the data within in the UI. The only validations would be certificate matching (already performed). Otherwise, the token data would be logged and presented in the mod UI, perhaps through means of a green tick indicator.
