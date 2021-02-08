[FlagWar for Towny Advanced](https://townyadvanced.github.io/wars)
==================================================================

FlagWar is one of the first official war systems in the Towny Advanced ecosystem, dating back
around 2011. FlagWar works similar to a strategy game, where players can capture regions of other Nations and
Towns quickly and with pin-point precision.

> I started getting re-involved with Towny’s development, and got some inspiration from users about
> how to do warring Nations. I also took a gander at some of the mechanics of a similar plugin that
> did PvP stuff right, Factions. I coded up some threaded tasks that created a huge beacon in the
> sky overtop the area under attack. The game mechanic was to attack and hold the area. Towny’s war
> event is the same thing, but there’s nothing physical. So I created a focus for the defenders.
> Attacking would have the attacker place a flag, which the defenders would need to break / take
> down. I eventually merged this into the Towny plugin.&nbsp;&mdash;&nbsp;[@Zren](https://github.com/Zren)
> &ndash; [from his blog][zren-blog]

It has since then been adapted over time to retain its core functionality, while it continues to
provide server communities with a simple, yet fast and effective, way to capture territory.

About mid-2020, an effort to split it back off from Towny began. FlagWar was finally fully split off in 2021, marking
its 10th anniversary.

Sections
--------
1) [Licensing](README.md#Licensing)
2) [Administrator Resources](README.md#Administrator Resources)
   - [Supported Releases](README.md#Supported Releases)
   - [Staying up to Date](README.md#Staying up to Date)
   - [Getting Support](README.md#Getting Support)
3) [Developer Resources](README.md#Developer Resources)
   - [Contributing Code][contrib-code]
   - [Contributing Documentation][contrib-docs] - WIP
   - [Localizing FlagWar][contrib-localize] - WIP
   - [Building FlagWar](README.md#Building FlagWar)
4) [Supporting the Project](README.md#Supporting the Project)

Licensing
---------

<img align="right" height="155" src="https://opensource.org/files/OSI_Approved_License.png">

FlagWar is licensed under the [Apache License, Version 2.0][apache-v2], which is approved by the
[Open Source Initiative][osi] and is [GPL Compatible][gpl-apache].

<!--TODO: Move this to a wiki page, or something. It's good stuff, but it clutters an already cluttered README file.
On why we chose to avoid reusing the Towny license for FlagWar:
- It's ill advised by Creative Commons, FSF, and OSI. See: https://creativecommons.org/faq/#can-i-apply-a-creative-commons-license-to-software
- It's not a Free Culture license, as it restricts commercial and derivative works
- It does not have provisions for contributions to the work, resulting in the messy need to have contributors sign over
  their copyright.
- If Towny Advanced dies off, all subprojects under it's license cannot be adapted or extended.
- Assuming the Spigot license remains legally applicable, using Towny's license would be in violation of the GNU GPLv3.

Why we choose the Apache License for FlagWar:
- Longevity: Adaptions can legally outlive the originating codebase and developers' interests.
- Server Friendly: Perpetual license to use, including any relevant included patents held by contributors.
- Developer Friendly: Adaptions permitted, and offers the free exchange of ideas. Contributor agreements baked directly
  into the license.
- Attribution: Attribution is given within each class, and any outside work can be cited in the NOTICE file. It is
  also required of forks to appropriately give attribution back to the project.
-->

Some portions, such as shaded libraries, may be alternatively licensed. See the [NOTICE][notice] for any alternative
licensing or copyright limitations. Additionally, please respect [Towny's license][cc by-nc-nd 3.0] when used in
conjunction. FlagWar does not give legal bypasses for Towny's usage restrictions.

Documentation found on the [FlagWar Wiki][wiki] is licensed under [CC BY 4.0][cc by].

Administrator Resources
-----------------------

### Supported Releases

| FlagWar Release | Release Date | Minimum Requirements                             |
|:--------------: | :----------: | :----------------------------------------------: |
| 0.1.0 (Latest)  | xxxxx        | Towny 0.96.7.1, Spigot 1.14.4                    |
| _Pre-History_   | _2011_       | _Included in Towny until v0.9x.x.x; no support._ |

> We recommend administrators look into [PaperMC](https://papermc.io/), or one of its forks.
> 
> While FlagWar does not use the PaperAPI, Towny does make use of the PaperLib library to provide
> some optimizations. The PaperMC project also offers greater flexibility for a server
> administrator to take advantage of when compared to CraftBukkit or Spigot.

### Staying up to Date

<img align=right src="https://user-images.githubusercontent.com/879756/65964779-3a067200-e423-11e9-9928-938b976af2c2.gif" height="155">

All Release builds and Development builds are being made available here on GitHub's [Releases][releases] page.
We encourage server admins to "watch" FlagWar on GitHub in order to receive update notifications.
Just click the watch button in the upper right and select "Releases Only".

### Getting Support

The documentation found on the [FlagWar Wiki][wiki] will be updated every time a Release version of FlagWar is tagged.
If you find the documentation insufficient, please open an issue, and we will assess the need.

On the [Issue Tracker][issue-tracker] you can file [bug reports][bug],
[feature requests][feature], or reveiw / submit a [QA discussion][discuss-towny] on the Towny discussion board.

[![Average Issue Resolution Time][iim-time-badge]][iim-time] [![Percentage of Issues 'Open'][iim-percent-badge]][iim-percent]

If you still need help, come and join us on the [Discord server][discord], where you can find cutting edge updates and
discussions on the development of FlagWar, as well as the rest of the plugins in the Towny Advanced family.

Developer Resources
-------------------

### Contributing Code

If you would like to contribute to the FlagWar code, first please read the [Contributing Guidelines][contributing].

For basic work, involving only minor changes (1-2 lines), you can use GitHub's built-in editor after
forking the project.

For anything more involved, you will need to fulfill the following requirements:
- A [Java Development Kit][jdk], for Java SE 8 or higher
- A competent dditor or an Integrated Development Environment (IDE)
    - Competent Editors: 
      [Atom][atom], [Notepad++][npp], [Sublime Text][sublime], [Vim][vim], [Visual Studio Code][vscode]
    - Recommendable IDEs: [Apache NetBeans][netbeans], [Eclipse IDE][eclipse], [IntelliJ IDEA][idea]
- Apache Maven (See [Building FlagWar](#building-flagwar))

> Note that some IDEs bundle a JDK and Apache Maven. And for the love of all that is code, do not use Microsoft Notepad.

### Contributing Documentation
> Section Reserved

### Localizing FlagWar
> Section Reserved

### Building FlagWar

Building FlagWar requires the use of [Apache Maven][maven], [Git][git] (optional), a [Java Development Kit][jdk] for
Java 8 (or greater), and an internet connection. 

> If you run into "command not found" issues, please make sure your JAVA_HOME and PATH environment variables have been
> set. (Don't bother with your M2_HOME, that's [deprecated][m2home].)

1) Clone FlagWar from GitHub. 
   > Unfamiliar with Git? See the [GitHub Docs][github-docs], and refer to the [Git Documentation][git-docs].
2) From your terminal, navigate into the `FlagWar` directory
3) Run `mvn clean package` to build FlagWar. This will put generated files into the `FlagWar/target` directory.
   > If you run into "command not found" issues, please make sure you have everything required and that your environment
   > variables have been set.
   > This includes: JAVA_HOME, MAVEN_HOME, and your PATH which should contain both.
   >
   > If you use a Debian/Ubuntu-based distribution AND get JAVA_HOME errors, try adding the `-P no-jdoc` flag to your
   > Maven commands.

Alternatively, you can build it through your IDE, provided that it bundles with Maven, or that
it can at the very least find it. Check your IDE's documentation regarding Maven support.

Supporting the Project
----------------------

If you've found FlagWar to be of use and would like to support the project, then thank you!

You can support the project in multiple ways:
- Contribute to the project, be it through [adding or expanding a localization][contrib-localize], endorsing the project,
  hunting for bugs, [writing code][contrib-code], or [writing documentation][contrib-docs]. Any help is appreciated.
- Sponsor a Developer:
  Sponsoring a developer is appreciated as it gives back to those who have spent time to keep the project going.  
  See the sidebar for open sponsorships, and learn about GitHub's [Sponsors Program][gh-sponsors].

<!-- Links -->
[apache-v2]: LICENSE "Apache License, Version 2.0"
[atom]: https://atom.io/ "A hackable text editor for the 21st Century (Free, Cross Platform)"
[bug]: https://github.com/TownyAdvanced/FlagWar/issues/new?assignees=&labels=&template=bug_report.md&title= "Report a FlagWar bug"
[cc by-nc-nd 3.0]: https://creativecommons.org/licenses/by-nc-nd/3.0/legalcode "Creative Commons Attribution-NonCommercial-NoDerivs 3.0 Unported"
[cc by]: https://creativecommons.org/licenses/by/4.0/ "Creative Commons Attribution 4.0 International"
[contrib-code]: README.md#contributing-code "Contributing Code"
[contrib-docs]: README.md#contributing-documentation "Contributing Documentation"
[contributing]: ./.github/CONTRIBUTING.MD "FlagWar Contributing Guidelines"
[discord]: https://discord.gg/gnpVs5m "Join the TownyAdvanced Discord server"
[discuss-towny]: https://github.com/TownyAdvanced/Towny/discussions/categories/q-a "View Towny's Q&A Discussion Board"
[eclipse]: https://www.eclipse.org/eclipseide/ "The Leading Open Platform for Professional Developers"
[feature]: https://github.com/TownyAdvanced/FlagWar/issues/new?assignees=&labels=&template=feature_request.md&title=Suggestion%3A+ "Request a new feature or tweak"
[gh-sponsors]: https://github.com/sponsors "Invest in the software that powers your world"
[git-docs]: https://git-scm.com/doc "Git Documentation"
[git]: https://git-scm.org/ "Git Version Control Software"
[github-docs]: https://docs.github.com/ "GitHub Documentation"
[gpl-apache]: https://www.gnu.org/licenses/license-list.html#apache2 "GPL Compatible Free Software Licenses"
[idea]: https://www.jetbrains.com/idea/ "The Capable and Ergonomic Java IDE by JetBrains"
[iim-percent]: http://isitmaintained.com/project/TownyAdvanced/FlagWar "Percentage of Issues 'Open'"
[iim-percent-badge]: http://isitmaintained.com/badge/open/TownyAdvanced/FlagWar.svg
[iim-time]: http://isitmaintained.com/project/TownyAdvanced/FlagWar "Average Issue Resolution Time"
[iim-time-badge]: http://isitmaintained.com/badge/resolution/TownyAdvanced/FlagWar.svg
[iim-time]: http://isitmaintained.com/project/TownyAdvanced/FlagWar "Average Issue Resolution Time"
[issue-tracker]: https://github.com/TownyAdvanced/FlagWar/issues "FlagWar Issue Tracker"
[jdk]: https://sdkman.io/jdks "JDK Distributions | SDKMAN!"
[contrib-localize]: README.md#localizing-FlagWar "Localizing FlagWar"
[m2home]: https://issues.apache.org/jira/browse/MNG-5607 "Don't use M2_HOME in mvn shell/command scripts anymore"
[maven]: https://maven.apache.org/ "Apache Maven Software Project Management and Comprehension Tool"
[netbeans]: https://netbeans.apache.org/ "Fits the Pieces Together"
[notice]: NOTICE "Legal Notices for FlagWar"
[npp]: https://notepad-plus-plus.org/ "A free (as in speech, and beer) source code editor and Notepad replacement (Free, Windows)"
[osi]: https://opensource.org/licenses "Licenses & Standards | Open Source Initiative"
[releases]: https://github.com/TownyAdvanced/FlagWar/releases "FlagWar Tagged Releases"
[sponsor-LlmDl]: https://github.com/sponsors/LlmDl "Sponsor LlmDl, the current TownyAdvanced lead developer and maintainer"
[sublime]: https://www.sublimetext.com/ "A sophisticated text editor for code, markup and prose (Trialware, Cross Platform)"
[vim]: https://www.vim.org "The ubiquitous text editor"
[vscode]: https://code.visualstudio.com "Code editing. Redefined. (Free, Cross Platform)"
[wiki]: https://github.com/TownyAdvanced/FlagWar/wiki "Official FlagWar Documentation"
[zren-blog]:https://zren.github.io/timeline/#bukkit-plugin--cellwar "Timeline / Projects | zren.github.io"
