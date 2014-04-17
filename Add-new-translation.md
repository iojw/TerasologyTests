Adding a new translation for the launcher is quite easy. You only need to change a bunch of text bundle files and one Java file.

Suppose you have done a translation to German. The necessary steps would be:
  * copy [`LabelsBundle_en.properties`](https://github.com/MovingBlocks/TerasologyLauncher/blob/develop/src/main/resources/org/terasology/launcher/bundle/LabelsBundle_en.properties) to a new file `LabelsBundle_de.properties` in ` src/main/resources/org/terasology/launcher/bundle/`. Replace the language suffix with the appropriate one (see http://en.wikipedia.org/wiki/ISO_639-1). Translate everything to your target language.
  * do the same for `MessageBundle_de.properties`
  * add a `settings_language_de=Deutsch (German)` entry to each `LabelsBundle_*.properties` file for other languages. This is used to display the new translation in the settings.
  * make the launcher aware that there is a new language: Modify [`src/main/java/org/terasology/launcher/util/Languages.java`](https://github.com/MovingBlocks/TerasologyLauncher/blob/develop/src/main/java/org/terasology/launcher/util/Languages.java) so that you create a new locale, add your language to the supported locales and select the settings label. 

To keep everything nice and clean we adivse you to use a **feature branch**:
  * `git chekout develop`
  * `git branch germanTranslation`
  * `git checkout germanTranslation`
  * Add/Change files
  * `git commit ....`
  * `git push`
  * Open pull request