## Null Core
As a software developer, I enjoy using my skills in circumstances around me. One of the ways I have found to do this is by coding mods for Minecraft. As I coded different projects, I found that I was reusing the same classes of code repeatably in each project and determined to create a solution. At first, I started designing my own version of the community's common fix for this problem by creating a library mod. However, I soon determined that this would be inefficient as having a library mod just for common functions did not make sense. It was also annoying to the user who would have to get a second mod in order for the first one to work. Consequently, I developed a dependency that could be loaded with either Maven or Gradle called Null Core.

<p align="center">
  <img width="300" src="https://user-images.githubusercontent.com/101227901/187602588-616c254b-cd0d-4890-af1a-1f23448e42bb.png" alt="Null Core's Project Icon">
  <br>
  <i>The Null Core Project's Logo</i>
</p>

Null Core takes advantage of the open source project [JitPack](https://jitpack.io/) in order to allow developers to either use Maven or Gradle to import the framework into their project. I have written a comprehensive tutorial on the Project's GitHub page to walk developers through the steps of using JitPack to load Null Core.

Null Core features well documented and coded short cuts that allow coders to develop mods faster with the [Spigot](https://www.spigotmc.org/) modding framework. It features an extend version of the base main class that allows logging to be reached faster, messages sent to players with ease, and for the mod to be able to quickly set and get it's personal colored tag.

<p align="center">
  <img width="500" src="https://user-images.githubusercontent.com/101227901/187603201-8f3c31ed-4d03-49b4-89f7-7dd3e8c72c28.png" alt="Null Core's AugmentedJavaPlugin Class">
  <br>
  <i>Console Messenger Methods that Automatically Translate in-game Color Codes</i>
</p>

Null Core also features a storage type known as Plugin Configuration that allows developers to easily store and read their mod's settings. This allows programmers to save time by not coding out massive lists of variables, getters, and setters for global mod settings. Instead they can create a Plugin Configuration object and store their variables inside.

<p align="center">
  <img width="500" src="https://user-images.githubusercontent.com/101227901/187603378-cd393a1f-4901-422a-98ad-eca8183105ee.png" alt="Null Core's PluginConfiguration Class">
  <br>
  <i>A Custom Setting Storage Type Known as PluginConfiguration</i>
</p>

If you wish to check out my work, progress, or code on Null Core, you can click [here](https://github.com/RT5Phantom/NullCore) for a link to the Null Core Project's repository.
