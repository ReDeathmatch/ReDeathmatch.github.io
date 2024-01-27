## Summary
The ReDeathmatch mod is a modern alternative that has active support from the creators. It fixes the shortcomings of existing alternatives and adds new features. The mod relies on community support for issue identification and resolution, and suggestions for new functionality are welcome.

| Name                              | ReHLDS Compatibility | Multilingual | Author Support | Documentation | Stability |
|:---------------------------------:|:--------------------:|:------------:|:--------------:|:-------------:|:---------:|
| ReDeathmatch by Sergey Shorokhov  | ✅                  | ✅          | ✅             | ✅           | ❌ (beta)  |
| CSDM ReAPI by wopox1337           | ✅                  | ✅          | ❌             | ❌           | ✅         |
| ReCSDM by ReHLDS team             | ✅                  | ❌          | ❌             | ❌           | ✅         |
| CSDM ReAPI by Vaqtincha           | ✅                  | ❌          | ❌             | ❌           | ❌         |
| CSDM 2.1.2 by BAILOPAN            | ❌                  | ❌          | ❌             | ✅           | ✅         |

## CSDM 2.1.2 by BAILOPAN
- Website: [https://www.bailopan.net/csdm/](https://www.bailopan.net/csdm/)
- Git: [https://github.com/Arkshine/CSDM](https://github.com/Arkshine/CSDM)
- Forum: [AlliedModders Forum](https://forums.alliedmods.net/forumdisplay.php?f=87)

The original CSDM mod provides a stable and well-functioning foundation. Parts of the mod that consume a lot of CPU resources have been moved to a separate Metamod module (written in C++), which reduces the load. The necessary code for working with AMX Mod X has been extracted into an API[^1]. Most of the logic is implemented through AMX Mod X plugins.

This mod is the only option for use with a regular HLDS server to date. It is not compatible with ReGameDLL.

It should be noted that the original CSDM mod does not support multilingualism, except for user modifications.

## ReCSDM by ReHLDS team
- Git: [https://bitbucket.org/Adidasman/recsdm/src/master/](https://bitbucket.org/Adidasman/recsdm/src/master/)
- Forum: [Dev-CS.ru](https://dev-cs.ru/resources/74/)

ReCSDM is a modification of the base CSDM by BAILOPAN to improve compatibility and functionality on ReHLDS & ReGameDLL. It includes small fixes and new features. It is the most popular and stable option for use with ReHLDS.

It should be noted that the ReCSDM mod does not support multilingualism, except for user modifications.

## CSDM ReAPI by Vaqtincha
- Forum: [GoldSrc.ru](https://goldsrc.ru/threads/1955/)

This is a reimagining of the CSDM mod developed by the BAILOPAN team. The new version incorporates enhanced functionality from ReHLDS & ReGameDLL and ReAPI, offering some performance improvements.

However, this version does not fully replace the original mod due to the absence of certain features. Specifically, the ability to pause the mod, support for Team Deathmatch mode, and item spawning mode (csdm_items) are missing in the new version.

Despite this, many new features and improvements have been added by rewriting outdated code and removing AMXX modules previously used in other CSDM mods, such as ReCSDM.

However, along with the improvements, there may be some issues with the respawn system. Please be aware of this.

It should be noted that the CSDM ReAPI mod by Vaqtincha does not support multilingualism, except for user modifications.

## CSDM ReAPI by wopox1337
- Git: [https://github.com/wopox1337/CSDM-ReAPI](https://github.com/wopox1337/CSDM-ReAPI)

This is an enhanced version of CSDM ReAPI by Vaqtincha, adding multilingual support and partially fixing the respawn system and minor bugs. It brings new functionality and improves integration with ReGameDLL by utilizing its updated features.

Development of this version has been discontinued by the author due to fundamental changes. Work on continuing the mod's concept is being done in ReDeathmatch.

[^1]: API (Application Programming Interface) is a set of methods and rules by which different programs or parts of a program communicate with each other and exchange data. For example, AMXModX uses HLDS API through integration via Metamod API, which provides a multitude of methods to work with the game engine.
